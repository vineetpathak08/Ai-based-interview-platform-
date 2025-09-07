# 🎯 VinPrep - AI-Powered Interview Platform

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/vineetpathak08/Ai-based-interview-platform-)

Master Your Interview Skills with AI-Powered Practice & Real-Time Feedback

## 📋 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [Environment Setup](#-environment-setup)
- [Running the Application](#-running-the-application)
- [Deployment](#-deployment)
- [Project Structure](#-project-structure)
- [Contributing](#-contributing)
- [License](#-license)

## ✨ Features

- 🤖 **AI-Powered Interviews** - Advanced AI interviewer with real-time conversation
- 📊 **Real-Time Feedback** - Instant analysis and scoring of interview performance
- 🎯 **Multiple Interview Types** - Technical, behavioral, and role-specific interviews
- 📈 **Performance Analytics** - Detailed charts and progress tracking
- 🔐 **Secure Authentication** - Firebase-based user authentication
- 📱 **Responsive Design** - Works seamlessly on desktop and mobile
- 📄 **PDF Reports** - Download detailed interview feedback reports
- 🎨 **Modern UI** - Beautiful interface built with Tailwind CSS and shadcn/ui

## 🛠 Tech Stack

- **Frontend**: Next.js 15, React 19, TypeScript
- **Styling**: Tailwind CSS, shadcn/ui components
- **Authentication**: Firebase Auth
- **Database**: Firebase Firestore
- **AI Integration**: VAPI AI, Google AI SDK
- **Charts**: Recharts
- **PDF Generation**: jsPDF, html2canvas
- **Deployment**: Vercel

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (version 18.0.0 or higher)
- **npm** (version 8.0.0 or higher)
- **Git**

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/vineetpathak08/Ai-based-interview-platform-.git
   cd Ai-based-interview-platform-
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

## 🔧 Environment Setup

1. **Copy the environment template**
   ```bash
   cp .env.example .env.local
   ```

2. **Configure Firebase**
   
   a. Go to [Firebase Console](https://console.firebase.google.com/)
   
   b. Create a new project or select existing one
   
   c. Enable Authentication and Firestore Database
   
   d. Go to Project Settings > General > Your apps
   
   e. Add a web app and copy the configuration
   
   f. Update `.env.local` with your Firebase config:
   ```bash
   NEXT_PUBLIC_FIREBASE_API_KEY=your_api_key
   NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
   NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
   NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_project.firebasestorage.app
   NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
   NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id
   NEXT_PUBLIC_FIREBASE_MEASUREMENT_ID=your_measurement_id
   ```

3. **Set up Firebase Admin SDK**
   
   a. Go to Project Settings > Service Accounts
   
   b. Generate a new private key
   
   c. Add the service account details to `.env.local`:
   ```bash
   FIREBASE_PROJECT_ID=your_project_id
   FIREBASE_CLIENT_EMAIL=firebase-adminsdk-xxxxx@your_project.iam.gserviceaccount.com
   FIREBASE_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\nyour_private_key\n-----END PRIVATE KEY-----\n"
   ```

4. **Configure VAPI AI**
   
   a. Sign up at [VAPI.ai](https://vapi.ai/)
   
   b. Get your API token from the dashboard
   
   c. Add to `.env.local`:
   ```bash
   NEXT_PUBLIC_VAPI_WEB_TOKEN=your_vapi_token
   ```

## 🏃‍♂️ Running the Application

1. **Development mode**
   ```bash
   npm run dev
   ```
   Open [http://localhost:3000](http://localhost:3000) in your browser.

2. **Development mode with Turbopack (faster)**
   ```bash
   npm run dev:turbo
   ```

3. **Production build**
   ```bash
   npm run build
   npm start
   ```

4. **Lint the code**
   ```bash
   npm run lint
   ```

## 🌐 Deployment

### Deploy to Vercel (Recommended)

1. **One-click deployment**
   
   Click the "Deploy with Vercel" button at the top of this README.

2. **Manual deployment**
   
   a. Install Vercel CLI:
   ```bash
   npm i -g vercel
   ```
   
   b. Deploy:
   ```bash
   vercel
   ```
   
   c. Follow the prompts and add your environment variables in the Vercel dashboard.

### Deploy to Other Platforms

The app can also be deployed to:
- Netlify
- Railway
- Heroku
- AWS Amplify

Make sure to set the environment variables on your chosen platform.

## 📁 Project Structure

```
vinPrep/
├── app/                          # Next.js app directory
│   ├── (auth)/                   # Authentication pages
│   │   ├── sign-in/
│   │   └── sign-up/
│   ├── (root)/                   # Main application pages
│   │   ├── interview/            # Interview pages
│   │   └── page.tsx              # Dashboard
│   ├── api/                      # API routes
│   │   ├── feedback/
│   │   ├── interviews/
│   │   └── vapi/
│   ├── globals.css               # Global styles
│   └── layout.tsx                # Root layout
├── components/                   # React components
│   ├── ui/                       # shadcn/ui components
│   ├── Agent.tsx                 # AI interview agent
│   ├── Dashboard.tsx             # Main dashboard
│   └── ...
├── constants/                    # Application constants
├── firebase/                     # Firebase configuration
├── lib/                          # Utility libraries
│   ├── actions/                  # Server actions
│   └── utils/
├── types/                        # TypeScript type definitions
├── public/                       # Static assets
└── scripts/                      # Utility scripts
```

## 🔥 Key Features Setup

### Firebase Firestore Collections

The app uses the following Firestore collections:

1. **users** - User profiles and settings
2. **userStats** - Interview statistics and performance data
3. **interviews** - Interview sessions and records

### Authentication Flow

- Sign up/Sign in with email and password
- Protected routes using Firebase Auth
- Persistent sessions

### AI Interview Flow

1. User selects interview type and difficulty
2. VAPI AI conducts the interview
3. Real-time feedback and scoring
4. PDF report generation

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add some amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

## 🐛 Troubleshooting

### Common Issues

1. **Build errors**: Make sure all environment variables are set correctly
2. **Firebase connection issues**: Verify your Firebase configuration
3. **VAPI AI not working**: Check your VAPI token and permissions
4. **Styling issues**: Clear your browser cache and restart the dev server

### Getting Help

- Open an issue on GitHub
- Check the [Next.js documentation](https://nextjs.org/docs)
- Review [Firebase documentation](https://firebase.google.com/docs)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) for the amazing React framework
- [Firebase](https://firebase.google.com/) for authentication and database
- [VAPI.ai](https://vapi.ai/) for AI conversation capabilities
- [shadcn/ui](https://ui.shadcn.com/) for beautiful UI components
- [Vercel](https://vercel.com/) for hosting and deployment

---

Made with ❤️ by [Vineet Pathak](https://github.com/vineetpathak08)

For questions or support, please open an issue or contact [your-email@domain.com](mailto:your-email@domain.com)
