1. Networking nedir?

Ağlar basitçe bağlantılı şeylerdir ve hayatın her alanında bulunabilir. Bir şehrin toplu taşıma sistemi, elektrik altyapısı ve komşularla tanışıp selamlaşmak gibi..

Bilgi işlemde ağ oluşturmak aynı olaydır ancak daha teknolojik versiyonu. Bilgi işlemlerde 2 cihadan milyarlarda cihaza kadar herhangi bir yerden bir ağ oluşturulabilir. Bu cihazlarlar bilgisaayrdan güvenlik kameralarına kadar her şeyi içerebilir.

2. İnternet nedir?

İnternet kendi içinde birçok küçük ağdan oluşan dev bir ağdır. İnternetin ilk ortaya çıkışı 1960'ların sonlarında ARPANET projesi kapsamındaydı. Ancak bildiğimiz şekliyle internet Tim Berners-Lee tarafından 1989 yılında World Wide Web'in yaratılmasıyla icat edildi.

İnterneti oluşturan küçük ağlara özel ağlar denir. Özel ağları birbirine bağlayan ağlara genel ağlar veya internet denir. Kısaca bir ağ iki türden biri olabilir:
-Özel Ağ
-Genel A

3. Bir Ağdaki Cihazları Tanıma

İletişim kurmak ve düzeni sağlamak için cihazların bir ağ üzerinde hem tanımlayıcı hem tanımlanabilir olması gerekir. Bir ağdaki cihazları tanımlamanın yolu insanlarda olana çok benzer:
-Ad Soyad
-Parmak İzi

İsmimizi değiştirebilir fakat parmak izimizi değiştiremeyiz. Her insanın bireysel bir parmak izi vardır. Bu da isimlerini değiştirseler bile arkasında hala bir kimlik olduğu anlamına gelir. Cihazlar da aynı şeye sahiptir; biri geçirgen olmak üzere iki tanımlama aracı. Bunlar:
-IP Adresi
-MAC Adresi (bunu bir seri numarası gibi düşün)

a. IP Adresleri

Kısaca bir IP Adresi, bir ağ üzerindeki bir ana bilgisayarı belirli bir süre için tanımalamanın bir yolu olarak kullanılabilir. 

192.168.1.1

IP Adresi, dört sekizliye bölünmüş bir sayı kümesidir. Her sekizlinin değeri, ağdaki cihazın IP adresi olarak özetlenecektir. Bu sayı IP adresleme ve alt ağ olarak bilinen bir teknikle hesaplanır. IP adresleri cihazdan cihaza değişebilir ancak aynı ağ içinde aynı anda birden fazla aktif olamaz.

IP adresleri, protokoller olarak bilinen bir dizi standartı takip eder. Bu protokoller, ağ oluşturmanın bel kemiğidir ve birçok cihazı aynı dilde iletişim kurmaya zorlar. Ancak cihazlar hem özel hem de genel ağ üzerinde olabilir. Nerede olduklarına bağlı olarak ne tür bir Ip adresine sahip oldukları belli olur: genel veya özel IP adresi.

İnternetteki cihazı tanımlamak için genel bir adres kullanılırken, diğer cihazları tanımlamak için özel bir adres kullanılır.

Giderek daha fazla cihaza bağlandıkça, halihazırda kullanımda olmayan bir genel adres almak giderek daha zor bir hale geliyor. Şimdiye kadar IPv4 olarak bilinen ve 2^32 IP adresinden (4.29 Milyar) oluşan bir sürümü tartıştık.

IPv6 bu sorunu çözmek için yeni bir IP adresleme şemasıdır. Avantajları:
-2^128 (340 Trilyon) adede kadar IP adresini destekleyerek IPv4 ile karşılaşılan sorunları çözer. 
-Yeni metodolojiler sayesinde daha verimli.

3. MAC Adresleri

Bir ağdaki aygıtların tümü, aygıtın anakartında bulunan bir mikroçip kartı olan fiziksel bir arabirime sahip olacaktır. Bu ağ arabirimine, oluşturulduğu fabrikada MAC (Media Access Control) adı verilen benzersiz bir adres atanmıştır. MAC adresi iki kolona bölünmüş ve iki nokta üstüste ile ayrılmış on iki karakterli, onaltılık bir sayıdır. Bu kolonlar ayırıcı olarak kabul edilir. Örneğin a4:c3:f0:85:ac:2d. İlk altı karakter ağ arayüzünü yapan şirketi temsil eder ve son altı karakter benzersiz bir sayıdır.

Kafeler ve otel gibi yerler "Misafir" veya "Genel" Wi-Fi'larını kullanırken genellikler MAC adresi kontrolünü kullanır. 

4. Ping (ICMP)

Ping, elimizdeki en temel araçlardan biridir. Ping, cihazlar arasındakş bağlantının performansını, örneğin bağlantını var olup olmadığını veya güvenilir olup olmadığını belirlemek için ICMP (Internet Control Mesaage Protocol) paketlerini kullanır. Cihazlar arasında dolaşan ICMP paketleri için geçen süre ping ile ölçülür. Bu ölçüm ICMP'nin echo paketi ve ardından hedef cihazdan gelen ICMP'nin echo yanıtı kullanılarak yapılır.





















