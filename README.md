# Teja's MERN Stack Developer Portfolio

🚀 A production-grade, modern web portfolio built with React 18, TypeScript, and deployed on GitHub Pages.

## Features

✨ **React 18 Concurrent Features**
- Suspense boundaries
- useTransition and useDeferredValue hooks
- Lazy code splitting

🎨 **Modern Tech Stack**
- React 18 + TypeScript + Vite
- Tailwind CSS for styling
- Framer Motion for animations
- React Router for client-side navigation

🤖 **AI/ML Integration**
- TensorFlow.js for client-side ML
- MobileNet for image classification
- Real-time predictions in browser

📱 **Responsive Design**
- Mobile-first approach
- Dark mode support
- Accessible components (a11y)

🚀 **Deployment**
- GitHub Pages (static hosting)
- GitHub Actions CI/CD
- Automated builds and deployments

## Live Demo

📌 Visit the deployed portfolio: [https://businesstar.github.io/teja-mern-portfolio](https://businesstar.github.io/teja-mern-portfolio)

## Quick Start

### Prerequisites
- Node.js 18+
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/businesstar/teja-mern-portfolio.git
cd teja-mern-portfolio

# Install dependencies
npm install

# Start development server
npm run dev
```

Visit `http://localhost:3000` in your browser.

### Build for Production

```bash
npm run build
```

### Deploy to GitHub Pages

```bash
npm run deploy
```

## Project Structure

```
teja-portfolio/
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions CI/CD
├── public/
│   ├── 404.html                # SPA routing hack
│   └── data/                   # Static JSON data
│       ├── experience.json
│       └── projects.json
├── src/
│   ├── components/             # Reusable components
│   │   ├── Hero.tsx
│   │   ├── AIPlayground.tsx
│   │   └── Timeline.tsx
│   ├── pages/                  # Page components
│   │   ├── Home.tsx
│   │   ├── Projects.tsx
│   │   ├── Experience.tsx
│   │   └── AIPlayground.tsx
│   ├── hooks/                  # Custom React hooks
│   │   └── useStaticData.ts
│   ├── App.tsx                 # Main app component
│   ├── main.tsx                # Entry point
│   └── index.css               # Global styles
├── index.html
├── vite.config.ts              # Vite configuration
├── tsconfig.json               # TypeScript config
├── tailwind.config.js          # Tailwind CSS config
└── package.json
```

## Available Scripts

### `npm run dev`
Start the development server with hot reload.

### `npm run build`
Build the project for production. Output goes to `dist/` folder.

### `npm run preview`
Preview the production build locally.

### `npm run deploy`
Build and deploy to GitHub Pages.

### `npm run predeploy`
Automatically runs before `npm run deploy`.

## GitHub Pages Configuration

### Enable GitHub Pages

1. Go to **Settings** → **Pages**
2. Under **Source**, select **GitHub Actions**
3. The workflow file will handle deployments automatically

### Update Repository Settings

In `package.json`, update the `homepage` field:

```json
"homepage": "https://YOUR_USERNAME.github.io/teja-mern-portfolio"
```

Also update in `vite.config.ts`:

```typescript
const REPO_NAME = 'teja-mern-portfolio';
export default defineConfig(({ mode }) => ({
  base: mode === 'production' ? `/${REPO_NAME}/` : '/',
  // ...
}));
```

## Technologies Used

### Frontend
- **React 18** - UI library with concurrent features
- **TypeScript** - Type safety
- **Vite** - Lightning fast build tool
- **Tailwind CSS** - Utility-first CSS
- **Framer Motion** - Animation library
- **React Router** - Client-side routing
- **React Query** - Data fetching and caching

### AI/ML
- **TensorFlow.js** - ML in JavaScript
- **MobileNet** - Image classification model
- **Client-side inference** - No backend required

### DevOps
- **GitHub Actions** - CI/CD pipeline
- **GitHub Pages** - Static hosting
- **Docker** - Containerization (optional)

## Performance Optimizations

🚀 **Bundle Optimization**
- Code splitting with lazy loading
- Tree shaking unused code
- Minification and compression
- Vendor chunk separation

⚡ **Runtime Performance**
- React concurrent features
- Suspense boundaries
- Deferred value updates
- Memoization of expensive computations

📊 **Build Metrics**
- Lighthouse score: 95+
- First Contentful Paint: <1s
- Time to Interactive: <2s

## Deployment Pipeline

```
Push to main
    ↓
GitHub Actions
    ↓
Install dependencies (npm ci)
    ↓
Run tests
    ↓
Build (npm run build)
    ↓
Deploy to GitHub Pages
```

## API Simulation

Since GitHub Pages only hosts static files, the portfolio uses JSON files to simulate API responses:

```typescript
// src/hooks/useStaticData.ts
export function useStaticData(endpoint: string) {
  return useMemo(() => {
    // Simulates API call
    return fetch(`/data/${endpoint}.json`).then(r => r.json());
  }, [endpoint]);
}
```

Static data files in `public/data/`:
- `experience.json` - Career history
- `projects.json` - Portfolio projects
- `skills.json` - Technical skills

## Features Showcase

### 🎯 AI Playground
Upload images to classify using TensorFlow.js running entirely in the browser. No backend or API calls required!

### 🎨 Dark Mode
Toggle between light and dark themes with smooth transitions.

### 📊 Interactive Timeline
Clickable career timeline with smooth animations.

### 🔍 Project Filtering
Filter projects by technology stack.

## Customization

### Update Personal Information

1. **Resume Data**: Edit `public/data/experience.json`
2. **Projects**: Edit `public/data/projects.json`
3. **Colors**: Modify `tailwind.config.js`
4. **Links**: Update social media links in component files

### Add New Pages

1. Create new file in `src/pages/`
2. Add route to `src/App.tsx`
3. Update navigation menu

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## SEO Optimization

- Semantic HTML
- Meta tags in `index.html`
- Open Graph tags for social sharing
- Mobile-friendly responsive design

## Testing

```bash
# Run tests
npm run test

# Run tests with coverage
npm run test:coverage
```

## Contributing

Feel free to fork and submit pull requests for any improvements!

## License

MIT License - feel free to use this for your own portfolio!

## Contact

- **LinkedIn**: [linkedin.com/in/teja](https://linkedin.com/in/teja)
- **GitHub**: [@businesstar](https://github.com/businesstar)
- **Email**: teja@example.com

## Acknowledgments

- React team for React 18 concurrent features
- TensorFlow.js for browser-based ML
- GitHub for free static hosting
- Tailwind CSS for styling utilities

---

**Built with ❤️ by Teja | Last Updated: 2024**
