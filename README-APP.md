# 🧠 MindMate App - Mental Health Companion

A feature-rich mental health companion application built with modern React and TypeScript. MindMate helps users track their emotional wellbeing, manage habits, journal thoughts, and receive AI-powered support through TheraBot.

![MindMate Logo](0-%20MindMate%20Logo.png)

## 🎯 Project Overview

MindMate App is designed to be a comprehensive mental wellness platform that runs entirely on the client-side with no data sent to servers. Users can:

- Track daily moods and emotional patterns
- Write and store private journal entries
- Monitor sleep habits and patterns
- Build and maintain positive habits
- Practice cognitive behavioral therapy (CBT) exercises
- Chat with an AI-powered mental health assistant (TheraBot)
- Access all features completely offline

![MindMate Mascot](Screenshot%202026-01-10%20204839.png)

## ✨ Key Features

### 1. **Mood Tracking** 📊
- Log daily moods with detailed notes
- Track emotional patterns over time
- Visualize mood trends with interactive charts
- Add context and notes to each mood entry

### 2. **Private Journaling** 📔
- Write and store personal journal entries
- Complete privacy - data never leaves your device
- Search and filter past entries
- Emotional context tagging

### 3. **Sleep Tracking** 😴
- Monitor sleep duration and quality
- Track sleep patterns
- Get insights on sleep correlations with mood
- Visualize sleep data over time

### 4. **Habit Building** 🎯
- Create and track positive habits
- Set goals and monitor progress
- Visual streak indicators
- Habit reminders and notifications

### 5. **CBT Exercises** 🧠
- Guided cognitive behavioral therapy techniques
- Thought records for managing negative thoughts
- Behavioral activation exercises
- Structured problem-solving tools

### 6. **AI Companion - TheraBot** 🤖
- 24/7 access to AI-powered mental health support
- Powered by Google's Gemini AI
- Conversational support and coping strategies
- Personalized suggestions based on user data

### 7. **Data Security & Privacy** 🔒
- End-to-end encrypted local storage
- No cloud sync or data transmission
- Offline-first architecture
- Complete user privacy and control

## 🎨 Visual Preview

### Icon Suite
![Awareness Icon](Screenshot%202026-01-21%20041600.png)
![Communication Icon](Screenshot%202026-01-23%20111213.png)
![Cloud Messaging Icon](Screenshot%202026-01-23%20111322.png)

## 🚀 Getting Started

### Prerequisites
- **Node.js**: 18.0 or higher
- **npm** or **yarn** package manager
- Modern web browser (Chrome, Firefox, Safari, Edge)

### Installation & Setup

1. **Clone the repository**
```bash
git clone <repository-url>
cd mindmate-app
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
# Optional: API base URL for backend integration
VITE_API_BASE_URL=http://localhost:3001

# Optional: Google Gemini API key for AI features
VITE_GEMINI_API_KEY=your_gemini_api_key_here
```

5. **Start development server**
```bash
npm run dev
# or
yarn dev
```

6. **Access the application**
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
```

## 📁 Project Architecture

### Directory Structure
```
mindmate-app/
├── src/
│   ├── components/          # React components
│   │   ├── Dashboard/       # Main dashboard views
│   │   ├── MoodTracker/     # Mood tracking components
│   │   ├── Journal/         # Journaling interface
│   │   ├── Habits/          # Habit tracking UI
│   │   ├── Chat/            # AI chat interface
│   │   ├── Auth/            # Authentication components
│   │   └── Common/          # Shared components (Nav, Footer, etc.)
│   │
│   ├── services/            # Business logic & API integration
│   │   ├── moodService.ts   # Mood tracking logic
│   │   ├── journalService.ts # Journal management
│   │   ├── habitService.ts  # Habit tracking
│   │   ├── aiService.ts     # AI/Gemini integration
│   │   └── storageService.ts # Local storage management
│   │
│   ├── utils/               # Utility functions & helpers
│   │   ├── encryption.ts    # Data encryption utilities
│   │   ├── validators.ts    # Input validation
│   │   ├── formatters.ts    # Data formatting
│   │   └── dateUtils.ts     # Date/time operations
│   │
│   ├── types.ts             # TypeScript type definitions
│   ├── constants.tsx        # Application constants
│   ├── auth.ts              # Authentication logic
│   ├── dataService.ts       # Data management
│   ├── App.tsx              # Root application component
│   ├── index.tsx            # Entry point
│   └── index.html           # HTML template
│
├── public/                  # Static assets
├── package.json             # Dependencies & scripts
├── tsconfig.json            # TypeScript configuration
├── vite.config.ts          # Vite build configuration
└── README.md               # This file
```

### Component Hierarchy

```
App
├── Layout
│   ├── Header
│   ├── Sidebar Navigation
│   ├── Main Content (Router)
│   │   ├── Dashboard
│   │   ├── MoodTracker
│   │   ├── Journal
│   │   ├── Habits
│   │   ├── CBT Exercises
│   │   ├── TheraBot Chat
│   │   └── Settings
│   └── Footer
└── Auth Portal (Login/Register)
```

## 🔧 Technology Stack

### Core Framework
- **React 19.2.3** - UI library with latest hooks
- **TypeScript 5.8** - Type-safe JavaScript
- **Vite 6.2.0** - Lightning-fast build tool

### Styling & UI
- **Tailwind CSS** - Utility-first CSS framework
- **Lucide React 1.23.0** - Beautiful icon library
- **Motion 12.42.2** - Smooth animations

### Data & Storage
- **Dexie 4.0.1** - IndexedDB wrapper for offline data
- **Zod 3.22.4** - TypeScript-first schema validation

### AI Integration
- **@google/genai 1.34.0** - Google Gemini AI SDK

### Visualization
- **Recharts 3.6.0** - Composable charting library

## 💾 Data Management

### Local Storage Architecture
The app uses **Dexie.js** (IndexedDB wrapper) for offline-first data storage:

```typescript
// Example data structure
interface MoodEntry {
  id: string;
  date: Date;
  mood: 1 | 2 | 3 | 4 | 5; // 1-5 scale
  notes: string;
  triggers: string[];
  activities: string[];
}

