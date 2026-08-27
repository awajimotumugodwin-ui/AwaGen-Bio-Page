# Prompt: Replicate the Godwin Awajimotumu Responsive Portfolio Design

## Role

Act as an expert front-end developer specializing in semantic HTML5, responsive CSS, accessibility, and pixel-accurate UI implementation.

Recreate the attached portfolio screenshot as closely as possible using **only HTML and CSS**.

Do not use JavaScript, Bootstrap, Tailwind, React, Vue, external UI frameworks, CSS libraries, or component libraries.

---

## Reference Design

Use the supplied reference screenshot as the primary visual reference.

The page is a dark, modern personal portfolio/biography website with:

- A very dark navy/charcoal overall background.
- A centered portfolio container/card.
- Gold/yellow accent color.
- White and light-gray typography.
- Subtle borders and shadows.
- Rounded corners.
- A large hero section.
- Circular/profile-image treatment.
- A social-media/contact strip.
- A services section with four service cards.
- Responsive mobile, tablet, and desktop layouts.

The final implementation should reproduce the visual hierarchy, spacing, proportions, alignment, typography, colors, borders, card treatments, and responsive behavior of the reference.

---

# 1. Technology Requirements

Use only:

- `index.html`
- `style.css`

HTML5 and CSS3 only.

Do not use:

- JavaScript
- Bootstrap
- Tailwind CSS
- React
- Vue
- jQuery
- Font Awesome
- Bootstrap Icons
- external CSS frameworks
- external JavaScript libraries

If icons are required, use inline SVG or simple CSS-based/icon text solutions directly in the HTML/CSS.

---

# 2. Page Identity

Use the following personal information:

**Name:**
Godwin Awajimotumu

**Short identity:**
Computer Science Undergraduate & Aspiring Full-Stack/Web Developer

**Hero introduction:**
I'm Godwin Awajimotumu.

Create a professional biography based on the following profile:

> Godwin Awajimotumu is a Computer Science undergraduate with a strong passion for web development, programming, science, and technology. He is developing practical skills in HTML, CSS, JavaScript, C++, and digital content creation, with an interest in building modern, responsive, accessible, and user-friendly digital experiences. He enjoys learning by building projects and continuously improving his technical and creative skills.

Do not invent employment history, companies, degrees, awards, clients, or professional certifications that were not provided.

---

# 3. Overall Layout

Create a centered portfolio page.

The body should:

- Fill at least the viewport height.
- Center the main portfolio container.
- Use a dark background.
- Have comfortable page padding.
- Prevent horizontal overflow.
- Use `box-sizing: border-box`.

Start with a mobile-first layout.

Use:

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

The page must remain usable at very narrow widths, including exactly **320px**.

---

# 4. Main Portfolio Container

Create one main wrapper/card containing the complete portfolio.

The container should have:

- Dark navy/charcoal background.
- Subtle border.
- Rounded corners.
- Subtle shadow.
- `overflow: hidden`.
- Responsive width.
- A maximum desktop width similar to the reference screenshot.

Do not use a fixed width that causes horizontal scrolling.

Prefer:

```css
width: 100%;
max-width: ...;
```

rather than a fixed desktop width.

---

# 5. Header / Navigation

Create a top navigation area.

### Left side

Display a simple gold circular/logo mark followed by:

**Godwin**
**Awajimotumu**

The surname/name accent should use the gold/yellow accent color.

### Navigation links

Include:

- Home
- About
- Services
- Portfolio
- Contact

The active Home link should have a subtle gold underline/accent.

### Right side

Include small social/contact icons for:

- TikTok
- Facebook
- Instagram
- X
- LinkedIn
- Slack
- Email

Also include a visible **GitHub** button/link.

On desktop, keep these elements arranged horizontally as shown in the reference.

On smaller screens, make the navigation responsive so it does not overflow.

A simple mobile navigation arrangement is acceptable, but do not use JavaScript.

---

# 6. Hero Section

Create a two-column desktop hero.

## Left side

Use:

```text
I'm
Godwin
Awajimotumu
```

The main name should be large, bold, and white.

Add a short gold horizontal accent line beneath the name.

Add this hero paragraph:

