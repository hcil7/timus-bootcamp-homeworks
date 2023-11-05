1) Javascript 1995 yılında Brandan Eich tarafından dinamik web siteleri inşa edebilmek için icat edilmiştir. 1996 yılında Microsoft'un Internet Explorer tarayıcısına eklenmesiyle tarayıcı tabanlı programlama dili olarak yaygınlaştı. Daha sonra, 1997'de European Computer Manufacturers Association (ECMA) standartlarını kabul ederek, ECMAScript adı altında standart hale getirildi. O günden bu güne Javascript çok fazla güncelleme aldı. 
JS'in aldığı en büyük güncellemeler

ES6 veya ECMAScript 2015: Büyük bir güncelleme olan ES6, JavaScript'e pek çok yeni özellik ekledi. Arrow fonksiyonlar, sınıflar, modüller, sabit değişkenler, yaygın kullanılan string ve dizi işlevleri gibi pek çok yeni özellik ES6 ile tanıtıldı.

ES7 veya ECMAScript 2016: ES7, ES6'dan sonra gelen bir diğer sürümdür. ES7 ile Array.prototype.includes() gibi küçük, fakat yararlı birkaç özellik eklendi.

ES8 veya ECMAScript 2017: ES8 ile birlikte JavaScript'e Asenkron Fonksiyonlar (Async Functions) ve Bekleme Operatörü (Async/Await) gibi büyük bir güncelleme geldi. Ayrıca Object.values(), Object.entries() gibi yeni yöntemler eklendi.

 Chrome V8 motorunu(js kodlarını derleyen mekanizma) tarayıcısının içinden çıkardıktan sonra node'un kurulu olduğu her yerde (server, mobile apps) uygulama geliştirilebilmeye başlanmıştır.

 2) İki programlama dilinin aralarındaki en büyük fark tabi ki sözdizimi (syntaxları). Örneğin değişken tanımlarken Javascipt'te değişkenin tipini (int, string) belirtmezken bu özellik Java'da belirtilir. En büyük ikinci fark ise derlenmeleridir. Java genellikle derlenir ve çalıştırılı" bir dildir. Java kaynak kodu Java Derleyicisi tarafından derlenerek bytecode adı verilen bir ara dil haline getirilir. JavaScript, genellikle "yorumlanır" bir dildir. Yani, JavaScript kaynak kodu tarayıcıda yorumlanarak çalıştırılır, herhangi bir derleme aşaması yoktur. Üçüncü en büyük fark ise kullanım yerleridir. Javascript web sitelerini dinamik hale getirmek için kullanılırken Java'nın böyle bir kullanımı yoktur. Javascript son yıllarda evrim geçirdiğinden dolayı çok çeşitli ortamlarda kullanılabilir.

 3) Javascript'te 2 çeşit veri vardır.
    1. İlkel (Primitive) Veri Tipleri:
        -String, Number, Boolean, Null, Undefined
    2. Referans Veri Tipleri(Gelişmiş Tipler):
        -Object, Array, Function

4) undefined: Bir değişkenin değerinin atanmamış veya tanımlanmamış olduğunu gösterir.
    null: Bir değişkenin değerinin bilinçli olarak atanmış bir boş değer olduğunu temsil eder. Yani bir değişkenin bellekte boş bir değere sahip olduğunu gösterir.

5) NaN : Not a Number demektir(SAYI DEĞİL) örn: 
const result = 10 / "abc";
console.log(result); // Çıktı: NaN

6) // Bu bir tek satırlık yorum.
/*
Çoklu
Satırlı
Yorum
*/

Dökümantasyon Yorumu
/**
 * Bu fonksiyon iki parametre alır ve toplamlarını döndürür.
 * @param {name} console'a yazdırılacak değer
 * @log {name} console'a name'i yaz
 */
function sayHello(name) {
    console.log("HELLO", name)
}

7)JavaScript'te global değişken bir programın herhangi bir yerinde tanımlanan ve programın her yerinden erişilebilen bir değişkenlere denir. Global değişkenlerin aşırı kullanımı bazı sorunlara neden olabilir. Özellikle büyük projelerde farklı kısımlardaki kodun global değişkenleri istenmeyen şekillerde değiştirebilmesi ve karmaşıklık yaratabilmesi gibi durumlar söz konusu olabilir. 

8)JavaScript'te this anahtar kelimesi mevcut bağlamda bulunan nesneyi referans almak için kullanılır. this bir fonksiyonun içinde veya nesne yönelimli programlama'da kullanıldığında, o anki çalışma zamanındaki nesneyi gösterir.

