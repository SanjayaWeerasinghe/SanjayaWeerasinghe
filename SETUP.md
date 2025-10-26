# 🚀 GitHub Profile README Setup Guide

This guide will help you set up your awesome GitHub profile with dynamic features!

## ✅ What's Already Done

Your README.md includes:
- Animated header with waving effect
- Dynamic typing text
- Profile view counter, followers, and stars badges
- Rust code block showcasing your skills
- Tech stack badges (Blockchain, Languages, Frameworks, Tools, Databases)
- GitHub stats widgets
- Contribution graphs
- GitHub trophies
- Featured projects section
- Social media links

## 📝 Customization Needed

### 1. Social Media Links (Required)

Update these placeholders in `README.md` (around lines 190-200):

```markdown
- LinkedIn: https://linkedin.com/in/your-linkedin
- Twitter: https://twitter.com/your-twitter
- Portfolio: https://your-portfolio.com
- Email: your.email@example.com
- Dev.to: https://dev.to/your-username
- Stack Overflow: https://stackoverflow.com/users/your-id
```

Replace with your actual profile URLs or remove the ones you don't use.

### 2. Support Links (Optional)

If you want to accept donations (around lines 210-215):
```markdown
- Buy Me a Coffee: https://buymeacoffee.com/your-username
- PayPal: https://paypal.me/your-username
```

Or remove the entire "Support My Work" section if not needed.

## 🤖 Setting Up Dynamic Features

### A. Snake Animation (Contribution Graph Snake)

The snake animation shows a snake eating your GitHub contributions!

**Setup Steps:**

1. Go to your repository settings
2. Navigate to **Settings** → **Actions** → **General**
3. Scroll to **Workflow permissions**
4. Select **Read and write permissions**
5. Check **Allow GitHub Actions to create and approve pull requests**
6. Click **Save**

The snake will generate automatically once you push the code. It runs:
- Daily at midnight (UTC)
- On every push to main branch
- Manually (via Actions tab)

### B. WakaTime Coding Stats (Optional)

WakaTime shows your coding activity, languages used, and time spent coding.

**Setup Steps:**

1. **Create WakaTime Account:**
   - Go to https://wakatime.com/
   - Sign up for free account
   - Install WakaTime plugin in your code editor (VS Code, etc.)

2. **Get API Keys:**
   - WakaTime API Key: https://wakatime.com/settings/api-key
   - Copy your API key

3. **Add Secrets to GitHub:**
   - Go to your repository **Settings** → **Secrets and variables** → **Actions**
   - Click **New repository secret**
   - Add two secrets:
     - Name: `WAKATIME_API_KEY`, Value: `your-wakatime-api-key`
     - Name: `GH_TOKEN`, Value: Create a Personal Access Token (see below)

4. **Create GitHub Personal Access Token:**
   - Go to https://github.com/settings/tokens
   - Click **Generate new token** → **Generate new token (classic)**
   - Name: `README_STATS`
   - Expiration: No expiration (or custom)
   - Scopes: Select `repo` and `user`
   - Click **Generate token**
   - Copy the token and add it as `GH_TOKEN` secret

### C. If You Don't Want WakaTime Stats

If you don't want to use WakaTime:

1. Remove this section from README.md:
   ```markdown
   ## 💻 Coding Activity

   <!--START_SECTION:waka-->
   <!--END_SECTION:waka-->
   ```

2. Delete the workflow file:
   ```bash
   rm .github/workflows/waka-readme.yml
   ```

## 🎨 Customizing Your Profile

### Changing Colors

The current theme uses:
- **Solana Green:** `#14F195`
- **Polkadot Pink:** `#E6007A`
- **Blue:** `#0e75b6`

You can change these in the badge URLs and widget themes.

### Popular Themes

Replace `theme=algolia` with:
- `theme=tokyonight`
- `theme=dracula`
- `theme=radical`
- `theme=merko`
- `theme=gruvbox`
- `theme=dark`
- `theme=onedark`

Example:
```markdown
![Stats](https://github-readme-stats.vercel.app/api?username=SanjayaWeerasinghe&theme=dracula)
```

### Adding More Badges

Find badges at: https://shields.io/ or https://simpleicons.org/

Format:
```markdown
![Name](https://img.shields.io/badge/NAME-HEX_COLOR?style=for-the-badge&logo=LOGO_NAME&logoColor=white)
```

## 🚀 Deployment

1. **Commit and Push:**
   ```bash
   git add .
   git commit -m "Add awesome GitHub profile README"
   git push origin main
   ```

2. **Enable GitHub Actions:**
   - Go to **Actions** tab in your repository
   - If workflows are disabled, click **Enable workflows**
   - Run the "Generate Snake" workflow manually first time

3. **Verify:**
   - Visit https://github.com/SanjayaWeerasinghe
   - Your profile README should appear on your profile page!

## 📚 Resources

- Awesome GitHub Profile READMEs: https://github.com/abhisheknaiidu/awesome-github-profile-readme
- GitHub Stats: https://github.com/anuraghazra/github-readme-stats
- Shields.io: https://shields.io/
- WakaTime: https://wakatime.com/
- Typing SVG: https://github.com/DenverCoder1/readme-typing-svg

## 🐛 Troubleshooting

**Snake animation not showing:**
- Make sure GitHub Actions has write permissions
- Check Actions tab for errors
- Wait for first workflow run to complete

**Stats not updating:**
- Verify secrets are added correctly
- Check workflow run logs in Actions tab
- Ensure WakaTime is tracking your coding activity

**Images not loading:**
- Wait a few minutes for external services to generate images
- Try clearing GitHub cache by adding `?v=1` to image URLs

## 💡 Tips

- Star your own repositories to increase your stats!
- Contribute regularly to maintain your streak
- Pin your best repositories to showcase them
- Keep your bio short and impactful
- Update "What I'm Currently Working On" regularly

---

**Need help?** Open an issue or check the resources above!