interface JournalEntry {
  id: string;
  date: Date;
  title: string;
  content: string;
  tags: string[];
  mood?: number;
}

interface HabitEntry {
  id: string;
  name: string;
  frequency: 'daily' | 'weekly';
  completedDates: Date[];
  streak: number;
  notes?: string;
}
```

### Data Encryption
- All sensitive data is encrypted before storage
- Uses standard encryption algorithms
- Decrypted only when needed for display/processing
- No data is ever sent to external servers

## 🔐 Security & Privacy

### Privacy First
- ✅ **100% Local Storage** - All data stays on your device
- ✅ **No Cloud Sync** - No data transmission to servers
- ✅ **Encrypted Storage** - Sensitive data is encrypted
- ✅ **Offline Capable** - Works without internet connection
- ✅ **No Tracking** - No analytics or user tracking
- ✅ **Open Source** - Code transparency and community review

### Data Safety Tips
1. Regularly backup your browser data
2. Use strong browser passwords
3. Clear sensitive data when sharing devices
4. Export data periodically for backups

## 🤖 AI Features - TheraBot

### How to Use AI Support
1. Navigate to the **Chat** section
2. Click **"Chat with TheraBot"**
3. Type your message or question
4. TheraBot responds with support, strategies, and resources

### AI Capabilities
- Emotional support and validation
- Coping strategy suggestions
- Psychoeducation on mental health
- CBT techniques and exercises
- Mood pattern analysis
- Personalized wellness suggestions

### Configuration
To enable AI features, add your Google Gemini API key:

```bash
# In .env.local
VITE_GEMINI_API_KEY=your_api_key_here
```

Get your API key from: https://ai.google.dev/

## 📱 Browser Compatibility

| Browser | Version | Support |
|---------|---------|---------|
| Chrome | 90+ | ✅ Full |
| Firefox | 88+ | ✅ Full |
| Safari | 14+ | ✅ Full |
| Edge | 90+ | ✅ Full |
| Mobile Safari (iOS) | 14+ | ✅ Full |
| Chrome Mobile | Latest | ✅ Full |

## ⚙️ Performance Optimizations

- **Code Splitting** - Lazy load components as needed
- **Bundle Optimization** - Tree-shaking unused code
- **Image Optimization** - Compressed and responsive images
- **Caching Strategy** - Service workers for offline support
- **Minimal Dependencies** - Lean bundle size (~500KB gzipped)

## 🐛 Troubleshooting

### Common Issues

**Issue: App won't start**
```bash
# Clear node_modules and reinstall
rm -rf node_modules package-lock.json
npm install
npm run dev
```

**Issue: Data not persisting**
- Check browser's IndexedDB storage (DevTools > Application)
- Ensure private/incognito mode is disabled
- Clear browser cache and try again

**Issue: AI features not working**
- Verify Gemini API key in `.env.local`
- Check API key permissions in Google Cloud Console
- Ensure API is enabled in your project

**Issue: Slow performance**
- Clear browser cache and temporary files
- Reduce number of stored entries
- Disable unnecessary animations in settings

## 📈 Analytics & Insights

The app provides built-in analytics:
- **Mood Trends** - 7, 30, 90-day patterns
- **Sleep Analytics** - Average duration and quality
- **Habit Success Rate** - Streak tracking and completion %
- **Correlation Analysis** - Link between mood and activities

## 🎓 Usage Guide

### First Time Setup
1. Create an account (local, no server required)
2. Set up mood scale preferences
3. Add 2-3 habits you want to track
4. Enable notifications (optional)
5. Explore the dashboard

### Daily Routine
1. **Morning** - Log mood and set daily intention
2. **Throughout Day** - Track habits and activities
3. **Evening** - Journal reflection and mood logging
4. **Before Bed** - Record sleep duration

### Weekly Review
1. Check mood trends
2. Review journal entries
3. Evaluate habit progress
4. Adjust goals if needed

## 🚀 Deployment

### Build for Production
```bash
npm run build
```

This creates an optimized build in the `dist/` directory.

### Deployment Options

**Static Hosting (Recommended)**
- Vercel
- Netlify
- GitHub Pages
- Firebase Hosting
- AWS S3 + CloudFront

**Example Vercel Deployment**
```bash
npm install -g vercel
vercel
```

## 🤝 Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

MIT License - See LICENSE file for details

## 🙏 Acknowledgments

- Google Gemini for AI capabilities
- React community for great libraries
- Mental health professionals for guidance
- All contributors and users

## 📞 Support & Feedback

- 📧 Email: support@mindmate.app
- 🐛 Report issues: GitHub Issues
- 💬 Discussions: GitHub Discussions
- 📱 Social: @MindMateApp

---

**Remember**: MindMate is a supportive tool, not a replacement for professional mental health care. Please reach out to qualified professionals for serious concerns.

Built with ❤️ for your mental wellness.