this, nasıl kullanıldığına ve nerede çağrıldığına bağlı olarak farklılık gösterir:
 -- console.log(this); // Tarayıcıda: window nesnesini gösterir, Node.js'te: global nesnesini gösterir.
 -- Nesne İçindeki this: Bir fonksiyon nesne içinde çağrıldığında, this o nesneyi gösterir.
 const obj = {
  name: 'Hasan',
  writeName: function() {
    console.log(this.name); // 'this', 'obj' nesnesini gösterir
  }
};

obj.logName(); // Çıktı: 'Hasan'


-- 
Class kullanarak tanımlanan bir sınıf içinde this anahtar kelimesi sınıfın örneklerini temsil eder. this, bir sınıfın yöntemleri içinde kullanıldığında o sınıfın örneğini işaret eder.

class Car {
  constructor(brand) {
    this.brand = brand;
  }

  getBrand() {
    return this.brand;
  }
}

const myCar = new Car('Toyota');
console.log(myCar.getBrand()); // Çıktı: 'Toyota'

9)JavaScript'te == ve === karşılaştırma operatörleridir. Bu operatörler, karşılaştırma yaparken farklı davranışlar sergilerler.

== (Eşitlik Operatörü): İki değeri karşılaştırırken, sadece değerlerin eşit olup olmadığını kontrol eder. Değerlerin türüne bakmadan eğer değerler aynıysa true döner.
Örnek:
console.log(5 == '5'); // true
console.log(1 == true); // true
console.log(0 == false); // true

=== : Bu operatör, hem değerlerin hem de türlerin aynı olup olmadığını kontrol eder. Eğer karşılaştırılan değerlerin değerleri ve türleri de aynıysa true döner.
Örnek:
console.log(5 === '5'); // false
console.log(1 === true); // false
console.log(0 === false); // false


10) | Anahtar Kelime | Kapsamı      | Yeniden Atanabilirlik | İlk Değer Atama Zorunluluğu |  Tekrardan aynı isimle tanımlanabilirlik | 
| -------------- | ------------ | --------------------- | ---------------------------- | -------------------
| let            | Block Scope | Evet                 | Opsiyonel                   | Hayır
| var            | Function Scope | Evet            | Opsiyonel                   | Evet
| const          | Block scoep | Hayır                | Zorunlu                      | Hayır


11)Arrow fonksiyonlar  diğer fonksiyonlara kıyasla bazı farklı özelliklere sahiptir.
this Bağlamı:

Arrow fonksiyonları, kendi this bağlamını oluşturmaz. Bunun yerine, dışarıdaki kapsamın this değerini alır. Bu özellik, fonksiyonlar içindeki this bağlamıyla ilgili sorunları çözmeye yardımcı olur.

arguments Objesi:

Arrow fonksiyonları, kendi arguments objesine sahip değildir. Bunun yerine, dışarıdaki kapsamın arguments objesini kullanır.

Sözdizimi:

Arrow fonksiyonlar daha kısa bir sözdizimine sahiptir. Fonksiyon gövdesi tek bir ifadeyse, süslü parantezler ve return ifadesi kullanmadan direkt ifadeyi döndürebilirler.

Arrow fonksiyonlar önce çağırılıp sonra tanımlanamazlar. Örneğin: 
sayHello(); // Hata alırsınız: Cannot access 'sayHello' before initialization

const sayHello = () => {
  console.log('Merhaba!');
}


12)
function getValue(color) {
  let result;
  switch (color) {
    case 'red':
      let redValue = 10;
      result = redValue * 2;
      break;
    case 'blue':
      let blueValue = 20;
      result = blueValue * 2;
      break;
    default:
      let defaultValue = 5;
      result = defaultValue * 2;
      break;
  }
  return result;
}

console.log(getValue('red'));  // Çıktı: 20


13)
Dışarıdan Hiçbir Yan Etki Almaz
Pure fonksiyonlar, dış dünyadan (global değişkenler, dosya okuma/yazma, kullanıcı girişi, vb.) hiçbir veri okumaz veya dışarıya etki etmez. Yani, fonksiyon içindeki işlemler, sadece fonksiyon parametreleriyle ve yerel değişkenlerle gerçekleşir.

Aynı Girdiye Karşılık Her Zaman Aynı Çıktıyı Üretir:
Aynı girdi değerleri verildiğinde, pure fonksiyonlar her zaman aynı çıktıyı üretir. Bu özellik, fonksiyonun deterministik olması anlamına gelir.

Yan Etki Oluşturmaz:
Pure fonksiyonlar, hesaplama yaparken dış dünya üzerinde herhangi bir yan etki oluşturmaz. Yani, fonksiyon çağrıldığında başka değişkenlerin, nesnelerin veya durumların değişmesine neden olmaz.
basit bir örnek:
function add(a, b) {
  return a + b;
}


