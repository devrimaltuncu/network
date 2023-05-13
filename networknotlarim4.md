1. ***Paketler ve Frameler

1a. **Paketler ve Frameler nedir?

Paketler ve frameler birlikte oluşturulduğunda daha büyük bir bilgi veya mesaj oluşturan küçük veri parçalarıdır. Ancak bunlar OSI modelinde iki farklı şeydir. Frame Data Link (2) katmanındadır, yani IP Adresleri gibi bilgiler yoktur. Bu boş bir zarfın içine dolu zarf koymak gibidir. İlk zarf pakettir ama içindeki zarf veri içerir yani framedir.
Bu süreç kapsülleme olarak adlandırılır. Kapsüllenen bilgi çıkarıldığında frame kalır.
Paketler ağa bağlı cihazlar arasında veri iletmenin etkili yollarından biridir. Bu veriler küçük parçalar halinde değiş tokuş edildiğinden, bir ağda bir kerede büyük mesajların gönderilmesinden daha az darboğaz meydana gelme olasılığı vardır.
Örneğin bir web sitesinden görsel yüklerken bu görsel bilgisayara bütün olarak değil küçük parçalar halinde yeniden kurgulanarak gönderilir.
Paketler gönderilen paketin türüne bağlı olarak farklı yapılara sahiptir. Ağ iletişimi, paketin bir aygıtta nasıl işlendiğine ilişkin bir dizi kural görevi gören standartlar ve protokollerle doludur. 
İnternet Protokolünü kullanan bir paket, bir ağ üzerinden gönderilen verilere ek bilgi parçaları içeren bir dizi başlığa sahiptir:
Time to Live - Paket hiçbir zaman bir ana bilgisayara ulaşmayı veya kaçmayı başaramazsa ağı tıkamaması için bir son kullanma zamanlayıcısı ayarlar.
Checksum - TCP/IP gibi protokoller için bütünlük denetimi sağlar. Herhangi bir veri değiştirilirse, bu değer beklenenden farklı olacaktır ve bu nedenler bozuk olacaktır.
Source Address - Verilerin nereye döneceğini bilmesi için paketin gönderildiği aygıtın IP adresi.
Destination Address - Paketin gönderildiği aygıtın IP adresi. Böylece verilerin bir sonraki adımda nereye gideceğini bilmesi sağlanır.

IP adresleme bilgilerine sahip bir veri parçasının adı nedir? Packet
IP adresleme bilgisi olmayan bir veri parçasının adı nedir? Frame

2.  **TCP/IP (The Three-Way Handshake) 

TCP (Transmission Control Protocol), ağda kullanılan kurallardan bir diğeridir.
Bu protokol OSI modeline çok benzer. TCP/IP protokolü dört katmandan oluşur ve muhtemelen OSI modelinin sadece özetlenmiş bir versiyonudur. Bu katmanlar:
Application
Transport
Internet
Network Interface

OSI modelinin çalışma şekline çok benzer şekilde, veri parçası (veya paket) üzerinden geçerken, TCP modelinin her katmanına bilgi eklenir. Bu işlem kapsülleme olarak bilinir - tersi dekapsülasyondur.
TCP'nin tanımlayıcı özelliklerinden biri, bağlantı tabanlı olmasıdır; bu, veri gönderilmeden önce TCP'nin hem istemci hem de sunucu görevi gören bir aygıt arasında bir bağlantı kurması gerektiği anlamına gelir.
Bu nedenle TCP, gönderilen herhangi bir verinin diğer uçta alınacağını garanti eder. Bu süreç Üçlü El Sıkışma (Three-Way Handshake) olarak adlandırılır.

**Avantajları: 

Verilerin bütünlüğünü garanti eder.
Yanlış sıradaki verilerle dolmaması için iki cihazı senkronize eder.
Güvenilirlik için çok daha fazla işlem gerçekleştirir.

**Dezavantajları:

İki cihaz arasında güvenilir bir bağlantı gerektirir. Küçük bir veri yığını alınmazsa, tüm veri yığını kullanılamaz ve yeniden gönderilmesi gerekir.
Bağlantı her zaman diğer cihazda rezerve edileceğinden, yavaş bir bağlantı başka bir cihazda tıkanıklık yaratabilir.
TCP, UDP'den önemli ölçüde daha yavaştır çünkü bu protokolü kullanan aygıtlar tarafından daha fazla iş (computing) yapılması gerekir.

TCP paketleri, enkapsüllemeden eklenen header olarak bilinen çeşitli bilgi bölümleri içerir. Bunlar:

Source Port - Bu değer, gönderenin TCP paketini göndermek için açtığı porttur. Bu değer rastgele seçilir (o sırada kullanımda olmayan 0-65535 portlarından).
Destination Port - Bu değer, bir uygulamanın veya hizmetin uzak ana bilgisayarda (veri alan) çalıştığı port numarasıdır; örneğin 80 numaralı portta çalışan bir web sunucusu. Source Porttan farklı olarak bu değer rastgele seçilmez. 
Source IP - Bu, paketi gönderen cihazın IP adresidir.
Destination IP - Bu, paketin hedeflendiği aygıtın IP adresidir.
Sequence Number - Bir bağlantı oluştuğunda, iletilen ilk veri parçasına rastgele bir sayı verilir.
Acknowledgement Number - Bir veri parçasına bir sıra numarası verildikten sonra, bir sonraki veri parçasının numarası + 1 sıra numarasına sahip olacaktır.
Checksum - Bu değer, TCP bütünlüğünü sağlayan şeydir. Çıktının hatırlandığı yerde matematiksel bir hesaplama yapılır. Alıcı cihaz matematiksel hesaplamayı yaptığında, çıktı gönderilenden farklıysa veriler bozuk olmalıdır.
Data - Verilerin, yani aktarılmakta olan bir dosyanın baytlarının depolandığı yerdir.
Flag - Handshake sırasında paketin her iki cihaz tarafından nasıl ele alınması gerektiğini belirler.

