# Proje Bilgisi Mimarisi Yönetmeliği

Ulus projelerden oluşmaktadır. Bu projelerin kendileri hakkında yeterli bilgiyi belirtmeleri gerekir.
Bu yönetmelik, projelerin kendileri hakkındaki bilgileri nasıl sunacağını belirler.

## [Versiyonlandırma Sistemleri](https://en.wikipedia.org/wiki/Version_control)

Tüm projeler zaman içerisinde değişebilir. Bu değişim bir versiyon kontrol sistemi tarafından takip altına alınmalıdır.

Ulus'un versyion kontrol sistemi seçimi [Git](https://en.wikipedia.org/wiki/Git)'tir. Ana nedeni herkes tarafından kullanılmasıdır.

## Bilginin Biçimi

Projelerin tüm bilgileri "özel bir program kullanmadan", insanların anlayabileceği bir formatta olmalıdır.
Yani, veri versiyon kontrol sistemine bir versiyon olarak kayıt edilirken PDF gibi tiplerde olmaz.

Ulus, tüm metin işleri için [Markdown](https://en.wikipedia.org/wiki/Markdown) kullanır(yönetmelik yazım yönetmeliği).
Bu nedenle projelerin tüm bilgilerinin mümkünse Markdown tipinde depolanması gerekir.
[CommonMark](https://commonmark.org/) ve [GFM](https://en.wikipedia.org/wiki/Markdown#GFM) üzerinden gidilmesi gerekir.

## Kök Markdown Dosyaları

Projenin sunulduğu her ortamda gösterilmesi zorunlu olan kök(root) markdown(aka .md) dosyaları vardır.
Bu dosyalar alakadar bilginin olası beklentisi nedeniyle yazılır. Yani bir dosya bağlam gereği beklenmiyorsa yazılmasına gerek yoktur.

Tüm dosyalar giriş(aka landing) sayfasında konumları ile belirtilmelidir.

### Tanımlı Kök Markdown Dosyaları

Aşağıda, projelerin kök dizininde kullanabileceği tüm tanımlı `.md` dosyaları listelenmektedir.
Her dosya; açıklaması ve hangi bağlamlara ait olduğunu belirten etiketlerle birlikte verilmiştir.

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
- `#makine` — İnsan için değil, yazılım araçları ve yapay zeka ajanları için yazılan dosyalar

---

| Dosya | Açıklama | Etiketler |
| --- | --- | --- |
| `README.md` | Projenin giriş noktası; amaç, kapsam, iletişim ve genel tanıtım | `#evrensel` |
| `SUMMARY.md` | Projenin alandan bağımsız, teknik olmayan bir okuyucuya hitap eden kapsamlı özeti. Bir kılavuz veya el kitabı niteliği taşır; projeyi bütünüyle kavramak isteyen herkes için yazılır | `#evrensel` |
| `CHANGELOG.md` | Versiyon bazlı değişikliklerin kısa ve yapılandırılmış kaydı | `#evrensel` `#operasyon` |
| `HISTORY.md` | Projenin genel tarihsel seyri; önemli kararlar ve dönüm noktaları. `CHANGELOG.md` versiyon odaklıyken `HISTORY.md` anlam ve bağlam odaklıdır | `#evrensel` `#operasyon` |
| `GLOSSARY.md` | Projeye özgü terimlerin, kısaltmaların ve kavramların tanımları | `#evrensel` |
| `FAQ.md` | Sık sorulan sorular ve yanıtları | `#evrensel` `#topluluk` |
| `MANIFESTO.md` | Projenin varoluş gerekçesi, kapsamı, sınırları ve uzun vadeli hedefleri. `SCOPE.md`, `ROADMAP.md`, `MISSION.md`, `VISION.md`, `VALUES.md` ve `CHARTER.md` bu dosya tarafından kapsanır | `#yönetim` `#raporlama` |
| `GOVERNANCE.md` | Karar alma yapısı, yetki seviyeleri ve liderlik düzeni; roller ile sorumluluklar; politika ve yönetmelik çerçevesi; onay mekanizmaları; olay müdahalesi ve yükseltme yolları; gözden geçirme ve denetim süreçleri; raporlama ve değerlendirme prosedürleri. `ROLES.md`, `MAINTAINERS.md`, `AUTHORS.md`, `ACKNOWLEDGEMENTS.md`, `POLICY.md`, `REGULATION.md`, `INCIDENT.md`, `REVIEW.md`, `APPROVAL.md`, `ROLLBACK.md`, `OFFBOARDING.md`, `REPORT.md`, `ASSESSMENT.md` ve `RATIONALE.md` bu dosya tarafından kapsanır | `#yönetim` `#yönetmelik` `#operasyon` `#raporlama` |
| `CODE_OF_CONDUCT.md` | Davranış standartları, etik ilkeler, gizlilik kuralları ve katılım rehberi. `ETHICS.md`, `PRIVACY.md` ve `ONBOARDING.md` bu dosya tarafından kapsanır | `#yönetmelik` `#topluluk` |
| `CONTRIBUTING.md` | Projeye nasıl katkı sağlanacağının teknik ve süreç odaklı rehberi | `#yönetmelik` `#topluluk` |
| `COMPLIANCE.md` | Bu projeye veya protokole uyumlu sayılmak için yerine getirilmesi gereken koşullar; işlevsel ve düzenleyici gereksinimler. `REQUIREMENTS.md` bu dosya tarafından kapsanır | `#yönetmelik` `#hukuki` |
| `LICENSE.md` | Kullanım hakları ve lisans koşulları | `#hukuki` |
| `LEGAL.md` | Hukuki sorumluluk reddi beyanları, resmi bildirimler ve dış kaynak atıfları. `DISCLAIMER.md`, `NOTICE.md` ve `REFERENCES.md` bu dosya tarafından kapsanır | `#hukuki` |
| `ARCHITECTURE.md` | Sistem yapısı ve tasarım genel görünümü; tasarım kararları ve gerekçeleri; süreçler, iş akışları ve yaşam döngüleri; şemalar, arayüz tanımları ve entegrasyon detayları. `DESIGN.md`, `PROCESS.md`, `WORKFLOW.md`, `LIFECYCLE.md`, `SCHEMA.md`, `API.md`, `CHECKLIST.md` ve `INTEGRATIONS.md` bu dosya tarafından kapsanır. `CONFIGURATION.md`, `DEPENDENCIES.md`, `DEPLOYMENT.md`, `MIGRATION.md` ve `VERSIONING.md` bağlam gerektirdiğinde ayrı tutulabilir | `#teknik` |
| `PERFORMANCE.md` | Performans kriterleri, ölçüm yöntemleri, hedefler ve kıyaslamalar. `BENCHMARKS.md` bu dosya tarafından kapsanır | `#teknik` |
| `SECURITY.md` | Güvenlik politikaları ve güvenlik açığı bildirimi; tehdit modeli ve saldırı yüzeyi analizi; erişim kontrolü ve rol tabanlı yetkilendirme kuralları; kimlik doğrulama ve şifreleme standartları; denetim izi ve kayıt politikası; veri işleme ve saklama prosedürleri. `THREAT-MODEL.md`, `ACCESS-CONTROL.md`, `AUTHENTICATION.md`, `AUTHORIZATION.md`, `ENCRYPTION.md`, `AUDIT.md` ve `DATA-HANDLING.md` bu dosya tarafından kapsanır | `#güvenlik` |
| `AGENTS.md` | Yapay zeka kodlama ajanlarına ve yazılım araçlarına proje hakkında yönlendirici bağlam sağlar; hangi dosyalara dokunulacağını, hangi komutların çalıştırılacağını ve projeye özgü kuralları tanımlar. `robots.txt`'nin web tarayıcıları için ne ise bu dosya da AI ajanları için odur. Amp, Codex, Cursor, Devin, Gemini CLI, GitHub Copilot ve VS Code tarafından desteklenen açık bir standarttır. `CLAUDE.md`, `GEMINI.md`, `.cursorrules` gibi araç bazlı dosyalar bu dosya tarafından kapsanır | `#makine` |