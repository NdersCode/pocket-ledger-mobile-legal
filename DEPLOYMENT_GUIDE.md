# Pocket Ledger Legal Website - Deployment Guide

This guide will help you deploy the Pocket Ledger legal website to GitHub Pages and configure it for Apple App Store and Google Play Store compliance.

## 🚀 Quick Deployment Steps

### 1. Create GitHub Repository

```bash
# Navigate to your local project
cd /path/to/pocket-ledger-legal-website

# Initialize git repository
git init

# Add all files
git add .

# Initial commit
git commit -m "Initial legal website deployment for Pocket Ledger"

# Add remote repository (replace with your GitHub username)
git remote add origin https://github.com/NdersCode/pocket-ledger-mobile-legal.git

# Push to GitHub
git push -u origin main
```

### 2. Enable GitHub Pages

1. Go to your repository on GitHub
2. Navigate to **Settings** → **Pages**
3. Under **Source**, select **Deploy from a branch**
4. Choose **main** branch and **/ (root)** folder
5. Click **Save**

Your website will be available at: `https://nderscode.github.io/pocket-ledger-mobile-legal/`

### 3. Verify Deployment

Visit these URLs to ensure they work:
- **Homepage:** `https://nderscode.github.io/pocket-ledger-mobile-legal/`
- **Privacy Policy:** `https://nderscode.github.io/pocket-ledger-mobile-legal/privacy-policy.html`
- **Terms & Conditions:** `https://nderscode.github.io/pocket-ledger-mobile-legal/terms-conditions.html`

## 📱 App Store Configuration

### Apple App Store Connect

1. **Navigate to App Information**
   - Go to App Store Connect → Your App → App Information
   - Scroll to **General Information**

2. **Add Privacy Policy URL**
   ```
   Privacy Policy URL: https://nderscode.github.io/pocket-ledger-mobile-legal/privacy-policy.html
   ```

3. **App Privacy Details**
   - Go to **App Privacy** section
   - Configure based on the privacy policy sections:
     - ✅ Contact Info (Email)
     - ✅ Financial Info (Transaction data)
     - ✅ Usage Data (Analytics)
     - ✅ Identifiers (Device ID for analytics)

### Google Play Console

1. **Store Listing**
   - Go to Play Console → Your App → Store Listing
   - Scroll to **Store Listing Contact**

2. **Privacy Policy URL**
   ```
   Privacy Policy: https://nderscode.github.io/pocket-ledger-mobile-legal/privacy-policy.html
   ```

3. **Data Safety**
   - Go to **Data Safety** section
   - Configure data collection based on privacy policy:
     - ✅ Personal info (Email, Name)
     - ✅ Financial info (Transaction records)
     - ✅ App activity (Usage analytics)
     - ✅ Device or other IDs (Analytics identifiers)

## ✅ Compliance Checklist

### Pre-Deployment Verification

#### ✅ Website Functionality
- [ ] All pages load correctly
- [ ] Navigation works on mobile and desktop
- [ ] Contact email links work
- [ ] Table of contents navigation works
- [ ] Print functionality works
- [ ] Dark mode support works

#### ✅ Legal Content Completeness
- [ ] Privacy Policy includes all required sections
- [ ] Terms & Conditions includes subscription terms
- [ ] Contact information is correct
- [ ] Effective dates are current
- [ ] Bundle ID matches app configuration
- [ ] Pricing information is accurate

#### ✅ Apple App Store Requirements
- [ ] Privacy Policy URL is publicly accessible
- [ ] No login required to view documents
- [ ] URL is not editable by users
- [ ] All data collection practices are disclosed
- [ ] Third-party services are documented
- [ ] User rights are clearly explained

#### ✅ Google Play Store Requirements
- [ ] Privacy Policy link works in all regions
- [ ] Data Safety information matches privacy policy
- [ ] Subscription terms are clearly stated
- [ ] Data deletion process is explained
- [ ] Children's privacy is addressed

### Post-Deployment Testing

#### ✅ Accessibility Testing
```bash
# Test with screen readers
# Test keyboard navigation
# Verify color contrast
# Check mobile responsiveness
```

#### ✅ Performance Testing
- [ ] Page load time < 3 seconds
- [ ] Works offline (cached)
- [ ] Mobile performance is good
- [ ] No console errors

#### ✅ SEO Verification
- [ ] Meta descriptions are present
- [ ] Page titles are descriptive
- [ ] URLs are clean and readable
- [ ] Content is properly structured

