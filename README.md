# Memezzy 🔥

Memezzy is a modern, cloud-based meme sharing platform that allows users to upload, share, and interact with memes in a sleek, user-friendly interface.

![Memezzy App Screenshot]
![Screenshot 2025-05-20 113532](https://github.com/user-attachments/assets/37e7f550-b4b3-49f9-8336-7bb043c0de6a)

## ✨ Features

- **User Authentication**: Secure email/password and Google sign-in options
- **Meme Uploads**: Support for images (JPG, PNG, GIF) and videos (MP4)
- **Interactive Feed**: Browse through trending memes with like, comment, and share functionality
- **Real-time Updates**: See new memes as they're uploaded
- **Responsive Design**: Works seamlessly across desktop and mobile devices
- **Cloud Storage**: Firebase-powered storage for reliable content delivery

## 🚀 Live Demo

[Check out the live demo here](#) ← *Replace with your actual deployment URL*

## 🛠️ Tech Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Backend**: Firebase Authentication & Storage
- **Design**: Custom CSS with responsive design principles
- **Animation**: CSS animations for smooth user experience

## 📸 Screenshots

### Trending Memes Feed
![Meme Feed]![Screenshot 2025-05-20 113532](https://github.com/user-attachments/assets/c4dc23cb-6fda-4b7b-a331-1dda178102fa)


### Authentication Modal
![Auth Modal]![Screenshot 2025-05-20 113550](https://github.com/user-attachments/assets/a24f0206-10ed-4aab-b566-5f11a808e22e)

### Upload Interface
![Upload Interface]![Screenshot 2025-05-20 113621](https://github.com/user-attachments/assets/98f042f6-c0fe-4eff-81d9-545646c2d70e)


## 💻 Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/memezzy.git
   cd memezzy
   ```

2. **Set up Firebase**
   - Create a new Firebase project at [firebase.google.com](https://firebase.google.com)
   - Enable Authentication (Email/Password and Google providers)
   - Create a Storage bucket
   - Update the Firebase configuration in `samp.html` with your own credentials:
   
   ```javascript
   const firebaseConfig = {
     apiKey: "YOUR_API_KEY",
     authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
     projectId: "YOUR_PROJECT_ID",
     storageBucket: "YOUR_PROJECT_ID.firebasestorage.app",
     messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
     appId: "YOUR_APP_ID",
     measurementId: "YOUR_MEASUREMENT_ID"
   };
   ```

3. **Deploy or run locally**
   - For local development, you can use a simple HTTP server:
     ```bash
     # Using Python
     python -m http.server 8000
     
     # Or with Node.js
     npx http-server
     ```
   - For deployment, you can use Firebase Hosting, GitHub Pages, or any static site hosting service

## 🔒 Security Rules

If using Firebase, make sure to set up appropriate security rules for your storage bucket:

```
rules_version = '2';
service firebase.storage {
  match /b/{bucket}/o {
    match /memes/{memeFile} {
      allow read: if true;  // Anyone can view memes
      allow write: if request.auth != null;  // Only authenticated users can upload
    }
  }
}
```

## 🧩 Future Enhancements

- Comment functionality
- Like counter and persistence
- User profiles and personalized feeds
- Meme categories and tags
- Search functionality
- Sharing to social media platforms

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 👏 Acknowledgements

- [Firebase](https://firebase.google.com) for authentication and storage
- [Google Fonts](https://fonts.google.com) for typography
