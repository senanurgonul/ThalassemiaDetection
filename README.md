# ThalassemiaDetection

**ThalassemiaDetection**, rutin kan tahlili (CBC) verileri kullanılarak çeşitli **talasemi (thalassemia)** alt tiplerini sınıflandırmayı amaçlayan bir makine öğrenimi projesidir. Genetik testlere gerek kalmadan, yalnızca hematolojik değerlerle doğru ve erken tanı koymayı hedefleyen bu çalışma, klinik karar destek sistemlerine katkı sağlamayı amaçlamaktadır.

---

## 🎯 Proje Amacı

Talasemi, kalıtsal bir kan hastalığıdır ve dünyada özellikle Akdeniz, Orta Doğu ve Güneydoğu Asya bölgelerinde yaygın olarak görülmektedir. Bu proje ile amaçlanan:

- **Genetik testlere gerek kalmadan** CBC verileriyle talasemi ve alt türlerini doğru şekilde sınıflandırmak
- Kliniklerde **düşük maliyetli ve erişilebilir** bir ön tanı aracı sunmak
- Farklı sınıflandırma modelleriyle **en etkili yaklaşımı belirlemek**
- Modelin **yorumlanabilirliğini artırarak** doktorlara karar sürecinde destek sağlamak

Talaseminin doğru şekilde sınıflandırılması, tedavi planlarının oluşturulması ve taşıyıcıların belirlenmesi açısından oldukça kritiktir. Bu nedenle projemiz, hem tıbbi doğruluk hem de pratik uygulanabilirlik açısından yüksek etkili bir sistem sunmayı hedeflemektedir.

---

## 🧬 Veri Seti

Veri seti, akademik iş birliğiyle Tayland'da yapılmış bir çalışmadan elde edilmiştir. Sadece akademik amaçlarla kullanıma açıktır.

### 📂 Dosyalar

- `csv_result-Train90.csv` — Eğitim verileri  
- `csv_result-Test90.csv` — Test verileri

### 📊 İçerdiği Özellikler (CBC Parametreleri)

- **MCV (Mean Corpuscular Volume):** Hücre hacmi, talasemi ve demir eksikliği anemisinde ayırıcı özelliktir.
- **MCH, MCHC:** Hemoglobin yoğunluğu
- **HbA2:** Özellikle beta talasemi taşıyıcılığı tanısında önemli
- **HbE, HbF, Hb Bart’s:** Özel hemoglobin türleri, talasemi alt tiplerinin ayrımında kritik rol oynar
- **HbA0, Hb D/S/CS/C:** Diğer varyantların sınıflandırılmasına yardımcı


### 📌 Veri Temizleme ve Hazırlama

- Nadir sınıflar kaldırıldı (örneğin: < 5 örnek)
- SMOTE ile azınlık sınıflar dengelendi
- Aşırı örnek içeren sınıflar downsample edildi (4000 → 500)
- Veri sızıntısı ve tekrar kayıtlar engellendi
- Stratified split ile dengeli eğitim/test ayrımı sağlandı

Veri seti, **11 sınıfa** ayrılmış olup hem yaygın hem de nadir görülen talasemi alt tiplerini kapsamaktadır.

---


## 🚀 Kurulum ve Kullanım

1. Gerekli paketleri yükleyin:

```bash
pip install pytorch-tabnet scikit-learn pandas matplotlib imblearn
```

2. Notebook'u çalıştırın:

```bash
jupyter notebook Untitled12.ipynb
```

Notebook içindeki adımları takip ederek verileri yükleyebilir, modelleri eğitebilir ve sonuçları analiz edebilirsiniz.

---m.

Bu proje ile sadece doğruluk değil, aynı zamanda **klinik anlamda güvenilir ve anlaşılabilir sonuçlar üreten** bir model hedeflenmiştir. Modelin en başarılı çıktısı olan **TabNet**, hem doğruluk hem de yorumlanabilirlik açısından dikkat çekmiştir.

