**Ağınızı Genişletmek

1. **Port Yönlendirmeye Giriş

Port yönlendirme (Port Forwarding), uygulamaları ve hizmetleri internete bağlamada önemli bir bileşendir. Port yönlendirme olmadan, web sunucuları gibi uygulamalar ve hizmetler yalnızca aynı aynı doğrudan ağ (Same Direct Network) içindeki cihazlar tarafından kullanılabilir. 

Port yönlendirmeyi bir güvenlik duvarının (firewall) davranışlarıyla karıştırmak kolaydır. Ancak bu aşamada port yönlendirmenin belirli portları açtığını anlamanız yeterlidir (paketlerin nasıl çalıştığını hatırlayın). Karşılaştırıldığında güvenlik duvarları, trafiğin bu portlardan geçip geçemeyeceğini belirler (bu portlar, port yönlendirme yoluyla açık olsalar bile).

Port yönlendirme, bir ağın yönlendiricisinde (router) yapılandırılır.

2. **Firewalls 101

Güvenlik duvarı, ağ içinde hangi trafiğin girip çıkmasına izin verildiğini belirlemekten sorumlu bir cihazdır. Güvenlik duvarını bir ağ için sınır güvenliği olarak düşünün. Bir yönetici, çok sayıda faktöre bağlı olarak trafiğin ağa girmesine veya ağdan çıkmasına izin verecek veya engelleyecek şekilde bir güvenlik duvarı yapılandırabilir. Bunlar:

Trafik nereden geliyor? Güvenlik duvarına belirli bir ağdan gelen trafiği kabul etmesi/reddetmesi söylendi mi?
Trafik nereye gidiyor? Güvenlik duvarına belirli bir ağa yönelik trafiği kabul etmesi/reddetmesi söylendi mi?
Trafik hangi port için? Güvenlik duvarına yalnızca 80 numaralı porta yönelik trafiği kabul etmesi/reddetmesi söylendi mi?
Trafik hangi protokolü kullanıyor? Güvenlik duvarına UDP, TCP veya her ikisi birden olan trafiği kabul etmesi/reddetmesi söylendi mi?

Güvenlik duvarları, bu soruların yanıtlarını belirlemek için paket denetimi gerçekleştirir.

Güvenlik duvarları her şekil ve boyutta gelir. Büyük miktarda veriyi işleyebilen özel donanım parçalarından veya Snort gibi yazılımlara kadar 2 ila 5 kategoriye ayrılabilir.

İki ana güvenlik duvarı kategorisi:

Stateful - Tek bir paketi incelemek yerine bir bağlantıdaki tüm bilgileri kullanır. Tüm bağlantıya dayalı olarak bir cihazın davranışını belirler.
Karar verme türü dinamik olduğu için Stateless güvenlik duvarlarına kıyasla birçok kaynağı tüketir. Örneğin bir güvenlik duvarı, daha sonra başarısız olacak bir TCP anlaşmasının ilk bölümlerine izin verebilir.
Bir ana bilgisayardan gelen bağlantı kötüyse, tüm cihazı engeller.

Stateless - Bireysel paketlerin kabul edilebilir olup olmadığını belirlemek için statik bir kurallar dizisi kullanır. Örneğin, kötü bir paket gönderen cihaz, tüm cihazın engellendiği anlamına gelmez.
Bu güvenlik duvarları alternatiflerinden çok daha az kaynak kullanır. Yalnızca kendi içlerinde tanımlanan kurallar kadar etkilidir. Bir kural tam olarak eşleşmezse, etkili bir şekilde işe yaramaz.
Bu güvenlik duvarları, bir dizi hosttan büyük miktarda trafik alırken (Distributed Denial-of-Service Attack (Dağıtılmış Hizmet Reddi Saldırısı) gibi) harikadır.

Güvenlik duvarları OSI modelinin hangi katmanlarında çalışır? Layer 3 ve Layer 4
Hangi güvenlik duvarı kategorisi tüm bağlantıyı denetler? Stateful
Hangi güvenlik duvarı kategorisi bireysel paketleri denetler? Stateless

3. **VPN Temelleri

Virtual Private Network (VPN), ayrı ağlardaki cihazların internet üzerinden birbirleri arasında ayrılmış bir yol (tünel olarak bilinir) oluşturarak güvenli bir şekilde iletişim kurmasını sağlayan bir teknolojidir. Bu tünel içerisinde bağlanan cihazlar kendi özel ağlarını oluştururlar.

Örneğin, yalnızca aynı ağ içindeki (örneğin bir işletme) cihazlar doğrudan iletişim kurabilir. Ancak, bir VPN iki ofisin bağlanmasına izin verir. 

VPN'in sunduğu bazı faydalar:

