# TEXNIK TOPSHIRIQ

# Mehmonxona boshqaruv tizimi (Hotel Management System --- HMS)

## Loyiha haqida umumiy ma'lumot

-   **Talaba:** Iskandarov Dilshodbek
-   **Guruh:** Masofaviy KIDT-236
-   **Mavzu:** 4-mavzu --- Mehmonxona boshqaruv tizimi
-   **Platforma:** Web ilova
-   **Loyiha turi:** Ma'lumotlar bazasiga asoslangan boshqaruv tizimi
-   **Hujjat turi:** Dasturiy ta'minot uchun texnik topshiriq

## 1. Loyihaning maqsadi

Mehmonxona boshqaruv tizimining asosiy maqsadi mehmonxona faoliyatiga
oid kundalik jarayonlarni yagona web ilova orqali avtomatlashtirishdan
iborat. Tizim xonalar, mijozlar, bron qilish, mehmonlarni joylashtirish
va chiqarish, qo'shimcha xizmatlar, to'lovlar hamda hisobotlarni
markazlashgan holda boshqarishi kerak.

Tizimdan mehmonxona administratori, menejeri, resepsionisti va
buxgalteri foydalanishi mumkin. Har bir foydalanuvchi faqat o'ziga
berilgan ruxsatlar doirasida amallarni bajarishi kerak.

## 2. Loyiha doirasi

### 2.1. Tizim tarkibiga kiradigan funksiyalar

1.  Foydalanuvchilar, rollar va ruxsatlarni boshqarish.
2.  Mehmonxona xonalari va xona turlarini boshqarish.
3.  Mijozlar ma'lumotlar bazasini yuritish.
4.  Xonalarni bron qilish va bandlikni tekshirish.
5.  Mehmonlarni joylashtirish va chiqarish.
6.  Qo'shimcha xizmatlar buyurtmalarini yuritish.
7.  To'lovlar, qarzdorlik va hisob-kitoblarni boshqarish.
8.  Dashboard va statistik hisobotlar.
9.  Audit jurnali, zaxira nusxasi va xavfsizlik nazorati.

### 2.2. Dastlabki versiyaga kiritilmaydigan, keyinchalik qo'shilishi mumkin bo'lgan funksiyalar

-   Onlayn bron qilish uchun ommaviy mijozlar portali.
-   Bank yoki to'lov tizimlari bilan bevosita integratsiya.
-   SMS va elektron pochta orqali avtomatik xabarnomalar.
-   Booking.com, Airbnb kabi tashqi platformalar bilan integratsiya.
-   Mobil ilova.
-   Ko'p filialli mehmonxona tarmog'ini boshqarish.

Bu funksiyalar alohida talab va kelishuv asosida keyingi versiyalarda
ishlab chiqilishi mumkin.

## 3. Foydalanuvchi rollari

  -----------------------------------------------------------------------
  Rol                                 Asosiy huquqlar
  ----------------------------------- -----------------------------------
  Administrator                       Barcha modullarni boshqarish,
                                      foydalanuvchilar va sozlamalarni
                                      boshqarish

  Menejer                             Xonalar, bronlar, mijozlar,
                                      xizmatlar va hisobotlarni nazorat
                                      qilish

  Resepsionist                        Mijozlarni ro'yxatga olish, bron
                                      yaratish, check-in va check-out

  Buxgalter                           Hisob-fakturalar, to'lovlar,
                                      qaytarishlar va moliyaviy
                                      hisobotlar

  Xodim                               Faqat o'z vazifasiga tegishli,
                                      administrator bergan ruxsatlar
  -----------------------------------------------------------------------

Ruxsatlar faqat rol nomiga qarab emas, alohida permissionlar orqali
boshqarilishi tavsiya etiladi. Masalan, foydalanuvchiga bronni ko'rish
huquqi berilib, uni bekor qilish huquqi berilmasligi mumkin.

# 4. Loyihani ishlab chiqishning 7 bosqichi

## 1-bosqich. Loyiha arxitekturasi va foydalanuvchilarni boshqarish

### Maqsad

Dastur uchun mustahkam texnik asos yaratish, frontend va backend
qismlarini tashkil qilish, ma'lumotlar bazasini ulash hamda
foydalanuvchilarni autentifikatsiya va avtorizatsiya qilish.

### Bajariladigan topshiriqlar

1.  Web ilovaning umumiy arxitekturasini ishlab chiqish.
2.  Frontend va backend loyihalarini yaratish.
3.  Ma'lumotlar bazasini yaratish va ulanish sozlamalarini tayyorlash.
4.  Foydalanuvchilarni tizimga kiritish (login) mexanizmini ishlab
    chiqish.
5.  Zarur bo'lsa, foydalanuvchi yaratish yoki taklif qilish funksiyasini
    qo'shish.
6.  Foydalanuvchi rollari va ruxsatlarini boshqarish.
7.  Tizimdan xavfsiz chiqish funksiyasini yaratish.
8.  Parolni tiklash mexanizmini loyihalash.
9.  Backend API uchun yagona xato javoblari va validatsiya qoidalarini
    belgilash.
