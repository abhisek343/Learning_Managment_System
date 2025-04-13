# E-Learning Management System

A full-stack Learning Management System (LMS) built with the MERN stack (MongoDB, Express.js, React, Node.js), allowing instructors to create and manage courses, and students to enroll and track their progress.

## Key Features

* **User Roles:** Separate interfaces and functionalities for Students and Instructors.
* **Authentication:** Secure JWT-based authentication (login, register, logout).
* **Course Management:** Instructors can CRUD (Create, Read, Update, Delete) courses and lectures.
* **Media Uploads:** Supports video uploads for lectures and image uploads for thumbnails (using Cloudinary).
* **Payment Integration:** Course purchasing via Stripe checkout.
* **Progress Tracking:** Students can view lectures and mark them as completed.
* **Search & Filter:** Students can search for courses and filter by category/price.
* **Responsive UI:** Client-side built with React, Vite, Shadcn UI, and Tailwind CSS.

## Tech Stack

* **Frontend:** React, Vite, Redux Toolkit (RTK Query), React Router, Tailwind CSS, Shadcn UI, Axios
* **Backend:** Node.js, Express.js, MongoDB, Mongoose
* **Authentication:** JWT, bcryptjs
* **Payments:** Stripe
* **Media:** Cloudinary, Multer

## Installation and Setup

### Prerequisites

* Node.js (>= 18)
* MongoDB instance (local or cloud)
* NPM or Yarn
* Git
* Cloudinary Account
* Stripe Account

### 1. Backend Setup (`/server`)

1.  Navigate to the server directory:
    ```bash
    cd server
    ```
2.  Install dependencies:
    ```bash
    npm install # or yarn install
    ```
3.  Create a `.env` file and add your credentials (see `.env.example` if available, or refer to the list below):
    ```# Required .env variables:
    MONGO_URI=<Your MongoDB Connection URI>
    PORT=9924
    SECRET_KEY=<Your JWT Secret Key>
    CLOUD_NAME=<Your Cloudinary Cloud Name>
    API_KEY=<Your Cloudinary API Key>
    API_SECRET=<Your Cloudinary API Secret>
    STRIPE_SECRET_KEY=<Your Stripe Secret Key>
    WEBHOOK_ENDPOINT_SECRET=<Your Stripe Webhook Secret Key>
    ```
4.  Start the development server:
    ```bash
    npm run dev # or yarn dev
    ```

### 2. Frontend Setup (`/client`)

1.  Navigate to the client directory (from the root):
    ```bash
    cd client
    ```
2.  Install dependencies:
    ```bash
    npm install # or yarn install
    ```
3.  (Optional) Create a `.env` file if you need to override the default server URL:
    ```# Example .env content:
    VITE_SERVER_URL=http://localhost:9924
    ```
4.  Start the development server:
    ```bash
    npm run dev # or yarn dev
    ```

## Usage

1.  Start both the backend and frontend servers.
2.  Navigate to the client URL (usually `http://localhost:5173`).
3.  Register a new user or log in.
4.  **Instructors:** Access the admin panel (e.g., `/admin/dashboard`) to create and manage courses/lectures.
5.  **Students:** Browse courses, purchase them via Stripe, and track progress in the "My Learning" section.

## Contributing

Contributions are welcome! Please fork the repository, create a feature branch, and submit a pull request.

## License

[MIT](LICENSE) (or specify your license if different)
