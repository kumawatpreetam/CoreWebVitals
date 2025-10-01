# Core Web Vitals (in simple terms)

Core Web Vitals are important checks from Google that show how users experience your website.  
They focus on speed, responsiveness, and stability.  

## 📊 The Three Core Web Vitals

1. **Loading speed**  
   - How fast the main content of your page shows up  
   - (so visitors don’t have to wait too long)

2. **Interactivity**  
   - How quickly your site reacts when someone clicks, taps, or types  

3. **Visual stability**  
   - How steady the page looks while loading  
   - (things shouldn’t jump or shift around suddenly)

---

## 🖼️ Mermaid Diagram

```mermaid
graph TD
    A[Core Web Vitals] --> B[Loading Speed]
    A --> C[Interactivity]
    A --> D[Visual Stability]

    B --> B1["How fast main content appears"]
    C --> C1["How quickly site reacts to clicks/taps"]
    D --> D1["How steady page looks (no shifting)"]
```

# 📌 Largest Contentful Paint (LCP)

## 🔎 What It Measures
- LCP checks **how fast the biggest part of your page** (like a main image, video, or headline text) shows up on the screen.  
- It’s about the **loading performance** that users actually feel.  

## ✅ Ideal Value
- **Good:** LCP should happen within **2.5 seconds** after the page starts loading.  
- **Needs Improvement:** Between **2.5s – 4s**.  
- **Poor:** More than **4 seconds**.  

---

## 🖼️ Mermaid Diagram

```mermaid
flowchart TD
    A[Largest Contentful Paint - LCP] --> B[What It Measures]
    A --> C[Ideal Value]

    B --> B1[Shows how fast the biggest part of the page appears]
    B --> B2[Focuses on loading performance users feel]

    C --> D[Good: <= 2.5s]
    C --> E[Needs Improvement: 2.5s - 4s]
    C --> F[Poor: > 4s]

    style D fill:##274472,stroke:#2E7D32,stroke-width:2px
    style E fill:#5885AF,stroke:#FF8C00,stroke-width:2px
    style F fill:#41729F,stroke:#B22222,stroke-width:2px
```

# 📌 First Input Delay (FID)

## 🔎 What It Measures
- FID checks **how quickly your site reacts** when a user first interacts with it.  
- Example: Clicking a button, tapping a link, or using a form.  

## ✅ Ideal Value
- **Good:** Less than **100 ms** (almost instant).  
- **Needs Improvement:** Between **100 – 300 ms**.  
- **Poor:** More than **300 ms** (feels slow or unresponsive).  

## ✅ Mermaid Diagram for FID

```mermaid
flowchart TD
    A[First Input Delay - FID] --> B[What It Measures]
    A --> C[Ideal Value]

    B --> B1[Measures site interactivity]
    B --> B2[Time for page to respond to first user action like a click]

    C --> D[Good: < 100 ms]
    C --> E[Needs Improvement: 100 - 300 ms]
    C --> F[Poor: > 300 ms]

    style D fill:#3B0404,stroke:#2E7D32,stroke-width:2px
    style E fill:#900020,stroke:#FF8C00,stroke-width:2px
    style F fill:#67595E,stroke:#B22222,stroke-width:2px
```

# 📌 Cumulative Layout Shift - CLS

## 🔎 What It Measures
- CLS checks the **visual stability** of your site.  
- It measures how much page content **moves or shifts** as the page loads.  
- Example: You try to click a button and an ad loads, pushing the button — that is a layout shift.

## ✅ Ideal Value
- **Good:** Less than **0.1** (stable).  
- **Needs Improvement:** **0.1 – 0.25**.  
- **Poor:** More than **0.25** (too jumpy).

```mermaid
flowchart TD
    A[Cumulative Layout Shift - CLS] --> B[What It Measures]
    A --> C[Ideal Value]

    B --> B1[Measures visual stability during page load]
    B --> B2[Tracks how much elements move or shift]

    C --> D[Good: < 0.1]
    C --> E[Needs Improvement: 0.1 - 0.25]
    C --> F[Poor: > 0.25]

    style D fill:#AA1945,stroke:#2E7D32,stroke-width:2px
    style E fill:#3B0918,stroke:#FF8C00,stroke-width:2px
    style F fill:#B8390E,stroke:#B22222,stroke-width:2px
```