10. Muhim foydalanuvchi amallari uchun audit jurnalini boshlang'ich
    darajada tashkil qilish.

### Funksional talablar

-   Har bir foydalanuvchi unikal login yoki elektron pochta orqali
    aniqlanishi kerak.
-   Parollar ochiq matn ko'rinishida saqlanmasligi, zamonaviy xavfsiz
    xeshlash algoritmi bilan xeshlanishi kerak.
-   Himoyalangan sahifalar autentifikatsiyasiz ochilmasligi kerak.
-   Foydalanuvchi faqat o'ziga ruxsat etilgan amallarni bajarishi kerak.
-   Administrator foydalanuvchini faollashtirishi, bloklashi yoki rolini
    o'zgartirishi mumkin bo'lishi kerak.
-   Kirish urinishlari va muhim boshqaruv amallari qayd etilishi kerak.
-   Maxfiy kalitlar va ulanish parollari kod ichida saqlanmasligi kerak.

### Tavsiya etiladigan sahifalar

-   Login sahifasi.
-   Parolni tiklash sahifasi.
-   Dashboard uchun asosiy maket.
-   Foydalanuvchilar ro'yxati.
-   Foydalanuvchi yaratish va tahrirlash sahifasi.
-   Rollar va ruxsatlar sahifasi.

### Bosqich yakunidagi natija

Ishlaydigan autentifikatsiya va avtorizatsiya mexanizmi, foydalanuvchi
rollari, frontend/backend loyihalari va ma'lumotlar bazasiga ulanish
tayyor bo'lishi kerak.

------------------------------------------------------------------------

## 2-bosqich. Mehmonxona xonalari va xona turlarini boshqarish

### Maqsad

Mehmonxonadagi xonalarni elektron shaklda ro'yxatga olish, ularning
xususiyatlari, narxlari va joriy holatini boshqarish.

### Bajariladigan topshiriqlar

1.  Xona turlarini yaratish va tahrirlash.
2.  Yangi xona qo'shish.
3.  Xona raqami, qavati va sig'imini belgilash.
4.  Har bir xona uchun standart narxni kiritish.
5.  Xona qulayliklari va tavsifini saqlash.
6.  Xona rasmlarini biriktirish imkoniyatini yaratish.
7.  Xona holatini boshqarish.
8.  Xonalarni qidirish, filtrlash va saralash.
9.  Xonani vaqtincha foydalanishdan chiqarish yoki ta'mir holatiga
    o'tkazish.
10. Xona ma'lumotlarini o'zgartirish tarixini zarur hollarda qayd etish.

### Xona turlari

-   Standart (Standard).
-   Ikki kishilik (Double).
-   Yarim lyuks (Junior Suite).
-   Lyuks (Suite).
-   Oilaviy xona (Family Room).

Xona turlari administrator tomonidan qo'shilishi va tahrirlanishi mumkin
bo'lishi kerak. Yuqoridagi ro'yxat namunaviy hisoblanadi.

### Xona holatlari

  Holat             Tavsif
  ----------------- -------------------------------------------
  Bo'sh va tayyor   Hozir joylashtirish mumkin
  Band              Kelajak uchun tasdiqlangan bron mavjud
  Yashamoqda        Xonada mehmon bor
  Tozalanmoqda      Mehmon chiqib ketgan, xona tayyorlanmoqda
  Ta'mirda          Xona vaqtincha foydalanilmaydi

**Muhim:** "Bron qilingan" holati bilan "hozir mehmon yashayapti"
holatini farqlash kerak. Xonaning joriy operatsion holati va kelajakdagi
bandlik jadvali alohida boshqarilishi lozim. Xona bandligini faqat bitta
status maydoniga tayanib aniqlash mumkin emas.

### Har bir xona uchun saqlanadigan ma'lumotlar

-   Xona ID raqami.
-   Xona raqami.
-   Qavat.
-   Xona turi.
-   Standart bir kechalik narxi.
-   Maksimal mehmonlar soni.
-   Xona tavsifi.
-   Qulayliklar (Wi-Fi, televizor, konditsioner va boshqalar).
-   Joriy operatsion holati.
-   Xona rasmlari.
-   Yaratilgan va yangilangan sana.

### Qo'shimcha funksiyalar

-   Xona raqami bo'yicha qidirish.
-   Xona turi bo'yicha filtrlash.
-   Narx bo'yicha saralash.
-   Ta'mirdagi xonalarni alohida ko'rsatish.
-   Xonalar ro'yxatini jadval yoki kartochka ko'rinishida ko'rsatish.

### Bosqich yakunidagi natija

Mehmonxonaning barcha xonalarini qo'shish, tahrirlash, qidirish va
ularning joriy holatini kuzatish imkoniyati yaratilishi kerak.

------------------------------------------------------------------------

