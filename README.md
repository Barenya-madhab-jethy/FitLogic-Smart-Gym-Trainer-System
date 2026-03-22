FitLogic - Smart Gym Trainer System 🏋️‍♂️💪


FitLogic is an intelligent web-based fitness application that acts as your personal gym trainer. It uses an AI-driven decision engine to analyze performance, prevent overtraining, balance muscle groups, and generate adaptive workouts in real-time. Works 100% offline with browser SQLite persistence.

✨ Key Features
Smart Decision Engine (js/rule-engine.js): Detects overtraining, workout imbalances, plateaus, and suggests optimal adjustments.
AI Chatbot (js/chatbot.js): 24/7 fitness assistant powered by DeepSeek API (api/deepseek-chat.php).
Progressive Workouts (js/workout-generator.js): Personalized plans based on sleep, stress, recovery, and goals.
Recovery Tracking: Monitors fatigue patterns and recommends deloads/active recovery.
SQLite Database (js/sql-db.js): Offline-first storage for workouts, history, settings with localStorage migration.
Performance Analytics (js/charts.js, js/fitness-score.js): Visual progress tracking and fitness scoring.
PWA Support (sw.js): Full offline capability, installable app.
Responsive Design: Mobile-first UI with dark theme, animations (css/animations.css).
Indian Nutrition Integration (nutrition.html).
Injury Mode (injury-mode.html): Safe progression post-injury (40% → 55% → 70% intensity).
🛠️ Tech Stack
Category	Technologies
Frontend	HTML5, Vanilla JS (ES modules), Bootstrap 5, Chart.js, Font Awesome
Database	sql.js (SQLite in browser), localStorage fallback
Build/Tools	ESLint (linting), Service Worker (PWA)
Backend	PHP (chat API only), fully client-side otherwise
Other	Responsive CSS Grid/Flexbox, CSS animations
No Node.js server required - Pure static site!

📁 File Structure
fitlogic/
├── index.html              # Landing page & demo
├── login.html              # Authentication
├── dashboard.html          # Main app dashboard
├── workout.html            # Workout generator
├── history.html            # Workout history (SQLite)
├── nutrition.html          # Nutrition tracker
├── settings.html           # User settings
├── injury-mode.html        # Injury recovery mode
├── api/
│   └── deepseek-chat.php   # AI Chatbot API
├── css/
│   ├── style.css
│   ├── auth.css
│   ├── responsive.css
│   └── animations.css
├── js/
│   ├── main.js             # Core app logic
│   ├── rule-engine.js      # Decision making core
│   ├── workout-generator.js
│   ├── sql-db.js           # SQLite database
│   ├── sql-db-fixed.js
│   ├── charts.js
│   ├── chatbot.js
│   ├── fitness-score.js
│   ├── offline-sync.js
│   └── functions.js
├── assets/images/          # Screenshots & icons
├── sw.js                   # Service Worker
├── package.json            # ESLint config
├── TODO.md                 # Current tasks
└── TODO_SQLite.md          # DB implementation notes
🚀 Quick Start
Live Demo: Open index.html in any modern browser (Chrome/Firefox recommended).
Development Server (optional):
npx serve .
Install as PWA: Click install icon in browser address bar.
Offline Mode: Fully functional without internet (except chatbot).
No installation required - Zero dependencies for runtime!

🧪 Development & Testing
# Lint code
npx eslint js/

# Auto-fix lint issues
npx eslint js/ --fix

# Check PWA compliance
npx lighthouse . --view
Current Status
See TODO.md for ongoing cleanup (ESLint fixes, console.log removal). SQLite implementation complete: TODO_SQLite.md.

📱 Screenshots
Dashboard	Decision Engine	Workout Generator
Dashboard	Decision Engine	Workout
🤖 Smart Features Demo
Real Workout Decision Logic (from js/rule-engine.js):

IF sleep < 5h → reduce intensity 30%, increase rest 20%
IF chest > 3 sessions → lock chest 48h, suggest back/mobility
IF performance drop → active recovery + deload week
Try the live demo on index.html#demo.

📋 Database Schema (SQLite)
Table	Purpose
users	User profiles & goals
workouts	Completed sessions
user_settings	Equipment, preferences
meal_logs	Nutrition tracking
fitness_scores	Performance metrics
Auto-migrates from localStorage on first load.

🔗 Pages Overview
dashboard.html: Main hub with charts & fitness score
workout.html: Generate & log workouts
history.html: Past workouts (paginated)
nutrition.html: Meal planning
settings.html: Customize app
feedback.html: User feedback
injury-mode.html: Post-injury protocols
🤝 Contributing
Fork the repo
Run npx eslint js/ --fix
Create feature branch
Test offline functionality
Submit PR
📄 License
MIT License - Use freely for personal/commercial projects.

🙌 Support
Issues: Create GitHub issue
Chatbot: Built-in AI assistant
Demo: Live Preview
Built with ❤️ for fitness enthusiasts. Train smart, not hard! 💪

Status: Production-ready • Offline-first • PWA-compliant
