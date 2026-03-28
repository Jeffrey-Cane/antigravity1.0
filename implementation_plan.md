# CANE's STORE — Grocery Ecommerce Site Launch Plan

A fast, launchable grocery storefront built with vanilla HTML/CSS/JS.
No backend required — product data is stored in a local JSON file,
and the cart is persisted via `localStorage`.

---

## Store Details

| Field | Value |
|---|---|
| Store Name | CANE's STORE |
| Currency | Kenya Shillings (KSh) |
| Categories | Fruits, Vegetables, Dairy, Bakery, Snacks, Drinks |

---

## Stack

| Layer | Choice | Reason |
|---|---|---|
| Structure | HTML5 | Simple, universal |
| Styling | Vanilla CSS (dark/light theme) | No build tools needed |
| Logic | Vanilla JavaScript | Zero dependencies |
| Data | `products.json` | Easy to edit, no DB needed |
| State | `localStorage` | Cart persists on refresh |
| Hosting | Open directly in browser / static host (Netlify, GitHub Pages) | Instant launch |

---

## Pages & Features

### 1. `index.html` — Home / Shop
- **Hero section** with banner image and CTA
- **Category filter bar** (Fruits, Vegetables, Dairy, Bakery, Snacks, Drinks)
- **Product grid** — card per item with image, name, price (KSh), and "Add to Cart" button
- **Search bar** — live filter as you type
- **Sticky navbar** with logo, search, and cart icon with badge counter

### 2. Cart Sidebar / Drawer
- Slides in from the right
- Shows items, quantities, subtotal in KSh
- Increase/decrease/remove items
- "Checkout" button (launches a simple order form modal)

### 3. Order Modal (Checkout)
- Name, address, phone, payment method (M-Pesa / Cash on Delivery)
- "Place Order" submits and shows a confirmation screen

### 4. `products.json` — Product Data
```json
[
  {
    "id": 1,
    "name": "Organic Apples",
    "category": "Fruits",
    "price": 350,
    "unit": "per kg",
    "image": "images/apples.jpg",
    "badge": "Organic"
  }
]
```

---

## Design System

- **Color palette**: Fresh green accent (`#22c55e`) on a clean off-white background, dark navbar
- **Font**: Google Fonts — `Outfit` (headings) + `Inter` (body)
- **Cards**: Subtle shadows, rounded corners, hover lift animation
- **Animations**: Smooth cart drawer slide, product card hover scale, badge pulse
- **Responsive**: CSS Grid adapts from 4 columns → 2 → 1 on mobile

---

## File Structure

```
antigravity1.0/
├── index.html
├── style.css
├── app.js
├── products.json
├── implementation_plan.md   ← this file
└── images/
    ├── hero.jpg
    └── (product images)
```

---

## Verification Plan

- Open `index.html` in browser — no server needed
- Add items to cart, refresh page — cart should persist
- Filter by category and search products
- Complete checkout flow and see confirmation
- Optionally drag folder into Netlify Drop for a live URL

---

*Plan created: 2026-03-28*
