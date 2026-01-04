# Quick Email Setup with Formspree (Recommended)

Formspree is the easiest way to add a working contact form to your portfolio. Here's how to set it up:

## Option 1: Formspree (Easiest - 2 minutes setup)

### Step 1: Create Formspree Account
1. Go to [formspree.io](https://formspree.io)
2. Sign up for a free account
3. Verify your email (azeeshan867@gmail.com)

### Step 2: Create New Form
1. Click "New Form" in your dashboard
2. Enter form name: "Portfolio Contact Form"
3. Add your email: azeeshan867@gmail.com
4. Copy the form endpoint URL (looks like: `https://formspree.io/f/abcd1234`)

### Step 3: Update Contact Form
Replace the form action in `ContactSection.vue`:

```vue
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" @submit="handleSubmit">
```

Replace `YOUR_FORM_ID` with your actual form ID from Formspree.

### Step 4: Test
1. Submit a test message through your contact form
2. Check your email (azeeshan867@gmail.com) for the message
3. Confirm the form endpoint in Formspree dashboard

## Option 2: Direct mailto (Instant but limited)

If you want something that works immediately without any setup:

```vue
<a href="mailto:azeeshan867@gmail.com?subject=Portfolio Contact&body=Hello Zeeshan," 
   class="btn-primary">
  Send Email Directly
</a>
```

## Option 3: EmailJS (More complex but more control)

Follow the detailed setup in `EMAIL_SETUP.md` for EmailJS configuration.

## Recommended Implementation

For immediate functionality, I recommend updating your current ContactSection.vue with Formspree:

1. **Replace the current form action** with Formspree endpoint
2. **Add proper name attributes** to form fields
3. **Keep the existing Vue.js interactivity** for better UX

## Features You'll Get:

✅ **Direct email delivery** to azeeshan867@gmail.com
✅ **Spam protection** built-in
✅ **Form validation** 
✅ **Auto-response** capability
✅ **Email notifications** 
✅ **Free tier** includes 50 submissions/month
✅ **No backend required**

## Form Field Mapping:

- `firstName` → First Name
- `lastName` → Last Name  
- `_replyto` → Reply-to email address
- `subject` → Email subject
- `message` → Message content

The form will automatically send structured emails to your Gmail inbox with all the visitor's information.

Would you like me to update your current ContactSection.vue with the Formspree integration?