Sırada Three-Way Handshake var. TWH birkaç özel mesaj kullanarak iletişim kurar. Bunlar:

SYN - Handshake sırasında bir istemci tarafından gönderilen ilk pakettir. Bu paket, bir bağlantı başlatmak ve iki cihazı birlikte senkronize etmek için kullanılır.
SYN/ACK - Bu paket, alıcı cihaz (server) tarafından istemciden senkronizasyon girişimini onaylamak için gönderilir.
ACK - Bir dizi mesajın/paketin başarıyla alındığını onaylamak için istemci veya sunucu tarafından kullanılabilir.
DATA - Bir bağlantı kurulduğunda, veriler (bir dosyanın baytları gibi) "DATA" mesajı yoluyla gönderilir.
FIN - Tamamlandıktan sonra bağlantıyı temiz (düzgün) şekilde kapatmak için kullanılır.
RST - Bu paket, tüm iletişimi aniden sonlandırır. Bu son çaredir ve işlem sırasında bir sorun olduğunu gösterir.

Gönderilen tüm verilere rastgele bir sayı dizisi verilir ve bu sayı dizisi kullanılarak ve 1 arttırılarak yeniden oluşturulur. Verilerin doğru sırayla gönderilebilmesi için her iki bilgisayarında aynı sayı dizisi üzerinde anlaşması gerekir:
SYN - Client
SYN/ACK - Server
ACK - Client

Device            İnitial Number Sequence (ISN)       Final Number Sequence

Client(Sender)                  0                        0 + 1 = 1 
Client(Sender)                  1                        1 + 1 = 2
Client(Sender)                  2                        2 + 1 = 3

2a. **TCP Bağlantısını Kapatma

İlk olarak, bir cihaz diğer cihazın tüm verileri başarıyla aldığını belirlediğinde TCP bağlantıyı kesecektir.
TCP, bir aygıttaki sistem kaynaklarını ayırdığından, TCP bağlantılarını mümkün olan en kısa sürede kapatmak gerekir.
Bir TCP bağlantısının kapatılmasını başlatmak için, cihaz diğer cihaza bir "FIN" paketi gönderecektir. Diğer cihazında bunu onaylaması gerekir.

Verilerin bütünlüğünü sağlayan bir TCP paketindeki başlık nedir? Checksum
Three-Way Handshake'in sırası nedir? SYN, SYN/ACK, ACK

3. **UDP/IP

UDP (User Datagram Protocol) cizaharlar arasında veri iletişimi için kullanılan başka bir protokoldür.

TCP'den farklı farklı olarak UDP, verilerin gönderilmesi için iki cihaz arasında sürekli bir bağlantı gerektirmeyen, durum bilgisi olmayan bir protokoldür. TWH gerçekleşmez ve iki cihaz arasında herhangi bir senkronizasyon olmaz.

UDP uygulamaların veri kaybını tolere edebildiği durumlarda veya dengesiz bir bağlantının olduğu senaryolarda kullanılır. 

**Avantajları:

TCP'den çok daha hızlıdır.
Paketlerin ne kadar hızlı gönderildiği üzerinde herhangi bir kontrol olup olmadığına karar vermek için uygulamadan (kullanıcı yazılımı) ayrılır.
TCP'nin yaptığı gibi sürekli bağlantı ayırmaz.

**Dezavantajları:

UDP verinin alınıp alınmadığına bakmaz.
Yazılımcılara bu anlamda oldukça esnektir.
Bu, dengesiz bağlantıların kullanıcı için korkunç bir deneyime yol açtığı anlamına gelir.

UDP paketleri, TCP paketlerinden çok daha basittir ve daha az başlığa sahiptir. Ancak her iki protokol de bazı standart başlıkları paylaşır:

Time to Live (TTL) - Paket için bir son kullanma zamanlayıcısı ayarlar, böylece hiçbir zaman ana bilgisayara ulaşmayı veya kaçmayı başaramazsa ağınızı tıkamaz.
Source Address - Verilerin nereye döneceğini bilmesi için paketin gönderildiği cihazın IP adresi.
Destination Address - Paketin gönderildiği aygıtın IP adresi. Verilerin bir sonraki adımda nereye gideceğini bilmesi sağlanır.
Source Port - Bu değer, gönderenin TCP paketini göndermek için açtığı porttur. Bu değer rastgele seçilir (o sırada kullanımda olmayan 0-65535 portlarından).
Destination Port - Bu değer, bir uygulamanın veya hizmetin uzak ana bilgisayarda (veri alan) çalıştığı port numarasıdır; örneğin 80 numaralı portta çalışan bir web sunucusu. Source Porttan farklı olarak bu değer rastgele seçilmez. 
Data - Verilerin, yani aktarılmakta olan bir dosyanın baytlarının depolandığı yerdir.

"UDP" terimi ne anlama geliyor? User Datagram Protocol
"UDP" ne tür bir bağlantıdır? Stateless
Bir dosyayı aktarmak için hangi protokolü kullanırsınız? TCP
Görüntülü arama yapmak için hangi protokolü kullanırsınız? UDP

4. **Buraya Portlar Gelecek Ama Acelesi Yok Bence
