# Rangoli Utsav 🪔
### A Diwali Special Rangoli Inspiration & Community Platform

**Rangoli Utsav** is a festive, cultural web platform dedicated to traditional and contemporary Indian Rangoli art, sacred geometry, and Diwali celebrations.

---
<img width="1534" height="729" alt="image" src="https://github.com/user-attachments/assets/641114d3-fbaf-4cda-beba-8d451e9d7caa" />

## 🌟 Key Features

1. **Diwali-Themed Hero & Ambience**:
   - Cultural visual anchor with authentic high-resolution photography.
   - Live interactive glowing Diya counter.
   - Quick stats and 4-column KPI strip.

2. **Curated Rangoli Gallery**:
   - 52+ authentic curated designs across all 8 cultural categories:
     - Traditional Rangoli (Sanskar Bharati, Chowk Purna, Alpana, Aipan, Mandana)
     - Floral Rangoli (South Indian Pookkalam, Lotus Mandap, Floating Brass Urli)
     - Peacock Rangoli (Royal Mayur, Dancing Birds, Plumed Plumes)
     - Mandala Rangoli (Sacred Sri Yantra, Surya Prakash, 16-petal Chakras)
     - Diwali Special Rangoli (Shubh Labh, Lakshmi Charan Paduka, Pancha Diya)
     - Easy Rangoli (5x5 Dot Pulli Kolam, Spoon & Bangle beginner tricks)
     - Modern Rangoli (Pastel Ombre, 3D Optical Cubes, Minimalist silhouettes)
     - Festival Rangoli (Ganeshotsav, Pongal Pots, Navratri Garba, Makar Sankranti)
   - Real-time search, difficulty filters, sorting, and like counts.

3. **Interactive Rangoli Maker Studio**:
   - HTML5 Canvas drawing with real-time radial symmetry (4-fold, 6-fold, 8-fold, 12-fold, mirror, and freehand).
   - Authentic Gulal powder colors (Gulal Pink, Marigold Orange, Turmeric Yellow, Peacock Blue, Leaf Green, Deep Plum, Chalk White).
   - Pulli Kolam dot grid overlay toggle.
   - Eraser mode, Undo/Redo stack, and canvas reset.
   - PNG download and direct 1-click submission to the Community Gallery.

4. **Community Rangoli Gallery & Upload Workflow**:
   - Registered users can upload handmade Rangoli photographs (JPG, PNG, WebP up to 5MB).
   - Client-side size & MIME validation with real-time preview and simulated upload progress.
   - Strict moderation workflow: submissions enter `PENDING` status. Only `APPROVED` designs appear in the public gallery.

5. **Protected Admin Moderation Console**:
   - Access-controlled moderator dashboard.
   - KPI metrics: Pending reviews, approved works, rejected submissions, total likes, and flagged reports.
   - 1-click Approve (with celebratory confetti), Reject with reason note, and Feature toggle.
   - Flagged content and report resolution.

6. **User Authentication & Profile**:
   - Sign in, registration, forgot password flow.
   - 1-click Demo Profiles (`Admin Demo` and `Artist Demo`) for instant testing.
   - "My Uploads" hub allowing users to view status (Pending, Approved, Rejected with admin notes), edit details, and delete submissions.

7. **Step-by-Step Tutorials**:
   - Masterclasses for beginners and advanced artists with materials checklist, estimated time, and numbered instructions.

8. **Diwali Light Celebration & Greeting Generator**:
   - Interactive Diya lighting that adds to global count.
   - Personalized festive greeting card generator with customizable recipient, sender, and blessing quotes with 1-click copy to clipboard.

---

## 🛠️ Technology Stack

- **Frontend**: React 19, TypeScript, Tailwind CSS v4, Lucide Icons, Canvas Confetti.
- **Backend / Database**: Supabase PostgreSQL with Row Level Security (RLS) & Supabase Storage.
- **Local Fallback Engine**: Built-in persistent browser engine that allows complete local offline exploration and instant review even before configuring external credentials.

---

## 🗄️ Supabase Database Architecture

The full PostgreSQL migration file is located at:
`supabase/migrations/001_initial_schema.sql`

It provisions:
- `profiles` table
- `rangoli_designs` table
- `rangoli_likes` table (with unique constraint per user/design)
- `rangoli_reports` table
- `tutorials` table
- Automatic like count trigger & user registration trigger
- Row Level Security (RLS) policies enforcing user boundaries and admin access
- Storage bucket `rangoli-photos` configuration

---

## 🚀 Deployment Instructions

### Deploy to Vercel

1. Push this repository to GitHub or GitLab.
2. Import the project into [Vercel](https://vercel.com).
3. The included `vercel.json` automatically configures SPA routing rewrites.
4. (Optional) In the Vercel project settings, add the environment variables:
   ```env
   VITE_SUPABASE_URL="https://your-project.supabase.co"
   VITE_SUPABASE_ANON_KEY="your-anon-public-key"
   ```
5. Click **Deploy**. The site works seamlessly both with and without Supabase configured!
"# rangoli-utsav" 
