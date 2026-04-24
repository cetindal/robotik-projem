# robotik-projem
Arduino ile Trafik Işığı Simülasyonu Raporu
Amaç:Bu çalışmanın amacı, Arduino Uno kullanarak kırmızı, sarı ve yeşil LED’ler yardımıyla bir trafik ışığı sisteminin temel mantığını simüle etmektir. Bu sayede dijital çıkışlar, zamanlama (delay) ve temel devre kurma becerileri öğrenilmiştir.
Kullanılan Malzemeler
1 adet Arduino Uno
1 adet breadboard
3 adet LED (kırmızı, sarı, yeşil)
3 adet 220Ω direnç
Jumper kablolar
USB kablosu
Devre Bağlantısı
Devre kurulumu şu şekildedir:
Kırmızı LED → Arduino dijital pin 12
Sarı LED → Arduino dijital pin 11
Yeşil LED → Arduino dijital pin 10
Her LED’in uzun bacağı (anot) ilgili pine bağlanmıştır
Kısa bacaklar (katot) direnç üzerinden GND’ye bağlanmıştır
Dirençler, LED’lerin fazla akım çekmesini önlemek için kullanılmıştır.
Çalışma Prensibi=
Arduino, dijital pinler aracılığıyla LED’leri sırasıyla yakıp söndürür:
Yeşil LED yanar (geçiş serbest)
Sarı LED yanar (hazırlık)
Kırmızı LED yanar (dur)
Bu döngü sürekli tekrar eder ve bir trafik lambasının çalışma mantığını taklit eder.
Arduino Kodu:
// C++ code
//
void setup()
{
  pinMode(11, OUTPUT);
  pinMode(10, OUTPUT);
  pinMode(9, OUTPUT);
}

void loop()
{
  digitalWrite(11, HIGH);
  delay(3000);
  digitalWrite(11, LOW);

  digitalWrite(10, HIGH);
  delay(1000);
  digitalWrite(10, LOW);

  digitalWrite(9, HIGH);
  delay(5000);
  digitalWrite(9, LOW);

  digitalWrite(11, HIGH);
  digitalWrite(10, HIGH);
  delay(1000);
  digitalWrite(11, LOW);
  digitalWrite(10, LOW);
}
Sonuç:
Bu proje ile Arduino kullanarak basit bir trafik ışığı sistemi başarıyla gerçekleştirilmiştir. LED kontrolü, zamanlama fonksiyonları ve devre kurulumu konularında temel bilgiler edinilmiştir.
