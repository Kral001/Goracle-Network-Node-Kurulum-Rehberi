<h1 align="center"> Goracle-Network-Node-Kurulum-Rehberi </h1>

![9](https://user-images.githubusercontent.com/98269269/224926668-6981427e-56d4-4d2a-9df6-e8ff8e134246.png)

Sunucu Gereksinimleri (VPS)
- CPU: 1-2
- RAM: 4 GB
- Depolama: 10 GB SSD
- Ubuntu: 20.04+

!!! İLK AŞAMADA HERKESİN BİR ALGORAND DÜĞÜM API HESABI OLMALI !!!

- Düğümü doğru bir şekilde kurmak için bir Algorand Düğüm API'sine ihtiyacınız olacak
https://developer.purestake.io/home adresinden ücretsiz bir API hesabı alabilirsiniz.

- PERA WALLET HAKKINDA!

!!! Kuruluma geçmeden önce şunu hatırlatmak istiyorum. Pera Wallet kullananlar için işlem onayları ''PERA WALLET MOBİL UYGULAMA'' üzerinden verilecek. Web sayfasından onay veriliyor mu bilmiyorum ama çok denedim ve bulamadım. Bulan olursa rehbere pull request yapabilirsiniz.

İşlemlere başlamadan önce Pera Wallet'ı aşağıdaki adımları izleyerek ''TESTNET'' ağına almayı unutmayınız!

![Adsız](https://user-images.githubusercontent.com/98269269/225688767-12f10e7b-9d1c-4083-95d0-b34ae9c59088.png)


# KURULUM

## 1. GORACLE DÜĞÜMÜNÜ BAŞLATIYORUZ
```
sudo apt update 
```
```
sudo apt upgrade
```

```
wget  -qP /usr/bin/ https://staging.dev.goracle.io/downloads/latest-staging/goracle &&  chmod u+x /usr/bin/goracle
```
- Bu komut sonrası ortaya çıkacak olan örnek görüntü şöyle olmalıdır;

![1](https://user-images.githubusercontent.com/98269269/224921641-b031d523-6e00-45af-8301-b596f796be54.png)

```
goracle init
```

- Bu komut sonrası ortaya çıkacak olan örnek görüntü şöyle olmalıdır;

![4](https://user-images.githubusercontent.com/98269269/226686230-fd82373f-fdc5-48aa-aca5-5438fa83850a.png)

1.1. Bu aşamada karşımıza iki adet soru çıkacak. Bunların ikisine de Y yazarak ENTER tuşuna basıyoruz. İkinci soruya Y yanıtını verdiğimizde bizden API Key'imizi isteyecek. 

## 1.2. Aşağıda yer alan görüntüdeki yerden (PureStake üzerinde oluşturduğumuz API keyimizi) kopyalıyoruz. (https://developer.purestake.io/home) Kopyaladığımız API Keyimizi, bizden istediği yere yapıştırıyoruz ve enter tuşuna basıyoruz.

![3](https://user-images.githubusercontent.com/98269269/224922901-2de5deea-549d-48d2-bbbc-ea4400952a64.png)

1.3. Ana Algorand Cüzdan Adresinizi Girin. https://testnet-app.goracle.io/nodes sayfasına gidin, cüzdanınızı bağlayın ve aşağıdaki ekran görüntüsünde üzerini belirginleştirdiğim yerdeki ANA ALGORAND CÜZDAN ADRESİNİZİ (Pera, Algosigner vb.) kopyalayın.

![1](https://user-images.githubusercontent.com/98269269/226684510-92b834ba-d963-4ddd-b22a-22aa12e62ddc.png)

1.4. Yukarıda kopyaladığınız ana algorand  cüzdan adresinizi terminale yapıştırın ve enter tuşuna basın.

![2](https://user-images.githubusercontent.com/98269269/226685577-9fe76cf5-b95b-4424-ac25-cceabcf0115c.png)


2.KATILIM ADRESİMİZİ KAYDEDİYORUZ

2.1.Sunucunuzda aşağıda işaretli olarak gösterilen linke tıklayarak katılım adresinizi sisteme kaydedin.

![5](https://user-images.githubusercontent.com/98269269/226687000-00f404c7-51a8-4da6-9723-7308301a2f1f.png)

2.2.Yukarıdaki işlem için linke tıkladığınızda aşağıdaki gibi bir ekranla karşılaşacaksınız (Bu aşamada Pera cüzdanınızı tekrar bağlamanız gerekebilir). Aşağıda gördüğünüz işaretli olan ''register'' butonuna basıyoruz ve node kayıt işlemimizi gerçekleştirmiş oluyoruz.

![6](https://user-images.githubusercontent.com/98269269/226687441-cc0a7907-d358-46dc-9a9f-6155dd553ae6.png)

2.3.Yapılan aşamalarda cüzdan onayı verirken Pera Wallet'ta mobil uygulama üzerinden işlem onayları verildiğini lütfen unutmayın.

- İşlemleri onayladıktan sonra aşağıdaki hatayı alırsanız, lütfen pop-up'ları etkinleştirdiğinizden ve cüzdanınızda Algo (https://bank.testnet.algorand.network/) olduğundan emin olun.

![6bf4abb8-675a-48fa-a2c7-71454e51b017](https://user-images.githubusercontent.com/98269269/226689706-22ed3a67-8cd6-4d7e-8726-f8e54ea46b02.png)

2.4. Ardından katılım adresinize Algo almanız gerekecektir. Bu aşamada aşağıda işaretlediğim yerdeki katılım adresinizi kopyalayın ve faucetten (https://bank.testnet.algorand.network/) KATILIM ADRESİNİZE Algo alın.

![8](https://user-images.githubusercontent.com/98269269/226690642-d815273f-53fa-4395-91de-24e4b87b21a5.png)

- Bu aşamada yalnızca erişim kodu olanlar işleme devam edebilecektir. Erişim kodları ilk etapta rastgele seçilmiş 1000 kişiye gönderilecektir. Sonrasında kısa bir süre sonra herkese açık hale gelecek ve herkes node kurabilecektir.

3.Test $GORA Tokenlerimizi aşağıdaki butona basarak talep ediyoruz. (İLK ETAPTA YALNIZCA 1000 KİŞİYE GÖNDERİLDİ. YAKINDA HERKESE AÇIK HALE GELECEK. EĞER MAİL GELMEDIYSE BU ADIMI ATLAYARAK 3.3'TEN DEVAM EDEBİLİRSİNİZ) 

![9](https://user-images.githubusercontent.com/98269269/226693585-5112bc0f-890a-4db1-a3ab-c1908303945b.png)

3.1.Bize mail olarak gönderilmiş olan erişim kodunu aşağıdaki yere yazarak onaylıyoruz.

![10](https://user-images.githubusercontent.com/98269269/226693795-1f921bdf-7c81-4bd6-9118-36699a8af608.png)

3.1.1.Yukarıdaki işlemi yaptıktan sonra test tokenlerimiz aşağıdaki şekilde görünecektir.

![11](https://user-images.githubusercontent.com/98269269/226693963-8499a879-acef-4b05-8bb5-65297b0d521c.png)

3.2.Şimdi elimizdeki test tokenlerinin bir kısmını stake edeceğiz. ''Add Stake'' butonuna basıyoruz.

![12](https://user-images.githubusercontent.com/98269269/226694166-76f591bf-c4bf-4534-b125-134dfb1cff42.png)

3.2.1.Karşımıza çıkan miktar yazma ekranına EN AZ 10.000 GORA olacak şekilde bir miktar belirleyerek yazıyoruz ve ''Confirm Stake'' butonuna basıyoruz.

![13](https://user-images.githubusercontent.com/98269269/226694458-5b79af44-300a-480a-8e67-5b45be151bd3.png)

- Bu işlemleri adım adım yaparken Pera Wallet mobil uygulamanızdan işlem onaylarını vermeyi unutmayın. Tüm onaylar tamamlandıktan bir süre sonra sayfayı yenilediğinizde tokenlerinizin stake edildiğini görebilirsiniz.

3.3..SON ADIM!

- Terminale dönüyoruz ve ENTER tuşuna basıyoruz.

- Eğer aşağıdaki gibi çıktı aldıysanız sonraki adıma geçebilirsiniz.

![image](https://user-images.githubusercontent.com/76253089/225603716-7a66a8ce-5928-4236-96ba-e05724e9c4cd.png)

## 4. Docker'ı Kuruyoruz

```
bash <(wget -qO- https://raw.githubusercontent.com/ttimmatti/dependencies/main/docker.sh)
```

- Komutu girdiğinizde çıktısı aşağıdakine benzer bir çıktı olmalıdır.

![6](https://user-images.githubusercontent.com/98269269/224924900-8d013feb-2bae-4565-84bb-a1f4ca2faaab.png)

## 5. Node'umuzu Çalıştırıyoruz

```
goracle docker-start --background
```
- Komutun çıktısı bu şekilde olmalıdır.

![7](https://user-images.githubusercontent.com/98269269/224925319-e099360c-a770-4e88-991c-7d173bfb47c8.png)

## 6. Loglarımızı Kontrol Etmek İçin

```
docker logs -f goracle-nr
```
- Bu çıktıyı görüyorsanız bu işlemi de başarılı bir şekilde gerçekleştirdiniz demektir.

![8](https://user-images.githubusercontent.com/98269269/224925594-b243555f-1641-4ccd-9605-db95591e5447.png)

- Tebrikler! Artık Goracle Network Node'umuz hazır :)

- NOT: Cüzdanınızda yeterince test algo tokeni yoksa https://bank.testnet.algorand.network/ adresinden alabilirsiniz. 

- NOT: Cüzdanınızdaki ve katılımcı adresinizdeki test algo miktarı 10'un altına düşmemelidir! Yoksa dashboardda kırmızı olarak görünür. Arada sırada https://bank.testnet.algorand.network/ adresinden hem cüzdan adresinize hem de katılımcı adresinize test algo almayı unutmayın.

- Docker'ı durdurmak için:

```
goracle docker-stop
```

- Verileri silmek için:

```
rm ~/.goracle
```

HATA DÜZELTMELERİ

- Aşağıdaki hataları alıyorsanız ne yaparak bu hataları düzeltebileceğinizi anlatıyorum. Lütfen adımları dikkatli bir şekilde gerçekleştiriniz.

![A](https://user-images.githubusercontent.com/98269269/228642983-3ccc489b-54cf-4131-a00a-df8e24385779.png)

![B](https://user-images.githubusercontent.com/98269269/228643441-59a10bd2-58ff-4b34-9750-858938ea1212.png)

- Bu sorunları düzeltebilmek için Algorand API uç noktanızı değiştirmeniz gerekiyor.

1. PureStake'e kaydolun https://developer.purestake.io/home
2. PureStake Api Anahtarınızı Alın

![c](https://user-images.githubusercontent.com/98269269/228643941-bf203ded-b87b-4e55-adb1-421c0f658dd9.png)

- Terminale gidin ve aşağıdaki komutu girin.

```
nano ~/.goracle
```

Kodu girdiğinizde şöyle bir çıktı alacaksınız:

![d](https://user-images.githubusercontent.com/98269269/228644282-b2e329eb-96cf-40ac-9489-52a1c53e25c5.png)

- Bu dosyayı aşağıdaki gibi görünecek şekilde değiştirmeniz gerekecek.

![e](https://user-images.githubusercontent.com/98269269/228644419-807911a8-5a99-4dfb-868e-df13dc68fa89.png)

Vurgulanan anahtarın SİZİN GERÇEK PURESTAKE API ANAHTARINIZ olduğu yer.

Bu nedenle, ilk iki satırı ilk dosyadan silmeli ve bunun yerine şu üç satırı eklemelisiniz:

"authKey": "YOUR_KEY", 
"server": "https://testnet-algorand.api.purestake.io/ps2", 
"authHeader": "x-api-key",

İşiniz bittiğinde Ctrl+x'e, ardından Y'ye ve ardından Enter'a basın.

Ardından aşağıdaki komutları sırayla girin.

```
goracle docker-stop
```

```
goracle docker-start --background
```

- Son olarak logları kontrol edin.

```
docker logs -f goracle-nr
```


