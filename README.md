
# Next.js SEO Starter & Optimization

This repository started as a template for the [Improving Web Vitals](https://nextjs.org/learn/seo/improve/lighthouse) example from the Next.js [Learn SEO course](https://nextjs.org/learn/seo/introduction-to-seo).

Through comprehensive technical auditing and refactoring, I have transformed it into an **optimized production-ready project**, focusing on achieving elite-level **Core Web Vitals** scores and superior technical SEO.
---
## 🚀 Next.js Performance & SEO Mastery
This project showcases advanced optimization techniques in Next.js to ensure a fast, stable, and search-engine-friendly user experience.

---

## 🛠 Advanced Optimizations Implemented

<img width="1026" height="1492" alt="Screenshot 2026-03-16 211155" src="https://github.com/user-attachments/assets/0963ca0e-31cf-4d56-a59b-2f75fbb811e7" />

### 📊 Performance Auditing with Lighthouse
I utilize **Lighthouse** as a primary tool to audit the application's performance. By analyzing the four main pillars—Performance, Accessibility, Best Practices, and SEO—I identify and eliminate bottlenecks in the critical rendering path, aiming for a perfect 100/100 score.

### 🖼 Automatic Image Optimization (`next/image`)
To solve **LCP (Largest Contentful Paint)** and **CLS (Cumulative Layout Shift)** issues, I implemented the `next/image` component:
* **Lazy Loading:** Images only load as they enter the viewport.
* **Modern Formats:** Automatic serving of WebP/AVIF formats.
* **Priority Loading:** Critical "Hero" images are prioritized to speed up the initial visual render.
* **Visual Stability:** Pre-defined aspect ratios prevent layout shifts during image loading.

### 📦 Bundle Size Reduction via Dynamic Imports
I leverage **Dynamic Imports** to split the JavaScript bundle. By using `import()` within event handlers (like search inputs), I ensure that heavy libraries (e.g., `fuse.js`, `lodash-es`) are only downloaded when the user actually needs them. This significantly reduces the **Total Blocking Time (TBT)**.

### 🧩 Conditional Component Loading (`next/dynamic`)
For heavy UI elements such as Modals or Code Samples, I use `next/dynamic`. This allows:
* **On-demand loading:** Components are fetched only when triggered by user action.
* **SSR Control:** Disabling server-side rendering for components that rely on browser-only APIs (`{ ssr: false }`).

### 🔡 Optimized Web Font Loading
Next.js optimizes web fonts by default by inlining font CSS and using `size-adjust` to minimize **CLS**. I’ve configured fonts to load without blocking the page render, ensuring a smooth transition and preventing "Flash of Unstyled Text" (FOUT).

### 📜 Third-Party Script Management
Using the `next/script` component, I manage the loading priority of external scripts (analytics, widgets, etc.) to prevent them from hijacking the main thread:
* **afterInteractive:** For non-critical scripts that should load after the page is usable.
* **lazyOnload:** For low-priority scripts that load during idle time.

---

## 🛠 Tech Stack
* **Framework:** Next.js (Pages Router)
* **Optimization Tools:** Lighthouse, Vercel Analytics
* **Libraries:** Fuse.js (Dynamic Search), Lodash-es

---
## 🚀 How to Run Locally
1. Clone the repository: `git clone  nextjs-lighthouse-five.vercel.app/`
2. Install dependencies: `npm install`
3. Run the development server: `npm run dev`
