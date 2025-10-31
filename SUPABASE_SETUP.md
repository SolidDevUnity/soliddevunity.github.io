# Supabase Setup Instructions

This login page uses Supabase for authentication. Follow these steps to set up your Supabase project:

## 1. Create a Supabase Account

1. Go to [https://supabase.com](https://supabase.com)
2. Sign up for a free account
3. Create a new project

## 2. Get Your Supabase Credentials

1. In your Supabase project dashboard, go to **Settings** → **API**
2. Copy the following values:
   - **Project URL** (this is your `supabaseUrl`)
   - **anon/public key** (this is your `supabaseKey`)

## 3. Configure the Login Page

1. Open `login.html`
2. Find these lines (around line 223):
   ```javascript
   supabaseUrl: 'YOUR_SUPABASE_URL',
   supabaseKey: 'YOUR_SUPABASE_ANON_KEY',
   ```
3. Replace `YOUR_SUPABASE_URL` with your Project URL
4. Replace `YOUR_SUPABASE_ANON_KEY` with your anon/public key

## 4. Set Up Email Authentication (Optional)

By default, Supabase requires email verification. You can:

1. Go to **Authentication** → **Providers** in your Supabase dashboard
2. Configure email settings
3. For development, you can disable email confirmation in **Authentication** → **Settings** → **Email Auth** → uncheck "Enable email confirmations"

## 5. Test the Login Page

1. Open `login.html` in your browser
2. Try creating a new account
3. Check your email for the verification link (if email confirmation is enabled)
4. Log in with your credentials

## Security Notes

- The `anon` key is safe to use in client-side code (it's designed for public use)
- Never commit your actual credentials to version control if they differ from the defaults
- Consider using environment variables or a config file that's gitignored for production

## Features

- ✅ Email/Password authentication
- ✅ User registration
- ✅ Session management
- ✅ Error handling
- ✅ Clean, responsive UI with Tailwind CSS
