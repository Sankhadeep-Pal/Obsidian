# Web Content Accessibility Guidelines

**WCAG** stands for **Web Content Accessibility Guidelines**.

It's a set of international standards published by the **W3C (World Wide Web Consortium)** to help make web content **more accessible** to people with disabilities—including visual, auditory, physical, speech, cognitive, and neurological disabilities.

## 📋 Why WCAG Matters in Web Design (especially CSS)

WCAG helps ensure that your website is:

- 🧑‍🦯 **Perceivable** (users can see or hear your content)

- 🎮 **Operable** (users can navigate with a keyboard, screen reader, etc.)

- 🧠 **Understandable** (easy to read and navigate)

- 🛠️ **Robust** (works well with assistive technologies)

## 🎨 In Terms of CSS, WCAG Covers Things Like:

### 1. **Color Contrast**
Text should have enough contrast with its background.

- Example:

```css
color: #333;
background-color: #fff;
```

- WCAG AA requires **4.5:1 contrast ratio** for normal text.

- Tools:
    
    - [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)
    
    - [Accessible Colors](https://accessible-colors.com/)

### 2. **Font Size**

- Text should be readable even when zoomed in.

```css
font-size: 1rem; /* instead of 12px */
```

### 3. **Focus States**

Visible outlines help keyboard users.

```css
button:focus {
  outline: 2px solid #005fcc;
}
```

### 4. **Avoiding Color-Only Cues**

Don’t rely solely on color to convey meaning. Use text or icons too.

```html
<!-- ❌ Bad -->
<span style="color: red;">Required</span>

<!-- ✅ Good -->
<span style="color: red;">* Required</span> <i class="fas fa-asterisk"></i>
```

### 🔍 Versions of WCAG

- **WCAG 2.0:** Baseline (most common)
    
- **WCAG 2.1:** Includes mobile & cognitive considerations
    
- **WCAG 2.2:** Adds more focus on navigation and input accessibility (published 2023)
    
- **WCAG 3.0:** Currently in draft—more flexible and inclusive
    

---