## 3-bosqich. Mijozlar ma'lumotlar bazasini boshqarish

### Maqsad

Mehmonxona xizmatlaridan foydalanuvchi mijozlar haqidagi ma'lumotlarni
markazlashgan holda saqlash va ularning tashriflari tarixini yuritish.

### Bajariladigan topshiriqlar

1.  Yangi mijoz qo'shish modulini yaratish.
2.  Mijoz ma'lumotlarini tahrirlash.
3.  Mijozlar ro'yxatini shakllantirish.
4.  Mijozlarni ism, telefon yoki hujjat ma'lumotlari orqali qidirish.
5.  Mijozning oldingi bronlari va tashriflari tarixini ko'rsatish.
6.  Mijozning to'lovlari va qarzdorligini ko'rsatish.
7.  Takroriy mijoz yozuvlarini aniqlashga yordam berish.
8.  Mijoz ma'lumotlarini eksport qilish imkoniyatini yaratish.
9.  Shaxsiy ma'lumotlarga kirishni rollar bo'yicha cheklash.

### Mijoz ma'lumotlari

  Maydon            Tavsif
  ----------------- ---------------------------------------
  Customer ID       Unikal mijoz identifikatori
  Ism               Mijoz ismi
  Familiya          Mijoz familiyasi
  Telefon           Aloqa raqami
  Elektron pochta   Email manzili, ixtiyoriy
  Hujjat turi       Pasport yoki ID-karta
  Hujjat raqami     Shaxsni tasdiqlovchi hujjat ma'lumoti
  Davlat            Fuqaroligi
  Tug'ilgan sana    Tug'ilgan sana, zarur bo'lsa
  Manzil            Yashash manzili, zarur bo'lsa
  Izoh              Qo'shimcha izoh

### Qo'shimcha funksiyalar

-   Mijoz profilini ko'rish.
-   Mijozning barcha bronlari va tashriflarini ko'rish.
-   Mijozning to'lov tarixini ko'rish.
-   Doimiy mijozlarni belgilash.
-   Mijozlar ro'yxatini PDF yoki Excel formatida eksport qilish.
-   Mijoz ma'lumotlarini o'zgartirish huquqini cheklash.

### Maxfiylik talablari

Pasport va boshqa shaxsiy ma'lumotlar maxfiy hisoblanadi. Ularni faqat
tegishli ruxsatga ega xodimlar ko'ra olishi kerak. Keraksiz shaxsiy
ma'lumotlarni yig'maslik, eksport qilish va saqlashni nazorat qilish
zarur.

### Bosqich yakunidagi natija

Mijozlarni ro'yxatga olish, tahrirlash, qidirish va ularning
mehmonxonadagi faoliyat tarixini ko'rish imkoniyati yaratilishi kerak.

------------------------------------------------------------------------

## 4-bosqich. Xonalarni bron qilish tizimi

### Maqsad

Mijozlar uchun xonalarni oldindan band qilish, belgilangan sanalar
oralig'ida bo'sh xonalarni aniqlash va bron jarayonini
avtomatlashtirish.

### Bajariladigan topshiriqlar

1.  Yangi bron yaratish modulini ishlab chiqish.
2.  Mijozni tanlash yoki yangi mijoz qo'shish.
3.  Kelish va ketish sanalarini belgilash.
4.  Kattalar va bolalar sonini kiritish.
5.  Belgilangan sanalar oralig'ida bo'sh xonalarni aniqlash.
6.  Xona turini va mavjud xonani tanlash.
7.  Bron narxini avtomatik hisoblash.
8.  Bronni tasdiqlash, tahrirlash va bekor qilish.
9.  Bron holatini kuzatish.
10. Bron bo'yicha izoh va maxsus talablarni saqlash.
11. Bron tasdig'i yoki ma'lumotnomasini chop etish imkoniyatini
    yaratish.

### Bron qilish jarayoni

1.  Mijozni tanlash.
2.  Kelish va ketish sanalarini kiritish.
3.  Mehmonlar sonini belgilash.
4.  Bo'sh xonalarni tekshirish.
5.  Mos xonani tanlash.
6.  Narx va umumiy summani hisoblash.
7.  Bron ma'lumotlarini tekshirish.
8.  Bronni tasdiqlash.

### Bron holatlari

  Holat                          Tavsif
  ------------------------------ --------------------------------
  Kutilmoqda (Pending)           Bron hali tasdiqlanmagan
  Tasdiqlangan (Confirmed)       Bron tasdiqlangan
  Bekor qilingan (Cancelled)     Bron bekor qilingan
  Joylashtirilgan (Checked-in)   Mijoz mehmonxonaga kelgan
  Yakunlangan (Completed)        Mijozning yashashi yakunlangan
  Kelmagan (No-show)             Mijoz bron bo'yicha kelmagan

### Narxni hisoblash

Misol:

-   Xona narxi: 300 000 so'm.
-   Tunlar soni: 3.
-   Jami xona qiymati: 900 000 so'm.

Formula:

