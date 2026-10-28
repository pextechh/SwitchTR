# Nintendo Switch Türkçe Sistem Yaması

**Geliştirici:** Pasha Bey  
**Hedef Platform:** Nintendo Switch (Atmosphère CFW)  
**Desteklenen Son Sürüm** 23.0.1

Bu proje, CFW (Atmosphère) yüklü Nintendo Switch konsollarının sistem arayüzünü Türkçe'ye çevirmek amacıyla **Pasha Bey** tarafından hazırlanmış yerelleştirme paketidir. 

Atmosphère'in sunduğu **LayeredFS** mimarisini kullanır; konsolun orijinal sistem dosyalarına (NAND/eMMC) kalıcı bir müdahalede bulunmaz, tamamen güvenli ve istenildiği zaman kolayca kaldırılabilir yapıdadır.

---

## Önemli Ön Koşul

Yamayı kullanabilmeniz için konsolunuzun mevcut sistem dilinin **İngilizce (English)** olması gerekmektedir. Başka bir dildeyken (Almanca, Fransızca, Japonca vb.) yama devreye girmez; çünkü bu yama sistemdeki İngilizce dil dosyalarının yerini almaktadır.

---

## Bölge ve Paket Seçenekleri

Konsolunuzun bağlı olduğu bölgeye veya bölge tercihinize göre uygun paketi seçmelisiniz:

| Paket Klasörü | Hedef Bölge | Açıklama |
| :--- | :--- | :--- |
| `Turkce_Yama_Avrupa_EU` | Avrupa (Europe) | Avrupa bölgesi cihazlar veya bölgesi Avrupa olarak ayarlanmış konsollar içindir. İngilizce dil seçeneğini Türkçe yapar. |
| `Turkce_Yama_Amerika_US` | Amerika (Americas) | Amerika bölgesi cihazlar veya bölgesi Amerika olarak ayarlanmış konsollar içindir. İngilizce dil seçeneğini Türkçe yapar. |

---

## Kurulum Adımları

1. **Konsol Dilini Kontrol Edin:** Konsolunuzun dilinin **İngilizce** olduğundan emin olun (**System Settings > System > Language > English**).
2. **Paketinizi Seçin:** Konsol bölgenize göre `Turkce_Yama_Avrupa_EU` (Avrupa) veya `Turkce_Yama_Amerika_US` (Amerika) klasörünü belirleyin.
3. **Kartı Bağlayın:** Cihazınızın microSD kartını bilgisayara takın (veya Hekate UMS / FTP ile bağlanın).
4. **Dosyaları Kopyalayın:** Seçtiğiniz klasörün içindeki **`contents`** klasörünü microSD kartınızdaki **`atmosphere`** dizininin içine atın:
   ```text
   microSD:/
   └── atmosphere/
       └── contents/
           ├── 0100000000000803/
           ├── 010000000000080B/
           ├── 0100000000001000/
           └── ... (diğer Title ID klasörleri)
   ```
5. **Cihazı Başlatın:** microSD kartı konsola takıp cihazı Atmosphère CFW ile açın.
6. **Kontrol Edin:** **Sistem Ayarları > Sistem > Dil** bölümüne girdiğinizde dil seçeneğinin **Türkçe (Pasha Bey)** olarak görüntülendiğini ve sistemin Türkçe olduğunu görebilirsiniz.

---

## Kaldırma

Yamayı konsoldan tamamen kaldırmak için microSD kartınızdaki `atmosphere/contents/` dizini altından bu yamaya ait Title ID klasörlerini silmeniz yeterlidir:

```text
0100000000000803, 010000000000080B, 010000000000080C,
0100000000001000, 0100000000001001, 0100000000001002,
0100000000001003, 0100000000001004, 0100000000001005,
0100000000001006, 0100000000001007, 0100000000001008,
0100000000001009, 010000000000100C, 010000000000100D,
0100000000001012, 0100000000001013, 0100000000001015, 0100000000001048
```

---

## Teknik Yapı

- Çeviri verileri Nintendo Horizon OS standartlarındaki `MSBT` (Message Binary Text) formatında derlenmiş ve `Yaz0 (.szs)` algoritmasıyla sıkıştırılmıştır.
- Atmosphère LayeredFS mekanizması sayesinde sistem dosyaları belleğe yüklenirken anlık olarak yamalanır, NAND hafızasına kalıcı yazım yapılmaz.

---

## Yasal Uyarı

Bu proje bağımsız bir yerelleştirme çalışmasıdır. Nintendo ve Nintendo Switch, Nintendo Co., Ltd.'nin tescilli ticari markalarıdır. Proje tamamen ücretsizdir ve ticari amaç taşımamaktadır.
Son Sürümler Releases Kısmındadır.

### (c) Pasha Network LLC. 2025-2026. All Rights Reserved.
