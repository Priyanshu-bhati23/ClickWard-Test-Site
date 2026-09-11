# ClickWard Test Site — BuildFast Demo

This is a **demo customer website** used to test ClickWard A/B testing.

## Setup

### 1. Install the ClickWard Snippet

Open `index.html` and find this comment near the bottom:
```
<!-- CLICKWARD_SNIPPET_PLACEHOLDER -->
```

Replace it with your ClickWard snippet:
```html
<script async src="https://YOUR-CLICKWARD-APP.vercel.app/sdk.js" data-experiment="YOUR_EXPERIMENT_ID"></script>
```

### 2. Target Element

The primary CTA button that ClickWard will A/B test is:
```html
<a href="#signup" id="hero-cta" class="btn-primary">
  Get Started Free
</a>
```

Set your experiment's **Target Selector** to: `#hero-cta`

### 3. Deploy to Vercel

1. Push this folder to a GitHub repo
2. Import in Vercel
3. Deploy — static HTML, zero configuration needed

### 4. Testing from 3 Devices

After deploying:
- Open the live Vercel URL on your **laptop**
- Open on your **phone** (different visitor ID → may get different variant)
- Open in **incognito mode** (another fresh visitor)

Each device gets independently assigned to a variant by the ClickWard SDK.

---

## File Structure

```
clickward-test-site/
├── index.html     ← Main site with hero CTA (#hero-cta)
├── style.css      ← Styles
├── package.json
└── README.md
```