`Xona qiymati = Bir kechalik narx × Tunlar soni`

Bronning yakuniy qiymatiga chegirma, soliq yoki qo'shimcha shartlar
qo'llansa, ular alohida ko'rsatilishi kerak. Bron tasdiqlanganidan keyin
narx o'zgarsa, eski narx tarixi saqlanishi lozim.

### Muhim texnik talablar

-   Bir xona bir xil sanalar oralig'ida ikki xil faol bron bilan band
    qilinmasligi kerak.
-   Sana oralig'i server tomonida tekshirilishi shart.
-   Bir vaqtning o'zida ikki foydalanuvchi bir xonani bron qilishga
    urinsa, ma'lumotlar bazasi darajasida ziddiyatning oldi olinishi
    kerak.
-   Ketish sanasi chiqish kuni sifatida qaraladi: bir mijoz ketadigan
    kuni boshqa mijoz kelishi mumkin.
-   Bekor qilingan bronlar bandlikni to'sib qo'ymasligi kerak.
-   Ta'mirdagi yoki foydalanishdan chiqarilgan xonalar bron uchun taklif
    qilinmasligi kerak.
-   Bronni bekor qilish sababi va amalni bajargan foydalanuvchi qayd
    etilishi kerak.

### Bosqich yakunidagi natija

Mijozlar uchun xonalarni bron qilish, mavjudlikni tekshirish, bronlarni
tasdiqlash va bekor qilish imkoniyati yaratilishi kerak.

------------------------------------------------------------------------

## 5-bosqich. Mijozlarni joylashtirish va mehmonxona xizmatlarini boshqarish

### Maqsad

Mehmonlarni amalda joylashtirish, ularning yashash muddatini nazorat
qilish, chiqarish va qo'shimcha xizmatlarni hisobga olish.

### Bajariladigan topshiriqlar

1.  Check-in modulini yaratish.
2.  Check-out modulini yaratish.
3.  Bron qilingan xonani mijozga biriktirish.
4.  Mijozning haqiqiy kelgan vaqtini qayd etish.
5.  Mijozning chiqib ketish vaqtini qayd etish.
6.  Yashash muddatini hisoblash.
7.  Qo'shimcha xizmatlar ro'yxatini yaratish.
8.  Xizmat buyurtmalarini mijoz hisobiga biriktirish.
9.  Xona tozalash holatini boshqarish.
10. Erta kelish yoki kech chiqish holatlarini qayd etish.

### Check-in jarayoni

1.  Resepsionist tasdiqlangan bronni tanlaydi.
2.  Mijoz ma'lumotlari va zarur hujjatlar tekshiriladi.
3.  Haqiqiy kelish vaqti qayd etiladi.
4.  Xona biriktiriladi yoki bron qilingan xona tasdiqlanadi.
5.  Joylashtirish amali yakunlanadi.
6.  Xonaning joriy holati "Yashamoqda" deb belgilanadi.

### Qo'shimcha xizmatlar

-   Nonushta.
-   Restoran.
-   Kir yuvish.
-   Xona tozalash.
-   Transfer.
-   Avtoturargoh.
-   Boshqa pullik xizmatlar.

### Xizmat buyurtmasi ma'lumotlari

-   Xizmat ID raqami.
-   Xizmat nomi.
-   Xizmat narxi.
-   Buyurtma sanasi va vaqti.
-   Buyurtma miqdori.
-   Mijoz yoki yashash yozuvi.
-   Xona.
-   Umumiy qiymat.
-   Buyurtmani kiritgan xodim.
-   Buyurtma holati.

### Check-out jarayoni

1.  Mijozning yashash yozuvi tanlanadi.
2.  Xona uchun hisoblangan summa tekshiriladi.
3.  Qo'shimcha xizmatlar qiymati qo'shiladi.
4.  To'lovlar va qarzdorlik tekshiriladi.
5.  Mijozning chiqib ketish vaqti qayd etiladi.
6.  Yashash yozuvi yakunlanadi.
7.  Xona "Tozalanmoqda" holatiga o'tkaziladi.
8.  Tozalash tugagach, xona "Bo'sh va tayyor" holatiga qaytariladi.

To'liq to'lov qilinmagan holatda check-outni yakunlashga ruxsat berish
yoki bermaslik biznes qoidasi sifatida administrator tomonidan
belgilanadigan bo'lishi mumkin. Agar qarz bilan chiqishga ruxsat
berilsa, qarzdorlik alohida qayd etilishi shart.

### Bosqich yakunidagi natija

Mehmonlarni joylashtirish, chiqarish, yashash muddatini nazorat qilish
va qo'shimcha xizmatlarni hisobga olish imkoniyati yaratilishi kerak.

------------------------------------------------------------------------

## 6-bosqich. To'lovlar va moliyaviy hisobotlarni boshqarish

### Maqsad

Mehmonxona xizmatlari uchun to'lovlarni qayd etish, mijoz hisobini
shakllantirish, qarzdorlikni aniqlash va moliyaviy hisobotlarni
tayyorlash.

