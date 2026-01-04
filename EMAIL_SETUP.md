# Email Configuration Setup Guide

This guide will help you set up EmailJS to enable the contact form to send emails directly to azeeshan867@gmail.com.

## Step 1: Create EmailJS Account

1. Go to [EmailJS website](https://www.emailjs.com/)
2. Sign up for a free account
3. Verify your email address

## Step 2: Create Email Service

1. In EmailJS dashboard, go to "Email Services"
2. Click "Add New Service"
3. Choose "Gmail" as your email provider
4. Connect your Gmail account (azeeshan867@gmail.com)
5. Note down the **Service ID** (e.g., "service_abc123")

## Step 3: Create Email Template

1. Go to "Email Templates" in EmailJS dashboard
2. Click "Create New Template"
3. Use this template content:

```
Subject: New Portfolio Contact: {{subject}}

From: {{from_name}}
Email: {{from_email}}
Subject: {{subject}}

Message:
{{message}}

---
This message was sent from your portfolio website contact form.
Reply-to: {{from_email}}
```

4. Set template variables:
   - `from_name`: {{from_name}}
   - `from_email`: {{from_email}}
   - `subject`: {{subject}}
   - `message`: {{message}}
   - `to_email`: azeeshan867@gmail.com

5. Note down the **Template ID** (e.g., "template_xyz789")

## Step 4: Get Public Key

1. Go to "Account" → "General"
2. Find your **Public Key** (e.g., "user_abc123xyz")

## Step 5: Update Configuration

Update the EmailJS configuration in `ContactSection.vue`:

```javascript
// Replace these with your actual EmailJS credentials
const EMAILJS_SERVICE_ID = 'your_service_id_here'     // From Step 2
const EMAILJS_TEMPLATE_ID = 'your_template_id_here'   // From Step 3
const EMAILJS_PUBLIC_KEY = 'your_public_key_here'     // From Step 4
```

## Step 6: Test the Contact Form

1. Start your development server: `npm run dev`
2. Navigate to the contact section
3. Fill out the form and submit
4. Check azeeshan867@gmail.com for the test message

## Alternative: Formspree (Easier Setup)

If you prefer a simpler solution, you can use Formspree:

1. Go to [Formspree.io](https://formspree.io/)
2. Create a free account
3. Create a new form with endpoint targeting azeeshan867@gmail.com
4. Update the form action in the template

## Environment Variables (Recommended)

For security, create a `.env` file in your project root:

```
VITE_EMAILJS_SERVICE_ID=your_service_id
VITE_EMAILJS_TEMPLATE_ID=your_template_id
VITE_EMAILJS_PUBLIC_KEY=your_public_key
```

Then update the configuration:

```javascript
const EMAILJS_SERVICE_ID = import.meta.env.VITE_EMAILJS_SERVICE_ID
const EMAILJS_TEMPLATE_ID = import.meta.env.VITE_EMAILJS_TEMPLATE_ID
const EMAILJS_PUBLIC_KEY = import.meta.env.VITE_EMAILJS_PUBLIC_KEY
```

## Security Notes

- EmailJS public key is safe to expose in frontend code
- Your Gmail credentials are never exposed
- EmailJS handles authentication securely
- Consider rate limiting in production

## Troubleshooting

1. **CORS Issues**: EmailJS handles CORS automatically
2. **Gmail Authentication**: Make sure 2FA is enabled and app password is used if needed
3. **Template Variables**: Ensure all template variables match the ones used in code
4. **Quotas**: Free EmailJS account has monthly limits

Once configured, visitors can send messages through your portfolio contact form, and you'll receive them directly in your Gmail inbox!
