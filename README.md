# Coretech-Website-Chatbot-

CoreTech Innovations - Chatbot WebsiteProject OverviewA professional React-based website for CoreTech Innovations featuring an intelligent FAQ chatbot, service showcase, and contact information.Technology Stack•Frontend: React 19 + TypeScript•Styling: Tailwind CSS 4 + shadcn/ui components•Routing: Wouter (client-side)•Build Tool: Vite•Package Manager: pnpmProject Structure

coretech_website/
├── client/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Chatbot.tsx          # Interactive chatbot component
│   │   │   └── ui/                  # shadcn/ui components
│   │   ├── lib/
│   │   │   └── faqData.ts           # FAQ data + keyword matching logic
│   │   ├── pages/
│   │   │   └── Home.tsx             # Main landing page
│   │   ├── App.tsx                  # Main app router
│   │   ├── index.css                # Global styles with design tokens
│   │   └── main.tsx                 # React entry point
│   ├── public/                      # Static assets
│   └── index.html                   # HTML template
├── server/
│   └── index.ts                     # Express server (static serving)
├── package.json
├── tsconfig.json
└── vite.config.ts


Key Features1. Intelligent Chatbot•Keyword Matching Engine: Matches user questions against 30+ FAQ entries•Stop Word Filtering: Removes common words for better matching accuracy•Multi-word Keyword Support: Handles phrases like "digital marketing"•Natural Responses: Greetings, help commands, and fallback messages


2. Modern Design•Color Scheme: Deep navy (#1a1f3a) with bright cyan (#00d4ff) accents•Typography: Poppins Bold for headlines, Inter Regular for body text•Responsive Layout: Mobile-first design with smooth animations•Professional UI: Gradient backgrounds, shadow effects, and smooth transitions3. Content Sections•Hero Section: Compelling brand messaging•Statistics: 320+ projects, 180+ experts, 94% retention rate, 12 time zones•Services: 6 core service offerings with icons•Chatbot: Interactive FAQ assistant•Contact: Phone, email, and location information


Setup InstructionsPrerequisites•Node.js 18+ (or use pnpm directly)•pnpm package managerInstallationCopy# Extract the ZIP file
unzip coretech_website_source.zip
cd coretech_website

# Install dependencies
pnpm install

# Start development server
pnpm dev

# Build for production
pnpm build

# Preview production build
pnpm preview


Development ServerThe app runs on http://localhost:3000 by default.Chatbot LogicKeyword Matching Algorithm1.Input Normalization: Convert user input to lowercase, remove punctuation2.Stop Word Filtering: Remove common words (what, does, is, etc.)3.Keyword Comparison:•Multi-word keywords: Check against cleaned input string (score +2)•Single-word keywords: Check against meaningful words (score +1)4.Best Match: Return FAQ entry with highest score (minimum 1)


Example Queries•"What services do you offer?" → Matches "services" keyword•"Internship programs" → Matches "internship" keyword•"How can I contact CoreTech?" → Matches "contact" keyword•"Tell me about ERP" → Matches "erp" keywordFAQ DataThe chatbot is powered by 30 FAQ entries covering:•Company information (founding, location, mission)•Services (web, mobile, ERP, UI/UX, marketing, cybersecurity)•Team and leadership•Internship programs•Contact information•Client success metrics


Design Philosophy: Modern Tech Minimalism•Clean geometric forms with purposeful whitespace•Hierarchy through scale and weight, not color•Functional elegance with subtle motion•Information density balanced with breathing roomCustomizationAdding New FAQ EntriesEdit client/src/lib/faqData.ts:


{
  question: "Your question here?",
  keywords: ["keyword1", "keyword2", "multi word keyword"],
  answer: "Your answer here"
}


Changing ColorsEdit client/src/index.css and update CSS variables:--primary: #1a1f3a;
--accent: #00d4ff;Modifying ServicesEdit client/src/pages/Home.tsx in the services array.Performance•Build Size: ~580 KB (JavaScript) + ~120 KB (CSS)•Gzip Size: ~171 KB (JS) + ~18 KB (CSS)•Load Time: < 2 seconds on average connectionBrowser Support•Chrome/Edge 90+•Firefox 88+•Safari 14+

•Mobile browsers (iOS Safari 14+, Chrome Android 90+)DeploymentThe project is ready for deployment on any static hosting platform:•Manus WebDev (included)•Vercel•Netlify•AWS S3 + CloudFront•Any Node.js hostingFuture Enhancements1.Add suggested question buttons for quick replies2.Implement conversation history with local storage3.Add user feedback system (thumbs up/down)4.Integrate with backend for dynamic FAQ updates5.Add analytics to track popular questions6.Multi-language supportLicenseMITAuthorBuilt for CoreTech Innovations Internship ProjectWebsite URL: https://coretechweb-jsbwvqsu.manus.space
Live Demo: Available at the URL above

Screen Shots 
Screenshot_20260611_235337_Chrome.jpg
Screenshot_20260611_235344_Chrome.jpg
