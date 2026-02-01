# 🦷 Smile Up Clinic Website

A modern, fast, and easy-to-maintain dental clinic website built with **Astro** and **Decap CMS**.

![Smile Up Clinic](public/images/logo.png)

## ✨ Features

- **Fast & Modern**: Built with Astro for blazing-fast performance
- **Easy Content Management**: Decap CMS for visual editing (no coding required)
- **Responsive Design**: Looks great on all devices
- **Contact Form**: Built-in form with email notifications
- **SEO Optimized**: Meta tags, Open Graph, and semantic HTML
- **Free Hosting**: Deploy to Netlify for $0/month

## 📁 Project Structure

```
dental-clinic/
├── public/
│   ├── admin/           # Decap CMS admin panel
│   │   ├── index.html
│   │   └── config.yml
│   └── images/          # Static images
│       └── logo.png
├── src/
│   ├── components/      # Reusable components
│   │   ├── Header.astro
│   │   └── Footer.astro
│   ├── content/         # CMS-managed content
│   │   ├── services/
│   │   ├── team/
│   │   ├── testimonials/
│   │   └── settings/
│   ├── layouts/
│   │   └── Layout.astro
│   ├── pages/           # Site pages
│   │   ├── index.astro
│   │   ├── services.astro
│   │   ├── about.astro
│   │   └── contact.astro
│   └── styles/
│       └── global.css
├── astro.config.mjs
├── netlify.toml
└── package.json
```

## 🚀 Deployment Guide (Step by Step)

### Step 1: Create a GitHub Account (if you don't have one)

1. Go to [github.com](https://github.com)
2. Click "Sign up" and create a free account

### Step 2: Upload Code to GitHub

1. Go to [github.com/new](https://github.com/new)
2. Name your repository: `smile-up-clinic`
3. Keep it **Public** (required for free Netlify)
4. Click "Create repository"
5. Upload all the files from this project

**Or use Git command line:**
```bash
cd dental-clinic
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/smile-up-clinic.git
git push -u origin main
```

### Step 3: Deploy to Netlify

1. Go to [netlify.com](https://netlify.com) and sign up (free)
2. Click "Add new site" → "Import an existing project"
3. Choose "GitHub" and authorize Netlify
4. Select your `smile-up-clinic` repository
5. Build settings should auto-detect:
   - **Build command**: `npm run build`
   - **Publish directory**: `dist`
6. Click "Deploy site"

🎉 Your site will be live in ~2 minutes at a URL like `random-name.netlify.app`

### Step 4: Set Up Custom Domain (Optional)

1. In Netlify, go to **Site settings** → **Domain management**
2. Click "Add custom domain"
3. Enter your domain (e.g., `smileupclinic.com`)
4. Follow DNS instructions to point your domain to Netlify

### Step 5: Enable Decap CMS (Content Editor)

1. In Netlify, go to **Site settings** → **Identity**
2. Click "Enable Identity"
3. Under "Registration preferences", select "Invite only"
4. Under "External providers", add "Google" (optional, for easy login)
5. Go to **Services** → **Git Gateway** → "Enable Git Gateway"
6. Go to **Identity** → "Invite users" → Add your email
7. Check your email and accept the invitation

### Step 6: Enable Contact Form Emails

1. In Netlify, go to **Forms**
2. Your contact form should appear automatically
3. Click on it → **Settings** → "Form notifications"
4. Add your email to receive form submissions

---

## 📝 How to Edit Content (For the Dentist)

### Accessing the Admin Panel

1. Go to `https://your-site.netlify.app/admin`
2. Click "Login with Netlify Identity"
3. Sign in with your email/password or Google

### What You Can Edit

| Section | Location in CMS |
|---------|-----------------|
| Services | Services → Add/Edit |
| Team Members | Team Members → Add/Edit |
| Testimonials | Testimonials → Add/Edit |
| Office Hours | Site Settings → General |
| Contact Info | Site Settings → General |
| Blog Posts | Blog Posts → Add/Edit |

### Adding a New Team Member

1. Go to **Team Members** → **New Team Member**
2. Fill in:
   - Name: Dr. John Smith
   - Role: General Dentist
   - Bio: Brief description
   - Photo: Upload image
   - Specialties: Add each specialty
3. Click **Publish**

### Adding a New Service

1. Go to **Services** → **New Service**
2. Fill in:
   - Title: Teeth Cleaning
   - Icon: 🦷 (use emoji)
   - Description: Brief description
   - Price: From $99
   - Features: Add list items
3. Click **Publish**

---

## 🔧 Local Development

If you want to make code changes:

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

### Running CMS Locally

```bash
# Install Decap CMS proxy
npx decap-server

# In another terminal, run the site
npm run dev

# Access CMS at http://localhost:4321/admin
```

---

## 🎨 Customization

### Changing Colors

Edit `src/styles/global.css` and update the CSS variables:

```css
:root {
  --color-primary: #20B2AA;      /* Main brand color */
  --color-primary-dark: #1a9690; /* Darker shade */
  --color-secondary: #0d4f4a;    /* Secondary color */
}
```

### Changing Fonts

The site uses **Poppins** from Google Fonts. To change:

1. Go to [fonts.google.com](https://fonts.google.com)
2. Select a font and copy the `@import` URL
3. Replace in `src/styles/global.css`

---

## 📧 Contact Form Setup

The contact form uses Netlify Forms (free). Submissions are:

1. Stored in Netlify dashboard (Forms section)
2. Emailed to you (if notifications are set up)

To change form fields, edit `src/pages/contact.astro`.

---

## 🆘 Troubleshooting

### CMS won't load
- Make sure Git Gateway is enabled in Netlify
- Clear browser cache and try again

### Form submissions not working
- Check that `data-netlify="true"` is on the form
- Verify the form name matches in the hidden input

### Site not updating after changes
- Netlify auto-deploys on Git push
- Check the Deploys tab for errors

---

## 📄 License

This project is created for Smile Up Clinic. Feel free to customize for your needs.

---

## 🙏 Support

Need help? Contact the developer or check:
- [Astro Documentation](https://docs.astro.build)
- [Decap CMS Documentation](https://decapcms.org/docs)
- [Netlify Documentation](https://docs.netlify.com)
