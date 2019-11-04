##  Linear Regression , Multiple Regression ve Polynomial Regressiona bir göz atalım..

|**Linear Regression**|  |
|-----------------|--|
|                 |  |


Elimizde Ms-Ölme sayısı ile ilgili bir veri olduğunu düşünelim Ms arttıkça ölme sayımızda bununla birlikte artmaktadır.Bizden Ms in 250 olduğundaki ölme sayımız istenirse nasıl bir yol izleriz ? 

![enter image description here](https://i.hizliresim.com/AOV6op.png)



Veri düzensiz olarak arttığı için artış miktarını almayı düşünme olasılığımız da elimizden alındı işte tam bu anda Lineer Regression devreye giriyor.

**Formülizasyon**
Lineer Regressionu formüle döktüğümzde tamda şu şekilde ifade edebiliriz -> y = a0+a1*x

Y = Çıktı Değeri

a0 = Başlangıç değeri olarak alabiliriz(Y eksenini ilk kesen nokta olarakta adlandırılabilir--Terim olarak anlamı ise Bias)

a1 = Tahmin ederken kullanacağımız eğim(Coeff veya slope şeklinde’de tanımlanabilir)


Y değerini tahmin ederken başlangıç değerimiz , ilgili eğimle bizim tahmin etmek istediğimiz değer çarpılıp a0 ile toplanır.

**Doğruluğu Nasıl Ölçebiliriz ?**
Formülü kullanarak bir şekilde bir sonuca ulaştık fakat bunun ne kadar doğru ne kadar yanlış olacağını nasıl ölçeriz ?

  

Burada devreye MSE(Mean Squared Error) giriyor bunun formülü ise şu şekilde;**

 
![](https://lh5.googleusercontent.com/gygUwPeZBu7aa-f_Cj3SkELHBrD6hsgXOOlw0Bd3_67Ag7iEP1A3offrpmS1ZKIwGgL6TTq1QTuknrDn9MMe_h1-FOKg3vJR3zRmhVX43sEDXYv5c21xLSJx9mxj9t6n7E2Hj_3k)

Yi : Gerçekten olması gereken değer

Y^i : Bizim tahmin ettiğimiz değer

n : elimizdeki toplam veri sayısı

  

Burada yaptığımız şey ise olması gereken değer ile tahmin ettiğimiz değerin farkının karesini almaktan geçiyor. Karesini alma sebebimiz ise negatif değerler elde edersek bunun diğerlerini sönümlemesini engellemek.

**Multiple Regression**

Üstteki örnekle aynı şekilde ifade edersek Ms in yanında birde Fps değişkeninin girdiğini düşünelim. 100Ms ve 240 Fps aldığımız bir uygulamada tahmin yapmak gerekirse nasıl yapabiliriz ?

İşte bu noktada da Multiple Regression devreye giriyor.

**Formülizasyon**

Multiple Regressionu formüle döktüğümzde tamda şu şekilde ifade edebiliriz -> y = a0+a1*x1+a2*x2....+an*xn

Y = Çıktı Değeri

a0 = Başlangıç değeri olarak alabiliriz(Y eksenini ilk kesen nokta olarakta adlandırılabilir--Terim olarak anlamı ise Bias)

a1,a2,...,an = Tahmin ederken kullanacağımız eğim(Coeff veya slope şeklinde’de tanımlanabilir)

x1,x2,...xn = Girdi değerlerimiz 
**Doğruluğu Nasıl Ölçebiliriz ?**

Lineer Regressiondaki gibi MSE'yi kullanabiliriz.

**Polynomial Regression**
Bizim tahmin ettiğimiz durumlar herzaman 1.dereceden olmayabilir(Daha karmaşık problemler) 2,3,4,5. dereceden durumları değerlendirmemiz gerekebilir bu tür durumlarda Polynomial Regression'u kullanabiliriz
![enter image description here](https://i.hizliresim.com/3O5YRA.png)

**Formülizasyon**
Polynomial Regressionu formüle döktüğümzde tamda şu şekilde ifade edebiliriz -> y = a0+a1*x1+a2*x^2+x ^n
Y = Çıktı Değeri

a0 = Başlangıç değeri olarak alabiliriz(Y eksenini ilk kesen nokta olarakta adlandırılabilir--Terim olarak anlamı ise Bias)

a1,a2,...,an = Tahmin ederken kullanacağımız eğim(Coeff veya slope şeklinde’de tanımlanabilir)

x1,x^2,...x ^n = Girdi değerlerimiz n ise değerlerin derecesini ifade eder 


****Birazda Kodlamak Gerek-Polynomial Regression-****
![enter image description here](https://i.hizliresim.com/9Yz2R5.png)

 - 14. Satırda datayı df ye aktardık
 - 16 ve 17. Satırda verilerin formatı (x,) şeklinde x satırdan 1 sütundan oluşan tipteydi sklearn bunu algılaması için formatını düzelttik
 - 18. Satırda Kaçıncı dereceye kadar ilerleyeceğimizi belirledik
 - 19. Satırda X değerlerimizin 18. Satırdaki belirlediğimiz derece kadar işledik
 - 21 ve 23.Satırda ise fit işlemlerini gerçekleştirdik
 - 27 den 31. Satıra kadar ise yaptıklarımızı görselleştirdik.
