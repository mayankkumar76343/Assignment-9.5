Assignment 9.5 — Responsive Landing Page: Finish & Review.1. Final project structure

text
Assignment-9.4/
├── index.html
├── style.css
└── images/
    └── workspace.jpg
Download a suitable workspace photo and save it as workspace.jpg inside the images folder. This avoids relying on an external image URL.

2. Updated index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <meta name="description"
          content="Discover modern tools to improve productivity, creativity, and teamwork.">

    <meta name="theme-color" content="#ffffff">

    <title>Launch — Build Something Amazing</title>

    <link rel="stylesheet" href="style.css">
</head>

<body>
    <header class="site-header">
        <div class="container navbar">
            <a href="#home" class="logo" aria-label="Launch home">
                Launch<span>.</span>
            </a>

            <nav class="nav-links" id="navigation" aria-label="Main navigation">
                <a href="#home">Home</a>
                <a href="#features">Features</a>
                <a href="#about">About</a>
                <a href="#contact">Contact</a>
            </nav>

            <a href="#contact" class="btn btn-primary nav-cta">
                Get Started
            </a>
        </div>
    </header>

    <main>
        <section class="hero section-padding" id="home">
            <div class="container hero-grid">
                <div class="hero-content">
                    <p class="eyebrow">WELCOME TO THE FUTURE</p>

                    <h1>
                        Build Something
                        <span>Amazing Today.</span>
                    </h1>

                    <p class="hero-description">
                        Bring your ideas to life with simple, powerful
                        tools designed to help you create, grow, and succeed.
                    </p>

                    <div class="hero-actions">
                        <a href="#features" class="btn btn-primary">
                            Explore Features <span aria-hidden="true">→</span>
                        </a>

                        <a href="#about" class="btn btn-secondary">
                            Learn More
                        </a>
                    </div>

                    <div class="hero-stats" aria-label="Our highlights">
                        <div>
                            <strong>10K+</strong>
                            <span>Happy Users</span>
                        </div>

                        <div>
                            <strong>99%</strong>
                            <span>Satisfaction</span>
                        </div>

                        <div>
                            <strong>24/7</strong>
                            <span>Support</span>
                        </div>
                    </div>
                </div>

                <div class="hero-visual">
                    <img
                        src="images/workspace.jpg"
                        alt="Bright, modern workspace with desks and chairs"
                        width="1000"
                        height="750"
                        fetchpriority="high"
                    >

                    <div class="floating-card">
                        <span class="check-icon" aria-hidden="true">✓</span>

                        <div>
                            <strong>Work smarter</strong>
                            <p>Achieve more every day</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="features section-padding" id="features">
            <div class="container">
                <div class="section-heading">
                    <p class="eyebrow">WHY CHOOSE US</p>

                    <h2>Everything You Need to Succeed</h2>

                    <p>
                        Powerful features designed to make your work
                        easier, faster, and more enjoyable.
                    </p>
                </div>

                <div class="feature-grid">
                    <article class="feature-card">
                        <div class="feature-icon" aria-hidden="true">⚡</div>
                        <h3>Fast Performance</h3>
                        <p>
                            Enjoy a smooth experience with tools built
                            for speed and productivity.
                        </p>
                    </article>

                    <article class="feature-card">
                        <div class="feature-icon" aria-hidden="true">🎨</div>
                        <h3>Modern Design</h3>
                        <p>
                            Explore a clean, attractive interface that
                            makes every interaction enjoyable.
                        </p>
                    </article>

                    <article class="feature-card">
                        <div class="feature-icon" aria-hidden="true">🔒</div>
                        <h3>Secure Platform</h3>
                        <p>
                            Keep your work protected with a focus on
                            security and reliability.
                        </p>
                    </article>
                </div>
            </div>
        </section>

        <section class="about section-padding" id="about">
            <div class="container about-content">
                <p class="eyebrow">YOUR NEXT STEP</p>
                <h2>Ready to get started?</h2>

                <p>
                    Take the next step and turn your ideas into reality.
                </p>

                <a href="#contact" class="btn btn-primary">
                    Get Started Today <span aria-hidden="true">→</span>
                </a>
            </div>
        </section>
    </main>

    <footer class="site-footer" id="contact">
        <div class="container footer-content">
            <a href="#home" class="logo footer-logo">
                Launch<span>.</span>
            </a>

            <p>
                © 2026 Launch. Created for Assignment 9.5.
            </p>

            <a href="#home" class="back-to-top">Back to top ↑</a>
        </div>
    </footer>
