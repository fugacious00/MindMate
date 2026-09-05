# 🧠 MindMate Website - Digital Wellness Gateway

A modern, responsive marketing and authentication website for MindMate. The website serves as the digital gateway to MindMate's mental health companion ecosystem, featuring a beautiful landing page, user onboarding, and dashboard access.

![MindMate Logo](0-%20MindMate%20Logo.png)

## 🎯 Project Overview

MindMate Website is the public-facing platform that introduces users to MindMate's capabilities, handles user authentication (sign in/sign up), and provides seamless navigation to the web and mobile applications. Built with modern web technologies, it delivers a fast, accessible, and engaging user experience.

![MindMate Mascot](Screenshot%202026-01-10%20204839.png)

## ✨ Key Features

### 1. **Landing Page** 🏠
- Eye-catching hero section with value proposition
- Feature showcase with visual demonstrations
- Testimonials and success stories
- Call-to-action buttons for onboarding
- Responsive design for all device sizes

### 2. **User Authentication** 🔐
- Sign in for existing users
- Sign up with email/password
- Form validation and error handling
- Secure authentication flow
- "Forgot Password" recovery option

### 3. **Responsive Design** 📱
- Mobile-first approach
- Perfect on phone, tablet, and desktop
- Touch-friendly interface
- Optimized images and lazy loading
- Progressive Web App (PWA) capabilities

### 4. **Dark Mode** 🌙
- System preference detection
- Manual theme toggle
- Smooth transitions
- WCAG compliant contrast ratios
- Persistent user preference

### 5. **Dashboard Access** 📊
- Quick links to MindMate App
- User profile management
- Account settings
- Data export options
- Subscription management

### 6. **Resources Hub** 📚
- Mental health education
- Tips and best practices
- Crisis resources
- FAQ section
- Blog/Articles area

### 7. **AI Chat Integration** 🤖
- TheraBot preview on website
- Quick mental health support
- Embedded chat widget
- Lead generation through engagement

### 8. **Social Integration** 🔗
- Social sharing buttons
- Social login options (optional)
- Community features
- Newsletter subscription

## 🎨 Visual Preview

### Design Elements
![Awareness Icon](Screenshot%202026-01-21%20041600.png)
![Communication Icon](Screenshot%202026-01-23%20111213.png)
![Cloud Messaging Icon](Screenshot%202026-01-23%20111322.png)

### Brand Colors
- **Primary** (Purple): #7C3AED
- **Secondary** (Pink): #EC4899
- **Accent** (Blue): #06B6D4
- **Light Background**: #F8FAFC
- **Dark Background**: #0F172A

## 🚀 Getting Started

### Prerequisites
- **Node.js**: 18.0 or higher
- **npm** or **yarn** package manager
- Modern web browser (Chrome, Firefox, Safari, Edge)

### Installation & Setup

1. **Clone the repository**
```bash
git clone <repository-url>
cd mindmate-website
```

2. **Install dependencies**
```bash
npm install
# or
yarn install
```

3. **Create environment configuration**
```bash
cp .env.example .env.local
```

4. **Configure environment variables**
```env
# API Configuration
VITE_API_BASE_URL=http://localhost:3001

# Environment type
VITE_ENV=development

# Optional: Analytics
VITE_ANALYTICS_ID=your_analytics_id

# Optional: Gemini API for chat
VITE_GEMINI_API_KEY=your_api_key
```

5. **Start development server**
```bash
npm run dev
# or
yarn dev
```

6. **Access the website**
Open your browser and navigate to `http://localhost:5173`

## 🛠️ Available Commands

```bash
# Start development server with hot reload
npm run dev

# Build optimized production bundle
npm run build

# Preview the production build locally
npm run preview

# Type checking with TypeScript
npm run tsc

# Lint code (if configured)
npm run lint

# Format code (if configured)
npm run format
```

## 📁 Project Architecture

### Directory Structure
```
mindmate-website/
├── src/
│   ├── components/          # Reusable UI components
│   │   ├── Navigation/      # Header/Navigation bar
│   │   ├── Footer/          # Footer component
│   │   ├── Hero/            # Hero section
│   │   ├── Features/        # Feature cards
│   │   ├── Testimonials/    # User testimonials
│   │   ├── CTA/             # Call-to-action buttons
│   │   ├── Forms/           # Login/Signup forms
│   │   ├── Cards/           # Reusable card components
│   │   └── Common/          # Other common components
│   │
│   ├── pages/               # Page-level components
│   │   ├── Home.tsx         # Landing page
│   │   ├── Login.tsx        # Login page
│   │   ├── Signup.tsx       # Sign up page
│   │   ├── Dashboard.tsx    # User dashboard
│   │   ├── Features.tsx     # Features page
│   │   ├── Resources.tsx    # Resources hub
│   │   ├── Pricing.tsx      # Pricing page
│   │   └── NotFound.tsx     # 404 page
│   │
│   ├── sections/            # Larger page sections
│   │   ├── HeroSection.tsx
│   │   ├── FeaturesSection.tsx
│   │   ├── PromoSection.tsx
│   │   ├── TestimonialSection.tsx
│   │   └── CTASection.tsx
│   │
│   ├── services/            # API & business logic
│   │   ├── authService.ts   # Authentication
│   │   ├── apiService.ts    # API calls
│   │   ├── userService.ts   # User management
│   │   └── aiService.ts     # AI/Chat integration
│   │
│   ├── types.ts             # TypeScript definitions
│   ├── constants.tsx        # App constants
│   ├── App.tsx              # Root component
│   ├── index.tsx            # Entry point
│   ├── index.css            # Global styles
│   └── index.html           # HTML template
│
├── public/                  # Static assets
│   ├── images/
│   ├── icons/
│   └── fonts/
│
├── package.json             # Dependencies & scripts
├── tsconfig.json            # TypeScript configuration
├── vite.config.ts          # Vite configuration
├── tailwind.config.js       # Tailwind CSS config
├── postcss.config.js        # PostCSS configuration
└── README.md               # This file
```

