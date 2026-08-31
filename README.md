# نمایش — NFT Marketplace

نسخه Full-stack starter برای یک بازار NFT فارسی.

## اجرا
1. Node.js 20+ نصب کنید.
2. `npm install`
3. PostgreSQL اجرا کنید و `.env` را از `.env.example` بسازید.
4. `npx prisma generate`
5. `npm run db:push`
6. `npm run dev`
7. برای قراردادها: `npm install @openzeppelin/contracts` سپس `npm run contract:compile`

## معماری
- Next.js App Router + TypeScript
- PostgreSQL + Prisma
- Solidity / ERC-721
- Marketplace با خرید مستقیم و کارمزد پلتفرم
- UI فارسی و RTL
- اتصال اولیه MetaMask در کلاینت

## نکات production
قبل از استفاده واقعی باید audit قراردادها، احراز هویت، rate limit، ذخیره‌سازی IPFS/S3، indexer تراکنش‌ها، سیستم escrow/مزایده، moderation، مدیریت secrets و تست‌های کامل اضافه شود.
