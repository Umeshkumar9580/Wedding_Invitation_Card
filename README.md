# 💍 Wedding Invitation Card

> **A beautiful digital wedding invitation with personalized greetings, animated elements, and real-time visitor tracking — built for Hridayansh × Jyoti's special day.**

🔗 **Live Demo:** [wedding-invitation-card-six.vercel.app](https://wedding-invitation-card-six.vercel.app)

---

## ✨ Features

- **Personalized Greeting** — Enter your name and get a custom invitation card with your name
- **Animated Invitation Cards** — Beautiful gallery with 3 wedding cards (Nimantran, Parichay, Karyakram)
- **Om / Swastik Animations** — Cultural religious spark animations on the landing screen
- **Card Lightbox** — Click any card thumbnail to view it fullscreen
- **Download Option** — Download your personalized invitation card
- **Guest List Section** — Password-protected "Hamare Mehman" section for admin use
- **Visitor Tracking** — Real-time visitor data saved to Firebase Firestore (name, device, browser, timestamp)
- **Admin Panel** — PIN-protected dashboard to view all visitors with CSV export
- **Responsive Design** — Works on all devices — mobile, tablet, desktop
- **Maroon / Gold Theme** — Traditional Indian wedding color palette

---

## 📸 Screenshots

| Landing Page | Invitation Card | Admin Panel |
|---|---|---|
| Name entry with animations | Personalized card view | Visitor list with CSV export |

---

## 🛠️ Tech Stack

| Technology | Usage |
|---|---|
| **HTML5 / CSS3** | Structure & styling |
| **Vanilla JavaScript** | Animations, interactions, logic |
| **Firebase Firestore** | Real-time visitor tracking |
| **Firebase Hosting / Vercel** | Deployment |

---

## 🔥 Firebase Setup

This project uses **Firebase Firestore** for visitor tracking.

### Configuration

The Firebase config is embedded in `index.html`:

```js
const firebaseConfig = {
  projectId: "weeding-invitation-card-eb8fd",
  // ...other config
};
```

### Firestore Rules

```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /visitors/{document} {
      allow read, write: if true;
    }
  }
}
```

### Data Collected per Visitor

| Field | Description |
|---|---|
| `name` | Guest's entered name |
| `ts` | Timestamp (Unix ms) |
| `dev` | Device type (Mobile / Desktop) |
| `br` | Browser name |
| `sw` / `sh` | Screen width / height |

---

## 🚀 Deployment

This project is deployed on **Vercel** with auto-deploy from GitHub.

```
Branch: main
Framework: Static HTML
Build Command: (none)
Output Directory: /
```

Every `git push` to `main` automatically deploys to Vercel.

---

## 📁 Project Structure

```
Wedding_Invitation_Card/
├── index.html          # Main file (all HTML, CSS, JS)
├── parichay.jpg        # Parichay card image
└── README.md           # This file
```

---

## 🔐 Admin Access

The admin panel is accessible from the bottom of the invitation page.

- Enter your **admin PIN** to unlock the visitor dashboard
- View all guests who have opened the invitation
- **Export to CSV** with one click

> ⚠️ Keep your admin PIN private. Change it in the `CFG` object inside `index.html`.

---

## 👰🤵 Wedding Details

| | |
|---|---|
| **Bride** | Hridaykanika – Jyoti |
| **Groom** | Hridayansh – Ajay Kumar |
| **Venue** | Mahoba, Uttar Pradesh |
| **Event** | Parinay Bandhan |

---

## 📄 License

This project is personal and created for private use. All rights reserved.

---

<p align="center">Made with ❤️ for a very special day</p>