### Page Flow Diagram
```
Landing Page (/)
├── Hero Section
├── Features Showcase
├── How It Works
├── Testimonials
├── Pricing
└── CTA → Sign Up / Sign In

Sign Up (/signup)
├── Email Registration
├── Password Setup
├── Verify Email
└── Create Profile

Sign In (/login)
├── Email Input
├── Password Input
├── Forgot Password Link
└── Submit

Dashboard (/dashboard)
├── User Profile
├── Quick Stats
├── Links to App
├── Settings
└── Logout
```

## 🔧 Technology Stack

### Core Framework
- **React 19.2.3** - Modern UI library
- **TypeScript 5.7** - Type-safe development
- **Vite 6.0.3** - Fast build tool and dev server

### Styling
- **Tailwind CSS 3.4** - Utility-first CSS framework
- **PostCSS 8.4** - CSS transformations
- **Autoprefixer 10.4** - Vendor prefixes

### Routing & Navigation
- **React Router 7.11.0** - Client-side routing
- **React Router DOM** - DOM bindings for routing

### UI Components & Icons
- **Lucide React 0.475** - Beautiful SVG icons
- **Motion 12.42.2** - Smooth animations

### Data Visualization
- **Recharts 3.6.0** - React charting library

### Forms & Validation
- **React Hook Form** (if used) - Efficient form handling
- **Zod** (if used) - TypeScript-first validation

### AI Integration
- **@google/genai 1.34.0** - Gemini AI API

### Development Tools
- **TypeScript** - Static type checking
- **ESLint** - Code quality
- **Prettier** - Code formatting

## 🎨 Design System

### Color Palette

```css
/* Primary Colors */
--color-primary: #7C3AED (Purple)
--color-primary-dark: #6D28D9
--color-primary-light: #A78BFA

/* Secondary Colors */
--color-secondary: #EC4899 (Pink)
--color-secondary-dark: #DB2777
--color-secondary-light: #F472B6

/* Accent Colors */
--color-accent: #06B6D4 (Cyan)
--color-success: #10B981 (Green)
--color-warning: #F59E0B (Amber)
--color-error: #EF4444 (Red)

/* Neutral */
--color-light: #F8FAFC
--color-dark: #0F172A
--color-gray: #64748B
```

### Typography

```css
/* Font Families */
--font-primary: 'Inter', system-ui, sans-serif
--font-mono: 'Fira Code', monospace

/* Font Sizes */
--text-xs: 0.75rem
--text-sm: 0.875rem
--text-base: 1rem
--text-lg: 1.125rem
--text-xl: 1.25rem
--text-2xl: 1.5rem
--text-3xl: 1.875rem
--text-4xl: 2.25rem
```

### Spacing Scale
```css
/* Based on 4px unit */
4px, 8px, 12px, 16px, 20px, 24px, 28px, 32px, 36px, 40px...
```

## 📱 Responsive Breakpoints

```
Mobile:    320px - 640px
Tablet:    641px - 1024px
Desktop:   1025px - 1440px
Large:     1441px+
```

## 🔐 Authentication Flow

### Sign Up Process
```
1. User fills signup form
2. Email validation
3. Password strength check
4. Submit to backend API
5. Account creation
6. Verification email sent
7. Email confirmation
8. Login & redirect to dashboard
```

### Sign In Process
```
1. User enters email & password
2. Credentials validated
3. API authentication
4. JWT token generated
5. Store auth token
6. Redirect to dashboard
7. Load user data
```

### Session Management
- JWT-based authentication
- Token stored in secure HttpOnly cookie (recommended)
- Auto-refresh on token expiry
- Logout clears session
- Session timeout after inactivity

## 🚀 Performance Optimization

### Implemented Optimizations
- **Code Splitting** - Lazy load routes and components
- **Image Optimization** - WebP format with fallbacks
- **CSS Minification** - Tailwind purging unused styles
- **Asset Caching** - Browser cache strategies
- **Lazy Loading** - Images and components
- **Bundle Analysis** - Keep bundle size minimal

