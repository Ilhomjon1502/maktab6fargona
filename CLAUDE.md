# 6-maktab × Codial sayti

Farg'ona shahridagi 6-maktabda o'tadigan tadbir uchun sayt. O'quvchilar pechat qilingan QR kodni skanerlaydi va shu saytga tushadi. Saytning asosiy vazifasi — Codial IT akademiyasini tanishtirish va bolalarni darsga yozilish formasiga yo'naltirish.

## Eng muhim qoida: manzil o'zgarmasligi kerak

- Jonli sayt: https://ilhomjon1502.github.io/maktab6fargona/
- Repo: https://github.com/Ilhomjon1502/maktab6fargona (public)
- QR kod shu manzilga olib boradi va allaqachon **pechat qilingan**. Shuning uchun:
  - repo nomini o'zgartirma, repo'ni o'chirma yoki private qilma;
  - GitHub Pages sozlamasini (`main` branch, `/` root) o'zgartirma;
  - `index.html` ildizda qolishi shart — boshqa papkaga ko'chirma, build tizimi qo'shma.

## Yangilash (deploy)

GitHub Pages `main` branch'dan avtomatik chiqaradi. Build yo'q.

1. `index.html` ni tahrirla.
2. `git add` → `git commit` → `git push`.
3. 30–90 soniyada jonli saytda paydo bo'ladi. Tekshirish:
   `curl -s https://ilhomjon1502.github.io/maktab6fargona/ | grep "<qidirilayotgan matn>"`

Commit xabarlari o'zbek tilida yoziladi. Push qilishga foydalanuvchi oldindan ruxsat bergan — bu loyihada saytni yangilash = push.

## Lokal ko'rish

`.claude/launch.json` da `site` konfiguratsiyasi bor (`python -m http.server 8000`). Browser pane'da `preview_start` → `site`. Faylni `file://` orqali ochsa, rasmlar ko'rinmaydi — server orqali och. Har doim telefon o'lchamida (375px) tekshir: bolalar saytni telefondan ochadi.

## Fayllar

- `index.html` — butun sayt, CSS ichida. Tashqi kutubxona, framework, JS yo'q — shunday qolsin (maktab internetida ham tez ochilsin).
- `img/codial-white.png` — oq logo (to'q fon uchun, hero'da).
- `img/codial.png` — rangli logo (oq fon uchun, footer'da).
- `img/tadbir/` — 2026-10-13 dagi tadbir rasmlari (WebP, ≤1200px, metadata'siz). `iqtidorlilar-*` — "Eng iste'dodlilar" bo'limi, `tadbir-*` — "Tadbirdan lavhalar" galereyasi. Yangi rasm qo'shsang, shu tarzda kichraytir. O'quvchilarning ism-familiyasini sayt matniga yozma.
- `qr/qr-maktab6.png` (2000px), `qr/qr-maktab6.svg` — pechat uchun QR kod. Manzil o'zgarmagani uchun qayta yaratish shart emas.

## Uslub

- Til: o'zbek, lotin yozuvi. Bolalarga **"sen"** deb murojaat qilinadi ("yozil", "o'rganasan").
- Brend ranglari (logodan): ko'k `#00527E`, to'q sariq `#FF9F00`. CSS o'zgaruvchilari `:root` da.
- Mobile-first, katta tugmalar, kam matn.
- Yolg'on shoshiltirish yozma ("joylar cheklangan" va h.k.) — faqat foydalanuvchi tasdiqlagan faktlar.

## Codial haqida faktlar (foydalanuvchi tasdiqlagan, 2026-10-13)

- Faqat **Farg'ona** filiali bor (Marg'ilon filiali yo'q).
- 2021-yilda Inha universiteti bitiruvchisi tashkil etgan.
- **11 yoshdan** boshlab o'qitadi.
- Kurslar va narxlar:
  | Kurs | Narx | Davomiyligi |
  |---|---|---|
  | Kompyuter savodxonligi | 500 000 so'm | 1 oy |
  | Vibe coding | 750 000 so'm | ko'rsatilmaydi |
  | Backend | 750 000 so'm | — |
  | Flutter | 750 000 so'm | — |
  | SMM | 750 000 so'm | — |
  | Kiberxavfsizlik | 750 000 so'm | — |

  Narxlar **oylik** (foydalanuvchi tasdiqlagan) — saytda "/ oy" deb ko'rsatiladi.
- Ijtimoiy tarmoqlar: Telegram https://t.me/codialuz · Instagram https://instagram.com/codialuz · YouTube https://youtube.com/@Codialuz
- Rasmiy veb-sayt yo'q (codial.uz ishlamaydi) — havola qo'yma.
- Tadbirda (2026-10-13) eng iste'dodli o'quvchilarga **Kompyuter savodxonligi** kursi uchun 100% va 50% bonus sertifikatlari berildi. Ishlatish tartibi (tadbirdagi slayddan): sertifikatni oladi → ota-onasi bilan Codial'ga keladi → bepul sinov darsiga yoziladi; bonus **7 kun** ichida amal qiladi.

## Darsga yozilish formasi

https://docs.google.com/forms/d/e/1FAIpQLScp8WSYWbmNAnGnI8BsWC_n4uGWP0D1zpC52tTn2b72hFYV5Q/viewform

Forma nomi "Faqat 6-maktab uchun". Maydonlar: ism, telefon, notebook bormi (Bor/Yo'q), sinf. Saytdagi "Qanday yozilaman?" qadamlari shu maydonlarga mos — forma o'zgarsa, ularni ham yangila. Saytda forma havolasi ikki joyda (hero va pastdagi CTA) — ikkalasini birga o'zgartir.
