# How to get your site live — step by step

This guide takes you from the folder of files you have now to a live website, free, with a blog you can update from your browser. No coding required after this setup.

The process takes about 20 minutes.

---

## What you need

- A free GitHub account — sign up at github.com
- A free Netlify account — sign up at netlify.com (you can use your GitHub login)

---

## Step 1: Upload the files to GitHub

1. Go to **github.com** and sign in.
2. Click the **+** button in the top right, then **New repository**.
3. Name it something like `matt-weston-site`. Leave everything else as default.
4. Click **Create repository**.
5. On the next page, look for the option that says **"uploading an existing file"** and click it.
6. Drag and drop the entire `matt-weston-site` folder contents into the upload area. Make sure to include all subfolders (admin, data, images).
7. Click **Commit changes**.

---

## Step 2: Deploy on Netlify

1. Go to **app.netlify.com** and sign in with your GitHub account.
2. Click **Add new site** → **Import an existing project**.
3. Choose **GitHub** and authorise Netlify to access your repos.
4. Select the `matt-weston-site` repository.
5. Leave all build settings as they are (Netlify will detect them automatically).
6. Click **Deploy site**.

Your site will be live in about 60 seconds at a random URL like `funny-name-12345.netlify.app`.

To use a custom domain (e.g. mattweston.co.uk), go to **Site settings → Domain management** and follow the instructions. This costs whatever your domain costs (around £10/year from Namecheap or GoDaddy) but Netlify itself stays free.

---

## Step 3: Set up the blog admin

This is a one-time setup that lets you write posts from your browser.

1. In Netlify, go to **Site settings → Identity** and click **Enable Identity**.
2. Under **Registration**, select **Invite only** (so only you can log in).
3. Scroll down to **Services → Git Gateway** and click **Enable Git Gateway**.
4. Go back to **Identity** and click **Invite users**. Enter your email address.
5. Check your email and accept the invite. Set a password.

That's it. You can now log in to your blog admin at:

`https://your-site-name.netlify.app/admin`

---

## How to write a new post

1. Go to your site's `/admin` URL (bookmark this).
2. Log in with the email and password you set above.
3. Click **Blog Posts** → **All Posts**.
4. Click **Add Posts** to add a new entry to the list.
5. Fill in: Title, Slug, Date, Summary, optional Cover Image and Content.
6. For the Slug: use the title in lowercase with hyphens instead of spaces. Example: `why-platforms-change-faster-than-you-think`.
7. Click **Publish** when you're ready.

The post will appear on your site within a minute or two.

---

## How to update your bio or career details

The bio and career section are in the `index.html` file. To edit them, open the file in any text editor (Notepad on Windows, TextEdit on Mac) and look for the `<!-- ABOUT -->` and `<!-- CAREER -->` sections. Edit the text and re-upload the file to GitHub by repeating step 1 above (GitHub will detect it's an update, not a new file).

---

## Adding a photo

1. Save your photo as `photo.jpg` inside the `images` folder.
2. In `index.html`, find the hero section and add `<img src="/images/photo.jpg" alt="Matt Weston">` where you want it to appear.
3. Re-upload the files to GitHub.

---

## File structure for reference

```
matt-weston-site/
├── index.html          Homepage
├── blog.html           All posts listing
├── post.html           Individual post view
├── netlify.toml        Netlify configuration
├── admin/
│   ├── index.html      Blog admin interface
│   └── config.yml      Admin configuration
├── data/
│   └── posts.json      Your blog posts (managed via admin)
└── images/             Uploaded images go here
```

---

## Getting a custom domain

If you want `mattweston.co.uk` or similar:

1. Buy the domain from Namecheap or GoDaddy (around £10/year).
2. In Netlify: **Site settings → Domain management → Add custom domain**.
3. Follow Netlify's instructions to point the domain at your site. It usually involves adding two DNS records at your domain registrar. Netlify has clear step-by-step guides for this.

---

If anything goes wrong, the Netlify support docs at **docs.netlify.com** cover every step above in detail with screenshots.
