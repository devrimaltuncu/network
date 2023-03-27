1. LAN'a Giriş

1a. Lan Topolojileri

a. Yıldız Topoloojisi

Yıldız toplojisinde cihazlar bir anahtar veya hub gibi merkezi bir ağ cihazı aracılığıya bağlanır. Günümüzde en yaygın bulunan topolojidir çünkü güvenilir ve ölçeklenebilirdir.
bu topolojide bir cihaza gönderilen herhangi bir bilgi bağlandığı merkezi cihaz üzerinden gönderilir.
Avantaj ve Dezavantajları:
Dahaza fazla kablolama ve özel ağ ekipmanı satın alınması gerektiğinden pahalıdır.
Diğer topolojilere göre daha çok ölçeklenebilirdir. Ağa talep arttıkça daha fazla cihaz eklemek kolay olur.
Ağ ne kadar ölçeklenirse ağı çaışır durumda tutmak için o kadar bakım gerekir. 
Cihazları birbirine bağlayan merkezi donanım arızalanırsa bu cihazlar artık veri gönderemez veya alamaz. Ama cihazlar genelde sağlamdır.

b. Otobüs Topolojisi

Omurga kablosu olarak bilinen tek bir bağlantıya dayanır. Bu topoloji bir ağacın dalına ve yapraklarına benzer.
Her bir cihaza gönderilen veriler aynı kablo boyunca hareket ettiğinden bağlı cihazlar aynı anda veri talep ediyorsa yavaşlamaya ve darboğaz olmaya eğilimlidir. Darboğaz zor sorun  gidermeye neden olur çünkü hangi cihazın verilerle sorun yaşadığını belirlemek zorlaşır.
Daha az maliyetlidir ve kurulumu kolaydır.
Omurga kablosu boyunca tek bir arıza noktası olur. Bu kablo koparsa cihazlar veri yolu boyunca veri alamaz veya iletemez.

c. Halka Topolojisi

Bilgisayarlar gibi cihazlar doğrudan birbirine bağlanır. Çok az kablolama gerekir ve yıldız topolojisinde olduğu gibi özel donanıma daha az bağımlıdır. Veriyi iletmek için döngü boyunca veri gönderir. Bu topolojide başka cihazdan alınan verilerii sadece kendi verisi yoksa gönderir. GÖnderecek verisi varsa başka cihazdan veri göndermeden önce kendi verisini gönderir.
Bu topolojide veriler tek bir yönde gittiği için oluşacak herhangi sorunda tamir ertmesi kolaydır. Büyük bir miktarda trafik ağ üzerinden geçmeiğinden darboğazlara daha az eğilimlidir. 

2a. Switch Nedir?

Ağ oluşturma özellikli birden fazla cihazı bir araya getirmek için tasarlamış ağ içindeki cihazlardır. Porta takılır. Switchler genelde çok sayıda cihazın bulunduğu ağlarda bulunur. Switchler cihazların takılması için 4, 8, 16, 24, 32 ve 64 bağlantı noktalarına sahip olur. 
Switchler hub ve repeaterlardan daha verimlidir. Switch hangi cihazın hangi bağlantı noktasına bağlı olduğunu takip eder. Bir paket aldığında bu paketi hub gibi her bağlantı noktasında tekrarlamak yerine yalnızca amaçlanan hedefe gönderir ve aü trafiğini azaltır.
Switchler ve routerlar birbirine bağlanabilir. Bu verilerin alınması için birden çok yol ekleyerek ağın güvenilirliğini arttırır. Bir yol bozulursa diğeri kullanılabilir. Paketlerin ulaşması daha uzun sürdüğü için ağın genel performansını düşürebilir fakat herhangi bir kesinti yaşanmaz.

3a. Router Nedir?

Ağları birbirine bağlamak veri iletmek routerın işidir.
Ağlar arasında dolaşan veri sürecine yönlendirme denir. (Routing) Routing verilerin başarılı bir şekilde ulaşması için ağlar arasında bir yol oluşturulmasıdır. Routing cihazlar birçok yolla bağlandığında kullanışlıdır.

LAN'ın açılımı nedir? Local Area Network
Yönlendiricilerin yaptığı işe verilen fiil nedir? Routing
Yerel ağdaki birden fazla cihazı merkezi olarak bağlamak ve verileri doğru konuma iletmek için hangi cihaz kullanılır? Switch
Hangi topolojinin kurulması uygun maliyetlidir? Otobüs 
Hangi topolojinin kurulumu ve bakımı pahalıdır? Yıldız

2. Alt Ağ (Subnetting) Oluşturma Üzerine Bir Başlangıç