### Bajariladigan topshiriqlar

1.  To'lovlarni boshqarish modulini yaratish.
2.  Mijoz hisobini avtomatik shakllantirish.
3.  Naqd va naqdsiz to'lovlarni qayd etish.
4.  Qisman to'lovlarni amalga oshirish.
5.  Qarzdorlikni hisoblash.
6.  To'lovni qaytarish operatsiyasini qayd etish.
7.  Chek yoki kvitansiya yaratish.
8.  Kunlik, haftalik, oylik va yillik hisobotlarni shakllantirish.
9.  To'lovlarni sana, mijoz, usul va xodim bo'yicha filtrlash.
10. Moliyaviy ma'lumotlarni PDF yoki Excel formatida eksport qilish.

### To'lov turlari

-   Naqd pul.
-   Bank kartasi.
-   Bank o'tkazmasi.
-   Boshqa elektron to'lov usullari.

Agar tashqi to'lov provayderi bilan integratsiya qilinmagan bo'lsa,
tizim faqat xodim kiritgan to'lov yozuvini qayd etadi. Bunday holatda
to'lov avtomatik ravishda bankdan tasdiqlangan deb ko'rsatilmasligi
kerak.

### Hisob-kitob namunasi

  Xizmat                      Qiymati
  -------------- --------------------
  3 kecha xona           900 000 so'm
  Nonushta               150 000 so'm
  Kir yuvish              50 000 so'm
  **Jami**         **1 100 000 so'm**
  To'langan              800 000 so'm
  **Qarz**           **300 000 so'm**

Formulalar:

`Jami = Xona qiymati + Qo‘shimcha xizmatlar + Qo‘llaniladigan soliqlar − Chegirmalar`

`Qarz = Jami − Jami to‘langan summa`

Hisob-kitoblarda pul qiymatlari suzuvchi nuqtali (float) turda emas,
aniq kasrli decimal turida saqlanishi kerak.

### Hisobotlar

-   Kunlik tushum.
-   Oylik tushum.
-   Yillik tushum.
-   To'lanmagan hisoblar.
-   Mijozlar bo'yicha xarajatlar.
-   To'lov usullari bo'yicha statistika.
-   Xonalar bandlik darajasi.
-   Xona turlari bo'yicha bandlik.
-   Qo'shimcha xizmatlar bo'yicha tushum.

### Texnik talablar

-   Har bir to'lov alohida yozuv sifatida saqlanishi kerak.
-   To'lovni amalga oshirgan foydalanuvchi qayd etilishi kerak.
-   To'lov sanasi va vaqti saqlanishi kerak.
-   Bir operatsiyani takroran yuborishdan himoya bo'lishi kerak.
-   To'lovni o'chirish o'rniga, qaytarish yoki bekor qilish amali audit
    izi bilan qayd etilishi kerak.
-   Hisobotlar tanlangan sana oralig'i bo'yicha shakllantirilishi kerak.
-   To'lov va hisob-kitoblar o'zaro tekshiriladigan bo'lishi kerak.

### Bosqich yakunidagi natija

Mehmonxonaning moliyaviy operatsiyalarini nazorat qilish, mijoz
hisoblarini yuritish va hisobotlarni olish imkoniyati yaratilishi kerak.

------------------------------------------------------------------------

## 7-bosqich. Dashboard, integratsiya, test va tizimni ishga tushirish

### Maqsad

Barcha modullarni yagona tizimga birlashtirish, boshqaruv panelini
yaratish, xatolarni aniqlash, xavfsizlikni tekshirish va dasturni
foydalanishga tayyorlash.

### Bajariladigan topshiriqlar

1.  Dashboard yaratish.
2.  Barcha modullarni o'zaro integratsiya qilish.
3.  Umumiy statistik ma'lumotlarni ko'rsatish.
4.  Grafik va diagrammalar yaratish.
5.  Qidiruv va filtrlash imkoniyatlarini takomillashtirish.
6.  Dastur xavfsizligini tekshirish.
7.  Backend va frontend testlarini o'tkazish.
8.  Ma'lumotlar bazasi zaxira nusxasini yaratish mexanizmini ishlab
    chiqish.
9.  Zaxira nusxadan tiklash jarayonini sinash.
10. Loyihani serverga joylashtirish.
11. Foydalanuvchi qo'llanmasini tayyorlash.
12. Yakuniy texnik hujjatlarni rasmiylashtirish.

### Dashboard tarkibi

Dashboard quyidagi ko'rsatkichlarni aks ettirishi kerak:

-   Jami xonalar soni.
-   Hozir bo'sh va tayyor xonalar.
-   Hozir mehmon yashayotgan xonalar.
-   Ta'mir yoki tozalashdagi xonalar.
-   Bugungi keluvchilar.
-   Bugungi ketuvchilar.
-   Bugungi bronlar.
-   Bugungi tushum.
-   To'lanmagan hisoblar.
-   Xonalar bandlik darajasi.

