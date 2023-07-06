## Hello World

Kotlinde:

* <code>fun</code> fonksiyon tanımlamak için kullanılan bir anahtar kelime.
* <code>main()</code> fonksiyonu Kotlin'de programın başladığı yerdir.
* Bir fonksiyonun içeriği(gövdesi) süslü parantezler <code>{}</code> arasına yazılır.
* <code>println()</code> ve <code>println()</code>  fonksiyonları standart ekrana çıktı vermek için kullanılan fonksiyonlardır.

<br/><br/>


## Değişkenler

Kotlinde:

* <code>val</code> anahtar kelimesi ile <u>değiştirilemeyen(read-only)</u> sadece okunabilir değişkenler oluşturulabilir.
* <code>var</code> anahtar kelimesi ile <u>değiştirilebilen(mutable)</u> değişkenler oluşturulabilir.
<br/>

Değişkene değer ataması yapmak için, atama operatörü olarak <code>=</code> operatörü kullanılıyor.


* [Kod Örneği İçin](src/main/kotlin/Variables.kt)

```kotlin
fun main() { 
    val popcorn = 5    // There are 5 boxes of popcorn
    val hotdog = 7     // There are 7 hotdogs
    var customers = 10 // There are 10 customers in the queue

    // Some customers leave the queue
    customers = 8
}
```

<div style="background-color: #004085">

```text
ℹ️ Değişkenler  programın başlangıcında main() fonksiyonunun dışında da tanımlanabilir. Bu şekilde tanımlanan
değişkenler üst düzey(top level) olarak tanımlanır.
``` 
</div>
* <code>customers</code> değişkeni değiştirilebilir(mutable) olduğundan dolayı ilk tanımlamadan sonra 
 değeri yeniden atanabilir.

<div style="background-color: #155724">

```text
 ℹ️ Kotlin varsayılan olarak tüm değişkenleri salt okunur(val) olarak tanımlanmasını öneriyor.
 Değerinin değişmesi ön görülen değişkenler mutable(var) olarak tanımlanmalıdır.
```
</div>

<br/><br/>


## String Templates

String templates  değişkenlerin içeriklerini standart konsol çıktısına yazdırmak için oldukça faydalı bir yöntemdir.
Değişkenlerde ve nesnelerdeki verilere erişip konsol çıktısında göstermek için şablon ifadelerini kullanabilirsiniz.
String ifadeler <code>""</code> çift tırnak içindeki karakter dizileridir. Template ifadeleri ise
her zaman <code>$</code> ifadesi ile başlar.

<br/>
Template ifadesi içerisindeki değişken ve nesneler üzerinde işlem yapmak için, <code>$</code>
ifadesinden sonra <code>{}</code> ifadesi arasında yapılabilir.

* [Kod Örneği İçin](src/main/kotlin/StringTemplates.kt)

```kotlin
fun main(){
    val customers = 10
    println("There are $customers customers")  // There are 10 customers
    println("There are ${customers + 1} customers") // There are 11 customers
}
```

* [String template ile ilgili daha fazla bilgi için](https://kotlinlang.org/docs/strings.html)


* <code>customer</code> değişkeni için tanımlanmış herhangi bir tip olmadığı göreceksiniz.
Kotlin türü kensidi <code>Int</code> olarak belirledi.

