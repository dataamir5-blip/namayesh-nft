# راه‌اندازی نسخه Production

این پروژه «production-ready starter» است، نه قرارداد ممیزی‌شده یا سرویس deploy شده.

## 1) نصب
`npm install`

## 2) دیتابیس
`.env` را از `.env.example` بسازید و `DATABASE_URL` را تنظیم کنید.
سپس:
`npx prisma generate`
`npm run db:push`

## 3) قرارداد
`npm install @openzeppelin/contracts`
کلید deployer را هرگز داخل repository نگذارید.
قراردادها را ابتدا روی testnet مستقر و تست کنید.

## 4) Polygon
برای Polygon PoS از chain ID 137 استفاده می‌شود. آدرس قرارداد deploy شده را در `NEXT_PUBLIC_CONTRACT_ADDRESS` قرار دهید.

## 5) قبل از mainnet
- audit مستقل قراردادها
- تست واحد و fuzz/invariant
- multisig برای treasury/admin
- محدودسازی API و احراز امضای wallet
- IPFS/Arweave pinning و backup
- indexer برای رویدادهای زنجیره
- monitoring و alerting
- moderation و گزارش محتوا
- بررسی حقوقی، مالیاتی و مقرراتی متناسب با حوزه فعالیت