> A Computer Science undergraduate with a strong passion for Web Development, Programming, Science and Technology. I build modern, responsive web applications and digital experiences.

Add two buttons:

### Primary button

**Hire Me →**

Use the gold accent background with dark text.

### Secondary button

**Download CV ↓**

Use a dark/transparent background with a subtle border.

The buttons should be links or buttons styled with CSS and should have hover states.

---

# 7. Fluid Typography

The main heading and hero paragraph must use **fluid CSS sizing**.

Do not use only fixed pixel values.

Use `clamp()`.

Example approach:

```css
.hero-title {
    font-size: clamp(2.2rem, 7vw, 5rem);
}
```

and:

```css
.hero-text {
    font-size: clamp(0.95rem, 2vw, 1.15rem);
}
```

Adjust the values as necessary to visually match the reference.

The heading must remain readable at 320px without causing horizontal overflow.

---

# 8. Profile Image

Use the supplied profile image as the hero profile image.

The image must be responsive.

Requirements:

- Do not let the image overflow the viewport.
- Do not allow horizontal scrolling.
- Maintain its aspect ratio.
- Use `max-width: 100%`.
- Keep the portrait visually prominent on desktop.
- Scale the image down appropriately on tablets and mobile.
- Do not crop the face awkwardly.
- Preserve the transparent/background characteristics of the supplied portrait if applicable.

A safe responsive pattern is:

```css
.hero-image img {
    width: 100%;
    max-width: 500px;
    height: auto;
    display: block;
}
```

Adjust the actual values to match the reference.

---

# 9. Required Responsive Breakpoints

Use a **mobile-first** approach.

The base styles should target mobile devices.

Then add exactly these minimum-width media queries:

```css
@media (min-width: 768px) {
    /* tablet */
}
```

and:

```css
@media (min-width: 1024px) {
    /* desktop */
}
```

## 320px requirement

Explicitly test the page at:

**320px width**

Confirm:

- The profile image does not overflow.
- The hero text remains inside the viewport.
- The heading wraps naturally.
- Buttons fit.
- Social links wrap appropriately.
- Service cards fit.
- No horizontal scrollbar appears.

## 768px requirement

At 768px and above:

- Transition toward the tablet two-column hero layout.
- Increase available spacing.
- Make the profile image larger.
- Arrange social/contact elements more horizontally.
- Make service cards more compact but still readable.

## 1024px requirement

At 1024px and above:

- Use the full desktop two-column hero.
- Increase spacing where appropriate.
- Display the four service cards in a horizontal row.
- Keep the navigation in one row.
- Make the overall composition closely resemble the desktop reference.

---

# 10. Content Breakpoints

Before finalizing the responsive CSS, inspect the layout at:

- 320px
- 375px
- 480px
- 768px
- 900px
- 1024px
- 1280px
- 1440px

Identify where:

- The hero columns become too narrow.
- The heading wraps awkwardly.
- The profile image becomes too large/small.
- Social links become crowded.
- Service cards become too narrow.
- Buttons no longer fit comfortably.

Use the two required media queries to resolve these layout changes.

Do not simply stretch the desktop design onto mobile.

---

# 11. Social / Contact Section

Create a horizontal social/contact strip beneath the hero.

Include all of these:

1. TikTok
2. Facebook
3. Instagram
4. X
5. LinkedIn
6. Slack
7. Email

Each item should contain:

- Its logo/icon.
- Platform name.
- Handle or contact text.
- A clickable `<a>` element.

Use placeholder handles only where an actual handle was not supplied.

Do not fabricate real account ownership.

Use clearly editable placeholders such as:

```text
@your_tiktok_handle
@your_instagram_handle
@your_x_handle
your.email@example.com
```

The GitHub link should be a separate visible button.

Use:

```html
<a href="YOUR_GITHUB_URL" target="_blank" rel="noopener noreferrer">
    GitHub
</a>
```

Make all links easy to replace later.

---

# 12. Social Icons

Since external icon libraries are prohibited:

- Use inline SVG icons, or
- Use simple text/icon representations created directly in HTML/CSS.

Each icon should have:

- A circular or rounded container.
- Subtle border.
- Good contrast.
- Hover effect.
- Accessible `aria-label`.

Example:

```html
<a href="#" aria-label="TikTok">
    <!-- inline SVG icon -->
</a>
```

Do not depend on external icon fonts.

---

# 13. Services Section

Create a section titled:

**What Can I Do For Your Needs**

Use a short introductory paragraph similar in tone to:

> I build fast, reliable and user-friendly solutions that help individuals and businesses create meaningful digital experiences.

Add a small statistics area inspired by the reference.

Use conservative, non-fabricated statistics such as:

- 10+ Projects
- 2+ Years Learning
- 4 Core Services
- 100% Commitment

Do not claim real clients or professional achievements that were not supplied.

---

# 14. Required Services

The service section must contain exactly these four services:

### 1. FRONT-END WEB DEVELOPMENT

Description:

> I create responsive and modern websites using HTML, CSS, JavaScript and contemporary web-development practices.

### 2. C++ PROGRAMMING

Description:

> I write structured C++ programs for learning, problem solving, algorithms and software-development practice.

### 3. JAVASCRIPT

Description:

> I build interactive web experiences and dynamic functionality using JavaScript and modern browser APIs.

### 4. VIDEO EDITING

Description:

> I edit engaging digital content for social media, presentations and online platforms with attention to pacing and visual storytelling.

---

# 15. Service Images

Create or use a separate image for each service.

Generate four visually consistent service illustrations:

1. Front-End Web Development
2. C++ Programming
3. JavaScript
4. Video Editing

The images should:

- Match the dark portfolio aesthetic.
- Use gold, white, gray and subtle blue/purple accents where appropriate.
- Have a modern technology-oriented appearance.
- Work well inside small service cards.
- Be visually distinct.
- Maintain the same aspect ratio.

Suggested filenames:

```text
frontend-development.png
cpp-programming.png
javascript-development.png
video-editing.png
```

Do not use copyrighted logos as the main artwork unless they are created as simple illustrative symbols.

---

# 16. Service Card Design

Each service card should have:

- Dark slightly lighter background than the main page.
- Subtle border.
- Rounded corners.
- Service image.
- Service title.
- Short description.
- Small gold "Learn More →" link.

Desktop:

```text
[ Front-End ] [ C++ ] [ JavaScript ] [ Video Editing ]
```

Tablet:

```text
[ Front-End ] [ C++ ]
[ JavaScript ] [ Video Editing ]
```

Mobile:

```text
[ Front-End ]
[ C++ ]
[ JavaScript ]
[ Video Editing ]
```

The exact mobile arrangement may be adjusted if needed for better usability.

---

# 17. Visual Style

Match the screenshot's overall visual language.

Use approximately:

### Main background

```css
#0f141c
```

### Secondary panel

```css
#171e27
```

### Gold accent

```css
#f5c32c
```

### Primary text

```css
#ffffff
```

### Secondary text

```css
#b8bec8
```

### Border

Use a subtle semi-transparent light border.

Do not overuse bright colors.

---

# 18. Typography

Use a clean modern sans-serif stack such as:

```css
font-family:
    Arial,
    Helvetica,
    sans-serif;
```

Use:

- Bold large headings.
- Medium navigation text.
- Smaller muted descriptions.
- Gold for selected accents.
- Good line-height for paragraphs.

Avoid excessive font weights and unnecessary decorative typography.

---

# 19. Spacing

Use consistent spacing throughout.

Use CSS variables where useful:

```css
:root {
    --bg: #0f141c;
    --panel: #171e27;
    --gold: #f5c32c;
    --text: #ffffff;
    --muted: #b8bec8;
    --border: rgba(255, 255, 255, 0.12);
}
```

Use responsive spacing with `clamp()` where appropriate.

For example:

```css
padding: clamp(1rem, 4vw, 3rem);
```

---

# 20. Accessibility

Implement:

- Semantic `<header>`.
- `<nav>`.
- `<main>`.
- `<section>`.
- `<footer>` where appropriate.
- Meaningful heading hierarchy.
- Descriptive `alt` text for the profile image and service images.
- Accessible link labels.
- Visible keyboard focus states.
- Sufficient text contrast.

Do not use headings merely for visual sizing.

---

# 21. Hover and Interaction Effects

Use CSS only.

