# ML Term Paper

Bu depo, sürdürülebilir kalkınma, enerji göstergeleri ve OECD ülkeleri üzerinde yapılan makine öğrenmesi çalışmalarını içerir. Notebook'larda veri hazırlama, keşifsel analiz, kümeleme, regresyon ve zaman serisi tabanlı model denemeleri bir araya getirilmiştir.

## Proje Özeti

Çalışmanın ana odağı, ülke bazlı ekonomik, enerji ve çevresel göstergeleri kullanarak SDG (Sustainable Development Goals) ile ilişkili analizler üretmektir. Depoda hem veri birleştirme ve ön işleme adımları hem de farklı model aileleri için denemeler yer alır.

Öne çıkan başlıklar:

- OECD ülkeleri için SDG ve enerji göstergelerinin karşılaştırılması
- K-Means ve Agglomerative Clustering ile kümeleme analizleri
- Random Forest ile tahmin denemeleri
- SARIMA, Holt-Winters ve LSTM gibi zaman serisi modellerinin performans karşılaştırmaları
- Görselleştirme ve yorumlama odaklı notebook çıktıları

## Dosya Yapısı

- [Machine_Learning.ipynb](Machine_Learning.ipynb): Ana analiz ve modelleme notebook'u.
- [Machine_Learning_Random.ipynb](Machine_Learning_Random.ipynb): Random Forest odaklı denemeler ve ilgili analizler.
- [Last_Version_2.ipynb](Last_Version_2.ipynb): Daha güncel sürüm; OECD, SDG ve kümeleme adımlarını içeren geniş notebook.
- [deneme/New_1.ipynb](deneme/New_1.ipynb): Yardımcı/deneme amaçlı notebook.
- [global_data.csv](global_data.csv): Ülke-yıl bazlı enerji, ekonomik ve coğrafi göstergeler.
- [oecd_sdg_ortalamalari.csv](oecd_sdg_ortalamalari.csv): OECD ülkeleri için SDG ortalamaları.
- [yeni_veri_seti.csv](yeni_veri_seti.csv): Birleştirilmiş veya işlenmiş analiz veri seti.
- [performans_tablosu.csv](performans_tablosu.csv): Modellerin hata ve başarı metrikleri.
- [deneme/sdg_index_2000-2022.csv](deneme/sdg_index_2000-2022.csv): 2000-2022 SDG endeks verisi.
- [deneme/oecd_ortalama_degerler_2000_2022.csv](deneme/oecd_ortalama_degerler_2000_2022.csv): OECD ortalama değerleri.
- [deneme/oecd_sdg_ortalamalari.csv](deneme/oecd_sdg_ortalamalari.csv): Deneme klasöründeki SDG ortalama çıktısı.

## Veri Setleri

### global_data.csv

Bu dosya ülke ve yıl bazında enerji, çevre, ekonomi ve coğrafya ile ilgili değişkenler içerir. Örnek sütunlar:

- `Entity`, `Year`
- Elektrik erişimi ve temiz yakıt kullanımı
- Yenilenebilir enerji kapasitesi ve enerji tüketimi
- Karbon emisyonları
- GDP büyümesi ve kişi başı gelir
- Nüfus yoğunluğu, alan, enlem ve boylam

### oecd_sdg_ortalamalari.csv

OECD ülkeleri için SDG ile ilişkili ortalama skorları içerir. Bu veri, ülke bazlı birleştirme ve karşılaştırma adımlarında kullanılmıştır.

### yeni_veri_seti.csv

Modelleme ve analiz için hazırlanmış, işlenmiş bir veri setidir. Notebook'larda kullanılan nihai özellik setlerinden biri olarak düşünülmelidir.

### performans_tablosu.csv

Farklı modellerin ülke bazlı performans metriklerini içerir. Dosyada Random Forest, SARIMA, Holt-Winters ve LSTM için RMSE, MAE ve R2 değerleri yer alır.

## Notebook İçeriği

Notebook'lar genel olarak şu adımları takip eder:

1. Veri okuma ve temizleme
2. Sütun adlarını düzenleme ve eksik değer analizi
3. OECD filtresi ve veri birleştirme
4. Korelasyon ve dağılım analizleri
5. Kümeleme modellemesi
6. Regresyon ve zaman serisi modelleme
7. Sonuçların grafiklerle yorumlanması

## Gereksinimler

Notebook'lar Python tabanlıdır. Çalıştırmak için tipik olarak aşağıdaki paketler gerekir:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `statsmodels`
- `plotly`
- `tensorflow` veya `keras` (LSTM notebook'ları için)

## Çalıştırma

1. Depoyu VS Code veya Jupyter Notebook ile açın.
2. Gerekli Python ortamını kurun ve paketleri yükleyin.
3. Ana notebook'lardan birini açın:
   - [Machine_Learning.ipynb](Machine_Learning.ipynb)
   - [Last_Version_2.ipynb](Last_Version_2.ipynb)
4. Hücreleri sırayla çalıştırın.

Örnek kurulum:

```bash
python -m venv .venv
.venv\Scripts\activate
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels plotly tensorflow
```

## Notlar

- Notebook'ların bazıları deneysel sürüm niteliğindedir ve çıktılar hücre bazında farklılık gösterebilir.
- Veri dosyaları yerel yollar yerine depo içindeki göreli yollarla okunacak şekilde kullanılırsa tekrar üretilebilirlik daha iyi olur.
- `deneme/` klasörü, alternatif veri hazırlama ve modelleme denemeleri için kullanılmıştır.
