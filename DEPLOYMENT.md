# GitHub Pages Deployment Guide

## Quick Start

1. **Create a new GitHub repository** named `resonaelabs.github.io`
2. **Upload all files** from this directory to the repository
3. **Enable GitHub Pages** in repository settings
4. **Set custom domain** to `resonaelabs.com`

## Detailed Setup Instructions

### Step 1: Create GitHub Repository

1. Go to GitHub and create a new repository
2. Name it `resonaelabs.github.io` (this is the GitHub Pages convention)
3. Make it public
4. Initialize with README (optional)

### Step 2: Upload Files

Upload all files from this directory to your repository:

```
github-pages/
├── index.html
├── assets/
│   ├── index-C77w-O8j.js
│   └── index-DLgZ6AsS.css
├── robots.txt
├── sitemap.xml
├── .nojekyll
├── CNAME
├── 404.html
├── site.webmanifest
├── favicon.ico
└── README.md
```

### Step 3: Configure GitHub Pages

1. Go to your repository settings
2. Scroll down to "Pages" section
3. Under "Source", select "Deploy from a branch"
4. Select "main" branch and "/ (root)" folder
5. Click "Save"

### Step 4: Set Custom Domain

1. In the Pages settings, add your custom domain: `resonaelabs.com`
2. Check "Enforce HTTPS"
3. Update your DNS settings to point to GitHub Pages

### Step 5: DNS Configuration

Add these DNS records to your domain:

```
Type: CNAME
Name: www
Value: resonaelabs.github.io

Type: A
Name: @
Value: 185.199.108.153
Value: 185.199.109.153
Value: 185.199.110.153
Value: 185.199.111.153
```

## SEO Verification

After deployment, verify these SEO elements:

1. **Google Search Console**: Submit your sitemap
2. **Meta Tags**: Check all meta tags are present
3. **Structured Data**: Validate JSON-LD schema
4. **Mobile-Friendly**: Test mobile responsiveness
5. **Page Speed**: Check Core Web Vitals

## Custom Domain Setup

### Option 1: Using CNAME (Recommended)

1. Create a CNAME record in your DNS:
   ```
   Type: CNAME
   Name: www
   Value: resonaelabs.github.io
   ```

2. Add A records for the root domain:
   ```
   Type: A
   Name: @
   Value: 185.199.108.153
   Value: 185.199.109.153
   Value: 185.199.110.153
   Value: 185.199.111.153
   ```

### Option 2: Using Apex Domain

If you want to use the apex domain (resonaelabs.com without www):

1. Add A records:
   ```
   Type: A
   Name: @
   Value: 185.199.108.153
   Value: 185.199.109.153
   Value: 185.199.110.153
   Value: 185.199.111.153
   ```

2. Add CNAME for www:
   ```
   Type: CNAME
   Name: www
   Value: resonaelabs.github.io
   ```

## Testing Your Deployment

1. **Visit your site**: https://resonaelabs.com
2. **Check mobile**: Test on different devices
3. **SEO tools**: Use Google PageSpeed Insights, GTmetrix
4. **Social sharing**: Test Open Graph tags on Facebook/Twitter
5. **Search engines**: Submit to Google Search Console

## Troubleshooting

### Common Issues

1. **404 errors**: Check file paths and case sensitivity
2. **CSS not loading**: Verify asset paths in HTML
3. **Custom domain not working**: Check DNS propagation (can take 24-48 hours)
4. **HTTPS issues**: Wait for GitHub to provision SSL certificate

### Debug Steps

1. Check GitHub Pages build logs
2. Verify all files are uploaded correctly
3. Test with temporary GitHub Pages URL first
4. Check browser console for errors

## Maintenance

### Regular Updates

1. **Content updates**: Edit HTML files directly
2. **SEO monitoring**: Check Google Search Console regularly
3. **Performance**: Monitor Core Web Vitals
4. **Security**: Keep dependencies updated

### Backup Strategy

1. Keep local copies of all files
2. Use Git for version control
3. Document any custom changes
4. Test changes locally before deploying

## Support

For technical support:
- **Email**: hello@resonaelabs.com
- **GitHub Issues**: Create an issue in the repository
- **Documentation**: Check GitHub Pages documentation

## Performance Optimization

### Current Optimizations

- Minified CSS and JavaScript
- Optimized images
- Lazy loading for 3D content
- Preconnect to external resources
- Efficient font loading

### Additional Recommendations

1. **CDN**: Consider using a CDN for global performance
2. **Caching**: Implement proper cache headers
3. **Compression**: Enable gzip compression
4. **Monitoring**: Set up performance monitoring

## Security Considerations

- HTTPS enforced
- No sensitive data in client-side code
- Secure headers implemented
- Regular security audits recommended