Add subtle transitions to:

- Navigation links.
- Social icons.
- Buttons.
- Service cards.
- GitHub button.

Example:

```css
transition:
    transform 0.2s ease,
    background-color 0.2s ease,
    border-color 0.2s ease;
```

Do not use excessive animations.

---

# 22. Mobile Layout Requirements

At 320px:

- The main container must fit inside the viewport.
- The hero should stack vertically.
- Profile image should scale down.
- Hero heading should wrap naturally.
- Hero paragraph should remain readable.
- Buttons should fit the available width.
- Social links should wrap into multiple rows if necessary.
- Service cards should become one-column.
- No element should cause horizontal scrolling.

Use:

```css
max-width: 100%;
```

where necessary.

Do not solve overflow by using:

```css
overflow-x: hidden;
```

as the primary fix.

Instead, identify and fix the element causing the overflow.

---

# 23. Desktop Layout Requirements

At 1024px and above:

Use a composition similar to the reference:

```text
-----------------------------------------------------
| Logo | Navigation               | Social | GitHub |
-----------------------------------------------------
|                                                   |
|  I'M                    |       PROFILE IMAGE     |
|  GODWIN                |                          |
|  AWAJIMOTUMU           |                          |
|                        |                          |
|  Bio                   |                          |
|  [Hire Me] [CV]        |                          |
|                                                   |
-----------------------------------------------------
| TikTok | Facebook | Instagram | X | LinkedIn ... |
-----------------------------------------------------
| What Can I Do For Your Needs | Service | Service |
|                              | Service | Service |
-----------------------------------------------------
```

Maintain the visual balance of the reference.

---

# 24. HTML Structure

Use a clean structure similar to:

```html
<body>
    <div class="portfolio">

        <header class="site-header">
            ...
        </header>

        <main>

            <section class="hero" id="home">
                ...
            </section>

            <section class="social-bar">
                ...
            </section>

            <section class="services" id="services">
                ...
            </section>

        </main>

    </div>
</body>
```

Keep the markup semantic and easy to edit.

---

# 25. CSS Architecture

Organize CSS in this order:

1. CSS variables
2. Reset
3. Base/body styles
4. Main container
5. Header/navigation
6. Hero
7. Profile image
8. Buttons
9. Social/contact bar
10. Services
11. Service cards
12. Hover states
13. Responsive breakpoint at 768px
14. Responsive breakpoint at 1024px

Comment each major section.

---

# 26. Final Quality Check

Before finishing, verify:

- [ ] Design closely resembles the reference screenshot.
- [ ] Only HTML and CSS are used.
- [ ] No JavaScript.
- [ ] No Bootstrap.
- [ ] No Tailwind.
- [ ] No external UI framework.
- [ ] Profile image is the supplied portrait.
- [ ] Profile image does not overflow at 320px.
- [ ] No horizontal scrolling at 320px.
- [ ] Hero heading uses `clamp()`.
- [ ] Hero paragraph uses `clamp()`.
- [ ] `@media (min-width: 768px)` exists.
- [ ] `@media (min-width: 1024px)` exists.
- [ ] Services include exactly the four requested services.
- [ ] Service images are included.
- [ ] TikTok link exists.
- [ ] Facebook link exists.
- [ ] Instagram link exists.
- [ ] X link exists.
- [ ] LinkedIn link exists.
- [ ] Slack link exists.
- [ ] Email link exists.
- [ ] GitHub button exists.
- [ ] All links are easy to edit.
- [ ] Navigation remains usable on mobile.
- [ ] Service cards adapt across mobile, tablet and desktop.
- [ ] Keyboard focus states are visible.
- [ ] Images have appropriate `alt` text.
- [ ] The page remains visually balanced at 320px, 768px, 1024px and larger desktop widths.

---

# 27. Expected Deliverables

Produce:

```text
project/
├── index.html
├── style.css
└── images/
    ├── profile.png
    ├── frontend-development.png
    ├── cpp-programming.png
    ├── javascript-development.png
    └── video-editing.png
```

The final result should be a polished, responsive personal portfolio for:

**GODWIN AWAJIMOTUMU**

It should preserve the visual character of the supplied reference while implementing the required responsive behavior and content.
