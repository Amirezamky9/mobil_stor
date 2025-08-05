<<<<<<< HEAD
# فروشگاه آنلاین موبایل - سرور و API

این مستند شامل دستورالعمل‌های لازم برای راه‌اندازی، توسعه و تست بک‌اند پروژه فروشگاه آنلاین موبایل است.

## پیش‌نیازها

-   Node.js (نسخه 18 یا بالاتر)
-   Yarn یا npm
-   PostgreSQL
-   Git

## ۱. راه‌اندازی محیط توسعه

**مرحله اول: کلون کردن پروژه**
```bash
git clone https://github.com/Amirezamky9/mobil_stor.git
cd my-mobile-store
```

[cite_start]**مرحله دوم: نصب وابستگی‌ها** [cite: 342]
```bash
npm install
# یا
yarn install
```

**مرحله سوم: تنظیم متغیرهای محیطی**
[cite_start]یک فایل به نام `.env.local` در ریشه پروژه ایجاد کرده و محتویات فایل `.env.example` را در آن کپی کنید.  سپس مقادیر آن را با اطلاعات محلی خود جایگزین نمایید.

**مرحله چهارم: راه‌اندازی پایگاه داده**
[cite_start]با استفاده از Prisma، مدل‌های داده را به پایگاه داده PostgreSQL خود اعمال کنید. [cite: 346]
```bash
npx prisma migrate dev --name init
```
این دستور، جداول را بر اساس اسکیمای تعریف شده در `prisma/schema.prisma` در دیتابیس شما ایجاد می‌کند.

**مرحله پنجم: اجرای پروژه**
سرور توسعه Next.js را اجرا کنید:
```bash
npm run dev
# یا
yarn dev
```
اکنون برنامه روی آدرس `http://localhost:3000` در دسترس است و API Endpoints در مسیر `/api` فعال هستند.

## ۲. تست API Endpoints

می‌توانید از ابزارهایی مانند Postman یا Insomnia برای تست APIها استفاده کنید.

-   **Base URL:** `http://localhost:3000`

**مثال: دریافت لیست محصولات**
-   **Method:** `GET`
-   **URL:** `http://localhost:3000/api/products?page=1&limit=10&sortBy=price&order=asc`

**مثال: ایجاد کاربر جدید (ثبت‌نام)**
-   **Method:** `POST`
-   **URL:** `http://localhost:3000/api/auth/register`
-   **Body (JSON):**
    ```json
    {
      "email": "test@example.com",
      "password": "strongpassword123",
      "name": "کاربر تستی"
    }
    ```
---
=======
# mobil_stor
>>>>>>> 7495a7e5204d94de2ef926ae64cbe66f1604a379
