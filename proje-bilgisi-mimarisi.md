# Proje Bilgisi Mimarisi Yönetmeliği

Ulus projelerden oluşmaktadır. Bu projeler kollektif olarak geliştirilir ve çoğu zaman halka açıktır.
Hem katkıda bulunanlar hemde gözlemciler için, Ulus'un tüm projeleri dökümante edilmelidir.
Dökümantasyonun yanı sıra, tüm proje süreci mümkün olduğu kadar kayıt altına alınmalıdır.
Bu yönetmelik, bir proje hakkındaki bilginin kayıt edilmesi üstüne kurallar içerir.
Ulus'un tüm projelerinde bu yönetmeliğin belirlediği standartlar uygulanır.

## [Versiyonlandırma Sistemleri](https://en.wikipedia.org/wiki/Version_control)

Projeler zaman içerisinde değişebilir. Bu değişim bir versiyon kontrol sistemi tarafından takip altına alınmalı.

Projelerin başlangıçlarından itibaren kayıt altına alınması bir seyir defteri mantığı görür.
Bu mantık sayesinde eskiden nelerin yapıldığı, hangi konularda hangi kararların verildiği gözlemlenebilir olur.

Ayrıca versiyon kontorl sistemleri çoğu zaman "brancing" yani dallandırma konseptini destekler.
Bu da aynı anda projenin farklı versiyonları ve özellikleri üstünde ciddi kollektif çalışma potansiyeli demektir.

Ulus'un versyion kontrol sistemi seçimi [Git](https://en.wikipedia.org/wiki/Git)'tir.
Git ana olarak yazılım geliştirme tasarlanmış için olsa da, bir versiyon kontrol sistemi olarak ciddi kabul görmüştür ve kendini kanıtlamıştır.
İnsan dili odaklı(dökümantasyon vb) çalışmalarda çıkarabileceği sorunların çözüldüğü başka bir alternatif bulunmamaktadır.
Herşeye rağmen Git güçlü bir versiyon kontorl sistemidir, ve Ulus dijital ortamda tuttuğu tüm metin tabanlı projelerinde Git kullanmalıdır.

## Bilginin Biçimi

