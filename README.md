# STM32-F410RB-EXTI-Kesmesi-ile-LED-Yakma-ve-Saya-Uygulamas-
STM32 mikrodenetleyici ile harici kesme (EXTI) kullanılarak butonlara basıldığında LED toggle işlemi yapılır ve bir sayaç artırılıp azaltılır. Proje, temel kesme ve GPIO kullanımını öğretici bir şekilde gösterir.
# STM32 Harici Kesme ile Buton ve LED Kontrolü

Bu proje, STM32 mikrodenetleyici kullanılarak harici kesmeler (EXTI) ile butonlara basıldığında LED'leri kontrol eden ve bir sayaç değerini artırıp azaltan basit bir uygulamadır.

## 🔧 Kullanılan Özellikler
- STM32 HAL kütüphanesi
- GPIO giriş/çıkış işlemleri
- EXTI (External Interrupt)
- Basit sayaç (counter) mantığı
- UART yapılandırması (şimdilik kullanılmıyor)

## ⚙️ Donanım Bağlantıları
| GPIO Pin | İşlev           |
|----------|-----------------|
| PA6      | Buton 1 (Sayaç +1, PA8 LED toggle) |
| PA7      | Buton 2 (Sayaç -1, PA9 LED toggle) |
| PA8      | LED 1           |
| PA9      | LED 2           |

## 🚦 Uygulama Mantığı
- **PA6 pinine** bağlı butona basıldığında:
  - PA8 LED’i toggle yapılır.
  - Sayaç `+1` artar.
- **PA7 pinine** bağlı butona basıldığında:
  - PA9 LED’i toggle yapılır.
  - Sayaç `-1` azalır.

## 💡 Geliştirme Ortamı
- STM32CubeIDE
- STM32F4 serisi (örnek: NUCLEO-F410RB)
- C dili (HAL Kütüphanesi)
