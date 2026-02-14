# Hat-Khoroch Privacy Policy

This repository hosts the privacy policy for the Hat-Khoroch mobile application.

## Hosting on GitHub Pages

1. **Create a new repository** on GitHub (e.g., `hat-khoroch-privacy-policy`)

2. **Upload files:**
   - Upload `privacy-policy.html` to the repository

3. **Enable GitHub Pages:**
   - Go to repository Settings
   - Scroll down to "Pages" section
   - Under "Source", select "main" branch
   - Click "Save"

4. **Access your privacy policy:**
   - Your policy will be available at: `https://[your-username].github.io/hat-khoroch-privacy-policy/privacy-policy.html`
   - Or rename `privacy-policy.html` to `index.html` for: `https://[your-username].github.io/hat-khoroch-privacy-policy/`

## Update App Settings

After hosting, update the privacy policy URL in:
- `lib/presentation/screens/settings_screen.dart` (line ~194)
- Google Play Console → Data safety section

## Required Changes Before Publishing

1. Replace `[your-email@example.com]` in `privacy-policy.html` with your actual contact email
2. Update the URL in the settings screen to your GitHub Pages URL

## Content

The privacy policy includes:
- Data collection details (account info, financial data)
- How data is used and stored (local + Firebase)
- User rights (access, export, delete)
- Security measures
- Contact information
- GDPR compliance

## Languages

The policy is available in both:
- English
- Bengali (বাংলা)
