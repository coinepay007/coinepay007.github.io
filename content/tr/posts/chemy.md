---
title: "Alchemy Kayıt Rehberi: Nasıl Hesap Oluşturulur ve API Key Alınır?"
slug: chemy
date: 2026-11-02
draft: false
---
# Alchemy Kayıt Rehberi: Nasıl Hesap Oluşturulur ve API Key Alınır?

Alchemy, Web3 geliştiricileri için tasarlanmış bir blockchain altyapı platformudur. Blockchain ağlarına bağlanmak, RPC endpoint'lerine erişmek, zincir üzerindeki verileri (on-chain) sorgulamak ve merkeziyetsiz uygulamalar geliştirmek için çeşitli araçlar ve hizmetler sunar.

Bir Web3 cüzdanı, NFT projesi, blockchain gezgini veya akıllı sözleşme uygulaması geliştiriyorsanız, projenizi bir blockchain ağına bağlamak için Alchemy hesabına ve API Key'e ihtiyacınız olabilir.

Bu rehberde Alchemy'ye nasıl kayıt olacağınızı, nasıl uygulama oluşturacağınızı, API Key'inizi nasıl alacağınızı ve bağlantının doğru çalışıp çalışmadığını nasıl kontrol edeceğinizi adım adım öğreneceksiniz.

Blockchain geliştirme ve çevrimiçi ödeme araçlarını araştırırken CoinePay ve TRXAPI gibi bağımsız hizmetlerle de karşılaşabilirsiniz. CoinePay sanal kart hizmetleri sunarken TRXAPI, TRON ağında enerji kiralama hizmeti sağlar. Bu iki hizmetin de Alchemy ile resmi bir bağlantısı veya ortaklığı yoktur.

💳 **CoinePay – Sanal Kart Hizmetleri**

Çevrimiçi ödeme seçeneklerini ve sanal kart hizmetlerini keşfedin.