</body>
</html>
3. Final responsive style.css

css

/* =========================
   1. Reset and base styles
========================= */

:root {
    --primary: #6658e8;
    --primary-dark: #5042ce;
    --text: #172033;
    --muted: #697184;
    --surface: #ffffff;
    --surface-soft: #f7f6ff;
    --border: #e9e8f2;
    --radius: 16px;
    --container: 1120px;
    --shadow: 0 16px 40px rgba(36, 29, 92, 0.10);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    scroll-padding-top: 90px;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    color: var(--text);
    background: var(--surface);
    line-height: 1.65;
    overflow-wrap: break-word;
}

img {
    display: block;
    max-width: 100%;
}

a {
    color: inherit;
    text-decoration: none;
}

button,
a {
    -webkit-tap-highlight-color: transparent;
}

a:focus-visible {
    outline: 3px solid var(--primary);
    outline-offset: 4px;
}

.container {
    width: min(var(--container), calc(100% - 48px));
    margin-inline: auto;
}

.section-padding {
    padding-block: 88px;
}

.eyebrow {
    margin-bottom: 16px;
    color: var(--primary);
    font-size: 0.78rem;
    font-weight: 800;
    letter-spacing: 2px;
}

/* =========================
   2. Header and navigation
========================= */

.site-header {
    position: sticky;
    top: 0;
    z-index: 10;
    background: rgba(255, 255, 255, 0.96);
    border-bottom: 1px solid var(--border);
}

.navbar {
    min-height: 78px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 24px;
}

.logo {
    flex-shrink: 0;
    font-size: 1.8rem;
    font-weight: 800;
    letter-spacing: -1px;
}

.logo span {
    color: var(--primary);
}

.nav-links {
    display: flex;
    align-items: center;
    gap: 28px;
}

.nav-links a,
.back-to-top {
    color: var(--muted);
    font-size: 0.94rem;
    transition: color 0.2s ease;
}

.nav-links a:hover,
.back-to-top:hover {
    color: var(--primary);
}

/* =========================
   3. Buttons
========================= */

.btn {
    min-height: 48px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    padding: 12px 22px;
    border: 1px solid transparent;
    border-radius: 9px;
    font-size: 0.94rem;
    font-weight: 700;
    text-align: center;
    transition:
        background-color 0.2s ease,
        color 0.2s ease,
        transform 0.2s ease;
}

.btn:hover {
    transform: translateY(-2px);
}

.btn-primary {
    color: #ffffff;
    background: var(--primary);
}

.btn-primary:hover {
    background: var(--primary-dark);
}

.btn-secondary {
    color: var(--text);
    background: #ffffff;
    border-color: #dcd9ed;
}

.btn-secondary:hover {
    border-color: var(--primary);
}

/* =========================
   4. Hero section
========================= */

.hero {
    background: linear-gradient(135deg, #faf9ff, #f0efff);
}

.hero-grid {
    display: grid;
    grid-template-columns: minmax(0, 1fr) minmax(0, 0.95fr);
    align-items: center;
    gap: 64px;
}

.hero-content h1 {
    max-width: 590px;
    font-size: clamp(2.5rem, 5vw, 4.25rem);
    line-height: 1.1;
    letter-spacing: -2.5px;
}

.hero-content h1 span {
    display: block;
    color: var(--primary);
}

.hero-description {
    max-width: 490px;
    margin-top: 24px;
    color: var(--muted);
    font-size: 1.06rem;
}

.hero-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 14px;
    margin-top: 30px;
}

.hero-stats {
    display: flex;
    flex-wrap: wrap;
    gap: 34px;
    margin-top: 44px;
}

.hero-stats div {
    display: grid;
    gap: 2px;
}

.hero-stats strong {
    font-size: 1.45rem;
    line-height: 1.3;
}

.hero-stats span {
    color: var(--muted);
    font-size: 0.82rem;
}

.hero-visual {
    position: relative;
    min-width: 0;
}

.hero-visual img {
    width: 100%;
    aspect-ratio: 4 / 3;
    object-fit: cover;
    border-radius: 20px;
    box-shadow: var(--shadow);
}

