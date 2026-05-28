# How to add real images later

Every image placeholder in the site looks like this in the HTML:

```html
<div class="img-slot">
  <span class="img-slot__label">Hero Image<br><small>...</small></span>
</div>
```

To replace it with a real image, simply put an `<img>` tag inside the same `div.img-slot`:

```html
<div class="img-slot">
  <img src="assets/your-photo.jpg" alt="Description">
</div>
```

The CSS will automatically:
- Cover the full slot area
- Sit on top of the placeholder label (which then disappears visually)
- Keep all spacing and aspect ratios intact

## Image dimensions suggested

Each placeholder shows the suggested dimensions (e.g. "1200 × 800"). These are guides — the slots are responsive and will adapt to any image, but using the suggested aspect ratios will give the best results.

## Where image slots exist

**index.html**
- Hero image (1200×800) — KL skyline / boardroom
- Featured mandate photo (1280×720)
- Team photo (960×1200)
- 5× pillar images (800×600 each)
- 6× client logos (the firm's clients)
- Testimonial portrait (600×600)

**services.html**
- Page hero image (800×600)
- 5× pillar deep-dive images (800×600 each)

**team.html**
- Page hero image (800×600)
- 5× team portraits (480×600 each — Alvin, Hong, Boon, Sze Thian, Agnes)

**news.html**
- Page hero image (800×600)
- Featured report cover (800×600)
- 9× news article images (600×375 each)

**contact.html**
- Page hero image (800×600)
- 1× office photo or Google Map embed (1200×800)

## Tip: Google Map embed instead of a photo

For the contact page office slot, you can drop in a Google Maps embed iframe instead of an image. Get the embed code from Google Maps (Share → Embed a map → COPY HTML), then paste inside the `.img-slot` div:

```html
<div class="img-slot">
  <iframe src="https://www.google.com/maps/embed?pb=..." 
          style="border:0; width:100%; height:100%; position:absolute; inset:0;" 
          allowfullscreen="" loading="lazy"></iframe>
</div>
```
