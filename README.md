# Workers Platform - Frontend Development Assignment

A modern, responsive web application for connecting users with skilled workers across various service categories.

---

## 🚀 How to Run Locally

### **Prerequisites**

- **Node.js:** v18.17.0 or higher
- **npm:** v9.0.0 or higher

### **Setup & Start**

```bash
# 1. Clone the repository
git clone <repository-url>
cd frontend_dev_assignment

# 2. Install dependencies
npm install

# 3. Start the development server
npm run dev

# 4. Open in your browser
http://localhost:3003
```

### **Build for Production**

```bash
npm run build     # Create an optimized production build
npm start         # Start the production server
```

### **Environment Variables**

Create a `.env.local` file if needed:

```bash
NEXT_PUBLIC_API_URL=https://api.workers-platform.com
```

---

## 📝 What Was Implemented

This assignment demonstrates practical skills in **React 19**, **Next.js 15 (App Router)**, **TypeScript**, and **Tailwind CSS v4**.  
The following features have been fully implemented:

1. **Responsive Grid Cards**  
   - Fully responsive workers grid (1–4 columns) with modern UI/UX, aspect ratio images, hover effects, and skeleton loading screens.

2. **Sticky Navbar**  
   - Position-fixed navbar with backdrop blur, scroll-responsive opacity/shadow, mobile hamburger menu, and animated transitions.

3. **Performance Optimizations**  
   - Lazy loading for images/components, memoization (`React.memo`, `useCallback`), custom data-fetching hooks, skeleton loaders, and error boundaries.

4. **Pagination**  
   - Server-side pagination with URL state, dynamic page numbers, ellipsis, and smooth scroll-to-results.

5. **Service Filters**  
   - Multi-select service categories, price range filtering, sort options, real-time application, filter persistence, and seamless pagination integration.

6. **API Integration**  
   - All data served via a RESTful API (`/api/workers`) with support for filtering, pagination, error handling, and query params.
   - Custom `useWorkers` React hook with SWR-like caching.

7. **Testing**  
   - Unit/component/integration tests using Jest and React Testing Library (see below for running instructions).

#### **Assumptions**
- Mock data (1000+ worker records) is used instead of a real backend.
- Placeholder images are used for workers.
- No user authentication system is implemented.
- Focus is on frontend engineering and UI/UX, not backend/PWA/offline.

---

## ⚖️ Trade-offs & Known Issues

- **Client-side Filtering:** Chosen for UX; limited by already-loaded data.
- **Static Data:** No backend; all data is mock.
- **Bundle Size:** Tailwind increases bundle size, but improves dev speed.
- **No Authentication:** No login/signup for users or workers.
- **Image Placeholders:** Real images can be added for production.
- **No PWA/Offline Support:** Only live web app functionality.

---

**Animations:**
- Navbar opacity/shadow on scroll
- Card hover scaling
- Loading skeletons
- Filter transitions
- Smooth page transitions

> _Tip: Add your own screenshots or a short GIF by placing them in a `/screenshots` folder and updating the Markdown above._

---

## 🧪 Unit & Component Tests

### **Testing Setup**
- **Framework:** Jest + React Testing Library
- **Environment:** jsdom

### **Run Tests**

```bash
# Run all tests
npm test

# Watch mode
npm run test:watch

# Coverage report
npm run test:coverage
```

### **Test Coverage**
- Component rendering
- User interactions
- API integration and mocking
- Error/loading state handling
- Filters and pagination

---

## 📦 Project Structure

```
src/
├── app/                    # App Router pages
│   ├── page.tsx           # Workers listing
│   ├── layout.tsx         # Root layout/navbar
│   └── api/               # API routes
├── components/            # UI components
│   ├── Navbar.tsx
│   ├── Filters.tsx
│   ├── Pagination.tsx
│   ├── WorkerCardSkeleton.tsx
│   └── ErrorBoundary.tsx
├── hooks/                 # Custom hooks
│   └── useWorkers.ts
└── types/                 # TypeScript types
    └── workers.ts
```

---

## 🤝 Contributing

1. Create a feature branch from `main`
2. Make/test your changes
3. Run lint & test: `npm run lint && npm test`
4. Create a pull request

---

**Built with** ❤️ **by Shreya for Frontend Development Assignment**

*This project demonstrates modern React development practices, responsive design, and comprehensive testing strategies for scalable web applications.*