Farklı coğrafi konumlardaki ağların bağlanmasına izin verir - Örneğin birden çok ofise sahip bir iletme, sunucu/altyapı gibi kaynaklara başka bir ofisten erişilebileceği anlamına geldiği için VPN'leri faydalı bulacaktır.
Gizlilik sunar - VPN teknolojisi, verileri korumak için şifreleme kullanır. Bu, yalnızca gönderildiği ve gönderildiği cihazlar arasında anlaşılabileceği anlamına gelir, yani veriler koklamaya karşı savunmasız değildir. Bu şifreleme, ağ tarafından şifrelemenin sağlanmadığı, halka açık WiFi bulunan yerlerde kullanışlıdır. Trafiğinizin başkaları tarafından görüntülenmesini önlemek için bir VPN kullanabilirsiniz.
Anonimlik sunar - Gazeteciler ve aktivistler, ifade özgürlüğünün kontrol altında tutulduğu ülkelerde küresel sorunlar hakkında güvenli bir şekilde haber yapmak için VPN'lere güveniyor. Genellikle trafiğiniz İSS'niz ve diğer aracılar tarafından görüntülenebilir ve bu nedenle izlenebilir. Bir VPN'nin sağladığı anonimlik düzeyi, yalnızca ağdaki diğer cihazların gizliliğe ne kadar saygı duyduğu kadardır. Örneğin tüm verilerinizi, geçmişinizi günlüğe kaydeden bir VPN kullanmak, VPN kullanmamakla temelde aynıdır.

VPN teknolojisi yıllar içinde gelişmiştir. Mevcut bazı VPN teknolojileri:

PPP - Bu teknoloji, kimlik doğrulamaya izin vermek ve verilerin şifrelenmesini sağlamak için PPTP tarafından kullanılır. VPN'ler, özel bir anahtar ve genel sertifika (SSH'ye benzer) kullanarak çalışır. Bağlanabilmeniz için özel anahtar ve sertifikanın eşleşmesi gerekir. Bu teknoloji kendi başına bir ağdan ayrılamaz (yönlendirilemez - non-routable).
PPTP - Point-to-Point Tunneling Protocol, PPP'den gelen verilerin seyahat etmesine ve bir ağdan ayrılmasına izin veren teknolojidir. PPTP'nin kurulumu çok kolaydır ve çoğu cihaz tarafından desteklenir. Bununla birlikte, alternatiflere kıyasla zayıf bir şekilde şifrelenmiştir.
IPSec - Internet Protocol Security, mevcut IP çerçevesini kullanarak verileri şifreler. IPSec'in ayarlanması alternatiflerine kıyasla zordur, ancak kurulum başarılı olursa güçlü şifreleme sunar ve ayrıca birçok cihazda desteklenir.

Hangi VPN teknolojisi yalnızca şifreler ve verilerin kimlik doğrulamasını sağlar? PPP
Hangi VPN teknolojisi IP çerçevesini kullanır? IPSec

4. **LAN Ağ Aygıtları

4a. **Router Nedir?

Ağları birbirine bağlamak ve aralarında veri iletmek bir yönlendiricinin işidir. Bunu yönlendirmeyi kullanarak yapar (routing - router).

Routing, ağlar arasında dolaşan veri sürecine verilen etikettir. Routing bu verilerin başarılı bir şekilde teslim edilebilmesi için ağlar arasında bir yol oluşturulmasını içerir. Routerlar, OSI modelinin 3. katmanında çalışır. Genellikle bir yöneticinin bağlantı noktası iletme veya güvenlik duvarı gibi çeşitli kuralları yapılandırmasına izin veren etkileşimli bir arabirime sahiptirler.

Routerlar özel cihazlardır ve switchlerle aynı işlevi gerçekleştirmezler. A bilgisayarının ağının B bilgisayarına ortadan iki routerla bağlı olduğunu düşünelim. Soru şu: Nasıl bir yol izlenecek? Hangi yolun izlenmesi gerektiğine farklı protokoller karar verecektir, ancak bazı faktörler şunları içerir:

En kısa yol hangisidir?
En güvenilir yol hangisidir?
Hangi yol daha hızlı ortama sahiptir (örn. bakır veya fiber)?

4b. **Switch Nedir?

Switch, birden fazla cihaza bağlanmak için bir araç sağlamaktan sorumlu özel bir ağ cihazıdır. 

Switchler, OSI Modelinin hem 2. katmanında hem de 3. katmanında çalışabilir. Ancak bunlar, katman 2 switchlerinin  katman 3'te çalışamaması anlamında özeldir.

Katman 2 switchleri, MAC adreslerini kullanarak frameleri (IP protokolü çıkarıldığı için bunlar artık packet değildir) bağlı cihazlara iletir. Framelerin doğru cihaza gönderilmesinden yalnızca bu switchler sorumludur. 

Katman 3 anahtarları, bir routerın bazı sorumluluklarını yerine getirebildikleri için katman 2'den daha karmaşıktır. Yani, bu switchler aygıtlara (katman 2'de olduğu gibi) frameler gönderecek ve packetleri IP protokolünü kullanarak diğer aygıtlara route edecektir.

Hareket halindeki bir katman 3 anahtarına baktığımızda iki IP adresi olduğunu görebiliriz:

192.168.1.1
192.168.2.1

VLAN (Virtual Local Area Network) adı verilen bir teknoloji, bir ağ içindeki belirli cihazların sanal olarak bölünmesine izin verir. Bu ayrım, hepsinin internet bağlantısı gibi şeylerden yararlanabileceği, ancak ayrı ayrı ele alınacağı anlamına gelir. Bu ağ ayrımı, belirli aygıtların birbiriyle nasıl iletişim kuracağını belirleyen kuralların geçerli olduğu anlamına geldiğinden güvenlik sağlar.

Bir routerın yaptığı eylemin fiili nedir? Routing
İki farklı anahtar katmanı nedir? Layer 2, Layer 3

