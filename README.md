![image](https://github.com/user-attachments/assets/5f5339a1-b9ce-4217-b8d9-ee7e87094f60)

# [Blog Post](https://medium.com/@yonghyun.jin13/the-only-boilerplate-you-need-for-take-home-project-9f7f9242d33c)

# Full-Stack Monorepo Boilerplate for Your Take-Home Projects

This is my go-to boilerplate for take-home projects, combining my favorite tech stack into a ready-to-ship monorepo setup. 
It saves ~4 hours of setup time per project and is designed to scale smoothly as your app grows.


## What's Inside?

This Turborepo includes the following apps and packages:

### **📦 Apps**

* **`web`** - A Next.js app for the frontend ([Next.js Docs](https://nextjs.org/docs))
* **`api`** - An Express.js app for the backend ([Express.js Docs](https://expressjs.com))

### **📚 Shared Packages**

* **`@repo/ui`** - A React component library shared across the monorepo
* **`@repo/supabase`** - Supabase setup
* **`@repo/eslint-config`** - Shared ESLint configuration for consistent linting across packages
* **`@repo/typescript-config`** - Shared TypeScript configurations for consistency

---

## 🚀 Key Features

* **Monorepo Efficiency**: Manage multiple apps and packages with a single codebase.
* **Next.js Frontend**: Fast and SEO-friendly frontend with TypeScript support.
* **Express.js Backend**: Robust API backend with full TypeScript support.
* **Reusable Components**: Centralized UI library for consistent design and reduced code duplication.
* **Consistent Code Quality**: Shared ESLint and TypeScript configurations.
* **Optimized Builds**: Blazing-fast build speeds with Turborepo caching.

---

## 📦 Installation

Clone this repository and install dependencies:

```bash
git clone https://github.com/sean3687/turbo-monorepo.git
cd turbo-monorepo
yarn install
```

---

## 📂 Setup Database

This section is for users who have just cloned the repository and need to set up the local database. This project uses Supabase for database management, with migrations handled through the Supabase CLI. Follow these steps to get your database up and running.

You can open up http://127.0.0.1:54323 to open supabase studio. 

```bash
DATABASE_URL=postgresql://postgres:postgres@localhost:54322/postgres
SUPABASE_URL=http://localhost:54321
SUPABASE_KEY=
NODE_ENV=development
```

```bash
cd packages
supabase init
```


## 📄 Scripts

Here are some useful scripts for development:

* **`yarn dev`** - Start both the Next.js frontend and Express.js backend
* **`yarn build`** - Build all apps and packages
* **`yarn lint`** - Run ESLint across the entire monorepo
* **`yarn check-types`** - Run TypeScript type checking

---

## 📁 Directory Structure

```
apps/
├── web/        # Next.js frontend
└── api/        # Express.js backend
packages/
├── ui/         # Shared React component library
├── supabase/   # Database 
├── eslint-config/ # Shared ESLint config
└── typescript-config/ # Shared TypeScript config
```


---

## 📂 Contributing

If you find a bug or have a feature request, please open an issue or submit a pull request.

---

## 🤝 License

This project is licensed under the MIT License.
