# Proje Bilgisi Mimarisi Yönetmeliği

Ulus projelerden oluşmaktadır. Bu projelerin kendileri hakkında yeterli bilgiyi belirtmeleri gerekir.
Bu yönetmelik, projelerin kendileri hakkındaki bilgileri nasıl sunacağını belirler.

## [Versiyonlandırma Sistemleri](https://en.wikipedia.org/wiki/Version_control)

Tüm projeler zaman içerisinde değişebilir. Bu değişim bir versiyon kontrol sistemi tarafından takip altına alınmalıdır.

Ulus'un versiyon kontrol sistemi seçimi [Git](https://en.wikipedia.org/wiki/Git)'tir. Bu seçimin ana nedeni piyasada herkesin kullanması ve alternatiflerine karşı daha kullanışlı olmasıdır.

## Bilginin Biçimi

Projelerin tüm bilgileri "üçüncü taraf bir program kullanmadan" insanların anlayabileceği bir formatta olmalıdır.
Yani veri, versiyon kontrol sistemine yeni bir versiyon olarak kayıt edilirken PDF gibi okunabilmesi için üçüncü taraf bir program gerektiren tiplerde olmaz.

Ulus, tüm metin işleri için [Markdown](https://en.wikipedia.org/wiki/Markdown) kullanır (yönetmelik yazım yönetmeliği).
Bu nedenle projelerin tüm bilgilerinin mümkünse Markdown tipinde depolanması gerekir.
[CommonMark](https://commonmark.org/) ve [GFM](https://en.wikipedia.org/wiki/Markdown#GFM) üzerinden gidilmesi gerekir.

## Kök Markdown Dosyaları

Projenin sunulduğu her ortamda gösterilmesi zorunlu olan kök (root) markdown (.md) dosyaları vardır.
Bu dosyalar ilgili bilginin olası beklentisi nedeniyle yazılır. Yani bir dosyaya ihtiyaç duyulması beklenmiyorsa yazılmasına gerek yoktur.

Tüm dosyalar giriş (landing) sayfasında konumları ile belirtilmelidir.

Aşağıda projelerin kök dizininde kullanabileceği tüm tanımlı `.md` dosyaları listelenmektedir.
Her dosya, açıklaması ve hangi bağlamlara ait olduğunu belirten etiketlerle birlikte verilmiştir.

**Etiketler:**

- `#evrensel` — Her projede bulunması beklenen dosyalar
- `#yönetim` — Organizasyonel yapı, otorite ve karar alma
- `#yönetmelik` — Kurallar, normlar ve uyumluluk
- `#teknik` — Sistem tasarımı, altyapı ve teknik detaylar
- `#operasyon` — Süreçler, işleyiş ve günlük prosedürler
- `#raporlama` — Değerlendirme, planlama ve belgeleme çıktıları
- `#topluluk` — Katılım, katkı ve iletişim
- `#güvenlik` — Güvenlik politikaları, tehdit ve erişim yönetimi
- `#hukuki` — Lisans, sorumluluk ve yasal bildirimler
- `#makineler` — İnsanlar için değil; yazılım araçları, tarayıcılar ve yapay zeka ajanları için yazılan dosyalar

---

| Dosya | Açıklama | Etiketler |
| --- | --- | --- |
| `README.md` | Projenin giriş noktası. Projenin ne olduğunu, ne işe yaradığını, nasıl kullanılacağını, iletişim bilgilerini ve genel tanıtımı içerir. Projeye ilk kez bakan herkesin okuduğu ilk dosyadır | `#evrensel` |
| `SUMMARY.md` | Projenin alandan ve teknik bilgiden bağımsız, herkese hitap eden kapsamlı özeti. Bir el kitabı veya kılavuz niteliği taşır; projeyi derinlemesine değil, yüzeysel olarak kavramak isteyen okuyucu için yazılır | `#evrensel` |
| `CHANGELOG.md` | Versiyon bazlı değişikliklerin kısa ve yapılandırılmış kaydı. Her versiyon için ne değişti, ne eklendi, ne kaldırıldı bilgisini tarihsel sırayla tutar | `#evrensel` `#operasyon` |
| `HISTORY.md` | Projenin genel tarihsel seyri; önemli kararlar, dönüm noktaları ve geçirilen dönüşümler. `CHANGELOG.md` versiyon ve değişiklik odaklıyken `HISTORY.md` anlam, bağlam ve gerekçe odaklıdır | `#evrensel` `#operasyon` |
| `GLOSSARY.md` | Projeye özgü terimlerin, kısaltmaların ve kavramların tanımları. Farklı geçmişlerden gelen okuyucuların ortak bir dil kurabilmesi için yazılır | `#evrensel` |
| `FAQ.md` | Projeyle ilgili sık sorulan sorular ve yanıtları. Tekrar eden sorular ile yanlış anlaşılmaya açık noktaları doğrudan ele alır | `#evrensel` `#topluluk` |
| `MANIFESTO.md` | Projenin varoluş gerekçesi, temel ilkeleri, kapsamı, sınırları ve uzun vadeli hedefleri. Projenin neden var olduğunu ve nereye gideceğini net biçimde ortaya koyar. `SCOPE.md`, `ROADMAP.md`, `MISSION.md`, `VISION.md`, `VALUES.md` ve `CHARTER.md` bu dosya tarafından kapsanır | `#yönetim` `#raporlama` |
| `GOVERNANCE.md` | Karar alma yapısı, yetki seviyeleri ve liderlik düzeni; roller ile sorumluluklar; politika ve yönetmelik çerçevesi; onay mekanizmaları; olay müdahalesi ve yükseltme yolları; gözden geçirme ve denetim süreçleri; raporlama ve değerlendirme prosedürleri. Projenin nasıl yönetildiğini ve kimin neye yetkili olduğunu tanımlar. `ROLES.md`, `MAINTAINERS.md`, `AUTHORS.md`, `ACKNOWLEDGEMENTS.md`, `POLICY.md`, `REGULATION.md`, `INCIDENT.md`, `REVIEW.md`, `APPROVAL.md`, `ROLLBACK.md`, `OFFBOARDING.md`, `REPORT.md`, `ASSESSMENT.md` ve `RATIONALE.md` bu dosya tarafından kapsanır | `#yönetim` `#yönetmelik` `#operasyon` `#raporlama` |
| `CODE_OF_CONDUCT.md` | Projede beklenen davranış standartları, etik ilkeler, gizlilik anlayışı ve katılım rehberi. Hem dışarıdan katılanlara hem de içerideki üyelere yönelik yazılır. `ETHICS.md`, `PRIVACY.md` ve `ONBOARDING.md` bu dosya tarafından kapsanır | `#yönetmelik` `#topluluk` |
| `CONTRIBUTING.md` | Projeye nasıl katkı sağlanacağının teknik ve süreç odaklı rehberi. Katkı türleri, iş akışı, inceleme süreci ve beklentiler burada açıklanır. `CODE_OF_CONDUCT.md`'den farklı olarak davranış değil, eylem odaklıdır | `#yönetmelik` `#topluluk` |
| `COMPLIANCE.md` | Bu projeye veya protokole uyumlu sayılmak için yerine getirilmesi gereken koşullar; işlevsel, teknik ve düzenleyici gereksinimler. "Bu projeyle uyumlu olmak için ne yapmanız gerekir?" sorusunu yanıtlar. `REQUIREMENTS.md` bu dosya tarafından kapsanır | `#yönetmelik` `#hukuki` |
| `LICENSE.md` | Projenin kullanım hakları ve lisans koşulları. Projenin nasıl kullanılabileceğini, dağıtılabileceğini ve türetilebileceğini hukuki çerçevede tanımlar | `#hukuki` |
| `LEGAL.md` | Hukuki sorumluluk reddi beyanları, resmi bildirimler ve dış kaynak atıfları. `LICENSE.md`'den farklı olarak kullanım hakları değil, sorumluluk sınırları ve yasal uyarıları içerir. `DISCLAIMER.md`, `NOTICE.md` ve `REFERENCES.md` bu dosya tarafından kapsanır | `#hukuki` |
| `ARCHITECTURE.md` | Sistem yapısı ve tasarım genel görünümü; tasarım kararları ve gerekçeleri; bileşenler arası ilişkiler; süreçler, iş akışları ve yaşam döngüleri; veri şemaları, arayüz tanımları ve entegrasyon detayları. Projeyi teknik olarak kavramak isteyen herkesin başvurduğu ana teknik belgedir. `DESIGN.md`, `PROCESS.md`, `WORKFLOW.md`, `LIFECYCLE.md`, `SCHEMA.md`, `API.md`, `CHECKLIST.md` ve `INTEGRATIONS.md` bu dosya tarafından kapsanır. `CONFIGURATION.md`, `DEPENDENCIES.md`, `DEPLOYMENT.md`, `MIGRATION.md` ve `VERSIONING.md` bağlam gerektirdiğinde ayrı tutulabilir | `#teknik` |
| `PERFORMANCE.md` | Projenin performans kriterleri, ölçüm yöntemleri, hedef değerler ve kıyaslama sonuçları. Her projenin bir performans beklentisi vardır; bu dosya o beklentileri ve nasıl ölçüldüğünü belgeler. `BENCHMARKS.md` bu dosya tarafından kapsanır | `#teknik` |
| `SECURITY.md` | Projenin güvenlik politikaları ve güvenlik açığı bildirimi; tehdit modeli ve saldırı yüzeyi analizi; erişim kontrolü ve rol tabanlı yetkilendirme kuralları; kimlik doğrulama ve şifreleme standartları; denetim izi ve kayıt politikası; veri işleme ve saklama prosedürleri. `THREAT-MODEL.md`, `ACCESS-CONTROL.md`, `AUTHENTICATION.md`, `AUTHORIZATION.md`, `ENCRYPTION.md`, `AUDIT.md` ve `DATA-HANDLING.md` bu dosya tarafından kapsanır | `#güvenlik` |
| `AGENTS.md` | Yapay zeka kodlama ajanlarına ve yazılım araçlarına proje hakkında yönlendirici bağlam sağlar. Hangi dosyalara dokunulacağını, hangi komutların çalıştırılacağını, projeye özgü kuralları ve genel proje bağlamını tanımlar. `robots.txt`'nin web tarayıcıları için ne ise bu dosya da AI ajanları için odur. `CONTEXT.md` ile örtüştüğü için bu dosya tarafından kapsanır. `CLAUDE.md`, `GEMINI.md`, `.cursorrules` gibi araç bazlı dosyalar da bu dosya tarafından kapsanır. Amp, Codex, Cursor, Devin, Gemini CLI, GitHub Copilot ve VS Code tarafından desteklenen açık bir standarttır. Web ortamında yayımlanan projeler için Git reposunun değil web sunucusunun kök dizinine ait olan `llms.txt` standardı da değerlendirilebilir | `#makineler` |
