# Reverso – Minimalist Fashion E-Commerce Web Application

Reverso is a modern and minimalistic fashion e-commerce web application built using React and TypeScript. It supports full shopping functionality, including user authentication, browsing products, managing a shopping cart, and placing orders using Stripe for secure payments.

The project uses Redux Toolkit and React Context API for global state management, and Material UI for styling and responsiveness. The architecture is modular and scalable for future development.

---

## Preview

![photo_2025-08-05 23 03 51](https://github.com/user-attachments/assets/127062f6-6182-47d7-8727-a82590f1275c)


---

## Project Overview

**Main Features:**
- User registration, login, logout
- JWT-based authentication with session persistence
- Product listing and detailed product pages
- Add-to-cart and checkout functionality
- Stripe payment integration (test key used)
- Responsive design using Material UI
- Contact and About pages
- Not Found (404) page
- React Router for navigation
- Context + Redux integration for state management
- Pre-configured for unit testing with React Testing Library

---

## Tech Stack

- React 18
- TypeScript
- Redux Toolkit
- React Router DOM
- Material UI & Emotion
- Stripe (Test Environment)
- Axios
- EmailJS
- React Testing Library
- Universal Cookie
- Create React App

---

## Getting Started

These instructions will help you set up and run the project locally.

### 1. Clone the repository

```bash
git clone https://github.com/your-username/reverso-react.git
cd reverso-react
```

### 2. Install dependencies

```bash
npm install
```

### 3. Start the development server

```bash
npm start
```

This will launch the app at `http://localhost:3000/`.

### 4. Run tests (optional)

```bash
npm test
```

---

## Running the App

- The app is built with Create React App and uses `npm start` to serve the frontend.
- All product logic is currently frontend-based. You can plug in your backend or API in the `services` folder.
- Session management uses cookies and localStorage.
- Stripe is integrated using a test public key. You can replace it with your own in `App.tsx`.

---

## Project Structure

```
public/
├── icons/
├── img/
├── video/
│   ├── hero-videos.mp4
│   ├── maniken.mp4
│   └── video-qoravoy.mp4
├── index.html
├── manifest.json
└── robots.txt

src/
├── app/
│   ├── components/        # Reusable UI elements (navbar, footer, etc.)
│   ├── context/           # Global context provider
├── css/                   # Global CSS styles
├── hooks/                 # Custom React hooks
├── libs/                  # Type definitions and utility types
├── MaterialTheme/         # Theme configuration for Material UI
├── pages/                 # Route-specific components
├── screens/               # High-level page structures and routes
├── service/               # API and logic services (e.g. Stripe, MemberService)
├── index.tsx              # Entry point
├── App.tsx                # Root application component
├── reportWebVitals.ts
├── setupTests.ts
├── react-app-env.d.ts

.env
.gitignore
package.json
tsconfig.json
yarn.lock
README.md
```

---

## Configuration Notes

- Stripe public test key is hardcoded in `App.tsx`:
  ```ts
  const stripePromise = loadStripe("pk_test_...");
  ```
  Replace with your own Stripe key if needed.

- Project uses strict TypeScript settings (`strict: true` in `tsconfig.json`).

- Path aliases are configured in `tsconfig.json` for cleaner imports:
  ```json
  "@components/*": ["src/components/*"]
  ```

- No backend is included — you can integrate one or connect to a headless CMS or Firebase as needed.

---

## What's Implemented

- Core e-commerce functionality
- Stripe test payment flow
- Static routing and authentication
- UI theming and layout

## What Can Be Improved or Added

- Full internationalization (i18n)

---

## License

This project is released under the MIT License.
