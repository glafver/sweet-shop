<div align="center">

# 🍬 Sweet Shop

An online candy shop that will sweeten your day!

**[🌐 Live demo](https://sweet-shop-glafver.netlify.app/)**

</div>

## 📖 About the project

**Sweet Shop** is a single-page application (SPA) for browsing and ordering sweets and treats. Users can explore the catalog, filter and search products, save favorites, add items to the cart, and place an order through a multi-step checkout.

The project was created as part of a **SkillUp** course assignment and uses the external [Bortakväll REST API](https://www.bortakvall.se/api/v2) to fetch product data and submit orders.

## ✨ Features

- 🏠 Home page with hero, benefits, brand logos, "New in" and subscribe sections
- 🛍️ Product catalog with search, category filters, sorting and star ratings
- 🔎 Dedicated product detail page (`/product/:id`)
- ❤️ Favorites (wishlist) persisted in `localStorage`
- 🛒 Shopping cart persisted in `localStorage` with quantity management
- 📦 Multi-step checkout: shipping → payment → order review, with form validation
- 🎉 Order confirmation with confetti animation
- 🔔 Toast notifications for user feedback
- 📱 Responsive interface
- ⚡ Scroll-to-top on navigation
- 🎨 Scroll/entrance animations

## 🛠️ Tech stack

| Category    | Technologies                                                                                     |
| ----------- | ------------------------------------------------------------------------------------------------ |
| Language    | [TypeScript](https://www.typescriptlang.org/)                                                     |
| UI library  | [React 18](https://react.dev/)                                                                    |
| Build tool  | [Vite](https://vitejs.dev/)                                                                       |
| Routing     | [React Router v6](https://reactrouter.com/)                                                       |
| API calls   | [Axios](https://axios-http.com/) + [React Query](https://tanstack.com/query/v3/)                  |
| Styling     | [Bootstrap 5](https://getbootstrap.com/) / [React Bootstrap](https://react-bootstrap.github.io/), [Sass](https://sass-lang.com/) |
| Icons       | [react-icons](https://react-icons.github.io/react-icons/)                                          |
| Animations  | [react-awesome-reveal](https://react-awesome-reveal.morello.dev/), [react-confetti](https://github.com/alampros/react-confetti) |
| Notifications | [react-toastify](https://fkhadra.github.io/react-toastify/)                                      |
| Linting     | [ESLint](https://eslint.org/)                                                                     |

## 📁 Project structure

```
sweet-shop/
├── public/                       # Static files
├── src/
│   ├── api/
│   │   └── api.ts                # API functions (axios)
│   ├── assets/                   # Brand logos and images
│   ├── components/
│   │   ├── cart_page/            # Cart item components
│   │   ├── home_page_sections/   # Home page sections (hero, benefits, etc.)
│   │   ├── order_page/           # Checkout blocks (shipping, payment, review)
│   │   ├── partials/             # Navbar, Footer, SearchBar, icons
│   │   └── products/             # ProductCard, ProductGrid, filters, ratings
│   ├── contexts/
│   │   ├── CartContext.tsx       # Cart context
│   │   ├── FavContext.tsx        # Favorites context
│   │   └── ProductsContext.tsx   # Products & filtering context
│   ├── helpers/
│   │   └── data.ts               # Shipping/payment methods, FAQ data
│   ├── hooks/
│   │   ├── useCart.ts            # Cart access hook
│   │   ├── useFav.ts             # Favorites access hook
│   │   └── useProducts.ts        # Products access hook
│   ├── pages/                    # Route pages
│   ├── styles/                   # SCSS partials
│   ├── types/
│   │   └── types.ts              # TypeScript types
│   ├── App.tsx                   # Root component and routes
│   ├── main.tsx                  # Entry point and providers
│   └── vite-env.d.ts
├── .env.example                  # Environment variables example
├── index.html
├── netlify.toml
├── _redirects
├── package.json
├── tsconfig.json
├── tsconfig.node.json
└── vite.config.ts
```

## 🧭 Routes

| Path            | Page                          |
| --------------- | ----------------------------- |
| `/`             | Home page                     |
| `/products`     | Product catalog               |
| `/product/:id`  | Product detail page           |
| `/new-in`       | New arrivals                  |
| `/cart`         | Shopping cart                 |
| `/order`        | Checkout                      |
| `/favorites`    | Favorites (wishlist)          |
| `/faq`          | Frequently asked questions    |
| `/contacts`     | Contact page                  |
| `*`             | 404 — Not found               |

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
