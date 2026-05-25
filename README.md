<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0ea5e9&height=200&section=header&text=VK%20Editorial&fontSize=60&fontAlignY=35&desc=Premium%20Video%20Editing%20Agency&descAlignY=55&descAlign=50" />
</div>

<h1 align="center">VK Editorial Agency - Portfolio Platform 🎬</h1>

<div align="center">
  <a href="https://github.com/vikashkumar302004"><img src="https://img.shields.io/badge/Developed%20By-Vikash_Kumar-0ea5e9?style=for-the-badge&logo=github" alt="Vikash Kumar" /></a>
  <img src="https://img.shields.io/badge/Client-VK_Editorial_Agency-black?style=for-the-badge" alt="VK Editorial" />
  <img src="https://img.shields.io/badge/Status-Live_&_Optimized-success?style=for-the-badge" alt="Status" />
</div>

<br/>

## 👨‍💻 About The Developer

This highly optimized portfolio platform was engineered as a **freelance project** for **VK Editorial Agency** by **Vikash Kumar** ([@vikashkumar302004](https://github.com/vikashkumar302004)). 

As a freelance software developer, I was tasked with taking a static UI, deeply optimizing its performance, integrating dynamic YouTube video carousels without React hydration conflicts, and globally rebranding the interface for a seamless, lag-free user experience.

---

## 🛠️ Technology Stack

<div align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/Framer-0055FF?style=for-the-badge&logo=framer&logoColor=white" />
  <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" />
</div>

---

## 🏗️ System Architecture & DOM Flow

The platform relies on a sophisticated client-side hydration engine that manipulates the DOM in real-time. Here is the architectural flow:

```mermaid
graph TD
    classDef highlight fill:#0ea5e9,stroke:#000,stroke-width:2px,color:#fff;
    classDef server fill:#1e293b,stroke:#0ea5e9,stroke-width:2px,color:#fff;
    classDef browser fill:#0f172a,stroke:#64748b,stroke-width:1px,color:#fff;

    A([🌍 Client Request]) -->|HTTPS| B[⚡ Vercel Edge Network]:::server
    B -->|Serves Static Build| C[DOM & Base Styles]:::browser
    
    subgraph Client-Side Engine
        C --> D{JavaScript Execution}
        D -->|Bootstraps| E[MutationObserver]
        D -->|Initializes| F[Carousel Injector]
        
        E -->|Real-time scan| G[Text & Branding Replacement]
        F -->|Identifies Breakpoints| H[Responsive Video Sync]
    end

    G --> I((✨ VK Editorial Branding)):::highlight
    H --> J((🎬 YouTube Iframes Loaded)):::highlight
```

### 🔄 Dynamic Video Carousel Logic

The carousel logic specifically handles server-side rendered (SSR) variants to avoid duplicate videos on mobile/desktop breakpoints:

```mermaid
sequenceDiagram
    participant Browser
    participant DOM
    participant Script
    participant YouTube

    Browser->>DOM: Loads Hidden/Visible SSR Carousel Variants
    Script->>DOM: querySelectorAll('.ssr-variant')
    Script->>Script: Filters out 'display: none' carousels
    Script->>DOM: Clones elements for infinite scroll loop
    Script->>YouTube: Fetches specific YouTube Video IDs
    YouTube-->>DOM: Injects embedded responsive iframes
    Note right of DOM: Videos autoplay, loop, and mute natively
```

---

## ⚡ Key Optimizations & Features

- **Zero-Lag DOM Rebranding:** Utilizes advanced `MutationObserver` patterns to detect and replace text nodes in milliseconds without freezing the main thread.
- **Responsive Video Injection:** A custom JavaScript engine accurately detects CSS media query breakpoints and applies the YouTube IFrame API strictly to the visible carousel, eliminating dual-render overlap bugs.
- **Strict Version Control Size Limits:** Bloatware and heavy source videos (`.mp4`, `ffmpeg.zip`) are meticulously ignored via `.gitignore` and `.vercelignore` to bypass GitHub's 100MB object size limits and keep Vercel deployments blazing fast.
- **Dynamic Theming:** Forcefully overrides third-party SVGs and CSS variables via JavaScript injection to enforce the brand's premium "Ocean Blue" identity (`#0ea5e9`).

---

## 🚀 Local Development Guide

To clone and run the optimized build locally:

```bash
# 1. Clone the repository
git clone https://github.com/vikashkumar302004/vikrant-portfolio.git

# 2. Enter the project directory
cd vikrant-portfolio

# 3. Start a local server (Requires Node.js)
npx serve .
```

Navigate to `http://localhost:3000` in your browser.  
*(Pro-tip: Use **Ctrl + Shift + R** to hard refresh and bypass cached scripts when making changes).*

---

<div align="center">
  <p><i>Building scalable, high-conversion interfaces for modern agencies.</i></p>
  <p><b>Copyright © 2026 | VK Editorial Agency | Developed by Vikash Kumar</b></p>
</div>
