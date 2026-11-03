---
title: "Cloudflare Rehberi: Yeni Başlayanlar İçin 10 Temel Özellik"
slug: cloudf
date: 2026-11-03
draft: false
---
# Cloudflare Rehberi: Yeni Başlayanlar İçin 10 Temel Özellik

## 1. Cloudflare Nedir?

Cloudflare, web sitesi sahiplerinin sitelerinin hızını, güvenliğini ve erişilebilirliğini artırmasına yardımcı olan bir internet hizmetleri platformudur.

Platform birçok önemli araç sunar:

- **DNS Yönetimi**: DNS kayıtlarını yönetmenizi ve ziyaretçileri doğru sunucuya yönlendirmenizi sağlar.
- **CDN**: Küresel sunucu ağı sayesinde web sitelerinin daha hızlı yüklenmesine yardımcı olur.
- **SSL/TLS**: Ziyaretçiler ile web sitesi arasındaki bağlantıları güvence altına alır.
- **DDoS Koruması**: Dağıtık hizmet engelleme saldırılarından kaynaklanan riskleri azaltmaya yardımcı olur.
- **WAF (Web Uygulaması Güvenlik Duvarı)**: Kötü amaçlı olabilecek istekleri filtreler.
- **Önbellekleme (Cache)**: Web sitesi kaynaklarını geçici olarak saklayarak yükleme hızını artırır.
- **Analytics**: Trafik ve güvenlik istatistiklerini takip etmenizi sağlar.
- **Workers**: Kodu doğrudan Cloudflare ağı üzerinde çalıştırmanıza olanak tanır.
- **Pages**: Statik web siteleri ve ön uç uygulamaları yayınlamanızı sağlar.

Cloudflare hem ücretsiz hem de ücretli planlar sunar. Yeni başlayanlar, platformun temel özelliklerini öğrenmek için ücretsiz planla başlayabilir.

## 2. Cloudflare Hesabı Nasıl Oluşturulur ve Web Sitesi Nasıl Eklenir?

Cloudflare özelliklerini kullanmaya başlamadan önce bir hesap oluşturmanız ve alan adınızı platforma eklemeniz gerekir.

### Adım 1: Cloudflare Hesabı Oluşturun

Resmî kayıt sayfasını ziyaret edin:

