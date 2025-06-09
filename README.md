# RideSmart Frontend 🚗

Welcome to the RideSmart Frontend! This is the user-facing part of the RideSmart application, built with **React**. It provides an intuitive interface for students to book rides, manage their accounts, and for drivers to manage their schedules.

---

## 🛠️ Tech Stack

* **[React](https://reactjs.org/)**: A powerful JavaScript library for building user interfaces.
* **[Vite](https://vitejs.dev/)**: A next-generation frontend tooling that provides a faster and leaner development experience.
* **[Flutterwave](https://flutterwave.com/us/)**: The payment gateway used to securely process ride payments.

---

## 🚀 Getting Started

Follow these instructions to get the project running on your local machine for development and testing.

### **Prerequisites**

Make sure you have the following software installed before you begin:

* **Node.js**: Required to run JavaScript on your machine. You can download it from [nodejs.org](https://nodejs.org/).
* **Git**: For cloning the repository from GitHub.
* **Yarn** (or **npm**): A package manager for installing project dependencies. You can install Yarn by running `npm install --global yarn`.

### **Installation & Setup**

1.  **Clone the Project**
    Open your terminal and run this command to download the project files.
    ```sh
    git clone https://github.com/DevOps-Journey-Pro/ridesmart-frontend/
    ```

2.  **Navigate to the Project Folder**
    ```sh
    cd ridesmart-frontend/
    ```

3.  **Install Dependencies**
    This command reads the `package.json` file and installs all the necessary libraries (like React).
    ```sh
    yarn install
    ```
    *(If you prefer using npm, you can run `npm install`)*

4.  **Set Up Environment Variables**
    The application needs a special file to hold configuration settings like API keys and URLs.
    * In the project's root directory, create a new file and name it `.env`.
    * Find the file named `.env.example`. Copy its entire contents.
    * Paste the contents into your newly created `.env` file.
    * Now, you must replace the placeholder values with your actual keys and URLs. See the configuration section below for a detailed explanation of each variable.

5.  **Start the Development Server**
    You're all set! This command will launch the application in development mode.
    ```sh
    yarn start
    ```
    Your browser should automatically open to `http://localhost:8080` (or whatever port you specified), where you can see the application live!

---

## ⚙️ Configuration: Environment Variables (`.env`)

The `.env` file is crucial for configuring the app without hard-coding values. Here’s what each variable does:

* `NODE_ENV="development"`
    Tells the application it's running in a development environment. This can be changed to `"production"` for a live deployment.

* `PORT="8080"`
    The port number on which your local development server will run.

* `VITE_DEV_APP_URL=http://localhost:8080`
    The **URL of your backend server** when you are running it locally. The frontend will send API requests to this address.

* `VITE_LIVE_APP_URL="localhost"`
    The URL of your **live, deployed backend server**. When you build the app for production, it will use this address to communicate with the backend.

* `VITE_APP_URL="Frontend Dev URL"`
    The base URL of the frontend application itself.

* `VITE_FLWPUBKTEST="Flutterwave Public Test key"`
    Your **public API key from Flutterwave**. This is used for processing payments. Make sure to use your *test* key for development. See the "Making Payments" section for more details.

* `VITE_UPLOAD_LOGO="..."`
    A default logo image URL, likely used for services like Cloudinary.

---

## 📜 Available Scripts

In the project directory, you can run:

### `yarn start`

This runs the app in development mode. The page will reload if you make edits, and you will see any errors in the console.

### `yarn build`

This command bundles the app into a `dist` folder for production. It correctly bundles React in production mode and optimizes the build for the best performance. The `dist` folder contains static HTML, CSS, and JavaScript files that are ready to be deployed on any web server like **Apache** or **Nginx**.

---

## 🧪 Demo & Testing

You can create accounts to test the application's features.

### **Passenger Login**

* **Matric No:** `FAS17SIO038`
* **Password:** `123456789`
* **Note on Signup:** New student accounts must use a Matric No. with the format `ABC12DEF345` (3 letters, 2 numbers, 3 letters, 3 numbers).

### **Making Payments**

To test the payment functionality:

1.  Log on to [developer.flutterwave.com](https://developer.flutterwave.com/) and create a free account.
2.  In your Flutterwave dashboard, find your **test public key**.
3.  Copy this key and paste it as the value for `VITE_FLWPUBKTEST` in your `.env` file.
4.  When making a payment in the app, use the test card details provided by Flutterwave [on this page](https://developer.flutterwave.com/docs/integration-guides/testing-helpers/).
