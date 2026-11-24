---
title: Cloudflare CDN Nasıl Kurulur? 2027 Kapsamlı Rehberi
slug: clou
date: 2026-11-24
draft: false
---
# **Cloudflare CDN Nasıl Kurulur? 2027 Kapsamlı Rehberi**

## **Giriş**

Cloudflare CDN, web sitelerinin hızını artırmaya, güvenliğini geliştirmeye ve ana sunucunun üzerindeki yükü azaltmaya yardımcı olan bir hizmettir. İçeriği dünya genelindeki sunucular aracılığıyla dağıtarak ziyaretçilerin web sitenize daha hızlı erişmesini sağlar.

Kişisel bir blog, kurumsal bir web sitesi veya çevrim içi mağaza yönetiyor olun, Cloudflare CDN kullanmak sitenizin performansını ve kararlılığını artırabilir.

Başlamadan önce aşağıdaki hizmetleri de inceleyebilirsiniz:

👉 **CoinePay 官方入口：**  
[https://www.coinepay.net/register?referrer=RFGSSDZ9](https://www.coinepay.net/register?referrer=RFGSSDZ9)

如果你同时使用 TRON（波场）网络进行 USDT 转账，也可以了解 **TRXAPI 提供的 TRON 能量租赁服务**：

👉 **TRXAPI 官方入口：**  
[https://login.trxapi.io/energy](https://login.trxapi.io/energy)

## **1. Cloudflare CDN Nedir?**

Cloudflare, CDN, DNS, güvenlik ve web sitesi performans optimizasyonu hizmetleri sunan bir platformdur.

CDN, Content Delivery Network (İçerik Dağıtım Ağı) anlamına gelir. Web sitenizin içeriğini dünyanın farklı bölgelerinde bulunan sunuculara dağıtır. Böylece ziyaretçiler, kendilerine daha yakın bir sunucudan içerik alabilir.

Cloudflare'ın başlıca avantajları şunlardır:

- Web sayfalarının daha hızlı yüklenmesi.
- Ana sunucuya gelen isteklerin azaltılması.
- DDoS saldırılarına karşı koruma.
- DNS yönetimi.
- SSL sertifikası ve HTTPS bağlantıları.
- Önbellekleme kuralları ve içerik dağıtım optimizasyonu.

## **2. Kuruluma Başlamadan Önce Gerekenler**

Web sitenizi Cloudflare'a bağlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. Size ait bir alan adı.
2. Alan adı yönetim paneline erişim.
3. Mevcut DNS kayıtlarının bilgileri.
4. Hosting veya sunucu yönetim paneline erişim.

E-posta hizmetlerinin veya alan adınıza bağlı diğer servislerin kesintiye uğramaması için mevcut DNS kayıtlarını önceden kaydetmeniz önerilir.

## **3. Cloudflare Hesabı Oluşturun**

Cloudflare'ın resmi web sitesine giderek bir hesap oluşturun.

Kayıt işlemini tamamladıktan sonra:

1. Cloudflare kontrol panelini açın.
2. Site ekleme seçeneğini seçin.
3. Alan adınızı girin.
4. Kurulum işlemine devam edin.

Cloudflare mevcut DNS kayıtlarını otomatik olarak tarayacak ve içe aktarmaya çalışacaktır.

## **4. Alan Adınızı Cloudflare'a Ekleyin**

Alan adınızı girdikten sonra Cloudflare sizden bir plan seçmenizi isteyecektir.

Kişisel web siteleri ve küçük projeler için ücretsiz Free planı genellikle başlangıçta yeterlidir.

Planınızı seçtikten sonra içe aktarılan DNS kayıtlarını kontrol edin.

## **5. DNS Kayıtlarını Kontrol Edin**

Bu, kurulumun en önemli aşamalarından biridir.

Cloudflare mevcut DNS kayıtlarını otomatik olarak aktarabilir. Ancak tüm bilgilerin doğru olduğundan emin olmanız gerekir.

En yaygın DNS kayıt türleri şunlardır:

**A Record**

Alan adını bir IPv4 sunucu adresine yönlendirir.

**AAAA Record**

Alan adını bir IPv6 adresine yönlendirir.

**CNAME Record**

Bir alt alan adını başka bir alan adına yönlendirir.

**MX Record**

Alan adınızın e-postalarını alacak sunucuları belirtir.

**TXT Record**

Alan adı doğrulaması, SPF, DKIM ve diğer yapılandırmalar için kullanılır.

Alan adınıza bağlı bir e-posta hizmeti kullanıyorsanız MX ve TXT kayıtlarına özellikle dikkat edin.

## **6. Cloudflare Proxy Özelliğini Etkinleştirin**

DNS kayıtları listesinde bazı kayıtların yanında bulut simgesi göreceksiniz.

İki temel seçenek bulunur:

**Proxied – Turuncu Bulut**

HTTP ve HTTPS trafiği Cloudflare ağı üzerinden geçer. Bu seçenek CDN ve Cloudflare güvenlik özelliklerini kullanmanızı sağlar.

**DNS Only – Gri Bulut**

Cloudflare yalnızca DNS çözümlemesi sağlar. Trafik doğrudan ana sunucuya bağlanır.

Web sitenizin A ve CNAME gibi web kayıtlarında CDN ve güvenlik özelliklerini kullanmak istiyorsanız Proxied seçeneğini etkinleştirebilirsiniz.

MX gibi proxy desteklemeyen kayıtları ise DNS Only olarak bırakın.

## **7. Alan Adınızın Nameserver Bilgilerini Değiştirin**

DNS kayıtlarını kontrol ettikten sonra Cloudflare size iki nameserver adresi sağlayacaktır.

Örneğin, adresler aşağıdaki biçime benzer olabilir:

- [alice.ns.cloudflare.com](http://alice.ns.cloudflare.com)
- [bob.ns.cloudflare.com](http://bob.ns.cloudflare.com)

Gerçek nameserver adresleri her alan adı için farklıdır.

Alan adı sağlayıcınızın hesabına giriş yapın ve eski nameserver adreslerini Cloudflare tarafından verilen adreslerle değiştirin.

Değişiklikleri kaydedin ve DNS yayılımının tamamlanmasını bekleyin.

Bu işlem birkaç dakika sürebileceği gibi kayıt kuruluşuna ve DNS yayılımına bağlı olarak 24 saat veya daha uzun sürebilir.

## **8. SSL/TLS Ayarlarını Yapılandırın**

Alan adınız etkinleştirildikten sonra Cloudflare kontrol panelindeki SSL/TLS bölümünü açın.

Burada farklı şifreleme modları arasından seçim yapabilirsiniz.

**Flexible**

Ziyaretçi ile Cloudflare arasındaki bağlantıyı şifreler, ancak Cloudflare ile ana sunucu arasındaki bağlantı şifrelenmez.

**Full**

Cloudflare ile ana sunucu arasında HTTPS bağlantısı kullanır, ancak sunucudaki sertifikanın geçerliliğini katı şekilde doğrulamaz.

**Full (Strict)**

Bağlantıyı şifreler ve ana sunucudaki SSL sertifikasının geçerliliğini doğrular.

Sunucunuzda geçerli bir SSL sertifikası varsa Full (Strict) modunu kullanmanız önerilir.

Web siteniz HTTPS için doğru şekilde yapılandırılmışsa Flexible modunu kullanmaktan kaçının. Aksi takdirde yönlendirme sorunları yaşanabilir.

## **9. Cache Ayarlarını Yapılandırın**

Cache, Cloudflare'ın web sitenizdeki görseller, CSS dosyaları ve JavaScript dosyaları gibi kaynakları geçici olarak saklamasını sağlar.

Böylece ziyaretçiler bu kaynakları doğrudan Cloudflare sunucularından alabilir ve her isteğin ana sunucuya ulaşması gerekmez.

Cache ayarlarını yapılandırmak için:

1. Caching bölümünü açın.
2. Mevcut önbellekleme ayarlarını kontrol edin.
3. İhtiyacınıza uygun cache seviyesini seçin.
4. Kaynakların önbellekte ne kadar süre saklanacağını belirleyin.

Tüm sayfaları kontrol etmeden önbelleğe almak önerilmez. Giriş sayfaları, alışveriş sepetleri ve kişiselleştirilmiş içerikler özel kurallar gerektirebilir.

## **10. Cache Rules Kurallarını Yapılandırın**

Cloudflare, önbellekleme işlemini yönetmek için özel kurallar oluşturmanıza olanak tanır.

Örneğin şu kuralları yapılandırabilirsiniz:

- Görseller ve statik dosyalar için cache kullanmak.
- Yönetim paneli sayfalarını önbellek dışında bırakmak.
- Giriş sayfalarını önbellek dışında tutmak.
- Belirli alt alan adları için farklı kurallar oluşturmak.
- Farklı içerik türleri için farklı cache süreleri belirlemek.

WordPress sitelerinde yönetim sayfalarının ve sık değişen içeriklerin yanlışlıkla önbelleğe alınmasını önlemek özellikle önemlidir.

## **11. Cloudflare Cache Belleğini Temizleyin**

Web sitenizi güncellediğiniz hâlde ziyaretçiler hâlâ eski sürümü görüyorsa Cloudflare eski içeriği önbellekten sunuyor olabilir.

Sorunu çözmek için:

1. Caching bölümünü açın.
2. Purge Cache seçeneğine gidin.
3. İstediğiniz temizleme yöntemini seçin.
4. İşlemi onaylayın.

Tüm önbelleği temizleyebilir veya yalnızca belirli URL'leri seçebilirsiniz.

Sık sık güncelleme yapıyorsanız yalnızca ilgili URL'lerin önbelleğini temizlemek daha verimli olabilir.

## **12. Cloudflare CDN'nin Çalışıp Çalışmadığını Kontrol Edin**

Kurulumdan sonra web sitenizin trafiğinin gerçekten Cloudflare üzerinden geçip geçmediğini kontrol etmelisiniz.

Tarayıcınızın geliştirici araçlarını açarak yüklenen kaynakların HTTP yanıt başlıklarını inceleyebilirsiniz.

En kullanışlı başlıklardan biri şudur:

`cf-cache-status`

Bu başlık aşağıdaki değerleri gösterebilir:

- HIT: Kaynak önbellekten sunulmuştur.
- MISS: Kaynak önbellekte bulunmamış ve ana sunucudan alınmıştır.
- BYPASS: Önbellek devre dışı bırakılmış veya atlanmıştır.
- DYNAMIC: Kaynak önbelleğe alınmaya uygun görülmemiştir.
- EXPIRED: Önbellekteki kopyanın süresi dolmuştur.

Her isteğin HIT döndürmesi gerekmez. Dinamik sayfalar doğrudan ana sunucudan sunulabilir.

## **13. Cloudflare Kurulumunda Sık Karşılaşılan Sorunlar**

**521 Hatası**

Ana sunucu Cloudflare bağlantısını reddediyor olabilir.

Sunucunun çalıştığını ve güvenlik duvarının Cloudflare IP adreslerinden gelen bağlantılara izin verdiğini kontrol edin.

**522 Hatası**

Cloudflare, ana sunucudan zamanında yanıt alamıyor olabilir.

Sunucu performansını, güvenlik duvarı kurallarını ve ağ bağlantısını kontrol edin.

**SSL Hatası**

Cloudflare SSL/TLS modu ile ana sunucudaki sertifika yapılandırması uyuşmadığında ortaya çıkabilir.

SSL sertifikasını ve seçilen şifreleme modunu kontrol edin.

**Web Sitesinde Eski İçerik Görüntülenmesi**

Eski sürüm hâlâ önbellekte saklanıyor olabilir.

Cache belleğini temizleyin ve alan adınıza uygulanan önbellekleme kurallarını kontrol edin.

## **14. Cloudflare Free ve Ücretli Planlar**

Cloudflare, Free planının yanı sıra farklı ücretli planlar da sunar.

**Free**

Bloglar, kişisel web siteleri ve küçük projeler için uygundur. Temel DNS, CDN ve güvenlik özelliklerini içerir.

**Ücretli Planlar**

Daha fazla özelliğe, gelişmiş kurallara, kapsamlı güvenlik seçeneklerine veya farklı destek hizmetlerine ihtiyaç duyan web siteleri için uygundur.

Ücretli bir plana geçmeden önce ek özelliklerin gerçekten gerekli olup olmadığını değerlendirin.

## **15. Kurulum Sonrası Kontrol Listesi**

Kurulumun tamamlandığını kabul etmeden önce aşağıdaki maddeleri kontrol edin:

- Alan adı Cloudflare'a eklenmiş olmalı.
- Nameserver adresleri doğru şekilde değiştirilmiş olmalı.
- DNS kayıtları doğru olmalı.
- MX ve TXT kayıtları korunmuş olmalı.
- Gerekli web kayıtlarında Proxy etkinleştirilmiş olmalı.
- SSL/TLS modu doğru yapılandırılmış olmalı.
- Web sitesi HTTPS üzerinden açılmalı.
- Cache kuralları dinamik özellikleri etkilememeli.
- Cloudflare etkinleştirildikten sonra web sitesi sorunsuz çalışmalı.

## **Sonuç**

Cloudflare CDN kurulumu, web sitenizin performansını, güvenliğini ve kararlılığını artırmanın etkili yollarından biridir.

Alan adınızı ekleyerek, DNS kayıtlarını kontrol ederek, nameserver adreslerini değiştirerek, SSL/TLS ayarlarını yapılandırarak ve cache optimizasyonu yaparak Cloudflare'ın temel özelliklerinden yararlanabilirsiniz.

Başlangıç için ücretsiz plan birçok web sitesi açısından yeterlidir. Projeniz büyüdükçe ek özelliklere ihtiyaç duyup duymadığınızı değerlendirebilirsiniz.

## **Cloudflare Resmî Kaynakları**

Cloudflare'a alan adı ekleme:  
[https://developers.cloudflare.com/fundamentals/manage-domains/add-site/](https://developers.cloudflare.com/fundamentals/manage-domains/add-site/)

DNS Proxy ayarları:  
[https://developers.cloudflare.com/dns/proxy-status/](https://developers.cloudflare.com/dns/proxy-status/)

Cache Rules yapılandırması:  
[https://developers.cloudflare.com/cache/how-to/cache-rules/](https://developers.cloudflare.com/cache/how-to/cache-rules/)

Cache temizleme:  
[https://developers.cloudflare.com/cache/how-to/purge-cache/](https://developers.cloudflare.com/cache/how-to/purge-cache/)