# Parça Baskı Durumu

> Kaynak: Klipper/Moonraker geçmişi (`172.16.16.244`) + `printer_data/gcodes`
> Son güncelleme: **09.11.2026**

## Özet

| | Adet |
|---|---:|
| ✅ Tamamlanan | 13 |
| ⬜ Kalan | 4 |
| ⚠️ Sorunlu dosya | 1 |

---

## ✅ Tamamlananlar

| Parça / Dosya | Süre | Tarih | Not |
|---|---:|---|---|
| `CRSD1sermoonhinge1.gcode` | 2 sa 17 dk | 13.09 | tamam |
| `CRSD1fuar_stnddskhldbase1.gcode` | 16 sa 50 dk | 14.09 | tamam |
| `CRSD1pin.gcode` | 30 dk | 20.09 | tamam |
| `CRSD1fuar_stnddskdrl.gcode` | 7 sa 45 dk | 20.09 | birkaç denemeden sonra tamam |
| `CRSD1rotilholder.gcode` | 2 sa 52 dk | 20.09 | tamam |
| `RC_CAT03_nose.gcode` | 38 dk | 24.10 | tamam (dosya arşivde yok) |
| `ROBOCAT_all.gcode` | 8 sa 18 dk | 24.10 | tamam |
| `P1_CASE.gcode` | 4 sa 02 dk | 25.10 | tamam |
| `RC_EYE_PETG.gcode` | 12 dk | 27.10 | tamam |
| `RC_M03_CARRIER.gcode` | 14 dk | 27.10 | tamam |
| `RC_M05_INSERTS2.gcode` | 9 dk | 27.10 | tamam |
| `RC_M04_SPACERS_250_90.gcode` | 24 dk | 09.11 | VM'de tamam (250/90) |
| `RC_M06_LID_250_90.gcode` | 1 sa 12 dk | 09.11 | VM'de tamam (250/90) |
| `TEST_adhesion.gcode` | 15 dk | 24.10 | test |

---

## ⬜ Kalanlar (basılacak)

| Parça / Dosya | Tahmini | Not |
|---|---:|---|
| `P2_LID.gcode` | 1 sa 09 dk | 25.10'da 67 dk'da iptal edilmiş — yeniden basılmalı |
| `CRSD1fuar_stndrotilsup.gcode` | 2 sa 22 dk | sadece 4 dk deneme, hiç bitmemiş |
| `CRSD1fuar_stnddskhldbase.gcode` | 4 sa 11 dk | hiç basılmamış |
| `CRSD1sermoonenclosure2.gcode` | 4 sa 28 dk | hiç basılmamış |

**Önerilen sıra:** `P2_LID` → `CRSD1fuar_stndrotilsup` → `CRSD1fuar_stnddskhldbase` → `CRSD1sermoonenclosure2`
(küçükten büyüğe; her baskı sonrası tabla temizliği gerekir)

---

## ⚠️ Sorunlu / yinelenen dosyalar

| Dosya | Durum |
|---|---|
| `RC_M06_LID4.gcode` | **0 byte** — bozuk, kullanılmaz |
| `DONE_ROBOCAT_all.gcode` | Basıldı, tekrar basılmamalı |
| `DONE_ROBOCAT_all_250_90.gcode` | Denendi, iptal edildi; aslı zaten basılmış |
| `RC_M06_LID2.gcode`, `RC_M06_LID3.gcode` | `RC_M06_LID_250_90` ile tamamlandı |
| `RC_M04_SPACERS.gcode`, `RC_M05_INSERTS.gcode` | 250/90 sürümleri/INSERTS2 ile tamamlandı |
| `P1_CASE_250_90.gcode` | `P1_CASE` zaten basılmış — tekrar basılmamalı |

---

## Notlar

- Baskı sıcaklıkları: **PETG 250 °C nozzle / 90 °C yatak** (dosyalarda 100 °C yazıyorsa düşürülür).
- Yazıcı host'u: Proxmox VM `printer-host` (`172.16.16.244`), Debian 13 + Klipper + Moonraker + Fluidd.
- USB: CH340 `1a86:7523` passthrough → `/dev/ttyUSB0`.
