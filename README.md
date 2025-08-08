# Titanic: Hayatta Kalma Analizi

Bu proje, Titanic felaketine ait yolcu verilerini kullanarak hayatta kalma oranlarını etkileyen faktörlerin derinlemesine bir keşifsel veri analizini (EDA) içermektedir. Projenin temel amacı, veri setindeki ilişkileri, dağılımları ve anormallikleri görselleştirme teknikleriyle ortaya çıkararak anlamlı içgörüler elde etmektir.

## 📊 Proje Amacı

Bu projenin ana hedefleri şunlardır:

* Titanic veri setinin yapısını ve içeriğini anlamak.
* Veri setindeki eksik ve aykırı değerleri tespit edip uygun yöntemlerle temizlemek.
* Yolcuların demografik bilgileri (cinsiyet, yaş) ve seyahat detayları (sınıf, biniş yeri) ile hayatta kalma durumu arasındaki ilişkileri incelemek.
* Elde edilen bulguları etkili veri görselleştirme teknikleri ile sunmak.
* Gelecekteki makine öğrenmesi modellemeleri için temel oluşturacak içgörüleri belirlemek.

##  veriseti

Bu projede kullanılan veri seti, Kaggle'ın "Titanic - Machine Learning from Disaster" yarışmasından temin edilmiştir. Veri seti, felakette yer alan 891 yolcunun demografik ve seyahat bilgilerini içermektedir.

* **Veri Kaynağı:** [https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv](https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv)

## 🛠️ Veri Temizliği ve Hazırlığı

Analize başlamadan önce veri seti üzerinde aşağıdaki temizlik ve hazırlık adımları uygulanmıştır:

* **Yaş (Age):** `Age` sütunundaki 177 adet eksik değer, aykırı değerlerin etkisini en aza indirmek amacıyla medyan değeri ile doldurulmuştur.
* **Kabin (Cabin):** `Cabin` sütunundaki eksik değer sayısının çok yüksek olması (687 adet) nedeniyle bu sütun analizden çıkarılmıştır.
* **Biniş Yeri (Embarked):** `Embarked` sütunundaki 2 adet eksik değer, en sık tekrar eden biniş yeri (mod) ile doldurulmuştur.

Bu adımlar sonucunda veri seti, keşifsel veri analizi için tutarlı ve güvenilir bir hale getirilmiştir.

## 📈 Analiz ve Bulgular

Yapılan analizler ve görselleştirmeler sonucunda aşağıdaki önemli bulgulara ulaşılmıştır:

### Hayatta Kalma Oranı

<p align="center">
  <img src="https://i.imgur.com/88575247-1ce9-4b8a-9ff8-4c5056855a53.png" width="600">
</p>

Veri setindeki yolcuların yaklaşık **%38'i** hayatta kalırken, **%62'si** hayatını kaybetmiştir. Bu durum, felaketin büyüklüğünü ve kurtarma çabalarının yetersizliğini gözler önüne sermektedir.

### Cinsiyetin Hayatta Kalma Üzerindeki Etkisi

<p align="center">
  <img src="https://i.imgur.com/07a4f987-ed6b-48d3-86c5-635553f95e71.png" width="600">
</p>

Cinsiyet, hayatta kalma oranını en güçlü şekilde etkileyen faktörlerden biridir. **Kadın yolcuların hayatta kalma olasılığı, erkek yolculara kıyasla belirgin şekilde daha yüksektir.** Bu bulgu, "önce kadınlar ve çocuklar" kurtarma protokolünün uygulandığına dair güçlü bir kanıt niteliğindedir.

### Yolcu Sınıfının Etkisi

<p align="center">
  <img src="https://i.imgur.com/709f09dc-62f0-4bde-adc4-957e212b6b0e.png" width="600">
</p>

Yolcu sınıfı (Pclass), hayatta kalma olasılığını önemli ölçüde etkilemektedir. **1. sınıf yolcuların hayatta kalma oranı, 2. ve 3. sınıf yolcularına göre çok daha yüksektir.** En düşük hayatta kalma oranı ise 3. sınıf yolcularında görülmektedir. Bu durum, sosyal sınıfın kurtarma önceliğinde belirleyici bir rol oynadığını göstermektedir.

### Yaş Dağılımının İncelenmesi

<p align="center">
  <img src="https://i.imgur.com/70f94567-8a38-4730-a435-d9ad18a7a5a3.png" width="600">
</p>

Yaş dağılımı incelendiğinde, **küçük yaştaki çocukların hayatta kalma oranının daha yüksek olduğu** gözlemlenmiştir. Buna karşın, **20-30 yaş aralığındaki genç yetişkinlerin** hayatta kalma oranlarının daha düşük olduğu görülmektedir. Bu durum, gençlerin kurtarma sırasında daha az öncelikli gruplar arasında yer aldığını düşündürmektedir.

## 🚀 Sonuç ve Gelecek Çalışmalar

Bu keşifsel veri analizi projesi, Titanic faciasında hayatta kalma olasılığının rastgele olmadığını; yolcunun **cinsiyeti, yaşı ve sosyal sınıfı** gibi faktörlerle doğrudan ilişkili olduğunu açıkça ortaya koymaktadır. Elde edilen bulgular, dönemin sosyal normları ve acil durum protokolleri hakkında değerli bilgiler sunmaktadır.

Gelecekteki çalışmalarda, bu projenin bulguları temel alınarak aşağıdaki konular daha detaylı incelenebilir:

* Aile büyüklüğünün (SibSp ve Parch sütunları) hayatta kalma üzerindeki etkisi.
* Farklı biniş yerlerinden (Embarked) gelen yolcuların hayatta kalma oranları arasındaki farklılıkların nedenleri.
* Bu veriler kullanılarak hayatta kalma olasılığını tahmin eden bir makine öğrenmesi modeli geliştirilmesi.

## 🔧 Kullanılan Teknolojiler

* **Python 3**
* **Pandas:** Veri manipülasyonu ve analizi
* **NumPy:** Sayısal işlemler
* **Matplotlib & Seaborn:** Veri görselleştirme
* **Jupyter Notebook:** Kodlama ve analiz ortamı

## ⚙️ Kurulum ve Çalıştırma

Bu projeyi yerel makinenizde çalıştırmak için aşağıdaki adımları izleyebilirsiniz:

1.  **Bu repoyu klonlayın:**
    ```bash
    git clone [https://github.com/kullanici-adiniz/titanic-analizi.git](https://github.com/kullanici-adiniz/titanic-analizi.git)
    ```
2.  **Proje dizinine gidin:**
    ```bash
    cd titanic-analizi
    ```
3.  **Gerekli kütüphaneleri yükleyin:**
    ```bash
    pip install -r requirements.txt
    ```
    *(Not: `requirements.txt` dosyasını `pip freeze > requirements.txt` komutuyla oluşturmanız gerekmektedir.)*

4.  **Jupyter Notebook'u başlatın:**
    ```bash
    jupyter notebook
    ```
5.  **`EDA_Raporu.ipynb` dosyasını açarak analizleri inceleyebilir ve yeniden çalıştırabilirsiniz.**
