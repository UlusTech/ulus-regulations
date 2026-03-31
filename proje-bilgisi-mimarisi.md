# Proje Bilgisi Mimarisi Yönetmeliği

Ulus projelerden oluşmaktadır. Bu projeler kolektif olarak geliştirilir ve çoğu zaman halka açıktır.
Hem katkıda bulunanlar hem de gözlemciler için Ulus'un tüm projeleri dökümante edilmelidir.
Dökümantasyonun yanı sıra tüm proje süreci mümkün olduğu kadar kayıt altına alınmalıdır.
Bu yönetmelik, bir proje hakkındaki bilginin kayıt edilmesi üstüne kurallar içerir.
Ulus'un tüm projelerinde bu yönetmeliğin belirlediği standartlar uygulanır.

## [Versiyonlandırma Sistemleri](https://en.wikipedia.org/wiki/Version_control)

Projeler zaman içerisinde değişebilir.
Bu değişim bir versiyon kontrol sistemi tarafından takip altına alınmalı.

Projelerin başlangıçlarından itibaren kayıt altına alınması bir seyir defteri mantığı görür.
Bu mantık sayesinde eskiden nelerin yapıldığı, hangi konularda hangi kararların verildiği gözlemlenebilir olur.

Ayrıca versiyon kontrol sistemleri çoğu zaman "branching" yani dallandırma konseptini destekler.
Bu da aynı anda projenin farklı versiyonları ve özellikleri üstünde ciddi kolektif çalışma potansiyeli demektir.

Ulus'un versiyon kontrol sistemi seçimi [Git](https://en.wikipedia.org/wiki/Git)'tir.
Git ana olarak yazılım geliştirme için tasarlanmış olsa da bir versiyon kontrol sistemi olarak ciddi kabul görmüştür ve kendini kanıtlamıştır.
İnsan dili odaklı (dökümantasyon vb.) çalışmalarda çıkarabileceği sorunların çözüldüğü başka bir alternatif bulunmamaktadır.
Her şeye rağmen Git, güçlü bir versiyon kontrol sistemidir ve Ulus dijital ortamda tuttuğu tüm metin tabanlı projelerinde Git kullanmalıdır.

## Bilginin Biçimi

