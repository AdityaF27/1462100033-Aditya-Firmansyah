Komponen yang Digunakan
Arduino Uno: Mikrokontroler yang digunakan untuk membaca data dari sensor suhu dan menampilkan hasilnya di LCD.
Sensor Suhu LM35: Sensor suhu yang memberikan output analog yang proporsional dengan suhu yang terukur.
LCD 16x2: Layar LCD yang digunakan untuk menampilkan nilai suhu dalam format teks.
Koneksi dan Fungsi
Sensor Suhu LM35:
Pin VCC (Pin 1): Diambil dari pin 5V pada Arduino Uno.
Pin GND (Pin 3): Diambil dari pin GND pada Arduino Uno.
Pin VOUT (Pin 2): Dihubungkan ke pin analog A0 pada Arduino Uno.
LCD 16x2:
Pin RS, E, D4-D7: Terhubung ke pin digital pada Arduino Uno. Dalam hal ini, beberapa pin digital seperti D2-D13 digunakan untuk mengendalikan LCD.
Pin RW: Biasanya dihubungkan ke ground untuk mode tulis.
Pin VSS: Diambil dari pin GND pada Arduino Uno.
Pin VDD: Diambil dari pin 5V pada Arduino Uno.
Pin V0: Diatur menggunakan potensiometer untuk mengatur kontras LCD.
Alur Kerja Rangkaian
Pengaturan Awal:

Saat sistem dinyalakan, Arduino Uno menginisialisasi sensor suhu LM35 dan LCD.
Arduino mengirimkan sinyal awal ke LCD untuk mengatur mode tampilan dan membersihkan layar.
Pembacaan Data dari Sensor:

Sensor suhu LM35 mengukur suhu lingkungan dan menghasilkan tegangan analog pada pin VOUT.
Tegangan ini dibaca oleh Arduino melalui pin analog A0.
Pengolahan Data:

Arduino melakukan pembacaan tegangan analog dan mengonversinya menjadi nilai suhu dalam derajat Celcius menggunakan rumus kalibrasi sensor LM35.
Formula umum: suhu (°C) = (Vout * 100), di mana Vout adalah tegangan output dari LM35 dalam volt.
Penampilan Data di LCD:

Arduino mengirimkan perintah dan data ke LCD melalui pin digital yang terhubung.
LCD menampilkan suhu yang terbaca dalam format teks, misalnya "SUHU RUANGAN: 33.20°C".
