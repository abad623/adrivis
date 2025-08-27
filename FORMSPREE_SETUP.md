# Formspree Setup Guide for Adrivis Waitlist

Since you're using GitHub Pages (static hosting), the waitlist form needs a third-party service to handle form submissions. This guide shows how to set up Formspree for free email collection.

## 🚀 Quick Setup (5 minutes)

### Step 1: Create Formspree Account
1. Go to [formspree.io](https://formspree.io)
2. Sign up for a free account (allows 50 submissions/month)
3. Verify your email address

### Step 2: Create a New Form
1. Click "New Form" in your Formspree dashboard
2. Name it "Adrivis Waitlist"
3. Copy the form endpoint URL (looks like: `https://formspree.io/f/xpznvqko`)

### Step 3: Update Your Website
1. Open `index.html`
2. Find this line:
   ```html
   <form class="waitlist-form" id="waitlistForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
3. Replace `YOUR_FORM_ID` with your actual form ID from step 2
4. Example:
   ```html
   <form class="waitlist-form" id="waitlistForm" action="https://formspree.io/f/xpznvqko" method="POST">
   ```

### Step 4: Update Success Redirect URL
1. In the same form, find this line:
   ```html
   <input type="hidden" name="_next" value="https://abad623.github.io/adrivis?success=true">
   ```
2. Make sure the URL matches your GitHub Pages URL
3. If your repository name is different, update accordingly

### Step 5: Test the Form
1. Commit and push your changes to GitHub
2. Wait for GitHub Pages to deploy (usually 1-2 minutes)
3. Visit your website and test the waitlist form
4. Check your email for the submission notification

## 📧 Email Notifications

### Configure Email Settings
1. In your Formspree dashboard, go to your form settings
2. Under "Notifications", add your email address
3. You'll receive an email for each waitlist signup

### Email Content
Each submission will include:
- **Email**: The user's email address
- **Subject**: "New Adrivis Waitlist Signup"
- **Timestamp**: When they signed up

## 🎨 Customization Options

### Custom Thank You Page (Optional)
Instead of showing the success message on the same page, you can create a dedicated thank you page:

1. Create `thank-you.html`:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Thank You - Adrivis</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="thank-you-page">
        <h1>🎉 You're on the list!</h1>
        <p>Thanks for joining the Adrivis waitlist.</p>
        <a href="index.html">← Back to Home</a>
    </div>
</body>
</html>
```

2. Update the form redirect:
```html
<input type="hidden" name="_next" value="https://abad623.github.io/adrivis/thank-you.html">
```

### Spam Protection
Formspree includes built-in spam protection, but you can add a honeypot field:

```html
<input type="text" name="_gotcha" style="display:none">
```

## 🔄 Alternative Solutions

If you prefer other options:

### 1. Google Forms
- Create a Google Form
- Embed it or redirect to it
- Free and reliable

### 2. Netlify Forms (if you switch hosting)
- Deploy to Netlify instead of GitHub Pages
- Built-in form handling
- 100 submissions/month free

### 3. EmailJS
- Send emails directly from frontend
- More complex setup
- Good for custom email templates

## 📊 Analytics

### Track Form Submissions
Add this to your Google Analytics (if you have it):

```javascript
// Add to script.js after form submission
gtag('event', 'waitlist_signup', {
    'event_category': 'engagement',
    'event_label': 'adrivis_waitlist'
});
```

## 🚨 Important Notes

1. **Free Tier Limits**: Formspree free tier allows 50 submissions/month
2. **Email Verification**: First submission requires email verification
3. **HTTPS Required**: Forms only work on HTTPS (GitHub Pages provides this)
4. **No Backend Needed**: Everything works with static hosting

## 🔧 Troubleshooting

### Form Not Working?
1. Check the form action URL is correct
2. Ensure you're using HTTPS
3. Verify the form method is "POST"
4. Check browser console for errors

### Not Receiving Emails?
1. Check spam folder
2. Verify email address in Formspree dashboard
3. Confirm form is properly configured

### Success Message Not Showing?
1. Check the `_next` URL is correct
2. Ensure JavaScript is enabled
3. Verify the success parameter is being passed

## 📈 Upgrade Options

When you outgrow the free tier:
- **Formspree Gold**: $10/month, 1000 submissions
- **Custom Backend**: Build your own with Node.js/Python
- **Email Marketing Platform**: Integrate with Mailchimp, ConvertKit, etc.

---

Your Adrivis waitlist is now ready to collect emails without any backend infrastructure! 🎉
