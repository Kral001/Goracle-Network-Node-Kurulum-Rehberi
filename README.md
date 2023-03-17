<h1 align="center"> Goracle-Network-Node-Kurulum-Rehberi </h1>

![9](https://user-images.githubusercontent.com/98269269/224926668-6981427e-56d4-4d2a-9df6-e8ff8e134246.png)

Sunucu Gereksinimleri (VPS)
- CPU: 2
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

## 1. Goracle Düğümünü Başlatıyoruz
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

- Bu komut sonrası ortaya çıkacak olan örnek görüntü şöyle olmalıdır; BURADA DİKKATİNİZİ ÇEKMEK İSTİYORUM! Üzeri beyaz olarak taranmış olan kısımda bir numara görüyorsunuz. Bu komutu girdiğimizde herkese özel bu şekilde bir kod verilecek. Katılımcı kodu olarak geçen bu kodu kopyalayın ve bir yere not edin. Birazdan bu kodla kayıt olacağız.

![2](https://user-images.githubusercontent.com/98269269/224921811-b336d610-4ed8-4dba-b38d-b85629d37f0c.png)

- Bu aşamada karşımıza iki adet soru çıkacak. Bunların ikisine de Y yazarak ENTER tuşuna basıyoruz. İkinci soruya Y yanıtını verdiğimizde bizden API Key'imizi isteyecek. 

## 1.1. Aşağıda yer alan görüntüdeki yerden (PureStake üzerinde oluşturduğumuz API keyimizi) kopyalıyoruz. (https://developer.purestake.io/home) Kopyaladığımız API Keyimizi, bizden istediği yere yapıştırıyoruz.

![3](https://user-images.githubusercontent.com/98269269/224922901-2de5deea-549d-48d2-bbbc-ea4400952a64.png)


- Goracle Katılımcı Adresinizi kopyalayın. (Bu adres, yukarıda yer alan ''init'' komutunu girdikten hemen sonra yukarıdaki fotoğrafta üzeri beyaz olarak işaretli olan kısımdaki koddur.) Daha sonra testnet portalındaki ''Nodes'' bölümüne gidin. (https://sandbox-app.goracle.io/nodes)

- Açılan sayfaya ana cüzdanınız ile giriş yapın ve katılımcı adresinizi yapıştırarak aşağıdaki şekilde kaydınızı gerçekleştirin.

![4](https://user-images.githubusercontent.com/98269269/224924150-acc85d50-36b0-45ba-aa2a-eaf0c6124807.png)

- Adresinizi kaydettikten sonra önce test tokenlerini almanız gerekiyor. Aşağıda gösterdiğim butona tıklayarak test tokenlerimizi alıyoruz.

![cx](https://user-images.githubusercontent.com/98269269/225569906-5d431c02-7497-490a-a153-12cff5950ebc.png)


- Şimdi tokenleri stake edeceğiz. İşaretli yerden bu işlemi de gerçekleştiriyoruz. En az 10.000 GORA token stake edebiliriz. Daha az stake etmeye çalışırsanız işlem gerçekleşmeyecektir.

![bb](https://user-images.githubusercontent.com/98269269/225570561-bbdc620f-6aca-4163-b358-ff8715e938d6.png)

- BURASI ÇOK ÖNEMLİ!!! BU İŞLEM YAPILMAZSA NODE ÇALIŞMIYOR!

Test algo ekranına (https://bank.testnet.algorand.network/) girdiğinizde Algorand cüzdan adresiniz ile token talep ettikten sonra, şimdi de ''KATILIMCI ADRESİNİZ'' ile token talep etmelisiniz. Katılımcı adresi dediğimiz adres; yukarıda üzerini beyaz ile belirginleştirdiğimiz bize verilen adrestir.

- Stake işlemini gerçekleştirdikten sonra ve tokenlerimizi aldıktan sonra sunucumuza geri dönüyoruz ve Enter tuşuna basıp kayıdımızı onaylıyoruz. Eğer aşağıdaki gibi çıktı aldıysanız sonraki adıma geçebilirsiniz.

![image](https://user-images.githubusercontent.com/76253089/225603716-7a66a8ce-5928-4236-96ba-e05724e9c4cd.png)

## 2. Docker'ı Kuruyoruz

```
bash <(wget -qO- https://raw.githubusercontent.com/ttimmatti/dependencies/main/docker.sh)
```

- Komutu girdiğinizde çıktısı aşağıdakine benzer bir çıktı olmalıdır.

![6](https://user-images.githubusercontent.com/98269269/224924900-8d013feb-2bae-4565-84bb-a1f4ca2faaab.png)

## 3. Node'umuzu Çalıştırıyoruz

```
goracle docker-start --background
```
- Komutun çıktısı bu şekilde olmalıdır.

![7](https://user-images.githubusercontent.com/98269269/224925319-e099360c-a770-4e88-991c-7d173bfb47c8.png)

## 4. Loglarımızı Kontrol Etmek İçin

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
./goracle docker-stop
```

- Verileri silmek için:

```
rm ~/.goracle
```

