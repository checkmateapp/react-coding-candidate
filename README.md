# Kiosk Quest (Live Coding) 🍔⚡
**30‑Minute React Live‑Coding Exercise**

Thanks for your interest! This short, fun, time‑boxed exercise is designed to assess how you build React components, manage state, and implement core React patterns in a live interview setting.

**Note**: This exercise builds on the same business logic as the Kiosk Quest take-home assignment (Python/Ruby on Rails). You'll be building the frontend for the same kiosk ordering system.

---

## 🎯 Goal

Build a simple kiosk ordering UI that displays a menu, allows users to add items to a cart, calculates totals with discounts, and submits orders.

Time expectation: **~35-40 minutes coding + separate discussion time**

---

## 🛠️ Setup

**Use the provided starter template**
- Navigate to `react_starter_template/`
- Open `index.html` in your browser (no build step required)
- Edit the JavaScript directly in the `<script type="text/babel">` tag in `index.html`

**CSS is already provided** - you don't need to write any CSS. Just use these 5 predefined class names:
- `container` - Grid layout for menu + cart (2fr 1fr)
- `menu-grid` - Grid layout for menu items
- `menu-item` - Individual menu item card
- `cart` - Cart section wrapper
- `button` - All buttons (same style)

The CSS is already included in the template file - no separate CSS file needed.

---

## 📦 Menu Data (already provided in template)

The `MENU_ITEMS` constant is already in the starter template - no need to copy it.

```javascript
const MENU_ITEMS = [
  { id: 1, name: "Cheeseburger", priceCents: 899, prepSeconds: 90 },
  { id: 2, name: "Fries", priceCents: 399, prepSeconds: 60 },
  { id: 3, name: "Milkshake", priceCents: 499, prepSeconds: 75 },
  { id: 4, name: "Salad", priceCents: 699, prepSeconds: 45 },
  { id: 5, name: "Nuggets", priceCents: 599, prepSeconds: 80 }
];
```

---

## 📝 Step-by-Step Exercise

Complete each step, then we'll discuss your approach before moving to the next.

### Step 1: Display Menu (5-7 minutes)
**Task:** Create a component that displays the 5 menu items in a list or grid. Show the name and price for each item.

---

### Step 2: Add to Cart (5-7 minutes)
**Task:** Add an "Add to Cart" button to each menu item. Display selected items in a cart summary. (Click multiple times to add multiples of the same item.)

**Data structure hint**: The cart should be an array of line items, where each item includes its quantity:
```javascript
// Example cart structure:
[
  { id: 1, name: "Cheeseburger", priceCents: 899, prepSeconds: 90, quantity: 2 },
  { id: 2, name: "Fries", priceCents: 399, prepSeconds: 60, quantity: 1 }
]
```

---

### Step 3: Calculate Totals (5-7 minutes)
**Task:** Implement pricing logic:
- `total = sum(priceCents * quantity)`
- Display total in the cart

---

### Step 4: Order Submission (5-7 minutes)
**Task:** Add a "Place Order" button that:
- Validates the cart is not empty
- Shows a success message with the order summary
- Clears the cart after successful submission

---

### Bonus 1: Discount Logic (5 minutes, if time permits)
**Task:** Add discount logic to the cart:
- If subtotal **≥ 2000 cents** ($20), apply **10% discount** (round to nearest cent)
- `final_total = subtotal - discount`
- Display subtotal, discount (if applicable), and final total in the cart

---

### Bonus 2: Prep Time Display (5 minutes, if time permits)
**Task:** Display the estimated prep time using a greedy algorithm:
- The kitchen has **2 parallel prep stations**
- For each line item: `line_prep = prepSeconds * quantity`
- Assign each `line_prep` to the station with the **lowest current load**
- `estimated_prep_seconds = max(station_1_load, station_2_load)`

---

## 💡 Tips

- Keep components small and focused
- Think about when to lift state up vs keep it local
- Consider readability over cleverness
- It's okay to make trade-offs under time pressure - we'll discuss them
- Ask clarifying questions if anything is unclear

Good luck — and have fun 🚀
