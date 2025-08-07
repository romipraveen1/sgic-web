# SGI Alumni Deep Link Landing Page

This is the web landing page for handling deep links to the SGI Alumni mobile app. It provides smart redirection based on whether the user has the app installed or not.

## 🚀 GitHub Pages Setup for Testing

Since `https://sgicalumni.com` is not yet deployed, we're using GitHub Pages for testing with the domain: `https://romipraveen1.github.io/sgic-web`

### Setup Instructions:

1. **Create a new repository** named `sgic-web` on your GitHub account (`romipraveen1`)

2. **Upload the files** from this `alumni-web-landing` folder to the repository:
   - `index.html` (main landing page)
   - Any assets folder if you have logos/images

3. **Enable GitHub Pages**:
   - Go to repository Settings
   - Scroll to "Pages" section
   - Select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Save

4. **Your landing page will be available at**: `https://romipraveen1.github.io/sgic-web`

### Testing Deep Links:

Once deployed, you can test the deep linking with URLs like:
- `https://romipraveen1.github.io/sgic-web/app/home/post/123`
- `https://romipraveen1.github.io/sgic-web/app/home/post/456`

## 📱 How It Works:

### For Mobile Users:
1. **App Installed**: Automatically redirects to the app and opens the specific post
2. **No App**: Shows download buttons for Play Store/App Store
3. **Fallback**: Manual "Open in App" button if auto-redirect fails

### For Desktop Users:
- Shows "Open Web App" option
- Provides download links for mobile app

## 🔧 Configuration:

The landing page is configured to work with:
- **App Scheme**: `sgicalumni://`
- **Web Domain**: `https://romipraveen1.github.io/sgic-web`
- **Deep Link Format**: `/app/home/post/{postId}`

## 🎯 Features:

- ✅ **Smart App Detection**: Tries to open the app automatically
- ✅ **Platform Detection**: Different behavior for iOS/Android/Desktop
- ✅ **Progressive Enhancement**: Works without JavaScript
- ✅ **SEO Optimized**: Open Graph and Twitter Card meta tags
- ✅ **Responsive Design**: Works on all screen sizes
- ✅ **Loading States**: Shows loading spinner during redirection
- ✅ **Fallback Options**: Manual buttons if auto-redirect fails

## 🔄 Migration to Production:

When `https://sgicalumni.com` is ready:

1. **Update the mobile app** configuration in:
   - `src/services/deepLinkService.ts`
   - `src/navigation/index.tsx`

2. **Deploy this landing page** to `https://sgicalumni.com`

3. **Update the configuration** to use the production domain

## 📝 Testing Checklist:

- [ ] Deploy to GitHub Pages
- [ ] Test deep link generation in mobile app
- [ ] Test link opening on mobile (with app)
- [ ] Test link opening on mobile (without app)
- [ ] Test link opening on desktop
- [ ] Test social media sharing
- [ ] Verify app store redirects work
- [ ] Test post navigation in app

## 🛠 Customization:

You can customize:
- **App Store URLs**: Update the actual App Store and Play Store URLs
- **Branding**: Add your logo to `/assets/logo.png`
- **Colors**: Modify the CSS gradient and colors
- **Messages**: Update the text content and call-to-action

## 📞 Support:

If you encounter any issues with the deep linking setup, check:
1. GitHub Pages is enabled and deployed
2. Mobile app has the correct domain in linking configuration
3. App scheme matches between web and mobile app
4. Post IDs are valid and exist in the backend