.floating-card {
    position: absolute;
    bottom: 24px;
    left: -24px;
    display: flex;
    align-items: center;
    gap: 12px;
    max-width: calc(100% - 16px);
    padding: 16px 20px;
    border: 1px solid rgba(233, 232, 242, 0.8);
    border-radius: 12px;
    background: #ffffff;
    box-shadow: var(--shadow);
}

.check-icon {
    display: grid;
    width: 38px;
    height: 38px;
    flex-shrink: 0;
    place-items: center;
    border-radius: 50%;
    color: #13834b;
    background: #e2f8ec;
    font-weight: 800;
}

.floating-card strong {
    font-size: 0.94rem;
}

.floating-card p {
    color: var(--muted);
    font-size: 0.78rem;
}

/* =========================
   5. Features
========================= */

.section-heading {
    max-width: 650px;
    margin: 0 auto 44px;
    text-align: center;
}

.section-heading h2,
.about h2 {
    font-size: clamp(1.8rem, 3.5vw, 2.6rem);
    line-height: 1.2;
    letter-spacing: -1px;
}

.section-heading > p:last-child,
.about-content > p:not(.eyebrow) {
    margin-top: 16px;
    color: var(--muted);
}

.feature-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 24px;
}

.feature-card {
    min-width: 0;
    padding: 30px;
    border: 1px solid var(--border);
    border-radius: var(--radius);
    background: #ffffff;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.feature-card:hover {
    transform: translateY(-5px);
    box-shadow: var(--shadow);
}

.feature-icon {
    display: grid;
    width: 54px;
    height: 54px;
    margin-bottom: 22px;
    place-items: center;
    border-radius: 13px;
    background: #f0efff;
    font-size: 1.55rem;
}

.feature-card h3 {
    margin-bottom: 10px;
    font-size: 1.18rem;
}

.feature-card p {
    color: var(--muted);
    font-size: 0.94rem;
}

/* =========================
   6. About / call to action
========================= */

.about {
    background: var(--surface-soft);
    text-align: center;
}

.about-content {
    max-width: 700px;
}

.about-content .btn {
    margin-top: 26px;
}

/* =========================
   7. Footer
========================= */

.site-footer {
    padding-block: 26px;
    color: #d9dce5;
    background: var(--text);
}

.footer-content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 18px;
}

.footer-logo {
    color: #ffffff;
    font-size: 1.5rem;
}

.footer-content p {
    font-size: 0.85rem;
    text-align: center;
}

.back-to-top {
    color: #ffffff;
}

/* =========================
   8. Tablet breakpoint
========================= */

@media (max-width: 900px) {
    .container {
        width: min(100% - 40px, var(--container));
    }

    .section-padding {
        padding-block: 68px;
    }

    .navbar {
        gap: 16px;
    }

    .nav-links {
        gap: 16px;
    }

    .hero-grid {
        grid-template-columns: minmax(0, 1fr) minmax(0, 0.9fr);
        gap: 32px;
    }

    .hero-content h1 {
        font-size: clamp(2.3rem, 5vw, 3.3rem);
        letter-spacing: -1.5px;
    }

    .hero-stats {
        gap: 22px;
    }

    .floating-card {
        left: -12px;
        bottom: 16px;
        padding: 12px 14px;
    }

    .feature-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }
}

/* =========================
   9. Mobile breakpoint
========================= */

@media (max-width: 650px) {
    .container {
        width: calc(100% - 36px);
    }

    .section-padding {
        padding-block: 52px;
    }

    .navbar {
        min-height: auto;
        padding-block: 15px;
        display: grid;
        grid-template-columns: 1fr auto;
        gap: 14px;
    }

    .logo {
        font-size: 1.6rem;
    }

    .nav-cta {
        min-height: 42px;
        padding: 9px 13px;
        font-size: 0.82rem;
    }

    .nav-links {
        grid-column: 1 / -1;
        grid-row: 2;
        display: flex;
        justify-content: flex-start;
        gap: 10px 20px;
        flex-wrap: wrap;
        padding-top: 3px;
    }

    .nav-links a {
        font-size: 0.86rem;
    }

    .hero-grid {
        grid-template-columns: minmax(0, 1fr);
        gap: 38px;
    }

    .hero-content h1 {
        font-size: clamp(2.4rem, 10vw, 3.4rem);
        letter-spacing: -1.6px;
    }

    .hero-description {
        font-size: 0.98rem;
    }

    .hero-actions {
        gap: 12px;
    }

    .btn {
        padding: 12px 16px;
    }

    .hero-stats {
        justify-content: space-between;
        gap: 16px;
        margin-top: 34px;
    }

    .hero-stats strong {
        font-size: 1.25rem;
    }

    .hero-stats span {
        font-size: 0.75rem;
    }

    .hero-visual img {
        aspect-ratio: 5 / 4;
        border-radius: 15px;
    }

    .floating-card {
        left: 10px;
        bottom: 12px;
        padding: 10px 12px;
    }

    .check-icon {
        width: 32px;
        height: 32px;
    }

    .features .section-heading {
        margin-bottom: 30px;
    }

    .feature-grid {
        grid-template-columns: minmax(0, 1fr);
        gap: 16px;
    }

    .feature-card {
        padding: 24px;
    }

    .footer-content {
        flex-direction: column;
        text-align: center;
        gap: 12px;
    }
}