Ko'rsatkichlar haqiqiy ma'lumotlar bazasidan olinishi kerak. Sinov
ma'lumotlari ishlab chiqarish muhitida haqiqiy statistika sifatida
ko'rsatilmasligi lozim.

### Testdan o'tkazish

Quyidagi holatlar tekshirilishi kerak:

-   Noto'g'ri login va parol bilan kirish.
-   Ruxsatsiz foydalanuvchining yopiq modullarga kirishi.
-   Bir xonani bir xil sanalarga ikki marta bron qilishga urinish.
-   Mijoz ma'lumotlarini noto'g'ri kiritish.
-   Bronni bekor qilish.
-   Mijozni joylashtirish va chiqarish.
-   Qisman va to'liq to'lovlar.
-   Qarzdorlikni to'g'ri hisoblash.
-   To'lovni qaytarish.
-   Hisobotlarning to'g'ri shakllanishi.
-   Ma'lumotlar bazasini zaxiralash va tiklash.
-   Telefon va planshet ekranlarida interfeysning to'g'ri ishlashi.

### Bosqich yakunidagi natija

Barcha funksiyalari birlashtirilgan, sinovdan o'tkazilgan, xavfsiz va
foydalanishga tayyor mehmonxona boshqaruv web ilovasi ishlab chiqilishi
kerak.

# 5. Tavsiya etiladigan texnologik stek

Quyidagi texnologiyalar loyiha uchun tavsiya etiladi. Zarurat bo'lsa,
ishlab chiqish boshlanishidan oldin ularni o'zgartirish mumkin.

  Qism               Texnologiya             Vazifasi
  ------------------ ----------------------- ----------------------------------------
  Frontend           React.js                Foydalanuvchi interfeysi
  Dasturlash tili    TypeScript              Frontend kodining tiplashtirilishi
  UI/CSS             Tailwind CSS            Dizayn va moslashuvchan interfeys
  Backend            ASP.NET Core Web API    Biznes mantiqi va API
  Backend tili       C#                      Server dasturlash
  ORM                Entity Framework Core   Ma'lumotlar bazasi bilan ishlash
  Database           PostgreSQL              Ma'lumotlarni saqlash
  API hujjati        Swagger / OpenAPI       API hujjatlari va sinash
  Versiya nazorati   Git                     Kod tarixini boshqarish
  Deploy             Docker                  Ilovani konteynerlarda ishga tushirish
  Reverse proxy      Nginx                   HTTP/HTTPS so'rovlarini yo'naltirish

## 6. Ma'lumotlar bazasining asosiy jadvallari

Quyidagi jadvallar boshlang'ich ma'lumotlar modeli sifatida tavsiya
etiladi. Yakuniy sxema ishlab chiqish davomida bog'lanishlar, cheklovlar
va normalizatsiya asosida aniqlashtiriladi.

     № Jadval nomi         Vazifasi
  ---- ------------------- --------------------------------------------
     1 Users               Tizim foydalanuvchilari
     2 Roles               Foydalanuvchi rollari
     3 Permissions         Ruxsatlar
     4 UserRoles           Foydalanuvchi va rol bog'lanishi
     5 RolePermissions     Rol va ruxsat bog'lanishi
     6 Rooms               Mehmonxona xonalari
     7 RoomTypes           Xona turlari
     8 RoomAmenities       Xona qulayliklari
     9 Customers           Mijozlar
    10 Reservations        Bronlar
    11 ReservationRooms    Bron tarkibidagi xonalar
    12 ReservationGuests   Bron tarkibidagi mehmonlar
    13 Stays               Haqiqiy joylashtirish va yashash yozuvlari
    14 Services            Qo'shimcha xizmatlar
    15 ServiceOrders       Xizmat buyurtmalari
    16 Invoices            Hisob-fakturalar
    17 InvoiceItems        Hisob tarkibidagi xizmat va xarajatlar
    18 Payments            To'lovlar
    19 Refunds             To'lov qaytarish yozuvlari
    20 Housekeeping        Xona tozalash vazifalari
    21 Expenses            Mehmonxona xarajatlari
    22 AuditLogs           Tizim amallari tarixi

### Ma'lumotlar bazasi bo'yicha muhim qoidalar

-   Har bir asosiy jadvalda unikal birlamchi kalit bo'lishi kerak.
-   Jadvallar orasidagi bog'lanishlar foreign key orqali belgilanishi
    kerak.
-   Telefon, hujjat raqami va boshqa maydonlar uchun zarur validatsiya
    bo'lishi kerak.
-   Sana va vaqt qiymatlari izchil formatda saqlanishi kerak.
-   Pul qiymatlari uchun `DECIMAL` yoki PostgreSQL `NUMERIC`
    ishlatilishi kerak.
-   Bron va to'lov kabi muhim operatsiyalar tranzaksiyalar orqali
    bajarilishi kerak.
