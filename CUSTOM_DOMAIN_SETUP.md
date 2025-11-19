# Custom Domain Setup - luminabridging.ca

## Overview
This document outlines the process to connect your custom domain `luminabridging.ca` (registered with Web Hosting Canada) to your GitHub Pages website.

---

## Step 1: GitHub Configuration

**Timeline:** Complete immediately

1. Go to your GitHub repository:
   - https://github.com/Lumina-Bridging-Inc/lumina-bridging-inc.github.io

2. Click **Settings** (gear icon in top right)

3. In the left sidebar, click **Pages**

4. Under "Custom domain" section:
   - Enter: `luminabridging.ca`
   - Click **Save**
   - GitHub will automatically create a CNAME file

5. GitHub will display a message confirming the custom domain is set

---

## Step 2: DNS Records Configuration at WHC

**Timeline:** Contact WHC support to add these records

### Contact Web Hosting Canada (WHC)

Choose one method:

**Option A: Live Chat (Fastest)**
- Go to https://clients.whc.ca
- Click the **Live Chat** button (usually bottom right)
- Hours: Available 24/7

**Option B: Phone**
- Call: **1-514-504-2113**
- Based in Montreal, Canada

**Option C: Support Ticket**
- Submit through clients.whc.ca Knowledge Base

### What to Tell WHC Support

Copy and paste this to WHC support:

```
I need to add DNS records to point luminabridging.ca to GitHub Pages.

Please add the following A records:
- 185.199.108.153
- 185.199.109.153
- 185.199.110.153
- 185.199.111.153

Please add the following AAAA records (IPv6):
- 2606:50c0:8000::153
- 2606:50c0:8001::153
- 2606:50c0:8002::153
- 2606:50c0:8003::153

Domain: luminabridging.ca
Purpose: GitHub Pages hosting
```

### DNS Records Details

| Record Type | Name | Value |
|------------|------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| AAAA | @ | 2606:50c0:8000::153 |
| AAAA | @ | 2606:50c0:8001::153 |
| AAAA | @ | 2606:50c0:8002::153 |
| AAAA | @ | 2606:50c0:8003::153 |

---

## Step 3: DNS Propagation & Verification

**Timeline:** 24-48 hours for global propagation

1. **Wait for DNS Propagation**
   - DNS changes can take 24-48 hours to propagate worldwide
   - Some changes may be visible within 5-10 minutes
   - Use a DNS checker: https://www.whatsmydns.net/

2. **Check GitHub Status**
   - Go back to GitHub Settings → Pages
   - Look for a **green checkmark** next to your custom domain
   - This indicates GitHub has verified the DNS records

3. **Enable HTTPS**
   - Once DNS is verified, GitHub automatically provisions an SSL certificate
   - This happens automatically (no action needed)
   - May take 5-10 minutes after DNS verification

---

## Step 4: Test Your Domain

Once DNS propagation is complete:

1. **Visit your domain:** https://luminabridging.ca
2. **Verify it loads** your Lumina Bridging website
3. **Check for HTTPS** - You should see a lock icon in your browser
4. **Test responsive design** on mobile and desktop

---

## Troubleshooting

### Domain still shows GitHub Pages URL
- **Cause:** DNS records haven't propagated yet
- **Solution:** Wait 24-48 hours, then refresh browser cache (Cmd+Shift+R on Mac)

### HTTPS not enabled
- **Cause:** GitHub still verifying DNS
- **Solution:** Check GitHub Pages settings - look for status message
- May take 5-10 minutes after DNS verification

### Domain not working after 48 hours
- **Check DNS records** using: https://www.whatsmydns.net/
- **Verify records are correct** - all 4 A records and all 4 AAAA records should be present
- **Contact WHC support** if records weren't added correctly

---

## After Setup Complete

Once your custom domain is working:

1. **Update bookmarks** - Point to `luminabridging.ca` instead of github.io URL
2. **Share your domain** - Update your GitHub org profile, business cards, etc.
3. **Monitor performance** - GitHub Pages provides automatic analytics

---

## Useful Links

- **GitHub Pages Docs:** https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site
- **WHC Client Portal:** https://clients.whc.ca
- **DNS Checker:** https://www.whatsmydns.net/
- **Your GitHub Repo:** https://github.com/Lumina-Bridging-Inc/lumina-bridging-inc.github.io

---

## Summary Timeline

| Step | Timeline | Status |
|------|----------|--------|
| GitHub configuration | Immediate | ✅ Complete |
| Contact WHC for DNS records | Today | ⏳ Pending |
| WHC adds DNS records | 2-5 minutes | ⏳ Pending |
| DNS propagation globally | 24-48 hours | ⏳ Pending |
| HTTPS certificate provisioned | 5-10 minutes after DNS | ⏳ Pending |
| **Domain live** | **48 hours max** | ⏳ Pending |

---

**Questions?** Contact either:
- GitHub Support: https://support.github.com
- WHC Support: 1-514-504-2113 or https://clients.whc.ca
