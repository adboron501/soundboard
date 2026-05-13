# 🎵 Soundboard App

A simple, modern soundboard web app built with React, TypeScript, Tailwind CSS, and Vite. Works as a Progressive Web App (PWA) that can be installed on iPhone and other mobile devices.

## Features

✨ **Key Features:**
- ⚡ Fast and responsive soundboard interface
- 📱 Works as a PWA - installable on iPhone, Android, and desktop
- 🎨 Beautiful, modern UI with Tailwind CSS
- 🔊 Plays MP4 audio files when buttons are clicked
- ➕ Add and remove sounds dynamically
- 🎯 Customizable button labels and colors
- 📴 Works offline (with service worker)
- 🚀 Built with Vite for lightning-fast development and builds

## Getting Started

### Prerequisites

- Node.js 16+ and npm (or yarn/pnpm/bun)

### Installation

1. **Install dependencies:**
```bash
npm install
```

2. **Add your sound files:**
   - Create a `sounds` folder in the `public` directory: `public/sounds/`
   - Add your MP4 audio files to this folder
   - Example: `public/sounds/sound1.mp4`

3. **Update sound configuration:**
   - Edit `src/App.tsx`
   - Update the `sounds` array with your sound file names and labels

### Development

Start the development server:

```bash
npm run dev
```

The app will open in your browser at `http://localhost:3000`

### Building for Production

Build the app for production:

```bash
npm run build
```

Preview the production build:

```bash
npm run preview
```

The built files will be in the `dist` directory, ready to be deployed to any static hosting service.

## How to Use

### On Desktop
- Click any sound button to play it
- Click the × button to remove a sound
- Click "+ Add New Sound" to add more sounds
- Customize the App.tsx to change labels, colors, and audio files

### On iPhone
1. Open the app in Safari
2. Tap the "Share" button (arrow pointing up)
3. Scroll down and tap "Add to Home Screen"
4. Give it a name and tap "Add"
5. The app will now appear as an icon on your home screen
6. Tap the icon to launch the app in fullscreen mode

### On Android
1. Open the app in Chrome
2. Tap the menu button (three dots)
3. Tap "Install app" or "Add to Home screen"
4. The app will now appear as an icon on your home screen

## Project Structure

```
soundboard-app/
├── public/
│   ├── manifest.json          # PWA manifest
│   └── sounds/                # Your audio files go here
├── src/
│   ├── components/
│   │   └── SoundButton.tsx    # Individual sound button component
│   ├── App.tsx                # Main app component
│   ├── main.tsx               # React entry point
│   ├── index.css              # Tailwind styles
│   └── vite-env.d.ts          # TypeScript declarations
├── index.html                 # HTML entry point
├── vite.config.ts             # Vite configuration
├── tsconfig.json              # TypeScript configuration
├── tailwind.config.js         # Tailwind CSS configuration
├── postcss.config.js          # PostCSS configuration
└── package.json               # Project dependencies
```

## Customization

### Adding Sounds

Edit `src/App.tsx` and add new items to the `sounds` array:

```typescript
const [sounds, setSounds] = useState<Sound[]>([
  {
    id: '1',
    label: 'My Sound',
    audioUrl: '/sounds/my-sound.mp4',
    color: 'bg-blue-500'
  },
  // Add more sounds here
])
```

### Changing Colors

Use any Tailwind color class:
- `bg-blue-500`, `bg-purple-500`, `bg-pink-500`, `bg-green-500`
- `bg-red-500`, `bg-yellow-500`, `bg-indigo-500`, `bg-cyan-500`
- etc.

### Styling

The app uses Tailwind CSS. Modify `tailwind.config.js` or edit component classes directly in the `.tsx` files.

## Deployment

### Recommended Hosting Services
- **Vercel** (free tier, best for Next.js-style apps)
- **Netlify** (free tier, drag-and-drop deployment)
- **GitHub Pages** (free, static hosting)
- **AWS Amplify** (free tier available)

### Basic Deployment Steps

1. Build the app:
```bash
npm run build
```

2. Deploy the `dist` folder to your hosting service
3. Enable HTTPS (required for PWA on most platforms)
4. Install as PWA from your mobile browser

## Browser Support

- ✅ Chrome/Edge (Android)
- ✅ Safari (iOS 15+)
- ✅ Firefox
- ✅ All modern browsers with PWA support

## Troubleshooting

### Sounds not playing
- Check that MP4 files are in `public/sounds/`
- Verify the audio URL matches the file name exactly
- Check browser console for errors (F12)
- Some browsers require user interaction before playing audio

### PWA not installing on iPhone
- Make sure you're using HTTPS (not on localhost)
- Check that `manifest.json` is valid
- Safari on iOS requires specific meta tags in `index.html`
- Try clearing Safari cache and cookies

### App not loading offline
- Make sure service worker is registered (check browser DevTools)
- Reload the page after first visit
- Service worker updates might take time to propagate

## Technologies Used

- **React 18** - UI framework
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling
- **Vite** - Build tool and dev server
- **Vite PWA Plugin** - Progressive Web App support
- **PostCSS** - CSS processing

## License

MIT License - Feel free to use this project for personal or commercial use.

## Tips & Tricks

💡 **Pro Tips:**
- Use short, memorable sound labels for better UX
- Test on your target device before finalizing
- Compress MP4 files for faster loading on mobile
- Use consistent color schemes for better visual hierarchy
- Consider adding sound categories or organizing in folders
- Add haptic feedback to buttons for better mobile feel

## Next Steps

Want to enhance your soundboard?
- Add sound volume controls
- Create sound categories/tabs
- Add recording functionality
- Implement sound keyboard shortcuts
- Add visual feedback (animations) when playing
- Create a settings page for customization
- Add sound favorites/history
- Implement drag-and-drop to reorder sounds

---

Enjoy your soundboard app! 🎉
