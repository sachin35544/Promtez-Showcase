# ✨ Promtez

**Discover, share, and reuse AI prompts.** Promtez is a mobile-first community platform where creators can explore image-based prompts, publish their own work, and connect with other AI enthusiasts.

🚀 **Live Demo:** [promtez.vercel.app](https://promtez.vercel.app/)

<p>
  <img src="https://img.shields.io/badge/Next.js-16.2.6-black?logo=next.js" alt="Next.js" />
  <img src="https://img.shields.io/badge/React-19.2.4-149ECA?logo=react" alt="React" />
  <img src="https://img.shields.io/badge/Firebase-Auth%20%2B%20Firestore-FFCA28?logo=firebase" alt="Firebase" />
  <img src="https://img.shields.io/badge/Tailwind%20CSS-4-06B6D4?logo=tailwindcss" alt="Tailwind CSS" />
</p>

## 🚀 Features

- **Explore & search** — Browse a paginated prompt feed with infinite scrolling and search.
- **Publish prompts** — Upload generated images through Cloudinary and save prompt details in Firestore.
- **Like & share** — Like prompts, view your liked posts, copy prompt text, and share posts.
- **Creator profiles** — View profiles, edit your details, and manage your own prompts.
- **Post management** — Edit or delete your posts and open shareable prompt pages.
- **Community safety** — Report inappropriate prompts and profiles.
- **Responsive experience** — Mobile-first interface with fullscreen image viewing.

## 🧰 Tech Stack

| Frontend | Backend & Services | Tools |
| --- | --- | --- |
| Next.js 16 · React 19 · JavaScript · TypeScript · Tailwind CSS 4 | Firebase Authentication · Cloud Firestore · Cloudinary | ESLint 9 · npm · Web Share API · Clipboard API |

## ⚙️ Run Locally

```bash
# Clone the repository
 git clone <your-repository-url>
 cd promtez

# Install dependencies
 npm install

# Start the development server
 npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

Before running the app, configure your Firebase project in `lib/firebase.js` and set up your Cloudinary cloud name and unsigned upload preset in the upload configuration. Use the configuration values expected by your project.

## 📁 Project Structure

```text
promtez/
├── app/           # App Router pages and routes
├── components/    # Reusable UI components (PostCard)
├── lib/           # Firebase initialization
└── public/        # Static assets
```

## 🔐 Authentication & Data

Promtez uses Google sign-in through Firebase Authentication. Prompt and report data is stored in Cloud Firestore, while uploaded images are delivered through Cloudinary.

---

<p align="center">Built for the AI creator community 💜</p>