### Performance Targets
- **First Contentful Paint (FCP)** < 1.5s
- **Largest Contentful Paint (LCP)** < 2.5s
- **Cumulative Layout Shift (CLS)** < 0.1
- **Bundle Size** < 300KB (gzipped)

## ♿ Accessibility

### WCAG 2.1 Compliance
- **Level A** - Fully compliant
- **Level AA** - Mostly compliant
- **Level AAA** - Partial compliance

### Accessibility Features
- Semantic HTML structure
- ARIA labels for interactive elements
- Keyboard navigation support
- Color contrast ratios (4.5:1 minimum)
- Screen reader optimization
- Focus indicators

## 📊 SEO Optimization

### On-Page SEO
- Meta tags and descriptions
- Open Graph tags for social sharing
- Structured data (JSON-LD)
- Sitemap generation
- Robots.txt

### Performance SEO
- Fast page load times
- Mobile-first indexing
- Core Web Vitals optimization

## 🔗 API Integration

### Backend Endpoints Used

```
POST   /api/auth/signup          - Register new user
POST   /api/auth/login           - User login
POST   /api/auth/logout          - User logout
POST   /api/auth/refresh         - Refresh token
GET    /api/auth/verify/:token   - Email verification

GET    /api/user/profile         - Get user profile
PUT    /api/user/profile         - Update profile
POST   /api/user/password        - Change password
GET    /api/user/settings        - Get settings

POST   /api/chat/message         - Send AI message
GET    /api/chat/history         - Get chat history

GET    /api/resources            - Get resources
GET    /api/blog                 - Get blog posts
```

## 📱 Mobile-First Approach

### Responsive Strategy
- Design for mobile first
- Progressively enhance for larger screens
- Touch-friendly interface (min 44px tap targets)
- Optimized images for different densities
- Mobile-friendly forms

### Mobile Testing
- Test on real devices
- Use Chrome DevTools mobile emulation
- Test with slow network (3G)
- Battery/CPU optimization

## 🌐 Internationalization (i18n)

To add multi-language support:

1. Install i18n library
```bash
npm install i18next react-i18next
```

2. Create translation files
```
src/locales/
├── en/
│   └── common.json
├── es/
│   └── common.json
└── fr/
    └── common.json
```

3. Configure i18n
4. Wrap app with I18nextProvider
5. Use useTranslation hook in components

## 🧪 Testing

### Testing Setup
```bash
npm install --save-dev vitest @testing-library/react @testing-library/jest-dom
```

### Test Files
```
src/
├── components/
│   └── __tests__/
│       └── Navigation.test.tsx
├── pages/
│   └── __tests__/
│       └── Home.test.tsx
└── services/
    └── __tests__/
        └── authService.test.ts
```

### Running Tests
```bash
npm run test           # Run tests
npm run test:watch    # Watch mode
npm run test:coverage # Coverage report
```

## 🚀 Deployment

### Build for Production
```bash
npm run build
```

This creates an optimized build in `dist/` directory.

### Deployment Platforms

**Vercel** (Recommended for React)
```bash
npm install -g vercel
vercel
```

**Netlify**
```bash
npm run build
# Then drag dist folder to Netlify
```

**AWS Amplify**
```bash
npm install -g @aws-amplify/cli
amplify init
amplify hosting add
amplify publish
```

**GitHub Pages**
```bash
# Update vite.config.ts with base: '/repo-name/'
npm run build
# Deploy dist folder to gh-pages branch
```

## 🐛 Troubleshooting

### Common Issues

**Issue: Hot reload not working**
```bash
# Restart dev server
npm run dev
```

**Issue: Tailwind styles not appearing**
- Check tailwind.config.js content paths
- Rebuild: `npm run build`
- Clear cache: `rm -rf node_modules .next`

**Issue: API calls failing**
- Verify VITE_API_BASE_URL in .env.local
- Check backend is running
- Verify CORS configuration

**Issue: Build fails**
```bash
# Clear cache and reinstall
rm -rf node_modules dist
npm install
npm run build
```

## 📈 Analytics & Tracking

Integrate analytics (optional):
```env
VITE_ANALYTICS_ID=google_analytics_id
VITE_MIXPANEL_ID=mixpanel_token
VITE_SEGMENT_WRITE_KEY=segment_key
```

## 🤝 Contributing

1. Fork repository
2. Create feature branch
3. Make changes
4. Test thoroughly
5. Submit pull request

## 📄 License

MIT License - See LICENSE file for details

## 🙏 Acknowledgments

- React & Vite communities
- Tailwind CSS framework
- All open-source contributors

## 📞 Support

- 📧 Email: support@mindmate.app
- 💬 Chat: In-app support
- 📱 Social: @MindMateApp
- 🐛 Issues: GitHub Issues

---

**Built with ❤️ for mental wellness**

Making mental health support accessible, affordable, and beautiful for everyone.