Projelerin tüm bilgileri "özel bir program kullanmadan", insanların anlayabileceği bir formatta olmalıdır.
Yani; veri, [versiyon kontrol sistemi](#versiyonlandırma-sistemleri)ne bir versiyon olarak kayıt edilirken PDF gibi tiplerde olamaz.
PDF, JPG, PNG, MP3, MP4 ve OBJ gibi dosya tipleri makina hedefli bir tiptedir ve saf hali ile insanlar okuyamaz.

Bir dosyanın erişimi için bir programın kullanılmasının zorunlu olması erişimi katmanlandırır.
Bu durum [şeffaflık](./şeffaflık-ve-berraklık.md) ideallerimize uygun değil.

Ulus, tüm metin işleri için [Markdown](https://en.wikipedia.org/wiki/Markdown) kullanır.
Bu durum [Yönetmelik Yazım Yönetmeliği](./yönetmelik-yazım-yönetmeliği.md)'nde belirtişmiştir.
Bu nedenle projelerin tüm bilgilerinin Markdown tipinde olması gerekir.
Sırası ile, [CommonMark](https://commonmark.org/) ve [GFM](https://en.wikipedia.org/wiki/Markdown#GFM) standartları tercih edilir.

## Kök Markdown Dosyaları

Projenin sunulduğu her ortamda gösterilmesi zorunlu olan kök(root) markdown(aka .md) dosyaları vardır.
Bu dosyalar alakadar bilginin olası beklentisi nedeniyle yazılır. Yani bir dosya bağlam gereği beklenmiyorsa yazılmasına gerek yoktur.

Burada standartize edilmiş bazı dosyalar, başka dosyalar yerine tercih edilmişir.
Bu nedenle DESIGN.md kullanmak yerine ARCHITECTURE.md kullanırız.
Böylece az dosya ile çok iş başarabiliriz.
Az olan dosya sayısı düşünme ve planlama miktarını da azaltır, bu da hız ve kolaylık demektir.

Kapsayıcı, çatı dosyalar konsepti kapsanan dosyaların kullanımını yasaklamaz.
İhtiyaç durumunda kapsayıcı dosyadan ayrılabilecek dosyalar kapsayıcı dosya ile birlikte listelenir.
Yinede ayırmamayı öneriyoruz; kapsanan dosyaların açıklamalarını bulunmuyor, bu kafa karışıklığına neden olabilir.

Tüm kök dosyaları giriş(aka landing, README) dosyasında konumları ile belirtilmelidir.

Aşağıda, projelerin kök dizininde kullanılabilecek tüm tanımlı bilgi dosyaları listelenmektedir.
*Dosyaların isimlerinin üstüne tıklayarak örnek dosyalara gidilebilir.*

### [README.md](./README.md)

İsmi İngilizce "read" yani "oku", ve "me" yani "beni" kelimelerinin birleşimidir.
Projeye bakan kişinin dikkatini çekmek, burdan başla demek için kullanılır.
Yani projenin giriş noktası, ilk izlenim dosyasıdır.

Dosya mimarisi şu şekildedir:

1. Dosya başlığı'nın altında/içinde projenin ne olduğu açıklanır.
2. "Ne İşe Yarar" altında projenin ne amaçlar ile kullanılmak üzere hazırlandığı yazar.
3. "Nasıl Kullanılır" altında basit bir kullanım kılavuzu bulunur. Ayrıca bir eğitici görevi de görmelidir.
4. "Diğer Konular" atlında diğer tüm bilgi dosyaları `- [Dosya](./DOSYA.md)` şeklinde listelenmelidir.

---

**Bu yönetmeliği uygulayan tüm projeler bu dosyanın dosya başlığı altında, internet adresi ile birlikte bu yönetmeliği kullandığını belirtmelidir.**

Okuyan veya düzenleyen kişinin beklentisinin yanı sıra, denetim ve takip için bu yol kullanılır. Bir kök bilgi dosyası olarak atıf edilen her bir dosya bu yönetmelik tarafından kapsanır.

Proje bilgisi mimarisi için bu yönetmeliğin kullanıldığı belirtilmezse, veya alakadar kök bilgi dosyası README tarafından atıf edilmiyorsa bu yönetmelik geçersizdir.

### [SUMMARY.md](./SUMMARY.md)

İsmi, "özet" anlamına gelir.
Projenin tüm bilgi dosyaları kapsamında yazılır.

Bir el kitabı(aka handbook) amacı görür.
Projeyi kullanıcıya açıklamayı hedefler.

Projenin açıklaması ([README.md](#readmemd)), mimarisi ([ARCHITECTURE.md](#architecturemd)), manifestosu ([MANIFESTO.md](#manifestomd)) ve güvenlik sistemleri ([SECURITY.md](#securitymd)) gibi konuları anlatımda karışık bir şekilde sunar.

Dosyanın belli bir mimarisi olmak zorunda değildir, anlatıcı ne anlatmak isterse o yazılmalıdır.

### [CHANGELOG.md](./CHANGELOG.md)

Versiyon bazlı değişikliklerin kısa ve yapılandırılmış kaydı. Her versiyon için ne değişti, ne eklendi, ne kaldırıldı bilgisini tarihsel sırayla tutar.

### [HISTORY.md](./HISTORY.md)

Projenin genel tarihsel seyri; önemli kararlar, dönüm noktaları ve geçirilen dönüşümleri anlatır.
[CHANGELOG.md](#changelogmd) versiyon ve değişiklik odaklıyken bu dosya anlam, bağlam ve gerekçe odaklıdır.

### [GLOSSARY.md](./GLOSSARY.md)

İsmi, "sözlük" anlamına gelir.
Projeye özgü terimlerin, kısaltmaların ve kavramların tanımlarını içerir.
Farklı geçmişlerden gelen okuyucuların ortak bir dil kurabilmesi için yazılır.

### [FAQ.md](./FAQ.md)

İsmi İngilizce "Frequently Asked Questions" yani "Sık Sorulan Sorular" ifadesinin kısaltmasıdır.
Projeyle ilgili tekrar eden sorular ile yanlış anlaşılmaya açık noktaları doğrudan ele alır.

### [MANIFESTO.md](./MANIFESTO.md)

Projenin varoluş gerekçesi, temel ilkeleri, kapsamı, sınırları ve uzun vadeli hedefleri. Projenin neden var olduğunu ve nereye gideceğini net biçimde ortaya koyar.

**Şu dosyaları kapsar:**

- `SCOPE.md`
- `ROADMAP.md`
- `MISSION.md`
- `VISION.md`
- `VALUES.md`
- `CHARTER.md`

### [GOVERNANCE.md](./GOVERNANCE.md)

Karar alma yapısı, yetki seviyeleri ve liderlik düzeni; roller ile sorumluluklar; politika ve yönetmelik çerçevesi; onay mekanizmaları; olay müdahalesi ve yükseltme yolları; gözden geçirme ve denetim süreçleri; raporlama ve değerlendirme prosedürleri. Projenin nasıl yönetildiğini ve kimin neye yetkili olduğunu tanımlar.

**Şu dosyaları kapsar:**

- `ROLES.md`
- `MAINTAINERS.md`
- `AUTHORS.md`
- `ACKNOWLEDGEMENTS.md`
- `POLICY.md`
- `REGULATION.md`
- `INCIDENT.md`
- `REVIEW.md`
- `APPROVAL.md`
- `ROLLBACK.md`
- `OFFBOARDING.md`
- `REPORT.md`
- `ASSESSMENT.md`
- `RATIONALE.md`

### [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md)

Projede beklenen davranış standartları, etik ilkeler, gizlilik anlayışı ve katılım rehberini içerir.
Hem dışarıdan katılanlara hem de içerideki üyelere yönelik yazılır.

**Şu dosyaları kapsar:**

- `ETHICS.md`
- `PRIVACY.md`
- `ONBOARDING.md`

### [CONTRIBUTING.md](./CONTRIBUTING.md)

Projeye nasıl katkı sağlanacağının teknik ve süreç odaklı rehberidir.
Katkı türleri, iş akışı, inceleme süreci ve beklentiler burada açıklanır.
[CODE_OF_CONDUCT.md](#code_of_conductmd)'den farklı olarak davranış değil, eylem odaklıdır.

### [COMPLIANCE.md](./COMPLIANCE.md)

Bu projeye veya protokole uyumlu sayılmak için yerine getirilmesi gereken koşulları; işlevsel, teknik ve düzenleyici gereksinimleri tanımlar.
"Bu projeyle uyumlu olmak için ne yapmanız gerekir?" sorusunu yanıtlar.

**Şu dosyaları kapsar:**

- `REQUIREMENTS.md`

### [LICENSE](./LICENSE)

Projenin kullanım hakları ve lisans koşullarını içerir.
Projenin nasıl kullanılabileceğini, dağıtılabileceğini ve türetilebileceğini hukuki çerçevede tanımlar.

### [LEGAL.md](./LEGAL.md)

Hukuki sorumluluk reddi beyanları, resmi bildirimler ve dış kaynak atıflarını içerir.
[LICENSE](#license)'dan farklı olarak kullanım hakları değil, sorumluluk sınırları ve yasal uyarıları kapsar.

**Şu dosyaları kapsar:**

- `DISCLAIMER.md`
- `NOTICE.md`
- `REFERENCES.md`

### [ARCHITECTURE.md](./ARCHITECTURE.md)

Sistem yapısı ve tasarım genel görünümü; tasarım kararları ve gerekçeleri; bileşenler arası ilişkiler; süreçler, iş akışları ve yaşam döngüleri; veri şemaları, arayüz tanımları ve entegrasyon detayları. Projeyi teknik olarak kavramak isteyen herkesin başvurduğu ana teknik belgedir.

**Şu dosyaları kapsar:**

- `DESIGN.md`
- `PROCESS.md`
- `WORKFLOW.md`
- `LIFECYCLE.md`
- `SCHEMA.md`
- `API.md`
- `CHECKLIST.md`
- `INTEGRATIONS.md`

**Gerektiğinde ayırılabilecek kapsanan dosyalar:**

- `CONFIGURATION.md`
- `DEPENDENCIES.md`
- `DEPLOYMENT.md`
- `MIGRATION.md`
- `VERSIONING.md`

### [PERFORMANCE.md](./PERFORMANCE.md)

Projenin performans kriterleri, ölçüm yöntemleri, hedef değerler ve kıyaslama sonuçlarını belgeler.
Her projenin bir performans beklentisi vardır; bu dosya o beklentileri ve nasıl ölçüldüğünü ortaya koyar.

**Şu dosyaları kapsar:**

- `BENCHMARKS.md`

### [SECURITY.md](./SECURITY.md)

Projenin güvenlik politikaları ve güvenlik açığı bildirimi; tehdit modeli ve saldırı yüzeyi analizi; erişim kontrolü ve rol tabanlı yetkilendirme kuralları; kimlik doğrulama ve şifreleme standartları; denetim izi ve kayıt politikası; veri işleme ve saklama prosedürleri.

**Şu dosyaları kapsar:**

- `THREAT-MODEL.md`
- `ACCESS-CONTROL.md`
- `AUTHENTICATION.md`
- `AUTHORIZATION.md`
- `ENCRYPTION.md`
- `AUDIT.md`
- `DATA-HANDLING.md`

### [AGENTS.md](./AGENTS.md)

Yapay zeka kodlama ajanlarına ve yazılım araçlarına proje hakkında yönlendirici bağlam sağlar.
Hangi dosyalara dokunulacağını, hangi komutların çalıştırılacağını, projeye özgü kuralları ve genel proje bağlamını tanımlar.
`robots.txt`'nin web tarayıcıları için ne ise bu dosya da AI ajanları için odur. Amp, Codex, Cursor, Devin, Gemini CLI, GitHub Copilot ve VS Code tarafından desteklenen açık bir standarttır. Web ortamında yayımlanan projeler için Git reposunun değil web sunucusunun kök dizinine ait olan `llms.txt` standardı da değerlendirilebilir.

**Şu dosyaları kapsar:**

- `CONTEXT.md`
- `CLAUDE.md`
- `GEMINI.md`
- `.cursorrules`
