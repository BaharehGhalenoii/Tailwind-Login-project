# 🔐 Tailwind Login

A modern, responsive login page built with Vanilla JavaScript and Tailwind CSS v4, powered by Vite  
This project demonstrates a complete authentication flow with client-side validation, token management, and a clean UI.

![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4.3-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-6.x-646CFF?style=flat-square&logo=vite&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

---

## 📸 Preview

> Add a screenshot of your project here.
> 
> ```
> ![Login Preview](./screenshot.png)
> ```

---

## ✨ Features

- 🎨 **Modern UI** with Tailwind CSS v4
- 📱 **Fully Responsive** — works on mobile, tablet, and desktop
- ✅ **Client-side Validation** — email format, password length
- 🔄 **Loading State** on submit button
- 👁️ **Show/Hide Password** toggle with SVG icons
- 💾 **Remember Me** — stores email in `localStorage`
- 🔗 **Real API Integration** using `fetch` (reqres.in)
- 🛡️ **Route Guard** — auto-redirect based on auth token
- 🚪 **Logout** — clears token and returns to login
- 🌐 **Persian Error Messages** — user-friendly feedback

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| **Vite** | Build tool & dev server |
| **Tailwind CSS v4** | Styling |
| **Vanilla JavaScript (ES6+)** | Logic & interactivity |
| **Fetch API** | HTTP requests |
| **LocalStorage** | Client-side persistence |
| **Reqres.in** | Mock authentication API |

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher)
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/tailwind-login.git
   cd tailwind-login
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the dev server**
   ```bash
   npm run dev
   ```

4. **Open in browser**
   ```
   http://localhost:5173
   ```

### Build for Production

```bash
npm run build
```

The output will be in the `dist/` folder.

### Preview Production Build

```bash
npm run preview
```

---

## 🔑 Demo Credentials

This project uses [reqres.in](https://reqres.in) as a mock API. Use these credentials to log in:

| Field | Value |
|-------|-------|
| **Email** | `eve.holt@reqres.in` |
| **Password** | `cityslicka` |

> ⚠️ Any other credentials will return an error — which is useful for testing error handling.

---

## 📁 Project Structure

```
tailwind-login/
├── index.html              # Entry HTML
├── package.json
├── vite.config.js          # Vite + Tailwind plugin config
├── src/
│   ├── main.js             # App logic (login, welcome, logout)
│   └── style.css           # Tailwind import
└── README.md
```

---

## 🧠 How It Works

### 1. Login Flow
- User enters email & password
- **Client-side validation** checks format
- Request sent to `reqres.in/api/login`
- On success, token is stored in `localStorage`
- User is redirected to the **Welcome** screen

### 2. Route Guard
- On app start, checks `localStorage.token`
- If token exists → render Welcome
- If not → render Login

### 3. Remember Me
- If checked, email is stored in `localStorage.rememberedEmail`
- On next visit, email is auto-filled and checkbox is pre-checked

### 4. Logout
- Removes `token` and `currentUser` from `localStorage`
- Redirects back to Login screen

---

## 🔒 Security Notes

> ⚠️ **This project is for learning purposes.**

- Tokens are stored in `localStorage` for simplicity.
- In **production**, tokens should be stored in **HttpOnly cookies** to prevent XSS attacks.
- **Never store passwords** in `localStorage` — only store non-sensitive data.

---

## 🗺️ Roadmap

- [x] Login form with Tailwind
- [x] Client-side validation
- [x] Show/hide password
- [x] Remember me
- [x] API integration
- [x] Route guard
- [x] Logout
- [ ] Signup page
- [ ] Forgot password
- [ ] Dark mode
- [ ] Social login (UI only)
- [ ] Deploy to Vercel

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!  
Feel free to check the [issues page](https://github.com/BaharehGhalenoii/tailwind-login/issues).

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Bahareh Ghalenoii**

- GitHub: [@YOUR_USERNAME](https://github.com/BaharehGhalenoii)
- Email: ghalenoiibahareh@gmail.com

---

## ⭐ Show Your Support

If this project helped you, please give it a ⭐ on GitHub!

---

## 🙏 Acknowledgments

- [Tailwind CSS](https://tailwindcss.com)
- [Vite](https://vitejs.dev)
- [Reqres.in](https://reqres.in) — Mock API for testing
- [Lucide Icons](https://lucide.dev) — SVG icons inspiration
