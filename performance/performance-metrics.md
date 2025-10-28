# 🚀 Web Performance Evaluation Sheet

| Metric | Target Score | Description | Test 1 | Test 2 | Test 3 | Result |
|---------|---------------|--------------|---------|---------|---------|---------|
| **FCP (First Contentful Paint)** | 3s | Time until the first piece of content is rendered on screen |  |  |  |  |
| **LCP (Largest Contentful Paint)** | 4s | Time until the largest visible element is rendered |  |  |  |  |
| **TTI (Time to Interactive)** | 7s | Time until the page becomes fully interactive |  |  |  |  |
| **CLS (Cumulative Layout Shift)** | 0.25 | Measures unexpected layout shifts (ideal ≤ 0.1) |  |  |  |  |
| **TBT (Total Blocking Time)** | 600ms | Total time the page is unresponsive to user input |  |  |  |  |
| **Response Time** | 1000ms | Server or API response time |  |  |  |  |

---

## 🌐 Web Performance Metrics

### **FCP (First Contentful Paint)**
This metric measures **how quickly the first piece of content** (such as text, image, or canvas) **is rendered on the screen** after the page starts loading.

- **Tool:** Using **Lighthouse (Automated)**
- **Good score:** ≤ **1.8s**
- **Improvement Tips:**
  - Optimize and preload critical CSS
  - Compress and serve images in next-gen formats (WebP, AVIF)
  - Minimize render-blocking JavaScript
  - Use caching and a fast CDN

---

### **LCP (Largest Contentful Paint)**
LCP measures **how long it takes for the largest visible piece of content** on the screen to **fully render** after the page starts loading.

- **Tool:** Using **Lighthouse (Automated Report)**
- **Good score:** ≤ **2.5s**
- **Improvement Tips:**
  - Optimize hero images (compress, resize, preload)
  - Inline critical CSS and preload fonts
  - Use SSR/SSG (Next.js) and CDN for faster delivery
  - Defer non-critical JavaScript
  - Cache API responses and server assets

---

### **TTI (Time to Interactive)**
TTI measures **how long it takes before the page becomes fully interactive** — when users can click, scroll, or input without delay.

- **Tool:** Using **Lighthouse (Performance Tab)**
- **Good score:** ≤ **3.8s**
- **Improvement Tips:**
  - Reduce JavaScript execution time
  - Split large bundles (code-splitting, lazy loading)
  - Optimize third-party scripts
  - Use `async` / `defer` attributes on non-critical scripts
  - Use Web Workers for heavy computations

---

### **CLS (Cumulative Layout Shift)**
CLS measures **the visual stability of a page** — how much elements shift unexpectedly during loading.

- **Tool:** Using **Lighthouse (Visual Stability Section)**
- **Good score:** ≤ **0.1**
- **Improvement Tips:**
  - Always include `width` and `height` on images/videos
  - Reserve space for ads, embeds, or dynamic content
  - Avoid inserting content above existing elements
  - Preload fonts to prevent reflow on load

---

### **TBT (Total Blocking Time)**
TBT measures **the total time between FCP and TTI** during which the main thread is blocked and cannot respond to user input.

- **Tool:** Using **Lighthouse (Performance Metrics)**
- **Good score:** ≤ **200ms**
- **Improvement Tips:**
  - Minimize long JavaScript tasks
  - Break up heavy computations
  - Optimize third-party scripts
  - Use web workers and requestIdleCallback()

---

### **Response Time**
Response Time measures **how quickly the server responds to the first request** — essentially the time between sending a request and receiving the first byte (TTFB).

- **Tool:** Using **Chrome DevTools Network Tab** or **API Monitoring**
- **Good score:** ≤ **600ms**
- **Improvement Tips:**
  - Use CDN caching for static assets
  - Optimize server/database queries
  - Enable compression (gzip, Brotli)
  - Keep payloads lightweight
  - Reduce API latency

---