-   Ma'lumotlarni fizik o'chirish o'rniga, zarur hollarda arxivlash yoki
    soft delete ishlatilishi kerak.
-   Tez-tez qidiriladigan ustunlar uchun tegishli indekslar yaratilishi
    kerak.

# 7. Umumiy funksional va nofunksional talablar

## 7.1. Funksional talablar

1.  Tizim foydalanuvchilarni autentifikatsiya qilishi kerak.
2.  Rollar va ruxsatlar asosida modullarga kirishni cheklashi kerak.
3.  Xonalar va xona turlarini boshqarishi kerak.
4.  Mijozlar ma'lumotlarini saqlashi va qidirishi kerak.
5.  Bronlarni yaratishi, o'zgartirishi va bekor qilishi kerak.
6.  Xona mavjudligini sanalar bo'yicha tekshirishi kerak.
7.  Mehmonlarni joylashtirish va chiqarishni qayd etishi kerak.
8.  Qo'shimcha xizmatlarni hisobga olishi kerak.
9.  To'lovlar va qarzdorlikni yuritishi kerak.
10. Dashboard va hisobotlarni shakllantirishi kerak.
11. Muhim amallar tarixini saqlashi kerak.

## 7.2. Nofunksional talablar

### Xavfsizlik

-   Tizim HTTPS orqali ishlashi kerak.
-   Parollar xavfsiz xeshlanishi kerak.
-   SQL Injection va XSS kabi keng tarqalgan hujumlardan himoya bo'lishi
    kerak.
-   API endpointlarida autentifikatsiya va avtorizatsiya tekshirilishi
    kerak.
-   Maxfiy ma'lumotlar loglarda ochiq ko'rinishda yozilmasligi kerak.
-   Foydalanuvchi sessiyalari xavfsiz boshqarilishi kerak.

### Ishlash tezligi

-   Oddiy sahifalar va ro'yxatlar odatiy ish yuklamasida tez ochilishi
    kerak.
-   Katta ro'yxatlar sahifalash (pagination) orqali yuklanishi kerak.
-   Qidiruv va filtrlash imkon qadar server tomonida bajarilishi kerak.
-   Ma'lumotlar bazasidagi so'rovlar indekslar yordamida
    optimallashtirilishi kerak.

### Moslashuvchanlik

-   Tizim kompyuter, planshet va smartfon ekranlariga mos bo'lishi
    kerak.
-   Interfeys asosiy zamonaviy brauzerlarda ishlashi kerak.
-   Foydalanuvchiga xatolar tushunarli tilda ko'rsatilishi kerak.

### Ishonchlilik

-   Ma'lumotlar muntazam zaxiralanishi kerak.
-   Zaxira nusxadan tiklash imkoniyati tekshirilishi kerak.
-   Muhim operatsiyalar tranzaksiyalar orqali bajarilishi kerak.
-   Xatolik yuz berganda ma'lumotlar qisman yoki noto'g'ri yozilib
    qolmasligi kerak.

# 8. Asosiy biznes qoidalari

1.  Xona bir vaqtning o'zida bir nechta faol bron bilan bir xil sana
    oralig'ida band qilinmasligi kerak.
2.  Bron uchun kelish sanasi ketish sanasidan oldin bo'lishi kerak.
3.  Mehmonlar soni xona sig'imidan oshmasligi kerak; oshirilsa, alohida
    ruxsat yoki qoida talab qilinadi.
4.  Ta'mirdagi xona bron qilish uchun mavjud deb ko'rsatilmasligi kerak.
5.  Bron narxi tasdiqlangan paytdagi shartlar asosida saqlanishi kerak.
6.  Bron bekor qilinganda uning tarixi saqlanishi kerak.
7.  Check-in faqat tegishli bron yoki ruxsat etilgan walk-in jarayoni
    orqali bajarilishi kerak.
8.  Check-out paytida yakuniy hisob shakllantirilishi kerak.
9.  To'lovlar alohida yozuvlarda saqlanishi va hisob bilan bog'lanishi
    kerak.
10. To'lovni qaytarish asl to'lov bilan bog'langan alohida operatsiya
    bo'lishi kerak.
11. Muhim ma'lumotlarni o'zgartirgan foydalanuvchi va amal vaqti qayd
    etilishi kerak.
12. Barcha hisob-kitoblarda pul aniqligi saqlanishi kerak.

# 9. Yakuniy topshiriladigan natijalar

Loyiha yakunlanganda quyidagilar taqdim etilishi kerak:

1.  Ishlaydigan mehmonxona boshqaruv web ilovasi.
2.  Frontend dasturiy kodi.
3.  Backend dasturiy kodi.
4.  Ma'lumotlar bazasi sxemasi va migratsiyalari.
5.  API hujjatlari.
6.  Administrator va boshqa foydalanuvchilar uchun boshqaruv paneli.
7.  Test natijalari.
8.  Loyihani o'rnatish va ishga tushirish yo'riqnomasi.
9.  Foydalanuvchi qo'llanmasi.
10. Zaxira nusxa olish va tiklash bo'yicha yo'riqnoma.
11. Zarur bo'lsa, loyiha taqdimoti va ekran tasvirlari.