Ağlar küçükten büyüğe tüm şekil ve boyutlarda bulunabilir. Alt ağ oluşturma, bir ağı kendi içinde daha küçük ağlara bölmek için veriler addır. Subnet oluşturmada ağa sığabilecek ana bilgisayar sayısı bölünür ve subnet mask denilen bir sayı ile ifade edilir. 
IP adresi sekizli (octet) adı verilen dört bölümden oluşur. Aynısı, 0 ile 255 (0-255) arasında değişen dört baytlık (32 bit) bir sayı olarak da temsil edilen bir alt ağ maskesi için de geçerlidir.

Subnetler IP adreslerini üç farklı şekilde kullanır:
Ağ adresini tanımlama
Host adresini tanımlama
Varsayılan ağ geçidini tanımlama

Subnet oluşturmanın bazı avantajları:
Verimlilik
Güvenlik
Tam kontrol

Bir ağı daha küçük parçalara bölmek için kullanılan teknik terim nedir? Subnetting
Bir alt ağ maskesinde kaç bit vardır? 32
Bir alt ağ maskesinin bir bölümünün (sekizli) aralığı nedir? 0-255
Bir ağın başlangıcını belirlemek için hangi adres kullanılır? Ağ Adresi
Bir ağ içindeki cihazları tanımlamak için hangi adres kullanılır? Host Adresi
Başka bir ağa veri göndermekten sorumlu cihazı tanımlamak için kullanılan ad nedir? Varsayılan Ağ Geçidi

3. ARP Protokolü

Adres Çözümleme Protokolü (Address Resolution Protocol) cihazların bir ağ üzerinde kendilerini tanımlamalarına izin vermekten sorumlu olan teknolojidir.
Basitçe ARP, bir aygıtın MAC adresini ağdaki bir IP adresiyle ilişkilendirmesine izin verir. Bir ağdaki her cihaz, diğer cihazlarla ilgili ilişkili MAC adreslerinin günlüğünü tutacaktır.
Cihazlar bir başkasıyla iletişim kurmak istediğinde, belirli bir cihazı aramak için tüm ağa bir yayın gönderir. Cihazlar, iletişim için bir cihazın MAC adresini (ve dolayısıyla fiziksel tanımlayıcısını) bulmak için ARP protokolünü kullanabilir.
3a. ARP Nasıl Çalışır?

Bir ağdaki her cihazın, bilgileri depolamak için önbellek adı verilen bir defteri vardır. ARP protokolü bağlamında, bu önbellek ağdaki diğer cihazların tanımlayıcılarını saklar.

Bu iki tanımlayıcıyı (IP adresi ve MAC adresi) birlikte eşleştirmek için ARP protokolü iki tür mesaj gönderir:
ARP Talebi
ARP Yanıtı

Bir ARP isteği gönderildiğinde, cihazın MAC adresinin istenen IP adresiyle eşleşip eşleşmediğini soran, cihaz tarafından bir ağda bulunan diğer tüm cihazlara bir mesaj yayınlanır. Cihaz istenen IP adresine sahipse, bunu onaylamak için ilk cihaza bir ARP yanıtı gönderilir. İlk cihaz şimdi bunu hatırlayacak ve önbelleğinde saklayacaktır (bir ARP girişi).

ARP'nin açılımı nedir? Adress Resolution Protocol
ARP Paketinin hangi kategorisi bir cihaza belirli bir IP adresine sahip olup olmadığını sorar? Request (Talep)
Ağdaki bir cihaz için fiziksel tanımlayıcı olarak hangi adres kullanılır? MAC Adresi
Ağdaki bir cihaz için mantıksal tanımlayıcı olarak hangi adres kullanılır? IP Adresi

4. DHCP Protokolü

Dinamik Ana Bilgisayar Yapılandırma Protokolü (Dynamic Host Configuration Protocol)
IP adresleri, fiziksel olarak bir cihaza girilerek manuel olarak veya otomatik olarak ve en yaygın olarak bir DHCP sunucusu kullanılarak atanabilir. Bir cihaz bir ağa bağlandığında, manuel olarak bir IP adresi atanmamışsa, ağda herhangi bir DHCP sunucusu olup olmadığını görmek için bir istek (DHCP Discover) gönderir. DHCP sunucusu daha sonra cihazın kullanabileceği bir IP adresiyle yanıt verir (DHCP Offer). Cihaz daha sonra sunulan IP Adresini (DHCP Request) istediğini onaylayan bir yanıt gönderir ve son olarak DHCP sunucusu bunun tamamlandığını onaylayan bir yanıt gönderir ve cihaz IP Adresini (DHCP ACK) kullanmaya başlayabilir.

Bir cihaz tarafından bir IP adresini almak için ne tür DHCP paketi kullanılır? DHCP Discover
Bir cihaz, kendisine DHCP sunucusu tarafından bir IP adresi sunulduğunda ne tür DHCP paketi gönderir? DHCP Request
Bir DHCP sunucusundan bir cihaza gönderilen son DHCP paketi nedir? DHCP ACK
