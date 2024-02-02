# AI-Powered LMS Platform

A cutting-edge Learning Management System built with Next.js 15, Sanity CMS, Clerk Authentication, and Stripe Payments. This platform combines modern web technologies with AI capabilities through LangChain, LangGraph, and IBM Watson Tools integration via Convex backend.

**Repository**: [ai-agent-langchain-langgraph-convex-clerk-ibm-wxtools-nextjs15](https://github.com/tarak6984/ai-agent-langchain-langgraph-convex-clerk-ibm-wxtools-nextjs15)

## Features

### For Students

- 📚 Access to comprehensive course content
- 📊 Real-time progress tracking
- ✅ Lesson completion system
- 🎯 Module-based learning paths
- 🎥 Multiple video player integrations (YouTube, Vimeo, Loom)
- 💳 Secure course purchases
- 📱 Mobile-friendly learning experience
- 🔄 Course progress synchronization

### For Course Creators

- 📝 Rich content management with Sanity CMS
- 📊 Student progress monitoring
- 📈 Course analytics
- 🎨 Customizable course structure
- 📹 Multiple video hosting options
- 💰 Direct payments via Stripe
- 🔄 Real-time content updates
- 📱 Mobile-optimized content delivery

### Technical Features

- 🚀 Server Components & Server Actions
- 👤 Authentication with Clerk
- 💳 Payment processing with Stripe
- 📝 Content management with Sanity CMS
- 🎨 Modern UI with Tailwind CSS and shadcn/ui
- 📱 Responsive design
- 🔄 Real-time content updates
- 🔒 Protected routes and content
- 🌙 Dark mode support

### UI/UX Features

- 🎯 Modern, clean interface
- 🎨 Consistent design system using shadcn/ui
- ♿ Accessible components
- 🎭 Smooth transitions and animations
- 📱 Responsive across all devices
- 🔄 Loading states with skeleton loaders
- 💫 Micro-interactions for better engagement
- 🌙 Dark/Light mode toggle

## Getting Started

### Prerequisites

- Node.js 18+
- npm/yarn
- Stripe Account
- Clerk Account
- Sanity Account

### Environment Variables

Create a `.env.local` file with:

```bash
# Sanity
NEXT_PUBLIC_SANITY_PROJECT_ID=your-project-id
NEXT_PUBLIC_SANITY_DATASET=production
# Read Token
SANITY_API_TOKEN=your-sanity-read-token
# Full Access Admin Token
SANITY_API_ADMIN_TOKEN=your-sanity-admin-token

# For Sanity Studio to read
SANITY_STUDIO_PROJECT_ID=your-project-id
SANITY_STUDIO_DATASET=production

# Next.js
NEXT_PUBLIC_BASE_URL=http://localhost:3000

# Stripe
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=your-stripe-publishable-key
STRIPE_SECRET_KEY=your-stripe-secret-key
STRIPE_WEBHOOK_SECRET=your-stripe-webhook-secret

# Clerk
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your-clerk-publishable-key
CLERK_SECRET_KEY=your-clerk-secret-key
```

### Installation

```bash
# Clone the repository
git clone https://github.com/tarak6984/ai-agent-langchain-langgraph-convex-clerk-ibm-wxtools-nextjs15.git

# Navigate to the project directory
cd ai-agent-langchain-langgraph-convex-clerk-ibm-wxtools-nextjs15

# Install dependencies
pnpm install

# Start the development server
pnpm dev

# Access the application at http://localhost:3000
# Access Sanity Studio at http://localhost:3000/studio
```

### Setting up Sanity CMS

1. Create a Sanity account
2. Create a new project
3. Install the Sanity CLI:
   ```bash
   npm install -g @sanity/cli
   ```
4. Initialize Sanity in your project:
   ```bash
   sanity init
   ```
5. Deploy Sanity Studio:
   ```bash
   sanity deploy
   ```

### Setting up Clerk

1. Create a Clerk application
2. Configure authentication providers
3. Set up redirect URLs
4. Add environment variables

### Setting up Stripe

1. Create a Stripe account
2. Set up webhook endpoints
3. Configure payment settings
4. Set up webhook forwarding for local development:
   ```bash
   stripe listen --forward-to localhost:3000/api/stripe-checkout/webhook
   ```

## Architecture

### Content Schema

- Courses

  - Title
  - Description
  - Price
  - Image
  - Modules
  - Instructor
  - Category

- Modules

  - Title
  - Lessons
  - Order

- Lessons

  - Title
  - Description
  - Video URL
  - Content (Rich Text)
  - Completion Status

- Students

  - Profile Information
  - Enrolled Courses
  - Progress Data

- Instructors
  - Name
  - Bio
  - Photo
  - Courses

### Key Components

- Course Management System

  - Content creation and organization
  - Module and lesson structuring
  - Rich text editing
  - Media integration

- Progress Tracking

  - Lesson completion
  - Course progress calculation
  - Module progress visualization

- Payment Processing

  - Secure checkout
  - Course enrollment
  - Stripe integration

- User Authentication
  - Clerk authentication
  - Protected routes
  - User roles

## Usage

### Creating a Course

1. Access Sanity Studio
2. Create course structure with modules and lessons
3. Add content and media
4. Publish course

### Student Experience

1. Browse available courses
2. Purchase and enroll in courses
3. Access course content
4. Track progress through modules
5. Mark lessons as complete
6. View completion certificates

## Development

### Key Files and Directories

```
/app                    # Next.js app directory
  /(dashboard)          # Dashboard routes
  /(user)              # User routes
  /api                 # API routes
/components            # React components
/sanity                # Sanity configuration
  /lib                 # Sanity utility functions
  /schemas             # Content schemas
/lib                   # Utility functions
```

### Core Technologies

- Next.js 15
- TypeScript
- Sanity CMS
- Stripe Payments
- Clerk Auth
- Tailwind CSS
- Shadcn UI
- Lucide Icons

## Features in Detail

### Course Management

- Flexible course structure with modules and lessons
- Rich text editor for lesson content
- Support for multiple video providers
- Course pricing and enrollment management

### Student Dashboard

- Progress tracking across all enrolled courses
- Lesson completion status
- Continue where you left off
- Course navigation with sidebar

### Video Integration

- URL Video Player
- Loom Embed Support
- Responsive video playback

### Payment System

- Secure Stripe checkout
- Course access management
- Webhook integration
- Payment status tracking

### Authentication

- User registration and login
- Protected course content
- Role-based access control
- Secure session management

### UI Components

- Modern, responsive design
- Loading states and animations
- Progress indicators
- Toast notifications
- Modal dialogs

## Future Enhancements

### Planned AI Integration Features:

- 🤖 **LangChain Integration**: Natural language processing for course content
- 🔄 **LangGraph Workflows**: Automated learning path generation
- 💾 **Convex Backend**: Real-time data synchronization and state management
- 🧠 **IBM Watson Tools**: Advanced analytics and intelligent recommendations
- 📊 **AI-Powered Analytics**: Student performance insights and predictions
- 💬 **Smart Chatbot**: AI assistant for student queries
- 🎯 **Personalized Learning**: Adaptive course recommendations

These features are planned for future development to create an intelligent, adaptive learning platform.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

**Tarak** - [GitHub Profile](https://github.com/tarak6984)

## Acknowledgments

- Built with Next.js 15, Sanity CMS, Clerk, and Stripe
- UI Components from shadcn/ui
- Icons from Lucide React

---

⭐ Star this repository if you find it helpful!