/* =========================
   10. Small mobile devices
========================= */

@media (max-width: 380px) {
    .container {
        width: calc(100% - 28px);
    }

    .nav-links {
        gap: 8px 14px;
    }

    .hero-content h1 {
        font-size: 2.25rem;
    }

    .hero-actions {
        flex-direction: column;
        align-items: stretch;
    }

    .hero-actions .btn {
        width: 100%;
    }

    .hero-stats {
        gap: 12px;
    }

    .hero-stats strong {
        font-size: 1.12rem;
    }

    .floating-card {
        gap: 8px;
        padding: 9px;
    }
}

/* =========================
   11. Accessibility
========================= */

@media (prefers-reduced-motion: reduce) {
    html {
        scroll-behavior: auto;
    }

    *,
    *::before,
    *::after {
        transition-duration: 0.01ms !important;
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
    }
}
4. Responsive design preview
SaaS Website Design by Design Adam on Dribbble
 
Desktop — 1200px and above

Two-column hero, horizontal navigation, and three feature cards in one row.

Saas Landing Page Design by Rifat Jahangir Ony on Dribbble
 
Tablet — 768px

Reduced spacing, flexible typography, and two feature cards per row.

How I defined a strong brand for a Scheduling SaaS
 
Mobile — 375px

Stacked hero content, wrapped navigation, full-width buttons, and single-column feature cards.

These are visual references, not screenshots captured from your actual code.

5. Test in Chrome DevTools
Open index.html in Chrome.

Right-click the page and select Inspect.

Click the device toolbar icon or press Ctrl + Shift + M.

Test these viewport widths:

Device

Width

What to check

Desktop

1440px

Hero alignment and three feature cards

Laptop

1024px

Navbar spacing and image proportions

Tablet

768px

Grid layout and text wrapping

Mobile

390px

Navigation, buttons, and image

Small mobile

320px

No horizontal scrolling or overlapping

Check the following manually:


Every navigation link scrolls to the correct section.

All buttons lead to valid sections.

The local image loads successfully.

No text or cards overlap.

There is no unintended horizontal scrolling.

Text remains readable at all widths.

Keyboard focus is visible when navigating with Tab.
To help detect horizontal overflow, open the browser console and run:


javascript
document.documentElement.scrollWidth <=
document.documentElement.clientWidth;
The expected result is true. Also inspect the page visually, since this test alone cannot detect every layout problem.

6. Take screenshots for submission
Capture three screenshots from your own running website:

desktop.png — desktop view at 1440px.

tablet.png — tablet view at 768px.

mobile.png — mobile view at 390px.

Use Chrome DevTools to set each viewport, then capture the page with your operating system's screenshot tool. Save the screenshots in a screenshots folder if your instructor wants them included in the repository.

7. Push the final changes to GitHub
Run these commands from the project folder:


bash
git add index.html style.css images/
git commit -m "Complete Assignment 9.5 responsive landing page"
git push origin main
If you also add screenshots:


bash
git add screenshots/
git commit -m "Add responsive design screenshots"
git push origin main
Your submission link will look like this:

https://github.com/YOUR-USERNAME/Assignment-9.4

Replace the example with your actual repository URL.

Final submission checklist

Tablet and mobile breakpoints implemented

Responsive navbar and content

Fluid typography and image sizing

Semantic HTML and accessible focus styles

Functional in-page navigation links

Reduced-motion accessibility support

Test every viewport in Chrome

Verify the local image exists and loads

Capture desktop, tablet, and mobile screenshots

Push final code and screenshots to GitHub

Submit the real GitHub repository URL