14)Rest operatörü, bir fonksiyon parametresi içinde değişken sayıda argümanları toplamak için kullanılan üç nokta (...) ile ifade edilen bir JavaScript özelliğidir. Bu özellik, bir fonksiyon içinde değişken sayıda argümanları bir diziye dönüştürmek için kullanılır.
function sum(...numbers) {
  return numbers.reduce((total, num) => total + num);
}

console.log(sum(1, 2)); // Çıktı: 3
console.log(sum(1, 2, 3)); // Çıktı: 6
console.log(sum(1, 2, 3, 4)); // Çıktı: 10

15)Object destructuring, JavaScript'te bir nesnenin içindeki özelliklere erişmek ve bu özellikleri ayrı değişkenlere atamak için kullanılan bir yapıdır. Bu yöntem, nesnenin özelliklerine tek tek erişme ihtiyacını azaltır ve daha okunabilir bir kod yazmamızı sağlar.
const person = {
  firstName: 'Hasan',
  lastName: 'Çil',
  age: 26,
  country: 'Turkey'
};

// Object destructuring kullanarak özelliklere erişim
const { firstName, lastName, age, country } = person;

console.log(firstName); // Çıktı: 'Hasan'
console.log(lastName); // Çıktı: 'Çil'
console.log(age); // Çıktı: 26
console.log(country); // Çıktı: 'Turkey'

16)
// 1. Dot notation ile obje oluşturma
const obj1 = {};
obj1.name = 'Hasan';
obj1.surname = 'Çil';

// 2. Köşeli parantez kullanarak obje oluşturma
const obj2 = {};
obj2[name] = "Hasan";
obj2[surname] = "Çil";

// 3. Object literal ile obje oluşturma
const obj3 = {
  name: 'Hasan',
  surname: 'Çil'
};

// 4. Object.create() metodu ile obje oluşturma
const obj4 = Object.create(null);
obj4.name = 'Hasan';
obj4.surname = 'Çil';

// 5. Object.assign() ile obje oluşturma
const obj5 = Object.assign({}, { name: 'Hasan', surname: 'Çil' });

// 6. Yapıcı fonksiyon (Constructor Function) kullanarak obje oluşturma
function Obj() {
  this.name = 'Hasan';
  this.surname = 'Çil';
}
const obj6 = new Obj();

17)const obj = {
  name: 'Hasan',
  surname: 'Çil'
};

const newObj = {};

for (const key in obj) {
  const value = obj[key];
  const newKey = key.length.toString(); 
  const newValue = value.toString().length; 
  newObj[newKey] = newValue; 
}

console.log(newObj); 

2-
const obj = {
  name: 'John',
  age: 25
};

const newObj = {};

Object.keys(obj).forEach(key => {
  const value = obj[key];
  const newKey = key.length.toString();
  const newValue = value.toString().length; 
  newObj[newKey] = newValue;
});

console.log(newObj); 

18)
| Özellik          | Cookie                                | Local Storage                        | Session Storage                      |
| ---------------- | ------------------------------------- | ------------------------------------ | ------------------------------------ |
| Depolama Alanı   | Tarayıcıda 4KB'a kadar veri saklanabilir | Tarayıcıda 5MB'a kadar veri saklanabilir | Tarayıcıda 5MB'a kadar veri saklanabilir |
| Veri Saklama Yeri| Tarayıcıda ve sunucuda gönderilebilir  | Yalnızca tarayıcıda saklanır         | Yalnızca tarayıcıda saklanır         |
| Saklama Süresi   | Belirlenebilir (Süreli veya süresiz)   | Süresiz (Kullanıcı veriyi silene kadar) | Oturum (session) süresi boyunca, tarayıcı kapandığında silinir |
| Veri Türü        | Yalnızca metin veri saklayabilir       | Metin, sayı, boolean ve nesneleri saklayabilir | Metin, sayı, boolean ve nesneleri saklayabilir |
| Veri Gönderimi   | Her HTTP isteğiyle sunucuya gönderilir | Sunucuya otomatik gönderilmez        | Sunucuya otomatik gönderilmez        |
| Kullanım Amacı   | Oturum bilgileri, tercihler, kimlik doğrulama | Genel tercihler, oturum dışı kalıcı veri | Oturum bazlı geçici veri saklamak için |

19)Senkron: işlemlerin sırayla adım adım ve birbirini takip eden şekilde gerçekleştiği işlem türüdür. İşlemler birbirine bağlıdır; bir işlem tamamlanmadan diğeri başlamaz. 
Asenkron: işlemlerin eşzamanlı olmayan veya paralel bir şekilde gerçekleştiği işlem türüdür. İşlemler birbirinden bağımsızdır ve işlem sırası önemli değildir. Bir işlem başlatıldıktan sonra sonucunu beklemeden diğer işlemler devam edebilir

