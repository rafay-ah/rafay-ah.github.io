---
description: Add Google Analytics to your portfolio
---

# Add Google Analytics to Your Portfolio

Google Analytics helps you understand who visits your portfolio, where they're from, and what they're interested in. This is valuable data for optimizing your portfolio and tracking engagement.

## Step 1: Create a Google Analytics Account

1. Go to [Google Analytics](https://analytics.google.com/)
2. Sign in with your Google account
3. Click **"Start measuring"** or **"Admin"** (gear icon)
4. Click **"Create Account"**

## Step 2: Set Up Your Property

1. **Account name**: Enter something like "Portfolio Analytics"
2. Click **"Next"**
3. **Property name**: Enter "Abdul Rafay Portfolio" (or your name)
4. **Reporting time zone**: Select your timezone
5. **Currency**: Select your currency
6. Click **"Next"**

## Step 3: Configure Your Business Information

1. **Industry category**: Select "Computers & Electronics" or "Jobs & Education"
2. **Business size**: Select "Small" (1-10 employees)
3. **How you plan to use Analytics**: Check relevant options like:
   - "Examine user behavior"
   - "Measure advertising ROI"
4. Click **"Create"**
5. Accept the Terms of Service

## Step 4: Set Up Data Stream

1. Select **"Web"** as your platform
2. **Website URL**: Enter your GitHub Pages URL (e.g., `https://yourusername.github.io`)
3. **Stream name**: Enter "Portfolio Website"
4. **Enhanced measurement**: Leave it ON (recommended)
5. Click **"Create stream"**

## Step 5: Get Your Measurement ID

After creating the stream, you'll see:
- **Measurement ID**: Looks like `G-XXXXXXXXXX`
- **Copy this ID** - you'll need it!

## Step 6: Add Analytics Code to Your Portfolio

You'll add the Google Analytics tracking code to your `index.html` file in the `<head>` section.

The code looks like this:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
<!-- End Google Analytics -->
```

**Replace `G-XXXXXXXXXX` with your actual Measurement ID!**

## Step 7: Deploy the Changes

After adding the code to your `index.html`:

```bash
git add index.html
git commit -m "Add Google Analytics tracking"
git push
```

Wait 2-3 minutes for GitHub Pages to rebuild your site.

## Step 8: Verify It's Working

1. Go back to Google Analytics
2. Click on **"Reports"** → **"Realtime"**
3. Open your portfolio website in a new tab
4. You should see yourself as an active user in the Realtime report!

## What to Track

### Key Metrics to Monitor:

1. **Users**: Total number of unique visitors
2. **Sessions**: Total number of visits
3. **Bounce Rate**: Percentage who leave after viewing one page
4. **Average Session Duration**: How long people stay
5. **Pages per Session**: How many pages they view
6. **Traffic Sources**: Where visitors come from (LinkedIn, direct, search, etc.)
7. **Geographic Location**: Where your visitors are located
8. **Device Category**: Mobile vs Desktop vs Tablet

### Useful Reports:

- **Realtime**: See who's on your site right now
- **Acquisition**: How people find your portfolio
- **Engagement**: Which pages are most popular
- **Demographics**: Age, gender, interests of visitors
- **Technology**: Devices, browsers, operating systems

## Privacy Considerations

### Best Practices:

1. **Add a Privacy Policy** (optional but recommended):
   - Mention you use Google Analytics
   - Explain it's for improving user experience
   - Note that it collects anonymous data

2. **Anonymize IP Addresses** (already default in GA4)

3. **Cookie Consent** (optional for personal portfolios):
   - For a simple portfolio, this is usually not required
   - If you want to be extra compliant, you can add a cookie banner

## Tips for Portfolio Analytics

### When to Check:

- **After sending applications**: See if recruiters visit
- **After LinkedIn posts**: Track traffic spikes
- **Weekly**: Monitor overall trends
- **Before interviews**: Check if the company visited

### What to Look For:

- **High bounce rate on projects?** → Add more engaging content
- **Low mobile traffic?** → Ensure mobile optimization
- **Visitors from target companies?** → Great sign!
- **Popular projects?** → Highlight them more prominently

### Pro Tip:

Set up **Custom Events** to track specific actions:
- Clicks on "Get in Touch" button
- Project card clicks
- Resume downloads (if you add one)
- External link clicks (LinkedIn, GitHub, etc.)

## Troubleshooting

### Not seeing data?

1. Wait 24-48 hours for initial data collection
2. Check Realtime report while visiting your site
3. Verify the Measurement ID is correct
4. Ensure the code is in the `<head>` section
5. Check browser console for errors (F12)

### Ad blockers:

- Many users have ad blockers that block Google Analytics
- Your actual traffic is likely 20-30% higher than reported
- This is normal and expected

## Success!

You now have professional analytics tracking on your portfolio! 📊

Use these insights to:
- Optimize your portfolio content
- Track engagement from job applications
- Understand your audience better
- Make data-driven improvements
