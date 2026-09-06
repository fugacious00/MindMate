# 🌐 MindMate Website



Beautiful marketing website and authentication gateway for MindMate.

---

## 🎯 Pages & Features

### 🏠 Landing Page
- Hero section with value proposition
- Feature showcase
- Testimonials
- Call-to-action buttons
- Beautiful animations

### 🔐 Authentication
- User sign up
- User login
- Password recovery
- Email verification

### 📊 Dashboard
- User profile
- Quick stats
- App links
- Settings & preferences

### 📚 Resources
- Mental health education
- Tips & strategies
- Crisis resources
- FAQ section

---

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Start development
npm run dev

# Build for production
npm run build
```

Open `http://localhost:5173`

---

## 🎨 Design

- **Responsive** - Mobile, tablet, desktop
- **Dark Mode** - System preference support
- **Accessible** - WCAG 2.1 compliant
- **Fast** - Optimized performance
- **Beautiful** - Modern, engaging UI

---

## 🎯 Color System

| Color | Hex | Use |
|-------|-----|-----|
| Primary | #7C3AED | Buttons, links, primary actions |
| Secondary | #EC4899 | Accents, highlights |
| Accent | #06B6D4 | Special elements |
| Success | #10B981 | Positive states |
| Error | #EF4444 | Errors, warnings |

---

## 📱 Responsive Breakpoints

```
Mobile:    320px - 640px
Tablet:    641px - 1024px
Desktop:   1025px - 1440px
Large:     1441px+
```

---

## 💻 Tech Stack

| Component | Technology |
|-----------|-----------|
| **Framework** | React 19 |
| **Language** | TypeScript |
| **Styling** | Tailwind CSS |
| **Routing** | React Router |
| **Build** | Vite |
| **Icons** | Lucide React |

---

## 🛠️ Development

### Commands

```bash
npm run dev          # Development server
npm run build        # Production build
npm run preview      # Preview build
npm run type-check   # Type checking
npm run lint         # Code quality
```

### Project Structure

```
src/
├── pages/          # Page components
├── components/     # Reusable UI
├── sections/       # Page sections
├── services/       # API calls
└── types/          # TypeScript types
```

---

## 🔐 Authentication Flow

1. User signs up with email
2. Verification email sent
3. Email confirmed
4. Profile created
5. Redirected to dashboard
6. Can launch app

---

## 🌙 Dark Mode

Automatically detects system preference:
- Light mode - default
- Dark mode - user preference
- Toggle switch available
- Smooth transitions

---

## 📊 Features

**User Management**
- Sign up & login
- Email verification
- Password recovery
- Profile editing
- Settings management

**Content**
- Landing page
- Resource hub
- Blog section
- FAQ
- Crisis links

**UX**
- Smooth animations
- Loading states
- Form validation
- Error messages
- Success feedback

---

## 🔗 API Integration

**User Authentication**
- Register new users
- Login & logout
- Token refresh
- Profile updates

**User Data**
- Fetch user profile
- Update preferences
- Export user data

**Content**
- Load resources
- Fetch blog posts
- Get FAQ

---

## 🧪 Testing

```bash
npm run test         # Run tests
npm run test:watch   # Watch mode
npm run e2e          # End-to-end tests
```

---

## 📈 Performance

- **Bundle size** < 300KB (gzipped)
- **First paint** < 1.5s
- **Lighthouse** 90+
- **Core Web Vitals** optimized

---

## ♿ Accessibility

- Semantic HTML
- ARIA labels
- Keyboard navigation
- Color contrast 4.5:1+
- Focus indicators
- Screen reader support

---

## 🚀 Deployment

```bash
# Build production bundle
npm run build

# Deploy to Vercel
vercel --prod

# Deploy to Netlify
netlify deploy --prod --dir=dist
```

---

## 🔐 Security

- HTTPS everywhere
- CORS configured
- CSRF protection
- Input validation
- No hardcoded secrets
- Environment variables

---

## 📖 Documentation

- **[QUICK-START.md](./QUICK-START.md)** - Fast setup
- **[ARCHITECTURE.md](./docs/ARCHITECTURE.md)** - System design
- **[DEPLOYMENT.md](./docs/DEPLOYMENT.md)** - Production

---

## 🤝 Contributing

1. Fork repository
2. Create feature branch
3. Make changes
4. Test thoroughly
5. Submit pull request

---

## ⚠️ Disclaimer

Website directs to MindMate App for wellness features.
MindMate is not a substitute for professional mental health care.

---

## 📄 License

MIT License

---

## 📞 Support

- 📧 support@mindmate.app
- 🐛 [Issues](https://github.com/mindmate/mindmate/issues)
- 💬 [Discussions](https://github.com/mindmate/mindmate/discussions)

---

<div align="center">

**Beautiful, responsive, secure marketing platform**

[Home](https://mindmate.app) • [Docs](./docs/) • [Issues](https://github.com/mindmate/mindmate/issues)

v1.0.0 • MIT License

</div>
