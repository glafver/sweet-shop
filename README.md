<div align="center">

# 🍬 Sweet Shop

An online candy shop that will sweeten your day!

**[🌐 Live demo](https://sweet-shop-glafver.netlify.app/)**

</div>

## 📖 About the project

**Sweet Shop** is a single-page application (SPA) for browsing and ordering sweets and treats. Users can browse the product catalog, filter products by category, add items to the cart, and place an order.

The project was created as part of a **SkillUp** course assignment and uses the external [Bortakväll REST API](https://www.bortakvall.se/api/v2) to fetch product data and submit orders.

## ✨ Features

- 🛍️ Product catalog with product cards (product grid)
- 🔍 Filter products by category (tags)
- 🔎 View detailed product information in a modal
- 🛒 Shopping cart persisted in `localStorage`
- ➕➖ Adjust item quantities in the cart
- 📦 Checkout with form validation
- ✅ Order confirmation after a successful submission
- 🏷️ Cart item count badge in the navigation bar
- 🚫 Stock availability checks (tracks `stock_quantity` and `stock_status`)
- 📱 Responsive interface

## 🛠️ Tech stack

| Category    | Technologies                                                                                     |
| ----------- | ------------------------------------------------------------------------------------------------ |
| Language    | [TypeScript](https://www.typescriptlang.org/)                                                     |
| UI library  | [React 18](https://react.dev/)                                                                    |
| Build tool  | [Vite](https://vitejs.dev/)                                                                       |
| Routing     | [React Router v6](https://reactrouter.com/)                                                       |
| API calls   | [Axios](https://axios-http.com/) + [React Query](https://tanstack.com/query/v3/)                  |
| Styling     | [Bootstrap 5](https://getbootstrap.com/) / [React Bootstrap](https://react-bootstrap.github.io/), [Sass](https://sass-lang.com/) |
| Icons       | [Bootstrap Icons](https://icons.getbootstrap.com/)                                                |
| Linting     | [ESLint](https://eslint.org/)                                                                     |

## 📁 Project structure

```
sweet-shop/
├── public/                    # Static files
├── src/
│   ├── api/
│   │   └── api.ts             # API functions (axios)
│   ├── components/
│   │   ├── CartItem.tsx        # Cart item row
│   │   ├── Navbar.tsx          # Navigation bar
│   │   ├── NavbarProductSelect.tsx # Product category selector
│   │   ├── OrderForm.tsx       # Checkout form
│   │   ├── OrderModal.tsx      # Order confirmation modal
│   │   ├── ProductCard.tsx     # Product card
│   │   ├── ProductGrid.tsx     # Product grid
│   │   └── ProductModal.tsx    # Product detail modal
│   ├── contexts/
│   │   ├── CartContext.tsx     # Cart context
│   │   └── ProductsContext.tsx # Products & filtering context
│   ├── hooks/
│   │   ├── useCart.ts          # Cart access hook
│   │   └── useProducts.ts      # Products access hook
│   ├── pages/
│   │   ├── CartPage.tsx        # Cart page (/cart)
│   │   └── ProductsPage.tsx    # Catalog page (/)
│   ├── types/
│   │   └── types.ts            # TypeScript types
│   ├── App.tsx                 # Root component and routes
│   ├── index.scss              # Global styles
│   └── main.tsx                # Entry point
├── .env.example                # Environment variables example
├── index.html
├── package.json
├── tsconfig.json
├── tsconfig.node.json
└── vite.config.ts
```

## 🚀 Getting started

### Prerequisites

- [Node.js](https://nodejs.org/) (LTS version recommended)
- [npm](https://www.npmjs.com/)

### Steps

1. **Clone the repository:**

   ```bash
   git clone https://github.com/glafver/sweet-shop.git
   cd sweet-shop
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Set up environment variables:**

   Create a `.env` file based on `.env.example`:

   ```bash
   cp .env.example .env
   ```

   Example `.env` contents:

   ```env
   VITE_USER_ID=13
   VITE_API_BASE_URL='https://www.bortakvall.se/api/v2'
   ```

4. **Start the development server:**

   ```bash
   npm run dev
   ```

   Open [http://localhost:5173](http://localhost:5173) in your browser.

## 📜 Scripts

| Command           | Description                                  |
| ----------------- | -------------------------------------------- |
| `npm run dev`     | Start the development server (Vite)          |
| `npm run build`   | Build the project (`tsc && vite build`)      |
| `npm run preview` | Preview the production build locally         |
| `npm run lint`    | Lint the code with ESLint                    |

## 🔌 API

The app interacts with the [Bortakväll v2 REST API](https://www.bortakvall.se/api/v2):

| Method  | Endpoint             | Description               |
| ------- | -------------------- | ------------------------- |
| `GET`   | `/products`          | Fetch all products        |
| `GET`   | `/products/:id`      | Fetch product details     |
| `GET`   | `/tags`              | Fetch categories (tags)   |
| `POST`  | `/users/:id/orders`  | Submit an order           |

## 👤 Author

Created by [glafver](https://github.com/glafver) as part of a course project.
