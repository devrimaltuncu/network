1. OSI Modeli 

1a. OSI Modeli Nedir?

OSI modeli (Open Systems Interconnetion Model) ağda kullanılan temel bir modeldir. Ağa bağlı tüm cihazların verileri nasıl göndereceğini, alacağını ve yorumlayacağını belirler.
OSI Modelinde cihazlar bir ağ üzerinde diğer cihazlarla iletişim kurarken farklı işlevlere sahip olabilirler. 
OSI Modeli yedi katmandan oluşur. Her katmanın farklı bir görevi vardır.
Her katmanda belirli süreçler gerçekleşir ve verilere bilgi parçaları eklenir. 

7.Uygulama (Application)
6.Sunu (Presentation)
5.Oturum (Session)
4.Taşıma (Transport)
3.Ağ (Network)
2.Veri Bağlantı (Data Link)
1.Fiziksel (Physical)

"OSI Modeli"ndeki "OSI" ne anlama geliyor? Open Systems Interconnection
OSI modelinde kaç katman var? 7
Verilere bilgi parçaları eklendiğinde anahtar terim nedir? Encapsulation

2. Yedinci Katman

OSI Modelinin uygulama katmanı en aşina olunan katmandır. Çünkü uygulama katmanı kullanıcının gönderilen veya alına  verilerle nasıl etkileşime girmesi gerektiğini belirleyen protokollerin bulunduğu katmandır.
E-posta istemcileri, tarayıcılar veya FileZilla gibi dosya sunucusu göz atma yazılımları gibi günlük uygulamalar, kullanıcıların gönderilen veya alınan verilerle etkileşime girmesi için kullanıcı dostu bir Grafik Kullanıcı Arayüzü (GUI) sağlar. Diğer protokoller, web sitesi adreslerinin IP adreslerine çevrilme şekli olan DNS'yi (Etki Alanı Adı Sistemi) içerir.

Kullanıcıların etkileşime girdiği yazılımların adına verilen teknik terim nedir? Graphical User Interface

3. Altıncı Katman

Bu katman standartlaştırmanın gerçekleşmeye başladığı katmandır. Geliştiriciler herhangi bir yazılı farklı şekilde geliştirebildikleri için yazılım nasıl çalışırsa çalışsın verilerin aynı şekilde ele alınması gerekir.
Bu katman, Uygulama katmanına (7) gelen ve giden veriler için bir tercüman görevi görür. Alıcı bilgisayar, bir bilgisayara gönderilen ve başka bir formatta gönderilen verileri de anlayacaktır. Örneğin bir e posta gönderdiğinizde diğer kullanıcı sizinkinden farklı bir istemci kullanıyor olabilir. Ancak e posta içeriği yine aynıdır.
Veri şifreleme gibi güvenlik özellikleri bu katmanda gerçekleşir.

Bu Katmanın hareket ettiği ana amaç nedir? Translator

4. Beşinci Katman

Veriler Sunum katmanından (6) doğru bir şekilde çevrildikten veya biçimlendirildikten sonra Oturum katmanı (5) verilerin gönderildiği diğer bilgisayarlarla bağlantı oluşturmaya başlar. Bir bağlantı kurulduğunda bir oturum da oluşturulur. Bağlantı aktifken oturum da aktiftir.
Oturum Katmanı (5), veri gönderilmeden ve alınmadan önce aynı sayfada olmalarını sağlamak için iki bilgisayarı senkronize eder. Sonra oturum katmanı gönderilen verileri daha küçük veri parçalarına bölmeye ve bu parçaları (paketleri) birer birer göndermeye başlar. Bağlantı kesilirse verilerin tamamı değil, henüz gönderilmemiş olan parçaların yeniden gönderilmesi gerekir. 
Oturumlar benzersizdir yani veriler farklı oturumlarda dolaşamaz, yalnızca her oturumda seyahat edebilir.

Bir bağlantı başarıyla kurulduğunda kullanılan teknik terim nedir? Session
"Küçük veri parçaları" için teknik terim nedir? Paketler

5.Dördüncü Katman

Verilerin bir ağ üzerinden iletilmesinde hayati bir rol oynar. Cihazlar arasında veri gönderildiğinde, çeşitli faktörlere göre karar verilen iki farklı protokolden biri izlenir: 
TCP
UDP

Transmission Control Protokol (TCP). Güvenilirlik ve garanti göz önünde bulundurularak tasarlanmıştır. Verilerin gönderilip alınması için geçen süre boyunca iki cihaz arasında sabit bir bağlantı sağlar.
TCP hata denetimini tasarımına dahil eder. Hata denetimi, TCP'nin Oturum katmanındaki (5) küçük yığınlardan gönderilen verilerin daha sonra aynı sırada alındığını ve yeniden birleştirildiğini nasıl garanti edebileceğidir.

TCP'nin Avantajları

