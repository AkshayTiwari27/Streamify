<h1 align="center">✨ Streamify - Fullstack Language Exchange & Communication Platform ✨</h1>


<p align="center">
  <strong>Connect, chat, and video call with language partners worldwide!</strong> Streamify is a feature-rich, full-stack application designed to facilitate language exchange through seamless real-time communication. Built with a modern MERN-like stack (MongoDB, Express, React, Node.js) and powered by the robust Stream API for chat and video functionalities.
</p>

---

## 🚀 Live Demo

You can check out the live deployed version of Streamify here:

**[➡️ Click here to visit Streamify Live!](https://streamify-n7eu.onrender.com/)**

*(Note: You will need to sign up for an account to explore the features.)*

---

## 🌟 Key Features

* **🌐 Real-time Messaging:** Instant one-on-one chat leveraging the **[Stream Chat SDK](https://getstream.io/chat/sdk/react/)**. Includes typing indicators, read receipts, and message reactions out-of-the-box.
* **📹 Real-time Video Calling:** High-quality one-on-one video calls powered by the **[Stream Video SDK](https://getstream.io/video/sdk/react/)**. Features include speaker layouts and call controls.
* **🤝 Language Exchange Focus:** Users specify native and learning languages during onboarding, enabling targeted connections. Language flags are displayed for easy identification.
* **🔍 User Discovery & Recommendations:** Find new language partners based on language goals and exclude existing friends or users who haven't completed onboarding.
* **👥 Robust Friend System:**
    * Send, receive, and accept friend requests.
    * View friends list and outgoing pending requests.
    * Backend logic prevents duplicate requests and self-requests.
* **🔔 Notification System:** Real-time updates for incoming friend requests and newly accepted connections.
* **🔐 Secure Authentication:**
    * User signup with password hashing (`bcryptjs`).
    * Login with JWT (JSON Web Tokens) securely stored in HttpOnly cookies.
    * Protected backend routes using custom authentication middleware.
* **👤 User Onboarding Flow:** A dedicated process for new users to set up their profile details (bio, languages, location, avatar) before accessing the main app. Includes random avatar generation.
* **🎨 Highly Customizable Theming:** Choose from **30+ themes** via DaisyUI, easily selectable through a UI dropdown, with state managed by Zustand.
* **📱 Responsive Design:** Built with Tailwind CSS and DaisyUI for a seamless experience across devices.
* **⚡ Modern & Efficient Frontend:**
    * Built with React and Vite for fast development and optimized builds.
    * Uses **TanStack Query (React Query)** for efficient data fetching, caching, and server state synchronization.
    * Leverages **Zustand** for simple, lightweight global client state management (theme).
    * Custom hooks (`useAuthUser`, `useLogin`, `useSignUp`, `useLogout`) for clean component logic.
* **🚀 Scalable Backend:**
    * Node.js & Express REST API.
    * MongoDB database with Mongoose ODM for structured data modeling (`User`, `FriendRequest` schemas).
    * Clear API routing structure (`auth`, `users`, `chat`).

---

## 🛠️ Tech Stack

* **Frontend:** React (Vite), JavaScript, Tailwind CSS, DaisyUI, TanStack Query, Zustand, Axios, Stream Chat SDK, Stream Video SDK, React Router, Lucide React (Icons)
* **Backend:** Node.js, Express.js, Mongoose, JWT (jsonwebtoken), bcryptjs, Stream SDK (Server), cookie-parser, cors, dotenv
* **Database:** MongoDB
* **APIs/Services:** Stream (Chat & Video)

---

## 🏗️ Architecture Overview

Streamify follows a standard client-server architecture:

1.  **Frontend (React):** Handles the user interface, client-side routing, state management (UI state via Zustand, server state via TanStack Query), and interacts with the backend API and Stream SDKs.
2.  **Backend (Node.js/Express):** Provides a RESTful API for authentication, user management, friend requests, and generating Stream tokens. Interacts with the MongoDB database and Stream's server-side APIs.
3.  **Database (MongoDB):** Stores user profiles, friend relationships, and friend request data.
4.  **Stream Platform:** Offloads the heavy lifting for real-time chat and video infrastructure, providing SDKs for seamless integration.

---

## 📋 Prerequisites

* Node.js (v18 or higher recommended)
* npm (v8+) or yarn
* MongoDB instance (local installation or a free cloud instance from [MongoDB Atlas](https://www.mongodb.com/cloud/atlas))
* A [Stream](https://getstream.io/) account (free tier available) to obtain API keys for Chat and Video.

---

## ⚙️ Setup & Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/AkshayTiwari27/Streamify.git](https://github.com/AkshayTiwari27/Streamify.git)
    cd streamify-video-calls
    ```

2.  **Set up Backend Environment Variables:**
    * Navigate to the `backend` directory: `cd backend`
    * Create a `.env` file in this directory.
    * Add the required variables:

        ```env
        PORT=5001
        # Get from MongoDB Atlas or your local setup
        MONGO_URI=your_mongodb_connection_string
        # Get from your Stream Dashboard (getstream.io)
        STEAM_API_KEY=your_stream_api_key
        STEAM_API_SECRET=your_stream_api_secret
        # Generate a strong random string (e.g., using a password manager or online generator)
        JWT_SECRET_KEY=your_strong_jwt_secret_key
        # Set to 'production' for deployment, 'development' for local run
        NODE_ENV=development
        ```

3.  **Set up Frontend Environment Variables:**
    * Navigate to the `frontend` directory: `cd ../frontend` (from `backend`)
    * Create a `.env` file in this directory.
    * Add the required variable:

        ```env
        # Use the same Stream API Key as in the backend .env
        VITE_STREAM_API_KEY=your_stream_api_key
        ```

4.  **Install Dependencies:**
    * Install backend dependencies:
        ```bash
        cd ../backend # Or 'cd backend' from root
        npm install
        ```
    * Install frontend dependencies:
        ```bash
        cd ../frontend # Or 'cd frontend' from root
        npm install
        ```

5.  **Run the Application:**
    * **Start the Backend:** (Terminal 1, in the `backend` directory)
        ```bash
        npm run dev
        ```
        *(The backend server should start, typically on port 5001, and connect to MongoDB).*
    * **Start the Frontend:** (Terminal 2, in the `frontend` directory)
        ```bash
        npm run dev
        ```
        *(Vite will start the development server, usually on port 5173).*

6.  **Access the App:** Open your browser and navigate to `http://localhost:5173` (or the port shown in the frontend terminal).

---

## 💡 Usage

1.  **Sign Up:** Create a new account.
2.  **Log In:** Access your account.
3.  **Onboarding:** Complete your profile by adding your bio, native/learning languages, and location.
4.  **Homepage:** View your current friends and discover recommended users.
5.  **Add Friends:** Send friend requests to recommended users.
6.  **Notifications:** Check for incoming friend requests and accept them.
7.  **Chat:** Click "Message" on a friend's card to start a real-time chat.
8.  **Video Call:** Initiate a video call from within the chat interface.

---

## 🤝 Contributing (Optional)

Contributions are welcome! If you'd like to contribute, please follow these steps:

1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/your-feature-name`).
3.  Make your changes.
4.  Commit your changes (`git commit -m 'Add some feature'`).
5.  Push to the branch (`git push origin feature/your-feature-name`).
6.  Open a Pull Request.

---

## 📜 License (Optional)

This project is licensed under the [MIT License](LICENSE) - see the LICENSE file for details (if you add one).

---

## 🙏 Acknowledgements (Optional)

* Thanks to [Stream](https://getstream.io/) for their powerful Chat and Video APIs.
* Thanks to the creators of the libraries and frameworks used.

---