# 10. Yetti bosqichning umumiy bajarilish jadvali

    Bosqich Ish nomi                          Asosiy natija
  --------- --------------------------------- --------------------------
          1 Arxitektura va foydalanuvchilar   Login, rollar, ruxsatlar
          2 Xonalarni boshqarish              Xonalar va xona turlari
          3 Mijozlarni boshqarish             Mijozlar bazasi
          4 Bron qilish                       Bron va bandlik nazorati
          5 Joylashtirish va xizmatlar        Check-in, Check-out
          6 To'lovlar va hisobotlar           Moliyaviy modul
          7 Dashboard va test                 Tayyor web ilova

# 11. AI agent uchun loyiha ustida ishlash bo'yicha ko'rsatmalar

Ushbu hujjat AI dasturlash agentiga loyiha talablari sifatida berilishi
mumkin.

AI agent quyidagi qoidalarga amal qilishi kerak:

1.  Avval texnik topshiriqni to'liq o'qib, talablarni tahlil qilsin.
2.  Kod yozishni boshlashdan oldin umumiy arxitektura, papkalar
    strukturasi, ma'lumotlar bazasi modeli va modullar o'rtasidagi
    bog'lanishlarni taklif qilsin.
3.  Tanlangan texnologiyalar va versiyalarni hujjatlashtirsin.
4.  Loyihani 7 bosqich bo'yicha ketma-ket ishlab chiqsin.
5.  Har bir bosqichni tugatgach, build va testlarni ishga tushirsin.
6.  Xatolarni tuzatmasdan keyingi bosqichga o'tmasin.
7.  Avval yaratilgan kod va ma'lumotlar bazasi strukturasi bilan
    moslikni saqlasin.
8.  Mavjud funksiyalarni sababsiz o'zgartirmasin yoki o'chirib
    yubormasin.
9.  Maxfiy kalitlar, parollar va ulanish ma'lumotlarini kodga yozmasin;
    environment variables ishlatsin.
10. Har bir muhim modul uchun qisqa texnik hujjat va testlar yaratsin.
11. Amalga oshirilmagan funksiyalarni tayyor deb ko'rsatmasin.
12. Talabda noaniqlik bo'lsa, taxminni yashirmasdan uni alohida qayd
    etsin va zarur bo'lsa savol bersin.
13. Har bir bosqich yakunida bajarilgan ishlar, yaratilgan fayllar, test
    natijalari va qolgan vazifalar haqida hisobot bersin.
14. Kodni tushunarli, modulli va keyinchalik kengaytirish mumkin bo'lgan
    shaklda yozsin.

### AI agent uchun tavsiya etiladigan ish tartibi

-   **1-qadam:** Talablarni tahlil qilish va arxitekturani tasdiqlash.
-   **2-qadam:** Ma'lumotlar bazasi modeli va migratsiyalarni yaratish.
-   **3-qadam:** Backend autentifikatsiyasi va umumiy API
    infratuzilmasini yaratish.
-   **4-qadam:** Frontend maketi va umumiy komponentlarni yaratish.
-   **5-qadam:** 2--6-bosqich modullarini ketma-ket ishlab chiqish.
-   **6-qadam:** Dashboard, integratsiya va testlarni bajarish.
-   **7-qadam:** Docker orqali ishga tushirish, hujjatlashtirish va
    yakuniy tekshiruv.

## 12. Loyiha muvaffaqiyat mezonlari

Loyiha quyidagi shartlar bajarilganda muvaffaqiyatli yakunlangan
hisoblanadi:

-   Barcha asosiy modullar ishlaydi.
-   Foydalanuvchi rollari va ruxsatlari to'g'ri ishlaydi.
-   Xona bandligi sanalar bo'yicha to'g'ri aniqlanadi.
-   Bir xonani bir xil vaqt oralig'ida ikki marta bron qilib bo'lmaydi.
-   Check-in va check-out jarayonlari to'g'ri bajariladi.
-   Xona va qo'shimcha xizmatlar qiymati to'g'ri hisoblanadi.
-   Qisman to'lov va qarzdorlik to'g'ri yuritiladi.
-   Hisobotlar ma'lumotlar bazasidagi haqiqiy ma'lumotlarga mos keladi.
-   Muhim amallar audit jurnalida qayd etiladi.
-   Ilova turli ekran o'lchamlarida foydalanishga yaroqli bo'ladi.
-   Loyihani o'rnatish va ishga tushirish bo'yicha hujjatlar mavjud
    bo'ladi.

------------------------------------------------------------------------

**Hujjat yakuni**

**Loyiha:** Mehmonxona boshqaruv tizimi (Hotel Management System)

**Talaba:** Iskandarov Dilshodbek

**Guruh:** Masofaviy KIDT-236

**Mavzu:** 4-mavzu
