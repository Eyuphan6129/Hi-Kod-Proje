# Öğrenci Başarısı Tahmin Projesi (Veri Bilimi)

Bu proje, Portekiz'deki iki ortaöğretim okulundan alınan öğrenci verilerini  kullanarak, öğrencilerin final notlarını (G3) tahmin etmeyi amaçlayan bir makine öğrenimi çalışmasıdır. [cite_start]Proje, `project.ipynb`  adlı Jupyter Notebook dosyasında geliştirilmiştir.

##  Proje Özeti

Çalışma, bir veri bilimi projesinin temel adımlarını içermektedir:
1.  **Veri Yükleme ve Temizleme:** `mat2.csv`  [cite_start]veri seti `pandas`  kullanılarak yüklendi ve incelendi.
2.  **Keşifsel Veri Analizi (EDA):** `matplotlib`  [cite_start]ve `seaborn`  kütüphaneleri kullanılarak veriler görselleştirildi. Kategorik (okul, cinsiyet, adres vb.) ve sayısal (yaş, çalışma süresi vb.) özelliklerin final notları üzerindeki etkisi `boxplot` ve `regplot` grafikleriyle analiz edildi.
3.  **Özellik Mühendisliği (Feature Engineering):** Model performansını artırmak için 'G1', 'G2', 'G3' notlarından 'Grade Total' (Toplam Not) ve 'Medu' (Anne Eğitimi), 'Fedu' (Baba Eğitimi) sütunlarından 'Parent_Edu' (Ebeveyn Eğitimi)  gibi yeni özellikler türetildi.
4.  **Modelleme:** Veri seti, `scikit-learn`  kütüphanesi kullanılarak makine öğrenimi modellerine hazırlandı. [cite_start]Kategorik veriler `get_dummies`  ile dönüştürüldü.
5.  **Model Karşılaştırma:** Final notunu (G3) tahmin etmek için üç farklı regresyon modeli eğitildi ve karşılaştırıldı:
    * Lineer Regresyon (Linear Regression) 
    * Karar Ağacı (Decision Tree Regressor) 
    * Random Forest (Random Forest Regressor) 

##  Sonuç

Modellerin performansı `R² Score` (R-kare) metriği kullanılarak değerlendirildi. [cite_start]**Random Forest** modeli, **~0.91 R² skoru**  ile en yüksek başarıyı göstererek final notlarını tahmin etmede en etkili model olarak belirlendi.

##  Nasıl Çalıştırılır?

1.  Bu depoyu (repository) klonlayın:
    ```sh
    git clone [https://github.com/](https://github.com/)[Eyuphan6129]/[Hi-Kod-Proje].git
    ```
2.  Proje klasörüne gidin:
    ```sh
    cd [Hi-Kod-Proje]
    ```
3.  Gerekli Python kütüphanelerini `requirements.txt` dosyasını kullanarak yükleyin:
    ```sh
    pip install -r requirements.txt
    ```
4.  Jupyter Notebook'u başlatın ve `project.ipynb`  dosyasını açın:
    ```sh
    jupyter notebook project.ipynb
    ```

##  Kullanılan Kütüphaneler

* [cite_start]**pandas**  (Veri işleme ve CSV okuma)
* [cite_start]**matplotlib**  (Veri görselleştirme)
* [cite_start]**seaborn**  (Gelişmiş veri görselleştirme)
* [cite_start]**scikit-learn (sklearn)**  (Makine öğrenimi modelleri ve metrikler için)
* [cite_start]**jupyter**  (Projenin geliştirildiği notebook ortamı)