20)
Promise: asenkron işlemleri daha düzenli ve yönetilebilir hale getirmek için kullanılan bir yapıdır. Asenkron operasyonlar özellikle veri alma, gönderme dosya okuma, yazma, ağ istekleri gibi işlemler genellikle işlemlerin tamamlanma sürelerinin belirsiz olduğu durumlarda kullanılır. Promiseler bu tür durumlarda işlemlerin sonuçlarını işlemek yönetmek ve daha okunaklı bir şekilde kod yazabilmek için kullanılır.

-- Array Soruları
var dolap = ["Shirt", "Pant", "TShirt"];

1. Son elemanı silip consola yazdırma
var sonEleman = dolap.pop();
console.log(dolap);

 2. İlk elemanı silip yerine “Hat” elemanını gönderip consola yazdırma
dolap.shift();
dolap.unshift("Hat");
console.log(dolap);

 3. Dolap değişkeninin array olup olmadığını kontrol etme
var isArray = Array.isArray(dolap);
console.log(isArray);

 4. "Pant" elemanının varlığını 3 farklı yöntemle kontrol etme
var method1 = dolap.includes("Pant");
var method2 = dolap.indexOf("Pant") !== -1;
var method3 = dolap.some(item => item === "Pant");
console.log(method1, method2, method3);

5. Elemanların karakter sayısını toplamak için fonksiyon
function karakterSayisiToplam(array) {
  return array.reduce((total, item) => total + item.length, 0);
}
console.log(karakterSayisiToplam(dolap));

 6. Tüm elemanları büyük harfe çevirip yeni değişkene 3 farklı yöntemle atama
var yeniDizi1 = dolap.map(item => item.toUpperCase());

 Yöntem 2: map() metodu ve ayrı bir fonksiyon kullanımı
function buyukHarfeCevir(item) {
  return item.toUpperCase();
}
var yeniDizi2 = dolap.map(buyukHarfeCevir);

Yöntem 3: for döngüsü kullanarak elemanları dönüştürme
var yeniDizi3 = [];
for (var i = 0; i < dolap.length; i++) {
  yeniDizi3.push(dolap[i].toUpperCase());
}

console.log(yeniDizi1, yeniDizi2, yeniDizi3);

7. Index sayıları key olacak şekilde objeye çevirme
var obje = {};
dolap.forEach((item, index) => {
  obje[index] = item;
});
console.log(obje);

8. slice ile splice farkı
slice(): Dizinin belli bir kısmını kopyalar ve orijinal diziyi değiştirmez. İlk değer başlangıç 2. değer kaça kadar sileceğidir.
splice(): Dizinin belli bir kısmını kesip çıkarır ve orijinal diziyi değiştirir. İlk değer başlangıç 2. değer kaç tane sileceğidir. Diğer parametreler ise Diziye ekleneceklerdir.

9. 
let tekrar_edeni_bul = (array) => { 
    array = array.sort((a, b) => a - b); 
    let tekrar_edenler = [] 
    for (index in array) { 
        if (array[index] === array[index - 1]) { 
            tekrar_edenler.push(array[index]); 
        } 
    } 
    return [...new Set(tekrar_edenler)]; 
} 
let arr = [1, 1, 2, 2, 3, 3, 4, 5, 6, 1]; 
console.log(tekrar_edeni_bul(arr));

9. 2. Tüm yinelenen sayıları silip yeni bir array oluşturma
const filterMehoduIle = arr.filter((item, index) => arr.indexOf(item) === index);
const setIle = [...new Set(arr)];
console.log("filter methodu ile:", filterMehoduIle);
console.log("Set ile:", setIle);

9. 3. Array içindeki en yüksek ve en düşük değeri bulma
const enBuyuk = Math.max(...arr);
const enKucuk = Math.min(...arr);
console.log("En Yüksek Değer (Math.max):", enBuyuk);
console.log("En Düşük Değer (Math.min):", enKucuk);


// En yüksek değeri bulma döngü kullanarak
let max = arr[0];
for (let i = 1; i < arr.length; i++) {
  if (arr[i] > max) {
    max = arr[i];
  }
}
console.log("En Yüksek Değer (Döngü):", max);

// En düşük değeri bulma döngü kullanarak
let min = arr[0];
for (let i = 1; i < arr.length; i++) {
  if (arr[i] < min) {
    min = arr[i];
  }
}
console.log("En Düşük Değer (Döngü):", min);


Çıktı Soruları
1) Error 1 yazılacağını düşünmüştüm ama cevap Error 1 ve Success 4 müş.
2) success
Defeat
error
Error caught yazar diye düşündüm ama 
success
Defeat
error
Error caught
Success: test
yazdı.