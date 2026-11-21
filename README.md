# ✨ Promtez

<p align="left">
  <a href="https://promtez.vercel.app/"><strong>🚀 Live Demo</strong></a>
</p>

**A community-driven hub to discover, share, and reuse AI prompts.** Promtez is a mobile-first platform where AI creators can explore image-based prompts, publish their own creations, and connect with other prompt enthusiasts.

<p>
  <img src="https://img.shields.io/badge/Next.js-16.2.6-black?logo=next.js" alt="Next.js" />
  <img src="https://img.shields.io/badge/React-19.2.4-149ECA?logo=react" alt="React" />
  <img src="https://img.shields.io/badge/Firebase-Auth%20%2B%20Firestore-FFCA28?logo=firebase" alt="Firebase" />
  <img src="https://img.shields.io/badge/Tailwind%20CSS-4-06B6D4?logo=tailwindcss" alt="Tailwind CSS" />
</p>

## ✨ Features

- **Discover prompts** — Paginated feed, live search across loaded posts, and infinite scrolling.
- **Publish creations** — Upload images with Cloudinary and store prompt metadata in Firestore.
- **Engage & share** — Like posts, browse liked prompts, copy prompt text, and share direct links.
- **Creator profiles** — View creators, update profile details, and manage your own posts.
- **Community moderation** — Report inappropriate posts and profiles.
- **Responsive UI** — Mobile-first layout, fullscreen image viewer, and reusable prompt cards.

## 🖼️ Screenshots

Add real app captures to a `screenshots/` folder using the filenames below. The image slots are ready to enable once the screenshots are added.

<!-- Uncomment these when the matching screenshot files are added.
<p align="center">
  <img src="./screenshots/home-feed.png" alt="Promtez home feed" width="260" />
  <img src="./screenshots/prompt-detail.png" alt="Promtez prompt detail" width="260" />
  <img src="./screenshots/create-post.png" alt="Promtez create post" width="260" />
</p>
-->

| Home Feed | Prompt Detail | Create Post |
| --- | --- | --- |
| `screenshots/home-feed.png` | `screenshots/prompt-detail.png` | `screenshots/create-post.png` |

## ⚙️ Tech Stack

| Frontend | Backend & Storage | Browser APIs & Tooling |
| --- | --- | --- |
| Next.js 16 · React 19 · JavaScript · TypeScript · Tailwind CSS 4 | Firebase Authentication · Cloud Firestore · Cloudinary | Web Share API · Clipboard API · IntersectionObserver · ESLint 9 |

## 🏗️ Architecture & Engineering Highlights

- **Cursor-based pagination** — Firestore `orderBy`, `limit(10)`, and `startAfter` load the feed in small batches; `IntersectionObserver` triggers the next page with a manual fallback.
- **Two-service publishing pipeline** — Images upload directly from the client to Cloudinary; the returned secure URL and prompt metadata are then saved in Firestore.
- **Optimistic interactions** — Like state updates immediately in the UI, with Firestore `arrayUnion` and `arrayRemove` persisting the change.
- **Reusable interaction layer** — A shared `PostCard` component centralizes copy, share, like, report, fullscreen viewing, and owner actions across feed surfaces.
- **Profile synchronization** — Creator name changes update the Firebase Auth profile and existing prompt documents through a Firestore batch.
- **Authenticated workflows** — Firebase Authentication tracks the signed-in user and gates publishing, liking, and profile-management actions. Firestore Security Rules should independently enforce data ownership and access permissions at the database layer.

## 🔒 Source Code Access

This is a **project showcase repository**. The application source code is not included here. Recruiters and hiring teams can request read-only code access or a technical walkthrough.

## 👤 Author & Contact

**Sachin Kumawat**  
Email: `your.email@example.com` · GitHub: `https://github.com/your-username`

---

<p align="center">Built for the AI creator community 💜</p>
