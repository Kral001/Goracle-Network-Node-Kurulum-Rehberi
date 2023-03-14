<h1 align="center"> Goracle-Network-Node-Kurulum-Rehberi </h1>

![9](https://user-images.githubusercontent.com/98269269/224926668-6981427e-56d4-4d2a-9df6-e8ff8e134246.png)

Sunucu Gereksinimleri (VPS)
- Cpu: 2
- Ram: 4gb
- Depolama: 10gb SSD
- Hızlı Internet
- Ubuntu: 20.04+

!!! İLK AŞAMADA HERKESİN BİR ALGORAND DÜĞÜM API HESABI OLMALI !!!

- Düğümü doğru bir şekilde kurmak için bir Algorand Düğüm API'sine ihtiyacınız olacak
https://developer.purestake.io/home adresinden ücretsiz bir API hesabı alabilirsiniz.

!!! Kuruluma geçmeden önce şunu hatırlatmak istiyorum. Pera Wallet kullananlar için işlem onayları ''PERA WALLET MOBİL UYGULAMA'' üzerinden verilecek. Web sayfasından onay veriliyor mu bilmiyorum ama çok denedim ve bulamadım. Bulan olursa rehbere pull request yapabilirsiniz.

KURULUM

1. Goracle Düğümünü Başlatıyoruz

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

1.1. Aşağıda yer alan görüntüdeki yerden (PureStake üzerinde oluşturduğumuz API keyimizi) kopyalıyoruz. (https://developer.purestake.io/home) Kopyaladığımız API Keyimizi, bizden istediği yere yapıştırıyoruz.

![3](https://user-images.githubusercontent.com/98269269/224922901-2de5deea-549d-48d2-bbbc-ea4400952a64.png)

- Goracle Katılımcı Adresinizi kopyalayın. (Bu adres, yukarıda yer alan ''init'' komutunu girdikten hemen sonra yukarıdaki fotoğrafta üzeri beyaz olarak işaretli olan kısımdaki koddur.) Daha sonra testnet portalındaki ''Nodes'' bölümüne gidin. (https://testnet-app.goracle.io/nodes)

- Açılan sayfaya ana cüzdanınız ile giriş yapın ve katılımcı adresinizi yapıştırarak aşağıdaki şekilde kaydınızı gerçekleştirin.

![4](https://user-images.githubusercontent.com/98269269/224924150-acc85d50-36b0-45ba-aa2a-eaf0c6124807.png)

- Adresinizi kaydettikten sonra payınızı arttırmanız gerekecek. İşaretli yerden bu işlemi de gerçekleştiriyoruz.

![5](https://user-images.githubusercontent.com/98269269/224924612-765808db-d4b6-455e-ae30-adc6d325d241.png)


2. Docker'ı Kuruyoruz

```
bash <(wget -qO- https://raw.githubusercontent.com/ttimmatti/dependencies/main/docker.sh)
```

- Komutu girdiğinizde çıktısı aşağıdakine benzer bir çıktı olmalıdır.

![6](https://user-images.githubusercontent.com/98269269/224924900-8d013feb-2bae-4565-84bb-a1f4ca2faaab.png)

3. Node'umuzu Çalıştırıyoruz

```
goracle docker-start --background
```
- Komutun çıktısı bu şekilde olmalıdır.

![7](https://user-images.githubusercontent.com/98269269/224925319-e099360c-a770-4e88-991c-7d173bfb47c8.png)

4. Loglarımızı Kontrol Etmek İçin

```
docker logs -f goracle-nr
```
- Bu çıktıyı görüyorsanız bu işlemi de başarılı bir şekilde gerçekleştirdiniz demektir.

![8](https://user-images.githubusercontent.com/98269269/224925594-b243555f-1641-4ccd-9605-db95591e5447.png)

- Tebrikler! Artık Goracle Network Node'umuz hazır :)