👉 [https://www.coinepay.net/register?referrer=RFGSSDZ9](https://www.coinepay.net/register?referrer=RFGSSDZ9)

⚡ **TRXAPI – TRON Enerji Kiralama**

Uyumlu blockchain işlemleri için TRON enerji kiralama hizmetlerini keşfedin.

👉 [https://login.trxapi.io/energy](https://login.trxapi.io/energy)

## 1. Alchemy Nedir?

Alchemy, geliştiricilerin kendi blockchain düğümlerini oluşturup yönetmelerine gerek kalmadan uygulamalarını farklı blockchain ağlarına bağlamalarına yardımcı olan bir altyapı platformudur.

Alchemy sayesinde geliştiriciler:

- Desteklenen blockchain ağlarına bağlanabilir.
- RPC API'leri aracılığıyla blockchain verilerine erişebilir.
- Cüzdan ve işlem bilgilerini sorgulayabilir.
- NFT ile ilgili verileri alabilir.
- Blockchain etkinliklerini ve işlemlerini takip edebilir.
- Web3 uygulamaları geliştirebilir ve yönetebilir.

Alchemy, özellikle yeni başlayanlar için hazır altyapı ve API hizmetleri sunarak blockchain geliştirme sürecini kolaylaştırır.

## 2. Alchemy'ye Kaydolmadan Önce Nelere İhtiyacınız Var?

Alchemy hesabı oluşturmadan önce aşağıdaki hazırlıkları yapmanız önerilir.

### Geçerli Bir E-posta Adresi

Kayıt olmak, hesabınızı doğrulamak veya önemli güvenlik bildirimlerini almak için bir e-posta adresine ihtiyacınız olabilir.

Kayıt süreci boyunca bu e-posta adresine erişebildiğinizden emin olun.

### Kararlı Bir İnternet Bağlantısı

Alchemy çevrimiçi bir platformdur. Web sitesine, kontrol paneline ve geliştirici araçlarına erişmek için internet bağlantısı gerekir.

### Kullanacağınız Blockchain Ağını Belirleyin

Hazır bir geliştirme projeniz varsa hangi blockchain ağına bağlanmak istediğinizi önceden belirleyin.

Örneğin:

- Ethereum Mainnet: Ethereum'un ana ağı.
- Ethereum Sepolia: Ethereum test ağı.
- Base: Ethereum teknolojisi üzerine kurulu bir blockchain ağı.

Blockchain geliştirmeye yeni başlıyorsanız, mevcut özellikleri öğrenmek için öncelikle bir test ağı kullanabilirsiniz.

## 3. Alchemy Hesabı Nasıl Oluşturulur?

### Adım 1: Alchemy Resmi Web Sitesini Açın

Alchemy'nin resmi web sitesini ziyaret edin:

[https://www.alchemy.com/](https://www.alchemy.com/)

Sayfada Sign Up, Sign In veya Get Started seçeneklerini bulun.

Hesap oluşturma işlemine başlamak için kayıt seçeneğine tıklayın.

### Adım 2: Hesabınızı Oluşturun

Kayıt sayfasında gösterilen talimatları izleyin.

Mevcut seçeneklere bağlı olarak e-posta adresinizle kayıt olabilir veya desteklenen üçüncü taraf giriş yöntemlerinden birini kullanabilirsiniz.

E-posta ile kayıt olmayı tercih ederseniz:

1. E-posta adresinizi girin.
2. İstenen hesap bilgilerini doldurun.
3. E-posta adresinizi doğrulamak veya ek güvenlik kontrollerini tamamlamak için verilen talimatları izleyin.
4. Kayıt işlemi tamamlandıktan sonra hesabınıza giriş yapın.

Kayıt yöntemleri ve doğrulama gereksinimleri zaman içinde değişebilir. Her zaman Alchemy'nin resmi web sitesinde gösterilen talimatları takip edin.

### Adım 3: Alchemy Dashboard'a Girin

Kayıt işlemi tamamlandıktan sonra Alchemy kontrol panelini açın:

[https://dashboard.alchemy.com/](https://dashboard.alchemy.com/)

Dashboard; uygulamalarınızı, API Key'lerinizi, blockchain ağlarınızı ve hizmet ayarlarınızı yönetebileceğiniz ana bölümdür.

Yeni bir kullanıcıysanız Alchemy hesabınız için varsayılan bir uygulama ve API Key otomatik olarak oluşturmuş olabilir.

Yeni bir uygulama oluşturmadan önce mevcut uygulamalarınızı kontrol edin. Varsayılan uygulamayı doğrudan kullanmanız mümkün olabilir.

## 4. Alchemy'de Uygulama (App) Nasıl Oluşturulur?

Alchemy uygulaması, projenizi seçtiğiniz blockchain ağlarına bağlar ve istek göndermek için gerekli erişim bilgilerini ve endpoint adreslerini sağlar.

Farklı projeler veya geliştirme ortamları için ayrı uygulamalar oluşturabilirsiniz.

### Adım 1: Apps Bölümünü Açın

Alchemy Dashboard'a giriş yapın.

Ekip menüsünden Team Overview bölümünü açın ve ardından Apps sekmesini seçin.

Create new app seçeneğini bulun ve tıklayın.

### Adım 2: Uygulama Bilgilerini Girin

Alchemy, yeni uygulamanızı yapılandırmanızı isteyecektir.

Mevcut ayarlar şunları içerebilir:

App Name: Projenizi tanımlayacak bir isim girin. Örneğin, My Web3 Project.

Description: Uygulamanın amacını açıklayan kısa bir metin ekleyin. Bu alan isteğe bağlı olabilir.

Chains: Uygulamanızın erişmesi gereken blockchain ağlarını seçin.

Services: Projenizin ihtiyaç duyduğu hizmetleri seçin.

Ethereum tabanlı bir uygulama geliştiriyorsanız ilgili Ethereum ağını seçin.

Yalnızca öğrenmek veya test yapmak istiyorsanız öncelikle bir test ağı kullanmayı değerlendirin.

### Adım 3: Uygulamayı Oluşturun

Uygulama ayarlarınızı kontrol edin.

Uygulama adının, seçilen ağların ve etkinleştirilen hizmetlerin doğru olduğundan emin olun.

İşlemi tamamlamak için Create App seçeneğine tıklayın.

Uygulama oluşturulduktan sonra Alchemy sizi uygulamanın ayrıntılar sayfasına yönlendirecektir.

## 5. Alchemy API Key Nasıl Alınır?

API Key, uygulamanızla ilişkili Alchemy hizmetlerine gönderilen isteklerin kimlik doğrulamasında kullanılır.

API Key'inizi bulmak için aşağıdaki adımları izleyin.

### Adım 1: Uygulamanızı Açın

Alchemy Dashboard içerisindeki Apps bölümüne gidin.

Yeni oluşturduğunuz uygulamayı bulun ve ayrıntılar sayfasını açmak için uygulama adına tıklayın.

### Adım 2: API Key'inizi Kopyalayın

Uygulama ayrıntıları sayfasında, genellikle sağ üst tarafta bulunan API Key alanını bulun.

Anahtarı kopyalamak için kopyalama düğmesine tıklayın.

Geliştirme projenizde kullanmak üzere anahtarı güvenli bir yerde saklayın.

Gerçek API Key'inizi herkese açık web sitelerinde, herkese açık GitHub depolarında veya yetkisiz kişilerin erişebileceği başka yerlerde paylaşmayın.

### Adım 3: API Endpoint Adresini Bulun

API Key'inizi aldıktan sonra uygulama ayrıntıları sayfasındaki Endpoints sekmesini açın.

Bu bölümde etkinleştirilmiş blockchain ağlarına ait HTTP ve WebSocket endpoint adreslerini görebilirsiniz.

Örneğin, Ethereum Mainnet için HTTP RPC endpoint adresi genellikle şu biçimdedir:

[https://eth-mainnet.g.alchemy.com/v2/YOUR_API_KEY](https://eth-mainnet.g.alchemy.com/v2/YOUR_API_KEY)

YOUR_API_KEY bölümünü Alchemy Dashboard'dan kopyaladığınız API Key ile değiştirin.

Her blockchain ağının endpoint adresi farklıdır. Her zaman seçtiğiniz ağa karşılık gelen adresi kullanın.

## 6. Alchemy API Key Nasıl Test Edilir?

API Key'inizi aldıktan sonra yapılandırmanın doğru olduğunu kontrol etmek için basit bir istek göndermeniz önerilir.

Bu örnekte Ethereum Mainnet ve en son blok numarasını sorgulamak için eth_blockNumber JSON-RPC yöntemi kullanılacaktır.

### Adım 1: RPC Endpoint Adresini Hazırlayın

Aşağıdaki biçimi kullanın:

[https://eth-mainnet.g.alchemy.com/v2/YOUR_API_KEY](https://eth-mainnet.g.alchemy.com/v2/YOUR_API_KEY)

YOUR_API_KEY bölümünü gerçek API Key'inizle değiştirin.

### Adım 2: curl Kullanarak İstek Gönderin

Bilgisayarınızda curl yüklüyse bir terminal açın ve aşağıdaki komutu çalıştırın:

```
curl https://eth-mainnet.g.alchemy.com/v2/YOUR_API_KEY \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_blockNumber","params":[],"id":1}'
```

Komutu çalıştırmadan önce YOUR_API_KEY bölümünü kendi API Key'inizle değiştirmeyi unutmayın.

### Adım 3: Yanıtı Kontrol Edin

API Key ve endpoint doğru yapılandırılmışsa aşağıdakine benzer bir JSON yanıtı almanız gerekir:

```
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "0x..."
}
```

result alanı, blok numarasını onaltılık formatta içerir.

İstek bir hata döndürürse API Key'in doğru olduğunu, ilgili ağın etkinleştirildiğini ve istek formatının geçerli olduğunu kontrol edin.

## 7. Alchemy API Key Kullanırken Dikkat Edilmesi Gerekenler

API Key, Alchemy hizmetlerine erişmek için kullanılan önemli bir kimlik bilgisidir. Hesabınızı ve uygulamalarınızı korumak için aşağıdaki güvenlik önerilerine uyun.

### API Key'inizi Herkese Açık Şekilde Paylaşmayın

Gerçek API Key'inizi herkese açık kod depolarında, çevrimiçi forumlarda veya herkesin erişebileceği web sayfalarında paylaşmayın.

Geliştirme projelerinde anahtarınızı ortam değişkenlerinde veya güvenli yapılandırma dosyalarında saklamayı tercih edin.

### API Keys ve Access Keys Arasındaki Farkı Anlayın

Alchemy, farklı amaçlar için çeşitli kimlik bilgileri sunar.

Uygulamaya ait API Key, genellikle uygulamayla ilişkili RPC endpoint'lerine ve desteklenen API'lere erişmek için kullanılır.

Access Keys ise belirli kimlik doğrulama ve yönetim senaryolarında kullanılır. Ayrıca ek izin kontrolleri sağlayabilir.

Bu iki kimlik bilgisinin birbirinin yerine kullanılabileceğini varsaymayın. Kullanmadan önce Alchemy'nin resmi belgelerini inceleyin.

### Doğru Blockchain Ağını Seçin

Uygulamanızın gerçekten kullanmak istediğiniz ağ için yapılandırıldığından emin olun.

Örneğin:

- Ethereum Mainnet, Ethereum'un üretim ağı için kullanılır.
- Ethereum Sepolia, test işlemleri için kullanılır.
- Base, ayrı bir blockchain ağıdır.

Yanlış ağa ait bir endpoint kullanmak beklenmeyen sonuçlara veya hatalara neden olabilir.

### Kullanımı ve Ücretleri Takip Edin

Alchemy farklı kullanım planları sunar. Mevcut özellikler, kullanım sınırları ve fiyatlar değişebilir.

Alchemy'yi üretim ortamındaki bir uygulamada kullanmadan önce Dashboard üzerinden mevcut planınızı, kullanım limitlerinizi ve faturalandırma bilgilerinizi kontrol edin.

Diğer blockchain hizmetlerinin de tamamen farklı amaçlara sahip olabileceğini unutmayın. Örneğin TRXAPI, TRON enerji kiralama hizmetlerine odaklanırken Alchemy blockchain geliştirme altyapısı sağlar.

TRXAPI resmi web sitesi:

[https://login.trxapi.io/energy](https://login.trxapi.io/energy)

## 8. Alchemy Kaydı Hakkında Sık Sorulan Sorular

### S1: Alchemy'ye Kayıt Olmak Ücretsiz mi?

Hesap oluşturmak ve platformu kullanmak iki farklı konudur.

Alchemy farklı kullanım planları sunar. Ücretsiz özellikler, istek limitleri ve fiyatlar mevcut plana bağlıdır.

Hesap oluşturmanız, tüm API isteklerinin ve hizmetlerin ücretsiz olduğu anlamına gelmez.

En güncel bilgiler için resmi fiyatlandırma sayfasını ziyaret edin:

[https://www.alchemy.com/pricing](https://www.alchemy.com/pricing)

### S2: Kayıt Olduktan Sonra API Key'imi Bulamazsam Ne Yapmalıyım?

Öncelikle Alchemy Dashboard'a giriş yapın ve Apps bölümünü açın.

Hesabınızda varsayılan bir uygulama olup olmadığını kontrol edin.

Bir uygulama varsa ayrıntılar sayfasını açarak API Key'inizi bulun.

Kullanılabilir bir uygulama yoksa Create new app seçeneğini seçin ve yapılandırma işlemini tamamlayın.

### S3: Birden Fazla Alchemy API Key Oluşturabilir miyim?

Farklı projeler veya geliştirme ortamları için birden fazla uygulama oluşturabilir ve bunların kimlik bilgilerini ayrı ayrı yönetebilirsiniz.

Örneğin geliştirme, test ve üretim ortamları için farklı uygulamalar kullanabilirsiniz.

Bu yöntem projelerin düzenlenmesini ve kullanımın ayrı ayrı takip edilmesini kolaylaştırır.

### S4: API Key'imi Diğer Geliştiricilerle Paylaşabilir miyim?

Gerekmedikçe API Key'inizi paylaşmanız önerilmez.

Diğer geliştiricilerin Alchemy hizmetlerinize erişmesi gerekiyorsa ekip izinlerini ve güvenli kimlik bilgisi yönetimi yöntemlerini kullanın.

Kişisel veya proje erişim bilgilerinizi herkese açık alanlarda paylaşmayın.

### S5: Alchemy API Key'im Neden Çalışmıyor?

En yaygın nedenler şunlardır:

1. API Key yanlış kopyalanmış olabilir.
2. RPC endpoint adresi yanlış olabilir.
3. Gerekli blockchain ağı etkinleştirilmemiş olabilir.
4. İstek yöntemi veya parametreleri geçersiz olabilir.
5. Uygulamanın kullanım veya izin kısıtlamaları olabilir.
6. İnternet bağlantısında bir sorun yaşanıyor olabilir.

Öncelikle uygulama ayarlarınızı ve endpoint yapılandırmanızı kontrol edin. Sorun giderme talimatları için Alchemy'nin resmi belgelerine de başvurabilirsiniz.

## 9. Sonuç: Alchemy Kaydınızı Tamamlayın ve API Key Alın

Alchemy'ye kaydolmak ve API Key almak, Web3 uygulamaları geliştirmek isteyen programcılar için önemli bir ilk adımdır.

Tüm süreç şu şekilde özetlenebilir:

1. Alchemy resmi web sitesini ziyaret edin.
2. Bir hesap oluşturun ve giriş yapın.
3. Alchemy Dashboard'u açın.
4. Projeniz için ayrı bir yapılandırmaya ihtiyacınız varsa yeni bir uygulama oluşturun.
5. Gerekli blockchain ağlarını ve hizmetleri seçin.
6. Uygulama ayrıntıları sayfasını açın ve API Key'inizi kopyalayın.
7. Doğru RPC adresini bulmak için Endpoints sekmesini kontrol edin.
8. Yapılandırmanın çalıştığını doğrulamak için bir test isteği gönderin.

Yeni başlayanların basit bir blockchain veri sorgusuyla başlaması önerilir. API Key'lerin, RPC endpoint'lerinin ve ağ yapılandırmasının nasıl çalıştığını öğrendikten sonra daha gelişmiş Web3 projelerine geçebilirsiniz.

Blockchain ile ilgili başka hizmetleri de araştırıyorsanız, bunların farklı kullanım amaçlarını anlamanız önemlidir. CoinePay sanal kart hizmetleri sunarken TRXAPI, TRON enerji kiralama hizmeti sağlar. Bu hizmetler bağımsızdır ve Alchemy ile resmi bir bağlantıları yoktur.

CoinePay resmi web sitesi:

[https://www.coinepay.net/register?referrer=RFGSSDZ9](https://www.coinepay.net/register?referrer=RFGSSDZ9)

TRXAPI resmi web sitesi:

[https://login.trxapi.io/energy](https://login.trxapi.io/energy)

## 10. Alchemy Resmi Web Sitesi ve Dokümantasyonu

En güncel kayıt talimatları, API yapılandırma adımları ve teknik bilgiler için aşağıdaki resmi Alchemy kaynaklarını inceleyebilirsiniz.

Alchemy resmi web sitesi:

[https://www.alchemy.com/](https://www.alchemy.com/)

Alchemy Dashboard:

[https://dashboard.alchemy.com/](https://dashboard.alchemy.com/)

API Key oluşturma:

[https://www.alchemy.com/docs/create-an-api-key](https://www.alchemy.com/docs/create-an-api-key)

Alchemy Hızlı Başlangıç Rehberi:

[https://www.alchemy.com/docs/alchemy-quickstart-guide](https://www.alchemy.com/docs/alchemy-quickstart-guide)

Access Keys oluşturma:

[https://www.alchemy.com/docs/how-to-create-access-keys](https://www.alchemy.com/docs/how-to-create-access-keys)

Bu kaynaklar uygulama oluşturma, API Key yönetimi, endpoint yapılandırması ve API istekleri gönderme hakkında ek bilgiler sağlar.

---

**Google Sites Yayınlama Önerileri**

Ana makale başlığını H1 olarak ayarlayın.

Ana bölümler için H2, alt başlıklar için H3 kullanın.

Okuyucuların komutları kolayca kopyalayabilmesi için kod örneklerini kod blokları içinde tutun.

Temiz ve kolay bir okuma deneyimi sağlamak için açık paragraflar ve açıklayıcı başlıklar kullanın. Gereksiz tablolardan kaçının.

Bu makaledeki CoinePay ve TRXAPI referansları bağımsız hizmetleri tanıtmaktadır. Bu hizmetleri Alchemy'nin resmi iş ortakları veya Alchemy ile entegre ürünler olarak göstermeyin.