## 🔧 Maintenance Schedule

### Monthly Tasks
- [ ] Verify all links are working
- [ ] Check website performance
- [ ] Review analytics (if implemented)
- [ ] Test mobile responsiveness

### Quarterly Tasks
- [ ] Review legal document content
- [ ] Check compliance with new regulations
- [ ] Update effective dates if content changed
- [ ] Performance optimization review

### Annual Tasks
- [ ] Complete legal document review
- [ ] Update privacy policy for new features
- [ ] Review third-party service integrations
- [ ] Security audit of hosting

## 🚨 Troubleshooting

### Common Issues

#### Website Not Loading
1. Check GitHub Pages status in repository settings
2. Verify DNS propagation (can take up to 24 hours)
3. Check for syntax errors in HTML files
4. Review GitHub Actions for build errors

#### Links Not Working
1. Verify file names match exactly (case-sensitive)
2. Check for special characters in URLs
3. Test links in incognito/private mode
4. Clear browser cache

#### Mobile Display Issues
1. Test on multiple devices and browsers
2. Check viewport meta tag configuration
3. Verify CSS media queries
4. Test with browser developer tools

### Support Resources

#### GitHub Pages Documentation
- [GitHub Pages Basics](https://docs.github.com/en/pages)
- [Custom Domains](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
- [Troubleshooting](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-jekyll-build-errors-for-github-pages-sites)

#### App Store Resources
- [Apple Privacy Requirements](https://developer.apple.com/app-store/app-privacy-details/)
- [Google Play Data Safety](https://support.google.com/googleplay/android-developer/answer/10787469)

## 📊 Analytics Setup (Optional)

### Google Analytics 4

1. **Create GA4 Property**
   - Go to Google Analytics
   - Create new property for the website

2. **Add Tracking Code**
   ```html
   <!-- Add to <head> section of each HTML file -->
   <script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
   <script>
     window.dataLayer = window.dataLayer || [];
     function gtag(){dataLayer.push(arguments);}
     gtag('js', new Date());
     gtag('config', 'GA_MEASUREMENT_ID');
   </script>
   ```

3. **Track Important Events**
   - Privacy Policy views
   - Terms & Conditions views
   - Contact link clicks

### Search Console

1. **Add Property**
   - Go to Google Search Console
   - Add your GitHub Pages URL

2. **Verify Ownership**
   - Use HTML tag method
   - Add meta tag to index.html

3. **Submit Sitemap**
   - GitHub Pages automatically generates sitemap.xml
   - Submit: `https://nderscode.github.io/pocket-ledger-mobile-legal/sitemap.xml`

## 🔒 Security Considerations

### HTTPS Enforcement
- GitHub Pages automatically provides HTTPS
- Always use HTTPS URLs in app store submissions
- Verify SSL certificate is valid

### Content Security
- No user-generated content to moderate
- Static files reduce security vulnerabilities
- Regular content reviews for accuracy

### Privacy Protection
- No cookies or tracking (unless analytics added)
- No personal data collection on website
- Compliant with privacy regulations

## 📋 Final Checklist

Before submitting to app stores:

#### ✅ Technical Verification
- [ ] Website is live and accessible
- [ ] All pages load without errors
- [ ] Mobile responsiveness confirmed
- [ ] HTTPS certificate is active
- [ ] URLs are permanent and stable

#### ✅ Content Verification
- [ ] All legal requirements are met
- [ ] Contact information is accurate
- [ ] App details match actual app
- [ ] Subscription pricing is correct
- [ ] Effective dates are current

#### ✅ Compliance Verification
- [ ] Apple App Store guidelines met
- [ ] Google Play Store policies met
- [ ] GDPR compliance confirmed
- [ ] CCPA compliance confirmed
- [ ] International regulations considered

---

## 🎉 Congratulations!

Your Pocket Ledger legal website is now ready for production use. The website meets all current Apple App Store and Google Play Store requirements for 2025, ensuring smooth app approval and ongoing compliance.

**Next Steps:**
1. Deploy to GitHub Pages using the steps above
2. Update your app store listings with the new URLs
3. Test the complete user flow from app to legal documents
4. Schedule regular maintenance and content reviews

**Support:**
- For technical issues: Create issue in GitHub repository
- For legal content questions: Consult with legal counsel
- For app store submission help: Review official documentation

*Created with care for Pocket Ledger's success! 🚀*