Projelerin tüm bilgileri "özel bir program kullanmadan" insanların anlayabileceği bir formatta olmalıdır.
Yani veri, [versiyon kontrol sistemi](#versiyonlandırma-sistemleri)ne bir versiyon olarak kayıt edilirken PDF gibi tiplerde olamaz.
PDF, JPG, PNG, MP3, MP4 ve OBJ gibi dosya tipleri makine hedefli bir tiptedir ve saf hali ile insanlar tarafından okunamaz.

Bir dosyanın okunması için özel bir programın kullanılmasının zorunlu olması erişimi katmanlandırır.
Bu durum [şeffaflık](./şeffaflık-ve-berraklık.md) ideallerimize uygun değil.

Ulus, tüm metin işleri için [Markdown](https://en.wikipedia.org/wiki/Markdown) kullanır.
Bu durum [Yönetmelik Yazım Yönetmeliği](./yönetmelik-yazım-yönetmeliği.md)'nde belirtişmiştir.
Bu nedenle projelerin tüm bilgilerinin Markdown tipinde olması gerekir.
Sırası ile [CommonMark](https://commonmark.org/) ve [GFM](https://en.wikipedia.org/wiki/Markdown#GFM) standartları tercih edilir.

## Kök Markdown Dosyaları

Projenin sunulduğu her ortamda gösterilmesi zorunlu olan kök (root) Markdown (.md) dosyaları vardır.
Bu dosyalar alakadar bilginin olası beklentisi nedeniyle yazılır.
Yani bir dosya bağlam gereği beklenmiyorsa yazılmasına gerek yoktur.

Burada standartize edilmiş bazı dosyalar, başka dosyalar yerine tercih edilmişir.
Bu nedenle DESIGN.md kullanmak yerine ARCHITECTURE.md kullanırız.
Böylece az dosya ile çok iş başarabiliriz.
Az olan dosya sayısı düşünme ve planlama miktarını da azaltır, bu da hız ve kolaylık demektir.

Kapsayıcı çatı dosyalar konsepti kapsanan dosyaların kullanımını yasaklamaz.
İhtiyaç durumunda kapsayıcı dosyadan ayrılabilecek dosyalar kapsayıcı dosya ile birlikte listelenir.
Yine de ayırmamayı öneriyoruz; kapsanan dosyaların açıklamaları bulunmuyor, bu durum kafa karışıklığına neden olabilir.

Tüm kök dosyaları giriş (landing yani README) dosyasında konumları ile belirtilmelidir.

Aşağıda, projelerin kök dizininde kullanılabilecek tüm tanımlı bilgi dosyaları listelenmektedir.
*Dosyaların isimlerinin üstüne tıklayarak örnek dosyalara gidilebilir.*

### [README.md](./README.md)

İsmi İngilizce "read" yani "oku" ve "me" yani "beni" kelimelerinin birleşimidir.
Projeye bakan kişinin dikkatini çekmek, burdan başla demek için kullanılır.
Yani projenin giriş noktası, ilk izlenim dosyasıdır.

Dosya mimarisi şu şekildedir:

1. Dosya başlığının altında/içinde projenin ne olduğu açıklanır.
2. "Ne İşe Yarar" altında projenin ne amaçlar ile kullanılmak üzere hazırlandığı yazar.
3. "Nasıl Kullanılır" altında basit bir kullanım kılavuzu bulunur. Ayrıca bir eğitici görevi de görmelidir.
4. "Diğer Konular" altında diğer tüm bilgi dosyaları `- [Dosya](./DOSYA.md)` şeklinde listelenmelidir.

---

**Bu yönetmeliği uygulayan tüm projeler bu dosyanın dosya başlığı altında internet adresi ile birlikte bu yönetmeliği kullandığını belirtmelidir.**

Okuyan veya düzenleyen kişinin beklentisinin yanı sıra denetim ve takip için bu yol kullanılır. Bir kök bilgi dosyası olarak atıf edilen her bir dosya bu yönetmelik tarafından kapsanır.

Proje bilgisi mimarisi için bu yönetmeliğin kullanıldığı belirtilmezse, veya alakadar kök bilgi dosyası README tarafından atıf edilmiyorsa bu yönetmelik geçersizdir.

Bu yönetmeliğin kullanıldığını belirtmek için şu kullanılabilir:

```markdown
Bu proje [Ulus](https://ulusgroup.org)'un [Proje Bilgi Mimarisi](https://github.com/UlusTech/ulus-regulations/blob/main/proje-bilgisi-mimarisi.md) yönetmeliğine göre yazılmıştır.
```

### [SUMMARY.md](./SUMMARY.md)

İsmi, "özet" anlamına gelir.
Projenin tüm bilgi dosyaları kapsamında yazılır.

Bir el kitabı (handbook) amacı görür.
Projeyi kullanıcıya açıklamayı hedefler.

Projenin açıklaması ([README.md](#readmemd)), mimarisi ([ARCHITECTURE.md](#architecturemd)), manifestosu ([MANIFESTO.md](#manifestomd)) ve güvenlik sistemleri ([SECURITY.md](#securitymd)) gibi konuları anlatımda karışık bir şekilde sunar.

Dosyanın belli bir mimarisi olmak zorunda değildir, anlatıcı ne anlatmak isterse o yazılmalıdır.

### [CHANGELOG.md](./CHANGELOG.md)

İsmi "change" yani "değişim" ve "log" yani "kayıt" kelimelerinin birleşimidir ve "Seyir Defteri" gibi bir anlam taşır.

Versiyon bazlı değişikliklerin kısa ve yapılandırılmış kayıt defteri.
Her versiyon için ne değişti, ne eklendi, ne kaldırıldı gibi bilgileri tarihsel sırayla tutar.

### [HISTORY.md](./HISTORY.md)

İsmi "Tarih" veya "Geçmiş" anlamına gelir.

Projede önemli kararlar verildiğinde, veya önemli bir sürüme/versiyona varıldığında bu dosya dahilinde kayıt alınır.
Anlatım çoğu zaman [CHANGELOG.md](#changelogmd)'ye atıfta bulunarak yapılır.

[CHANGELOG.md](#changelogmd)'nin aksine her bir versiyonda yazılmaz.
Sadece önemli veya büyük olan gelişmeler yazılır.

Bu dosya sürümler ile değil, bir hikaye anlatımı tipinde yazılır.

Projenin anlam ve bağlamının takip edilebilmesi için kullanılır.

**Şu dosyaları kapsar:**

- `RATIONALE.md`: Sebep ve gerekçeler bu dosyada anlatılır.

### [GLOSSARY.md](./GLOSSARY.md)

İsmi, "sözlük" anlamına gelir.
Projeye özgü terimlerin, kısaltmaların ve kavramların tanımlarını içerir.

Farklı geçmişlerden gelen okuyucuların ortak bir dil kurabilmesi için yazılır.

Her bir kelime bir başlık olarak yazılmalıdır.
Bu, projeye özel terminolojilerin başka dosyalardan atıf edilebilmesini sağlar.

**Örnek kullanım:**

```markdown
# Lorem Ipsum

[Yönetmelikler](./GLOSSARY.md/yonetmelik) Ulus'un yapı taşlarıdır.
```

### [FAQ.md](./FAQ.md)

İsmi İngilizce "Frequently Asked Questions" yani "Sıkça Sorulan Sorular" ifadesinin kısaltmasıdır.

Projeyle ilgili tekrar eden sorular ile yanlış anlaşılmaya açık noktaları doğrudan ele alır.

Aşırı kısa cevaplar verilmelidir.
Mümkün olan yerlerde "daha fazla detay için X.md dosyasını okuyun" gibi yönlendirmeler bulundurmalıdır.

### [MANIFESTO.md](./MANIFESTO.md)

Manifesto; bir kişinin, grubun veya hareketin inançlarını, amaçlarını ve ilkelerini kamuoyuna açıkça ilan ettiği yazılı bildirgedir.
Kelime İtalyanca "manifesto"dan gelir, o da Latince "manifestus" (açık, aşikar) kökünden türemiştir.

Projelerin içerikleri kadar arkasındaki fikirler, idealler de önemlidir.
Bu dosya, bu proje üstünde çalışan kişilerin idealleri ve motivasyonlarını, manifestolarını gösterir.

**Bu dosya şu dosyaları kapsar:**

- `SCOPE.md`: Projenin neyi hedeflediği ve hangi alanı kapsadığı bu dosyada belirtilir.
- `MISSION.md`: Görev veya amaç genelde maifestonun bir parçasıdır.
- `VISION.md`: Vizyon manifestonun bir parçasıdır.
- `VALUES.md`: Nelere değer verildiği ve nelerin idealize edildi manifesto konseptinin bir parçasıdır.

### [ROADMAP.md](./ROADMAP.md)

İsminin anlamı; "road" yani "yol", "map" yani "harita" anlamına gelen kelimelerin birleşimi olan "Yol haritası"'dır.

Projenin önündeki hedeflenen şeyler bu dosyada yazılır.
Bir özelliğin planlanması bu dosyaya yazılması demektir.
Bu dosya geçmişi tutmaz, sadece geleceğe bakar.

"Ne yapmak istiyoruz" konseptinde bir dosyadır.

### [GOVERNANCE.md](./GOVERNANCE.md)

İsim, "yönetişim" veya "yönetim" gibi anlamlara denk gelir.
Çoğu zaman "hükümet" anlamına gelen "government" kelimesi ile karıştırılır, ama burada "yönetim işleri" olarak kullanılır.

Bu dosya, projede yönetimsel yapının nasıl olduğunu anlatır.
Kim ne yapar, süreçler nasıl işler; öğrenmek isteyenlerin bakacağı yerdir.

**Bu dosyada şunlar yer alabilir:**

1. Kim: Roller, yetkiler, hiyerarşi veya paralel düzen
2. Ne: Politikalar ve karar alma yapısı
3. Süreç: Onay, olay müdahalesi, gözden geçirme mekanizmaları
4. İşletim: Raporlama, değerlendirme, offboarding

**Şu dosyaları kapsar:**

- *Kim:*
  - `ROLES.md`: Roller ve yetki seviyeleri bu dosyada tanımlanabilir.
  - `MAINTAINERS.md`: Sorumlu geliştirici gruplar veya kişiler burada listelenir.
  - `AUTHORS.md`: Projeyi oluşturan ya da düzenleyenlerin bilgisi bu dosyada bulunur.
  - `ACKNOWLEDGEMENTS.md`: Katkıda bulunanların tanınması bu dosyada yer alır.
- *Ne:*
  - `POLICY.md`: Proje politikası bu dosyada belirlenir.
- *Süreç:*
  - `INCIDENT.md`: Olay müdahalesi ve yükseltme yolları bu dosyada açıklanır.
  - `REVIEW.md`: Gözden geçirme ve denetim süreçleri bu dosyada yer alır.
  - `APPROVAL.md`: Onay mekanizmaları bu dosyada tanımlanır.
  - `ROLLBACK.md`: Geri alma prosedürleri bu dosyada açıklanır.
- *İşletim:*
  - `OFFBOARDING.md`: Ayrılış süreçleri bu dosyada tanımlanır.
  - `REPORT.md`: Raporlama prosedürleri bu dosyada yer alır.
  - `ASSESSMENT.md`: Değerlendirme süreçleri bu dosyada açıklanır.

### [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md)

İsmi, "code" yani "kural" ve "conduct" yani "davranış" kelimelerinden oluşur.
Davranış kuralları veya sözleşmesi anlamına gelir.

Bu dosya projenin sosyal kurallarını içerir.
Cinsel içerikli ögelerin veya zorbalığın yasaklanması gibi konularda kullanılır.
Yani davranış standartlarını belirler.

Bu projede çalışan kişilerin bazı etik konularda ortak bir yolu kabul etmesi için vardır.
Etik ilkeler, gizlilik anlayışı gibi konulara değinir.

Bu dosya bir katılım rehberi görevi de görür, projeye yeni katılan kişilerin okuması için idealize edilmiştir.
Proje ile alakalı tüm çalışmalarda etkilidir.  

Hem dışarıdan katılanlara hem de içerideki üyelere yönelik yazılır.

**Şu dosyaları kapsar:**

- `ETHICS.md`: Etik ilkeler davranış kurallarının fikir temelini oluşturur.
- `PRIVACY.md`: Gizlilik anlayışı davranış standartlarının bir parçasıdır.
- `ONBOARDING.md`: Davranış kuralları projeye yeni katılanların ilk okuması gereken belgedir.

### [CONTRIBUTING.md](./CONTRIBUTING.md)

İsmi, "katkıda bulunmak" anlamına gelir.
Projeye katkıda bulunmak isteyen kişilere bir rehber olması için yazılır.

Çoğu zaman ana yazım nedeni, projede çalışmak isteyen insanlara detayları sunmaktır.
Bu nedenle tekniktir, süreç odaklıdır.

**Şunları içerebilir:**

- Katkı türleri
- İş akışı (workflow)
- İnceleme süreci ve katkılara karşı beklentiler

[CODE_OF_CONDUCT.md](#code_of_conductmd)'den farklı olarak davranış değil, eylem odaklıdır.
Projedeki katkı ve çalışma kültürüne değinir.

### [COMPLIANCE.md](./COMPLIANCE.md)

İsmi, "uyum" ve "itaat" gibi anlamlara denk gelir.
Projeye veya protokole uymak veya itaat etmek için koşulları bulundurur.

Bir proje veya protokol tam olarak uygulanmasa bile çalışabilir.
Bu dosya minimum uyumluluk gereksinimlerini belirtir.
Uyumluluk seviyeleri belirleyip bu seviyeler üstünden yargılara varılabilmesini sağlayabilir.

Çoğu zaman örnekler veya direkt "bu uyumlu" gibi listeler bulundurur.
Özellikle protokollerde "Implementations" yani "Uygulamalar" olarak görülür.
Bu listeler hem bu projeyi, hem de uyumlu olan projeyi öne çıkarmak için kullanılabilir.
Topluluğun büyümesi için önemli bir şeydir.

**Şu dosyaları kapsar:**

- `REQUIREMENTS.md`: Projenin gereksinimleri bu dosyada belirlenir, çoğu zaman ikinci bir dosyaya gerek olmaz.

### [LICENSE](./LICENSE)

İsmi, "Lisans" anlamına gelir.
Projenin kullanım hakları ve lisans koşullarını içerir.
Projenin nasıl kullanılabileceğini, dağıtılabileceğini ve türetilebileceğini hukuki çerçevede tanımlar.

Bu dosya `.md` uzantısına sahip değildir ve olmamalıdır.
Otomatik sistemler çoğu zaman düz "LICENSE" ismini arar, bu uyumluğun kaybı lisans ihlallerine neden olabilir.

Lisans projenin [manifestosu](#manifestomd)nun bir parçasıdır.
Proje ne kadar kullanıma açık olursa o kadar yüksek potansiyele sahiptir.
Projeleri kısıtlamak teoride artılara sahip olsa da pratikte bir o kadar çok şeyi de kötü etkiler.
Bire bir tekrardan dağıtmanın yani başka bir deyişle redistribute etmenin yasak olduğu lisansları öneririz.

*Her ne kadar önermesek de lisansları bir kurum yönetmediği için istediğiniz lisansı kendiniz yazabilirsiniz.*
*Ama bu çoğu zaman kötü bir fikirdir, yasal bilgi eksikliği ve bilinmeyen bir lisansa karşı toplulukta oluşabilecek negatif hissiyatlar örnek sonuçlardır.*

<https://spdx.org/licenses/>, <https://license.md/> veya <https://choosealicense.com/> adreslerini kullanarak lisansları inceleyebilirsiniz.

### [LEGAL.md](./LEGAL.md)

İsmi, "hukuki" veya "yasal" anlamına gelir.

Projenin hukuki bilgilerini içerir.

**Bu dosyada şunlar yer alır:**

- Sorumluluk sınırları: projenin kullanımından doğabilecek zararlara karşı ne ölçüde sorumlu tutulabileceği,
- Resmi bildirimler: telif hakkı, marka kullanımı veya yasal zorunluluklar,
- Üçüncü taraf atıfları: projede kullanılan dış kaynakların hukuki gereklilikleri

[LICENSE](#license)'dan farklı olarak kullanım haklarını değil, yasal uyarıları ve sorumluluk redlerini kapsar.

**Şu dosyaları kapsar:**

- `DISCLAIMER.md`: Uyarılar ve sorumluluk reddi beyanları bu dosyada bulunur.
- `NOTICE.md`: Resmi bildirimler bu dosyada yer alır.
- `REFERENCES.md`: Projenin dayandığı dış kaynaklar, atıflar ve bağımlılıklar bu dosyada listelenebilir.

### [ARCHITECTURE.md](./ARCHITECTURE.md)

İsmi, "mimari" veya "yapı" anlamına gelir.
Projenin mimari yapısının açıklamasını içerir.
Bu dosyayı okuyan bir kişi, projenin tüm mimarisini anlayabilmelidir.

Bu dosya teknik terimler içerir, terimleri "x nedeniyle y'yi kullanıyoruz" şeklinde açıklar.
İçerik, projenin mimarisini açıklamalıdır.
Burada mimari, işleyiş gibi şeylere karşılık gelir.
Bu dosyanın teknik olmayan versiyonu [SUMMARY.md](#summarymd) olarak yorumlanabilir.

Her ne kadar projeden projeye değişecek olsa da, her proje her zaman bir mimariye sahiptir.

Sistem yapısı ve tasarım genel görünümü, tasarım kararları ve gerekçeleri, bileşenler arası ilişkiler, süreçler, iş akışları ve yaşam döngüleri, veri şemaları, arayüz tanımları ve entegrasyon detayları. Projeyi teknik olarak kavramak isteyen herkesin başvurduğu ana teknik belgedir.

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
Her projenin bir performans beklentisi vardır, bu dosya o beklentileri ve nasıl ölçüldüğünü ortaya koyar.

**Şu dosyaları kapsar:**

- `BENCHMARKS.md`

### [SECURITY.md](./SECURITY.md)

Projenin güvenlik politikaları ve güvenlik açığı bildirimi, tehdit modeli ve saldırı yüzeyi analizi, erişim kontrolü ve rol tabanlı yetkilendirme kuralları, kimlik doğrulama ve şifreleme standartları, denetim izi ve kayıt politikası, veri işleme ve saklama prosedürleri.

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
`robots.txt` web tarayıcıları için ne ise bu dosya da AI ajanları için odur. Amp, Codex, Cursor, Devin, Gemini CLI, GitHub Copilot ve VS Code tarafından desteklenen açık bir standarttır. Web ortamında yayımlanan projeler için Git reposunun değil web sunucusunun kök dizinine ait olan `llms.txt` standardı da değerlendirilebilir.

**Şu dosyaları kapsar:**

- `CONTEXT.md`
- `CLAUDE.md`
- `GEMINI.md`
- `.cursorrules`
