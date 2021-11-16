############################

############################
# LUCENE
############################

############################

# Apache Lucene
İlk başta sadece java için tasarlanan fakat daha sonra birçok programlama için geliştirilen indexleme ve arama motoru kütüphanesidir.

Bir dökümanı (database, list, text file...) parçalara böler, indexler ve daha sonra da arama yapılabilmesini sağlar. bunların tümü için ayrı ayrı programlama dillerine API'ler yazılmıştır. Lucene sunucu gibi kendi başına çalışmaz.

querydsl'in, Lucene'nin query (arama) tarafı için desteği vardır.

# Apache Lucene example with code

```xml
<properties>
    <lucene.version>6.6.0</lucene.version>
</properties>
 
<dependency>
    <groupId>org.apache.lucene</groupId>
    <artifactId>lucene-core</artifactId>
    <version>${lucene.version}</version>
</dependency>
<dependency>
    <groupId>org.apache.lucene</groupId>
    <artifactId>lucene-analyzers-common</artifactId>
    <version>${lucene.version}</version>
</dependency>
<dependency>
    <groupId>org.apache.lucene</groupId>
    <artifactId>lucene-queryparser</artifactId>
    <version>${lucene.version}</version>
</dependency>
```

```java
import java.io.IOException;
import java.nio.file.Paths;
import java.util.ArrayList;
import java.util.List;
 
import org.apache.lucene.analysis.standard.StandardAnalyzer;
import org.apache.lucene.document.Document;
import org.apache.lucene.document.Field;
import org.apache.lucene.document.StringField;
import org.apache.lucene.document.TextField;
import org.apache.lucene.index.IndexWriter;
import org.apache.lucene.index.IndexWriterConfig;
import org.apache.lucene.store.FSDirectory;
 
public class LuceneWriteIndexExample 
{
    private static final String INDEX_DIR = "/home/userX/lucene_data";
 
    public static void main(String[] args) throws Exception 
    {
        IndexWriter writer = createWriter();
        List<Document> documents = new ArrayList<>();
         
        Document document1 = createDocument(1, "Ayse", "Koroglu", "helloworld.com");
        documents.add(document1);
         
        Document document2 = createDocument(2, "Mehmet", "Baskaonglu", "google.com");
        documents.add(document2);
         
        //Let's clean everything first
        writer.deleteAll();
         
        writer.addDocuments(documents);
        writer.commit();
        writer.close();
    }
 
    private static Document createDocument(Integer id, String firstName, String lastName, String website) 
    {
        Document document = new Document();
        document.add(new StringField("id", id.toString() , Field.Store.YES));
        document.add(new TextField("firstName", firstName , Field.Store.YES));
        document.add(new TextField("lastName", lastName , Field.Store.YES));
        document.add(new TextField("website", website , Field.Store.YES));
        return document;
    }
 
    private static IndexWriter createWriter() throws IOException 
    {
        FSDirectory dir = FSDirectory.open(Paths.get(INDEX_DIR));
        IndexWriterConfig config = new IndexWriterConfig(new StandardAnalyzer());
        IndexWriter writer = new IndexWriter(dir, config);
        return writer;
    }
}
```

Yukarıdaki kod execute edilince "/home/userX/lucene_data" altında dosyaların oluştuğunu göreceğiz.

Şimdi farklı bir program ile yine lucene kullanarak bu dizinde arama yapalım:

```java
import java.io.IOException;
import java.nio.file.Paths;
 
import org.apache.lucene.analysis.standard.StandardAnalyzer;
import org.apache.lucene.document.Document;
import org.apache.lucene.index.DirectoryReader;
import org.apache.lucene.index.IndexReader;
import org.apache.lucene.queryparser.classic.QueryParser;
import org.apache.lucene.search.IndexSearcher;
import org.apache.lucene.search.Query;
import org.apache.lucene.search.ScoreDoc;
import org.apache.lucene.search.TopDocs;
import org.apache.lucene.store.Directory;
import org.apache.lucene.store.FSDirectory;
 
public class LuceneReadIndexExample 
{
    private static final String INDEX_DIR = "c:/temp/lucene6index";
 
    public static void main(String[] args) throws Exception 
    {
        IndexSearcher searcher = createSearcher();
         
        //Search by ID
        TopDocs foundDocs = searchById(1, searcher);
         
        System.out.println("Total Results :: " + foundDocs.totalHits);
         
        for (ScoreDoc sd : foundDocs.scoreDocs) 
        {
            Document d = searcher.doc(sd.doc);
            System.out.println(String.format(d.get("firstName")));
        }
         
        //Search by firstName
        TopDocs foundDocs2 = searchByFirstName("Brian", searcher);
         
        System.out.println("Total Results :: " + foundDocs2.totalHits);
         
        for (ScoreDoc sd : foundDocs2.scoreDocs) 
        {
            Document d = searcher.doc(sd.doc);
            System.out.println(String.format(d.get("id")));
        }
    }
     
    private static TopDocs searchByFirstName(String firstName, IndexSearcher searcher) throws Exception
    {
        QueryParser qp = new QueryParser("firstName", new StandardAnalyzer());
        Query firstNameQuery = qp.parse(firstName);
        TopDocs hits = searcher.search(firstNameQuery, 10);
        return hits;
    }
 
    private static TopDocs searchById(Integer id, IndexSearcher searcher) throws Exception
    {
        QueryParser qp = new QueryParser("id", new StandardAnalyzer());
        Query idQuery = qp.parse(id.toString());
        TopDocs hits = searcher.search(idQuery, 10);
        return hits;
    }
 
    private static IndexSearcher createSearcher() throws IOException {
        Directory dir = FSDirectory.open(Paths.get(INDEX_DIR));
        IndexReader reader = DirectoryReader.open(dir);
        IndexSearcher searcher = new IndexSearcher(reader);
        return searcher;
    }
}
```

# Tokenization
Doğal Dil işlemede en sık kullanılan terimlerden biridir. bir cümleyi, phrase'lere, kelimelere bölme işlemine verilen isimdir.

Piyasada birçok tokenizer bulabiliriz. örnekler: CamelCase tokenizer, URL tokenizer, path tokenizer and N-gram tokenizer.

örneğin; "C:\WINDOWS\system32\rundll32.exe" textini tokenize etmek için "URL tokenizer" kullanmak şarttır.