Verilerin doğruluğunu garanti eder.
Birbirine veri dolmasını önlemek için iki cihazı senkronize edebilir.
Güvenilirlik için çok daha fazla işlem gerçekleştirir.

TCP'nin Dezavantajları

İki cihaz arasında güvenilir bir bağlantı gerektirir. Küçük bir veri yığını alınmazsa tüm veri yığını kullanılamaz.
Bağlantı her zaman alıcı bilgisayarda ayrılacağından yavaş bir bağlantı başka bir cihazda tıkanıklık yaratabilir.
TCP, UDP'den daha yavaştır çünkü protokolü kullanan aygıtların daha zala iş yapması gerekir.

TCP, dosya paylaşımı, internette gezinme veya e posta gönderme gibi durumlar için kullanılır. Nedeni bu hizmetlerin verilerinin doğru ve eksiksiz ulaşması gerekliliğidir.

User Datagram Protocol (UDP). TCP kadar gelişmiş değildir. Hata denetimi ve güvenilirlik gibi özellikleri yoktur. UDP aracılığıyla gönderilen herhangi bir veri hedefe ulaşsın yada ulaşmasın gönderilir. İki cihaz arasında senkronizasyon veya garanti yoktur.

UDP'nin Avantajları

TCP'den çok daha hızlıdır.
Paketlerin ne kadar hızlı gönderildiği üzerinde herhangi bir kontrol olup olmadığına karar vermek için uygulama katmanından ayrılır.
TCP'nin yaptığı gibi bir aygıtta sürekli bağlantı ayırmaz.

UDP'nin Dezavantajları

UDP verilerin alınıp alınmadığını umursamaz.
Yazılımcılara bu anlamda oldukça esnektir.
Dengesiz bağlantılar kullanıcı için korkunç bir deneyime yol açar.

UDP gönderilen küçük veri parçalarının olduğu durumlarda kullanışlıdır. Örneğin ARP ve DHCP veya video akışı gibi daha büyük dosyalar.

Hangi protokol verilerin doğruluğunu garanti eder? TCP
Verilerin diğer cihaz tarafından alınıp alınmadığına hangi protokol önem vermez? UDP
E-posta istemcisi gibi bir uygulama hangi protokolü kullanır? TCP
Dosyaları indiren bir uygulama hangi protokolü kullanır? TCP
Video akışı yapan bir uygulama hangi protokolü kullanır? UDP

6.Üçüncü Katman

Verilerin yönlendirilmesi ve yeniden birleştirilmesinin sağlandığı yerdir (Küçük parçalardan daha büyük parçalara). İlk olarak veri yığınlarının gönderileceği en uygun yolu belirler.
Bu katmandaki bazı protokoller, verilerin bir cihaza ulaşmak için izlemesi gereken optimal yolun tam olarak ne olduğunu belirler. Bu protokoller OSPF (Open Shortest Path First) ve RIP (Routing Information Protocol)'ü içerir. Hangi rotanın seçileceğine karar veren faktörler:

En kısa yol hangisidir?
En güvenli yol hangisidir?
Hangi yolun daha hızlı fiziksel bağlantısı var?

Bu katmanda her şey 192.168.1.100 gibi IP adresleri üzerinden halledilir. IP adreslerini kullanarak paketleri iletebilen router gibi aygıtlar, 3. Katman aygıtları olarak bilinirler.

Paketler bir ağ boyunca en uygun yolu kullanacak mı? Evet
"OSPF" kısaltması ne anlama geliyor? Open Shortest Path First
"RIP" kısaltması ne anlama geliyor? Routing Information Protocol
Bu katmanda ne tür adresler ele alınır? IP Adresleri

7.İkinci Katman

İletimin fiziksel olarak adreslenmesine odaklanır. Ağ katmanından bir paket alır ve alıcı uç noktanın fiziksel MAC adresini ekler. Ağ özelliklli her bilgisayarın içinde benzersiz bir MAC adresiyle birlikte gelen bir Ağ Arabirim Kartı (NIC - Network Interface Card) bulunur.
MAC adresleri üretici tarafından belirlenir ve tam anlamıyla karta yazılır. Sahte olabilmelerine rağmen değiştirilemezler. Bilginin tam olarak nereye gönderileceğini belirlemek için kullanılan fiziksel adrestir.
Verileri iletime uygun bir formatta sunmak Veri Bağlantı katmanının işidir.

Ağa bağlı tüm cihazların birlikte geldiği donanım parçasının adı nedir? Network Interface Card

8.Birinci Katman

Bu katmanda ağda kullanılan donanımın fiziksel bileşenlerine atıfta bulunulur. Cihazlar ikili bir numaralandırma sisteminde (1 ve 0) birbirleri arasında veri aktarmak için elektrik sinyallerini kullanır.

Hem 0 hem de 1 olan numaralandırma sisteminin adı nedir? Binary
Cihazları birbirine bağlamak için kullanılan kabloların adı nedir? Ethernet Kablosu

