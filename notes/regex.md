############################

############################
# REGEX
############################

############################


# regular expression (or regex or reg-ex or regexp or rational expression)

arama yapabilmek için karakterlerden oluşan özel bir ifade dilidir.

birçok implementasyonu vardır. örnek: 
- IEEE POSIX'ta belirtilen: BRE (or Basic Regular Expressions)
- IEEE POSIX'ta belirtilen: ERE (or Extended Regular Expressions)
- IEEE POSIX'ta belirtilen: SRE (or Simple Regular Expressions)
- Perl Compatible Regular Expressions (or PCRE) kaynak: (source-id: 52) 1inci paragraf.

Unicode veritabanında her karakterin meta-bilgileri mevcut. Eğer kullandığımız regex kütüphanesi bu bilgileri saklıyor ise; o zaman aşağıdaki gibi kontroller ile de regex yazabiliriz:

- Alphabetic
- Ideographic
- Letter
- Lowercase
- Uppercase
- Titlecase
- Punctuation
- Control
- White_Space
- Digit
- Hex_Digit
- Noncharacter_Code_Point
- Assigned 

kaynak: (source-id: 53) "Unicode support" başlığı.

# regex kullanımı

(aşağıdaki syntax bilgileri hangi notasyon standardına göre yazıldı bilmiyorum. aşağıdaki bilgiler farklı kaynaklardan toplama olduğundan farklı standartlara ait bile olabilirler.)

| regex          | what it returns                                                                                                                                                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ^merhaba       | starts with "merhaba"                                                                                                                                                                                                                                      |
| merhaba yusuf$ | ends with "merhaba yusuf"                                                                                                                                                                                                                                  |
| merhaba        | contains "merhaba"                                                                                                                                                                                                                                         |
| ab#            | a, ac, abc, abb, abbc döndürebilir. a kesin var. b'den istenildiği kadar olabilir. # karakteri sadece bir önceki karakter için bir kuralı kapsar. eğer bir önceki karakter birden fazla karakter olacak ise; a(bc)# olarak parantez içinde gruplandırılır. |
| a(bc)#         | a, abc, abcbc, abce döndürebilir.                                                                                                                                                                                                                          |
| ab+            | # karakteri ile aynıdır. tek farkı en az 1 adet b olmalıdır. ab, abb, abc                                                                                                                                                                                  |
| ab?            | # karakteri ile aynıdır. tek farkı en fazla 1 adet b olmalıdır. a, ab, ac                                                                                                                                                                                  |
| a?b+$          | ab, b, bb, abb, abbb dolar ile bittiğini belirttiğimizden en sağa c gibi farklı karakterler gelemez                                                                                                                                                        |
| ab{2}          | {} # gibi sadece bir önceki karakter için geçerli bir kural belirtir. {2} 2 tane b olması gerektiğini belirtiyor. abb, abbc, abbc                                                                                                                          |
| ab{2,}         | en az 2 adet b olmalıdır. abbb, abb, abbc                                                                                                                                                                                                                  |
| ab{3,5}        | en az 3 en fazla 5 adet b olabilir. abbbc, abbb                                                                                                                                                                                                            |
| hi∣hello       | hi veya hello içerenler döner.                                                                                                                                                                                                                             |
| (b∣cd)ef       | bef yada cdef içeren textler döner                                                                                                                                                                                                                         |
| [ab]           | [] sadece bir karakteri temsil ediyor. (a∣b) ile aynı şeydir.                                                                                                                                                                                              |
| [a-d]          | [abcd] ve (a∣b∣c∣d) ile aynı şey.                                                                                                                                                                                                                          |
| [a-zA-Z]       | regex aksi belirtilmedikçe case sensitive'dir. bu sebeple büyük küçük tüm alfabeyi kapsatır.                                                                                                                                                               |
| [0-9]          | sadece rakam olduğunu belirtir.                                                                                                                                                                                                                            |
| [a-zA-E0-8]    | ufak karakterler tüm alfabe, büyük karakterlerde a'dan e'ye kadar olan karakterler, sayılarda ise 0'dan 8'e kadra olan karakterler                                                                                                                         |
| a.b            | . bir karakteri temsil ediyor. acb, abb                                                                                                                                                                                                                    |
| ..             | en az 2 karakter olan değerler döner                                                                                                                                                                                                                       |

özel karakterler kullanılacak ise öncesinde backslash "\" kullanılmalıdır.

# javascript'te regex

```js
var myRegexObject = /hello world/i; // literal notation
// or
var myRegexObject = new RegExp('hello world', 'i'); // first param is 'pattern' and the second param is 'modifiers'.
// or
var myRegexObject = new RegExp(/hello world/, 'i');

var sonuc = "hello world coder".search(myRegexObject);
```

## Modifiers

- /i

Perform case-insensitive matching.

- /g

Perform a global match (find all matches rather than stopping after the first match)

- /m

Perform multiline matching.

## functions of RegExp object

- compile()

  Deprecated. Compiles a regular expression.

- exec(str)

  Tests for a match in a string. Returns the first match.

  ```js
  regex.exec("hello"); // returns the found string.
  ```

- test(str)

  Tests for a match in a string. Returns true or false.

  ```js
  regex.test("hello"); // returns true or false.
  ```

  test and exec functions are always moving the pointer. Therefor "regex.lastIndex" will increase everytime we call test or exec.

- toString()

  Returns the string value of the regular expression.