[https://dash.cloudflare.com/sign-up](https://dash.cloudflare.com/sign-up)

E-posta adresinizi girin ve hesabınızı oluşturmak için bir parola belirleyin.

### Adım 2: Web Sitenizi Ekleyin

Hesabınıza giriş yaptıktan sonra web sitesi veya alan adı ekleme seçeneğini seçin.

Alan adınızı girin. Örneğin:

`example.com`

Cloudflare mevcut DNS kayıtlarını analiz edecek ve başlangıç yapılandırmasını önerecektir.

### Adım 3: DNS Kayıtlarını Kontrol Edin

İçe aktarılan DNS kayıtlarını dikkatlice inceleyin.

En önemli kayıt türleri şunlardır:

- **A**: Bir alan adını IPv4 adresine bağlar.
- **AAAA**: Bir alan adını IPv6 adresine bağlar.
- **CNAME**: Bir alan adını başka bir alan adına yönlendirir.
- **MX**: E-posta mesajlarını alan posta sunucularını tanımlar.
- **TXT**: Alan adı doğrulaması ve e-posta yapılandırması gibi işlemlerde kullanılan metin bilgilerini saklar.

E-posta hizmetinizin kesintiye uğramaması için özellikle e-posta ile ilgili DNS kayıtlarını dikkatlice kontrol edin.

### Adım 4: Ad Sunucularını (Nameservers) Değiştirin

Cloudflare size iki adet ad sunucusu (nameserver) sağlayacaktır.

Alan adınızı satın aldığınız kayıt kuruluşunun web sitesine giriş yapın ve mevcut ad sunucularını Cloudflare tarafından verilenlerle değiştirin.

Değişikliklerin yayılması biraz zaman alabilir. Yapılandırma doğrulandıktan sonra Cloudflare, belirlediğiniz ayarlara göre alan adınızın trafiğini yönetmeye başlayacaktır.

## 3. Cloudflare'ın Yeni Başlayanlar İçin 10 Temel Özelliği

### Özellik 1: DNS Yönetimi

DNS yönetimi, Cloudflare'ın en önemli özelliklerinden biridir.

Alan adınızın DNS kayıtlarını yönetmenize ve ziyaretçilerin sunucunuza nasıl yönlendirileceğini belirlemenize yardımcı olur.

Cloudflare kontrol panelinde **DNS** bölümünü açarak kayıtları görüntüleyebilir ve düzenleyebilirsiniz.

Başlıca iki proxy modu bulunur:

- **Proxied (turuncu bulut)**: HTTP/HTTPS trafiği Cloudflare ağı üzerinden geçer. Böylece proxy, CDN ve ilgili koruma hizmetlerinden yararlanabilirsiniz.
- **DNS Only (gri bulut)**: Cloudflare yalnızca DNS çözümlemesi sağlar. Trafik platformun proxy hizmetinden geçmez.

Standart bir web sitesi için kullanılan A ve CNAME kayıtları genellikle Proxied modunda yapılandırılabilir.

Dikkat: Özellikle e-posta hizmetleri olmak üzere bazı hizmetler özel DNS yapılandırmaları gerektirir. Hizmetin düzgün çalışmaya devam edeceğinden emin olmadan bu kayıtları değiştirmeyin.

### Özellik 2: CDN ve Web Sitesi Hızlandırma

Cloudflare, küresel bir içerik dağıtım ağına (CDN) sahiptir.

Bir ziyaretçi web sitenizi açtığında bazı kaynaklar, ziyaretçinin bulunduğu konuma yakın bir Cloudflare veri merkezinden sunulabilir.

Bu, gecikmeyi azaltabilir ve sayfaların daha hızlı yüklenmesine yardımcı olabilir.

Genellikle önbelleğe alınabilen kaynaklar şunlardır:

- Görseller.
- CSS dosyaları.
- JavaScript dosyaları.
- Yazı tipleri.
- Diğer statik kaynaklar.

Cloudflare proxy hizmetini etkinleştirmek için DNS bölümünü açın ve web sitenizle ilgili desteklenen kayıtların turuncu bulut simgesiyle işaretlendiğinden emin olun.

Daha sonra web sitenizin ihtiyaçlarına göre önbellek ayarlarını ve ilgili kuralları yapılandırabilirsiniz.

### Özellik 3: SSL/TLS ve HTTPS Şifreleme

SSL/TLS, ziyaretçiler ile web siteniz arasındaki bağlantıların güvenliğini sağlamaya yardımcı olur.

Doğru yapılandırılmış bir HTTPS sitesi, aktarılan verileri korur ve ziyaretçilerin güvenini artırır.

Cloudflare kontrol panelinde şu bölüme gidin:

**SSL/TLS → Overview**

Burada farklı şifreleme modları bulunur:

- **Off**: Cloudflare ile ziyaretçi arasında şifreleme yoktur.
- **Flexible**: Ziyaretçi ile Cloudflare arasındaki bağlantı HTTPS kullanır, ancak Cloudflare ile kaynak sunucu arasındaki bağlantı HTTP kullanır.
- **Full**: Ziyaretçi, Cloudflare ve kaynak sunucu arasındaki bağlantı şifrelenir; ancak kaynak sunucunun sertifikası sıkı şekilde doğrulanmaz.
- **Full (strict)**: Bağlantı şifrelenir ve kaynak sunucunun sertifikası doğrulanır.

Kaynak sunucunuzda geçerli ve doğru yapılandırılmış bir sertifika varsa genellikle **Full (strict)** modu önerilir.

Yanlış SSL yapılandırması 525 veya 526 gibi hatalara neden olabilir. Bu hatalarla karşılaşırsanız kaynak sunucunuzun sertifikasını ve yapılandırmasını kontrol edin.

### Özellik 4: Önbellekleme ve Cache Rules

Önbellekleme, belirli kaynakların geçici olarak saklanmasını sağlar. Böylece her ziyaret sırasında bu kaynakların yeniden kaynak sunucudan alınması gerekmez.

Bu özellik web sitesinin performansını artırabilir ve sunucu üzerindeki yükü azaltabilir.

Cloudflare'da önbellek ayarlarını ve **Cache Rules** özelliğini kullanarak hangi kaynakların hangi koşullarda önbelleğe alınacağını belirleyebilirsiniz.

Dosyaları veya görselleri güncellediğiniz hâlde ziyaretçiler eski sürümü görüyorsa önbelleği temizleyebilirsiniz.

Şu bölüme gidin:

**Caching → Configuration → Purge Cache**

Ardından uygun önbellek temizleme seçeneğini belirleyin.

Dikkat: Giriş sayfalarını, alışveriş sepetlerini, kişisel sayfaları ve ödeme bilgileri içeren sayfaları dikkatli bir yapılandırma olmadan önbelleğe almayın.

### Özellik 5: DDoS Koruması ve Web Sitesi Güvenliği

DDoS saldırıları, çok sayıda istek göndererek bir web sitesini erişilemez hâle getirmeyi amaçlar.

Cloudflare, birçok DDoS saldırısı türünü tespit etmek ve etkilerini azaltmak için koruma mekanizmaları sunar.

Ayrıca kontrol panelindeki güvenlik olaylarını inceleyerek hangi isteklerin engellendiğini veya şüpheli olarak işaretlendiğini görebilirsiniz.

Bu koruma, web sitenizin erişilebilirliğini artırmaya yardımcı olur ancak tüm tehditlere karşı mutlak güvenlik garantisi vermez.

Bu nedenle kaynak sunucunuzu, yönetici hesaplarınızı ve web sitenizde kullandığınız uygulamaları da güvenli hâle getirmeniz önemlidir.

### Özellik 6: WAF (Web Uygulaması Güvenlik Duvarı)

Cloudflare WAF, web uygulamanız için risk oluşturabilecek HTTP isteklerini filtrelemenizi sağlar.

Aşağıdakiler de dahil olmak üzere çeşitli kötü amaçlı isteklerin tespit edilmesine veya engellenmesine yardımcı olabilir:

- SQL Injection saldırıları.
- XSS (Cross-Site Scripting) saldırıları.
- Şüpheli istekler.
- Bazı güvenlik açıklarını istismar etme girişimleri.

Cloudflare, yönetilen kurallar ve özel kurallar sunar.

**Managed Rules**, önceden hazırlanmış kural kümelerini kullanmanızı sağlar. **Custom Rules** ise filtreleme koşulları üzerinde daha fazla kontrol sunar.

Ayarlar web sitenizin ihtiyaçlarına göre düzenlenmelidir. Çok katı kurallar gerçek ziyaretçileri engelleyebilir veya bazı site özelliklerinin çalışmasını bozabilir.

### Özellik 7: Redirect Rules ve URL Yönlendirmeleri

Redirect Rules, ziyaretçileri bir URL adresinden başka bir URL adresine otomatik olarak yönlendirmenizi sağlar.

Bu özellik, web sitenizin yapısını değiştirdiğinizde, alan adınızı yenilediğinizde veya URL adreslerini standartlaştırmak istediğinizde kullanışlıdır.

En yaygın iki yönlendirme türü şunlardır:

- **301**: Kalıcı yönlendirme.
- **302**: Geçici yönlendirme.

Örneğin, eski bir sayfayı yeni bir URL adresine yönlendirerek 404 hatalarını önleyebilir ve ziyaretçilerin gezinmesini kolaylaştırabilirsiniz.

Yönlendirme döngülerini veya yanlış hedef adresleri önlemek için kuralları her zaman kontrol edin.

### Özellik 8: Analytics ve İstatistikler

Cloudflare Analytics, web sitenizin trafiği ve güvenliğiyle ilgili çeşitli verileri görüntülemenizi sağlar.

Şu bilgileri inceleyebilirsiniz:

- İstek sayısı.
- Aktarılan veri miktarı.
- Önbellekten sunulan kaynaklar.
- Güvenlik olayları.
- Trafikle ilgili bazı eğilimler.

Bu bilgiler, web sitenizin Cloudflare ağını nasıl kullandığını anlamanıza ve olası sorunları belirlemenize yardımcı olur.

Dikkat: Cloudflare Analytics, Google Analytics'in doğrudan yerine geçmez. İki hizmet aynı ölçümleri yapmaz ve istatistikleri birbirinden farklı olabilir.

### Özellik 9: Cloudflare Workers

Cloudflare Workers, geleneksel bir sunucuyu kendiniz yönetmek zorunda kalmadan Cloudflare ağı üzerinde kod çalıştırmanıza olanak tanır.

Bu özellik şu amaçlarla kullanılabilir:

- API oluşturmak.
- HTTP isteklerini işlemek.
- Özel iş mantığı eklemek.
- Yanıtları değiştirmek.
- Dağıtık hizmetler geliştirmek.

Bu sayede geliştiriciler belirli işlevleri kullanıcılara daha yakın noktalarda çalıştırabilir.

Kullanım limitleri ve sunulan özellikler, Cloudflare planına ve hizmet yapılandırmasına bağlıdır.

Resmî dokümantasyon:

[https://developers.cloudflare.com/workers/](https://developers.cloudflare.com/workers/)

### Özellik 10: Cloudflare Pages

Cloudflare Pages, statik web sitelerini ve ön uç uygulamalarını yayınlamaya olanak tanıyan bir platformdur.

Otomatik dağıtım süreçleri için GitHub deposuna bağlanabilir.

Genel işlem adımları şöyledir:

1. GitHub hesabınızı bağlayın.
2. Projenizin deposunu seçin.
3. Gerekirse derleme komutunu (Build command) yapılandırın.
4. Çıktı dizinini (Build output directory) belirtin.
5. Yayınlama işlemini başlatın.
6. Gerekirse özel alan adınızı yapılandırın.

Cloudflare Pages özellikle dokümantasyon siteleri, statik bloglar ve ön uç projeleri için uygundur.

Resmî dokümantasyon:

[https://developers.cloudflare.com/pages/](https://developers.cloudflare.com/pages/)

## 4. Yeni Başlayanlar İçin Önerilen Cloudflare Ayarları

Web sitenizi Cloudflare'a yeni bağladıysanız basit bir yapılandırmayla başlamanız daha iyi olacaktır.

Önerilen adımlar şunlardır:

1. Alan adınızı ekleyin ve ad sunucularının doğru yapılandırıldığını doğrulayın.
2. Özellikle web sitesi ve e-posta hizmetleriyle ilgili DNS kayıtlarını kontrol edin.
3. SSL/TLS ayarlarını kaynak sunucuda kurulu sertifikaya göre yapılandırın.
4. Desteklenen web sitesi kayıtları için Cloudflare proxy hizmetini etkinleştirin.
5. Statik kaynaklar için önbellekleme ayarlarını yapılandırın.
6. Güvenlik ve WAF ayarlarını gözden geçirin.
7. İstatistikleri ve güvenlik olaylarını takip edin.

Aynı anda çok fazla ayarı değiştirmekten kaçının. Böylece bir sorun ortaya çıktığında sorunun kaynağını belirlemek daha kolay olur.

## 5. Sık Karşılaşılan Cloudflare Sorunları ve Çözümleri

### Sorun 1: Cloudflare'a Bağlandıktan Sonra Web Sitesi Çalışmıyor

Olası nedenler:

- DNS kayıtları yanlış yapılandırılmıştır.
- Ad sunucularının yayılması henüz tamamlanmamıştır.
- Kaynak sunucunun IP adresi yanlıştır.
- Kaynak sunucu Cloudflare üzerinden gelen bağlantıları engelliyordur.

Çözümler:

1. DNS kayıtlarını kontrol edin.
2. Sunucunun IP adresinin doğru olduğundan emin olun.
3. Sunucunun güvenlik duvarı ayarlarını kontrol edin.
4. Cloudflare kontrol panelindeki bağlantı durumunu inceleyin.

### Sorun 2: 522 Hatası

522 hatası genellikle Cloudflare'ın kaynak sunucuyla gerekli süre içinde bağlantı kuramadığını gösterir.

Olası nedenler:

- Sunucu çevrim dışıdır veya aşırı yüklenmiştir.
- Güvenlik duvarı bağlantıları engelliyordur.
- Sunucu zamanında yanıt vermiyordur.
- Ağ yapılandırmasında bir sorun vardır.

Çözümler:

- Kaynak sunucunun çalıştığını kontrol edin.
- Güvenlik duvarı kurallarını inceleyin.
- Cloudflare IP adreslerinin engellenmediğinden emin olun.
- Sorun devam ederse barındırma sağlayıcınızla iletişime geçin.

### Sorun 3: 525 Hatası

525 hatası, Cloudflare ile kaynak sunucu arasındaki SSL el sıkışmasının başarısız olduğunu gösterir.

Çözümler:

- Sunucunun SSL sertifikasının doğru şekilde kurulduğunu kontrol edin.
- Sunucunun uyumlu bir TLS yapılandırmasını desteklediğinden emin olun.
- Cloudflare SSL/TLS ayarlarını inceleyin.
- Gerekirse barındırma sağlayıcınızla iletişime geçin.

### Sorun 4: Görseller veya Dosyalar Güncellenmiyor

Bu sorun genellikle önbellekleme ile ilgilidir.

Çözümler:

1. Cloudflare kontrol panelini açın.
2. Caching bölümüne gidin.
3. Purge Cache seçeneğini seçin.
4. İlgili önbelleği temizleyin.
5. Web sitesini yenileyerek sonucu kontrol edin.

### Sorun 5: Ücretsiz Plan Yeterli mi?

Kişisel bir web sitesi, blog veya küçük bir kurumsal site için Cloudflare'ın ücretsiz planı başlangıçta yeterli olabilir.

Bu plan DNS yönetimi, proxy, CDN ve bazı güvenlik özellikleri gibi temel işlevlere erişim sağlar.

Daha gelişmiş ihtiyaçları olan web siteleri; trafik hacmine, güvenlik gereksinimlerine ve ihtiyaç duydukları özelliklere bağlı olarak ücretli planları değerlendirebilir.

## 6. Cloudflare Resmî Kaynakları

Bilginizi geliştirmek ve en güncel talimatlara ulaşmak için aşağıdaki resmî kaynaklardan yararlanabilirsiniz:

- Resmî web sitesi: [https://www.cloudflare.com/](https://www.cloudflare.com/)
- Kontrol paneli: [https://dash.cloudflare.com/](https://dash.cloudflare.com/)
- Geliştirici dokümantasyonu: [https://developers.cloudflare.com/](https://developers.cloudflare.com/)
- DNS dokümantasyonu: [https://developers.cloudflare.com/dns/](https://developers.cloudflare.com/dns/)
- SSL/TLS dokümantasyonu: [https://developers.cloudflare.com/ssl/](https://developers.cloudflare.com/ssl/)
- WAF dokümantasyonu: [https://developers.cloudflare.com/waf/](https://developers.cloudflare.com/waf/)
- Workers dokümantasyonu: [https://developers.cloudflare.com/workers/](https://developers.cloudflare.com/workers/)
- Pages dokümantasyonu: [https://developers.cloudflare.com/pages/](https://developers.cloudflare.com/pages/)

Alan adınızın veya sunucunuzun önemli ayarlarını değiştirmeden önce resmî dokümantasyonu incelemeniz önerilir.

## 7. Sonuç: Cloudflare Yeni Başlayanlar İçin Uygun mu?

Cloudflare, web sitelerinin performansını, güvenliğini ve yönetimini geliştirmeye yardımcı olan birçok araç sunar.

Bu rehberde ele alınan 10 özellik, yeni başlayan kullanıcıların temel ihtiyaçlarını kapsar:

1. DNS Yönetimi.
2. CDN ve web sitesi hızlandırma.
3. SSL/TLS ve HTTPS.
4. Cache ve Cache Rules.
5. DDoS Koruması.
6. WAF.
7. Redirect Rules.
8. Analytics.
9. Workers.
10. Pages.

Başlangıçta bu özelliklerin tamamını öğrenmeniz gerekmez. Önce alan adınızı bağlayın, DNS kayıtlarını kontrol edin, HTTPS yapılandırmasını tamamlayın ve temel özellikleri etkinleştirin. Daha sonra gelişmiş araçları aşamalı olarak öğrenebilirsiniz.

## 8. Çevrim İçi Ödeme ve TRON Enerji Hizmetleri

💳 **CoinePay – Sanal Kart Hizmetleri**

Çevrim içi ödeme seçeneklerini ve sanal kart hizmetlerini keşfedin.

👉 [https://www.coinepay.net/register?referrer=RFGSSDZ9](https://www.coinepay.net/register?referrer=RFGSSDZ9)

⚡ **TRXAPI – TRON Enerji Kiralama**

Uyumlu blockchain işlemleri için TRON enerji kiralama hizmetlerini keşfedin.

👉 [https://login.trxapi.io/energy](https://login.trxapi.io/energy)

Not: CoinePay ve TRXAPI bağımsız üçüncü taraf hizmetleridir. Cloudflare ürünleri değildir ve Cloudflare ile resmî bir iş ortaklıkları bulunmamaktadır.

## 9. Kaynaklar

- Cloudflare: [https://www.cloudflare.com/](https://www.cloudflare.com/)
- Resmî dokümantasyon: [https://developers.cloudflare.com/](https://developers.cloudflare.com/)
- DNS: [https://developers.cloudflare.com/dns/](https://developers.cloudflare.com/dns/)
- SSL/TLS: [https://developers.cloudflare.com/ssl/](https://developers.cloudflare.com/ssl/)
- WAF: [https://developers.cloudflare.com/waf/](https://developers.cloudflare.com/waf/)
- Analytics: [https://developers.cloudflare.com/analytics/](https://developers.cloudflare.com/analytics/)
- Workers: [https://developers.cloudflare.com/workers/](https://developers.cloudflare.com/workers/)
- Pages: [https://developers.cloudflare.com/pages/](https://developers.cloudflare.com/pages/)