# 📌 Field Data

## 🔎 Definition
- Field Data shows the **real-world performance** of your website.  
- It comes from **actual users** on different devices and networks, not just lab tests.  

## 🛠️ Source
- Collected from users who have visited your site.  
- Data comes from the **Chrome User Experience Report (CrUX)**, where users opt in to share performance data.  
- Covers a wide range of real-world conditions (slow/fast networks, mobile/desktop devices, etc.).  

## 📊 Metrics Included
- **Largest Contentful Paint (LCP):** How fast the largest element (image, video, text) becomes visible.  
- **First Input Delay (FID):** How quickly the page responds to the first user interaction.  
- **Cumulative Layout Shift (CLS):** How stable the page looks while loading.  

## ✅ Usefulness
- Gives insight into **how people actually experience your site**.  
- Helps identify performance problems that happen in the real world (like slow internet or weaker devices).

```mermaid
flowchart TD
    A[Field Data] --> B[Definition]
    A --> C[Source]
    A --> D[Metrics]
    A --> E[Usefulness]

    B --> B1[Real-world performance from actual users]
    B --> B2[Reflects different devices and networks]

    C --> C1[Collected from real visitors]
    C --> C2[From Chrome User Experience Report - CrUX]

    D --> D1[Largest Contentful Paint - LCP]
    D --> D2[First Input Delay - FID]
    D --> D3[Cumulative Layout Shift - CLS]

    E --> E1[Shows real user experience]
    E --> E2[Helps find issues with network or device performance]
```

# 📌 Lab Data

## 🔎 Definition
- Lab Data refers to performance metrics collected in a **controlled environment**.  
- It uses simulated conditions (like fixed device types or internet speeds).  
- Generated by tools such as **Lighthouse** that run performance tests on a single device or virtual environment.  

## 🛠️ Source
- Collected through **automated tests** under predefined conditions.  
- These conditions can include specific network speeds, device settings, and browser environments.  

## 📊 Metrics
- **Performance Metrics:** First Contentful Paint (FCP), Speed Index, Time to Interactive (TTI), and more.  
- **Other Data:** Suggestions for optimizing resources, reducing load times, and improving overall performance.  

## ✅ Usefulness
- Provides a **consistent baseline** for testing performance.  
- Helps diagnose specific issues in a controlled setting.  
- Useful for **validating improvements** before pushing them live.  

```mermaid

flowchart TD
    A[Lab Data] --> B[Definition]
    A --> C[Source]
    A --> D[Metrics]
    A --> E[Usefulness]

    B --> B1[Collected in controlled environment]
    B --> B2[Generated by tools like Lighthouse]

    C --> C1[Automated tests]
    C --> C2[Predefined network speeds and devices]

    D --> D1[Performance Metrics: FCP, Speed Index, TTI]
    D --> D2[Other Data: Suggestions for optimizations]

    E --> E1[Provides consistent baseline]
    E --> E2[Helps diagnose and validate improvements]
```

# 📌 Critical Rendering Path (CRP)

## 🔎 Definition
- The **Critical Rendering Path (CRP)** is the sequence of steps the browser follows to turn **HTML, CSS, and JavaScript** into a fully rendered webpage.  
- Optimizing the CRP is important because it directly affects **how fast a page becomes visible and usable** for visitors.  

## 🛠️ Steps in the Critical Rendering Path
1. **DOM Construction** – Building the structure of the page from HTML.  
2. **CSSOM Construction** – Building the style information from CSS.  
3. **Render Tree Construction** – Combining the DOM and CSSOM to figure out what each element should look like.  
4. **Layout (Reflow)** – Calculating the position and size of every element on the page.  
5. **Painting** – Filling pixels on the screen with colors, text, images, and borders.  
6. **Compositing** – Putting everything together into the final page for the user to see and interact with.  

```mermaid

flowchart TD
    A[Critical Rendering Path] --> B[DOM Construction]
    B --> C[CSSOM Construction]
    C --> D[Render Tree Construction]
    D --> E[Layout - Reflow]
    E --> F[Painting]
    F --> G[Compositing]
   ```
