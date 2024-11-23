
# Steam Video Oyunu Analizleri

Bu proje, Steam platformundaki video oyunlarının verilerini analiz etmeye ve anlamlı görselleştirmeler ile sonuçlar çıkarmaya odaklanmıştır. Aşağıda proje hakkında detaylı bilgiler bulunmaktadır.

---

## Kullanılan Kütüphaneler

Projede kullanılan Python kütüphaneleri şunlardır:

- matplotlib
- numpy
- os
- pandas
- re
- seaborn
- sklearn
- warnings

---

## Analiz Süreci ve Yapılan Adımlar

Projede gerçekleştirilen bazı temel adımlar şunlardır:

### # Bu Python 3 ortamı, birçok yararlı analitik kütüphanesi yüklü olarak gelir # Bu, kaggle/python Docker görüntüsü tarafından tanımlanır: https://github.com/kaggle/docker-python # Örneğin, yüklemek için birkaç yararlı paket şunlardır # doğrusal cebir # veri işleme, CSV dosyası G/Ç (ör. pd.read_csv) # Giriş veri dosyaları salt okunur "../input/" dizininde mevcuttur # Örneğin, bunu çalıştırmak (çalıştır'a tıklayarak veya Shift+Enter'a basarak) giriş dizini altındaki tüm dosyaları listeler # "Tümünü Kaydet ve Çalıştır"ı kullanarak bir sürüm oluşturduğunuzda çıktı olarak korunan geçerli dizine (/kaggle/working/) 20 GB'a kadar yazabilirsiniz # Ayrıca /kaggle/temp/ dizinine geçici dosyalar yazabilirsiniz, ancak bunlar geçerli oturumun dışına kaydedilmez

### # Kütüphanelerin Yüklenmesi

### # Verilerin keşfi

### # "play" eylemi için bilgiler, bana daha alakalı görünüyor. # burada, ortalama hesaplamada alakalı olmayan Hours = 1.0 ile action = 'purchase'i hariç tutmak istiyoruz

### Bu kodda, bir oyuncunun her oyun satın aldığında onu oynayıp oynamadığını kontrol edeceğiz.

---

## Önemli Çıktılar

Aşağıda analizden elde edilen bazı örnek çıktıların bir özeti verilmiştir:

```
/kaggle/input/steam-video-games/steam-200k.csv

      UserID                        Game    Action  Hours  Other
0  151603712  The Elder Scrolls V Skyrim  purchase    1.0      0
1  151603712  The Elder Scrolls V Skyrim      play  273.0      0
2  151603712                   Fallout 4  purchase    1.0      0
3  151603712                   Fallout 4      play   87.0      0
4  151603712                       Spore  purchase    1.0      0
5  151603712                       Spore      play   14.9      0
6  151603712           Fallout New Vegas  purchase    1.0      0
7  151603712           Fallout New Vegas      play   12.1      0
8  151603712               Left 4 Dead 2  purchase    1.0      0
9  151603712               Left 4 Dead 2      play    8.9      0
          count          mean           std     min         25%         50%  \
UserID  70489.0  1.058812e+08  7.150365e+07  5250.0  49342564.0  91690667.0   
Hours   70489.0  4.887806e+01  2.293352e+02     0.1         1.0         4.5   
Other   70489.0  0.000000e+00  0.000000e+00     0.0         0.0         0.0   

                75%          max  
UserID  155673786.0  309903146.0  
Hours          19.1      11754.0  
Other           0.0          0.0  
UserID     Action  
26122540   play          7
           purchase     10
30007387   purchase      2
53875128   play        197
           purchase    505
59945701   play         22
           purchase     43
63024728   play          1
           purchase      1
76933274   play          1
           purchase      1
126340495  play         17
           purchase     29
140954425  play          1
           purchase      1
150128162  play          1
           purchase      1
151603712  play         26
           purchase     40
176410694  play          1
           purchase      1
187131847  play          1
           purchase      1
194895541  play          2
           purchase      2
197278511  play          1
           purchase      1
197455089  play          1
           purchase      1
218323237  play          3
           purchase      3
234941318  purchase      1
256193015  purchase      1
297811211  play          3
           purchase      3
302186258  play          1
           purchase      1
dtype: int64
Oyun Sayısı : 5155
Kullanıcı Sayısı : 12393
Toplam Satın Alma Sayısı  : 129511
Toplam oyun sayısı bilgisi  : 70489

```

---

## Kurulum ve Çalıştırma

1. **Gereksinimler**: Bu proje için Python 3.7+ ve gerekli kütüphaneler gereklidir. İlgili kütüphaneleri yüklemek için şu adımları takip edin:

   ```bash
   pip install -r requirements.txt
   ```

2. **Notebook'u Çalıştırma**: Jupyter Notebook'u başlatın ve `steam-video-oyunu-analizleri.ipynb` dosyasını açın. Tüm hücreleri sırasıyla çalıştırarak analizi gerçekleştirin.

---

## Projenin Amacı

Bu çalışma, Steam'deki oyunların popülerlik, fiyatlandırma, değerlendirme gibi özellikleri arasındaki ilişkileri analiz etmek ve veri bilimi yöntemlerini kullanarak oyun endüstrisi hakkında içgörüler elde etmek için yapılmıştır.

---

## Lisans

Bu proje MIT Lisansı ile lisanslanmıştır. Daha fazla bilgi için `LICENSE` dosyasını kontrol edebilirsiniz.
