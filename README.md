# chill-code

A simple website built with Next.js. Right now it shows a **Hello, world** page.

This guide is written for people who are **not developers**. Follow each step in order.

---

## What you need before starting

You only need to install these **once** on your computer.

### 1. Node.js (runs the project on your computer)

Node.js is the program that runs this website on your machine.

1. Go to [https://nodejs.org](https://nodejs.org)
2. Download the **LTS** version (the big green button)
3. Run the installer and click **Next** through all steps (default settings are fine)
4. When finished, restart your computer (recommended)

**Check it worked**

Open **Terminal** (Mac) or **Command Prompt** (Windows) and type:

```bash
node --version
```

You should see a version number like `v22.x.x`. If you see an error, Node.js is not installed correctly yet.

### 2. Git (downloads the project files)

Git lets you download and update the project from GitHub.

1. Go to [https://git-scm.com/downloads](https://git-scm.com/downloads)
2. Download Git for your computer (Windows, Mac, or Linux)
3. Run the installer (default settings are fine)

**Check it worked**

```bash
git --version
```

You should see a version number like `git version 2.x.x`.

### 3. A free Vercel account (puts the site on the internet)

Vercel hosts the website so other people can open it in a browser.

1. Go to [https://vercel.com/signup](https://vercel.com/signup)
2. Sign up (GitHub login is the easiest option)
3. You do not need to pay anything for a basic site

### 4. A free GitHub account (stores the project online)

If you do not have one yet:

1. Go to [https://github.com/signup](https://github.com/signup)
2. Create your account

---

## Step 1: Get the project on your computer

### Option A — Download from GitHub (easiest)

1. Open [https://github.com/alexneres/chill-code](https://github.com/alexneres/chill-code)
2. Click the green **Code** button
3. Click **Download ZIP**
4. Unzip the file
5. Move the `chill-code` folder somewhere easy to find (for example: `Documents/chill-code`)

### Option B — Use Git in Terminal

```bash
git clone https://github.com/alexneres/chill-code.git
cd chill-code
```

---

## Step 2: Open the project folder in Terminal

You need to be **inside** the project folder before running commands.

**Mac**

1. Open **Terminal**
2. Type `cd ` (with a space after `cd`)
3. Drag the `chill-code` folder into the Terminal window
4. Press **Enter**

**Windows**

1. Open **Command Prompt**
2. Type `cd ` (with a space after `cd`)
3. Drag the `chill-code` folder into the window
4. Press **Enter**

You should now be in the project folder.

---

## Step 3: Install the project dependencies

The project needs extra files (packages) to work. Install them once:

```bash
npm install
```

This can take 1–3 minutes. Wait until it finishes and you see the command prompt again.

If you see errors about network or timeout, run the same command again:

```bash
npm install
```

---

## Step 4: Run the site on your computer

Start the local version of the website:

```bash
npm run dev
```

When it is ready, you will see something like:

```text
Local: http://localhost:3000
```

1. Open your web browser (Chrome, Safari, Firefox, etc.)
2. Go to [http://localhost:3000](http://localhost:3000)
3. You should see **Hello, world**

**To stop the site**

Go back to Terminal and press `Ctrl + C`.

---

## Step 5: Put the site on the internet (Vercel)

This is the easiest way for non-technical users. No extra commands needed after the first setup.

### 5.1 Push the project to GitHub (if it is not there yet)

If someone else set up the repo for you, you can skip to **5.2**.

In Terminal, inside the `chill-code` folder:

```bash
git add .
git commit -m "Setup project"
git push
```

If Git asks you to log in, follow the prompts in the browser.

### 5.2 Connect GitHub to Vercel

1. Go to [https://vercel.com/new](https://vercel.com/new)
2. Log in to Vercel
3. Click **Import** next to the `chill-code` repository
   - If you do not see it, click **Adjust GitHub App Permissions** and allow access to the repo
4. On the setup screen:
   - **Framework Preset:** Next.js (should be detected automatically)
   - **Root Directory:** leave as `.`
   - **Build Command:** leave default
   - **Output Directory:** leave default
5. Click **Deploy**
6. Wait 1–2 minutes

When it finishes, Vercel shows a link like:

```text
https://chill-code-xxxxx.vercel.app
```

Open that link — your site is live on the internet.

### 5.3 Update the live site later

Every time new changes are pushed to GitHub, Vercel rebuilds the site automatically.

1. Make changes to the project (or ask a developer to do it)
2. Push to GitHub:

```bash
git add .
git commit -m "Describe what changed"
git push
```

3. Wait about 1–2 minutes
4. Refresh your Vercel URL in the browser

---

## Optional: Deploy using Vercel CLI (for people comfortable with Terminal)

Only use this if you prefer commands instead of the Vercel website.

```bash
npx vercel login
npx vercel --prod
```

Follow the prompts in the browser and Terminal.

---

## Common problems

### `command not found: node` or `command not found: npm`

Node.js is not installed, or Terminal was opened before installation finished.

- Install Node.js from [nodejs.org](https://nodejs.org)
- Close and reopen Terminal
- Run `node --version` again

### `npm install` fails or times out

- Check your internet connection
- Run `npm install` again
- If you are on a work network, a firewall may be blocking downloads

### Page does not load at `localhost:3000`

- Make sure `npm run dev` is still running (do not close that Terminal window)
- Check the Terminal for errors
- Try [http://127.0.0.1:3000](http://127.0.0.1:3000) instead

### Vercel deploy failed

- Make sure the project builds locally first:

```bash
npm run build
```

- If that works, try deploying again from the Vercel dashboard

---

## Project structure (simple overview)

| Folder / file | What it is for |
| --- | --- |
| `app/` | Website pages |
| `components/` | Reusable UI pieces |
| `lib/` | Helper code |
| `db/` | Database files (for later) |
| `public/` | Images and static files |
| `package.json` | List of project dependencies |

---

## Tech used in this project

- **Next.js** — website framework
- **Tailwind CSS** — styling
- **Vercel** — hosting

More tools (database, forms, tests) will be added as the project grows.

---

## Need help?

1. Read the **Common problems** section above
2. Ask the person who gave you this project
3. Share a screenshot of any error message — that helps a lot
