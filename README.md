# MentorConnect

MentorConnect is an innovative platform designed to bridge the gap between mentors and mentees, providing a streamlined, user-friendly experience to facilitate professional growth, skill development, and personal mentoring. The app enables users to easily connect with industry experts, gain valuable insights, and receive guidance tailored to their specific career goals. With features like profile matching, session scheduling, and live mentoring sessions, MentorConnect empowers users to achieve their full potential by making mentorship accessible, effective, and personalized.


## Table of Contents

* [Screenshots](#screenshots)
* [Acknowledgements](#acknowledgements)
* [Technologies](#technologies)
* [Usage](#usage)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
  * [Environment Variables Setup](#environment-variables-setup)
  * [Run The App](#run-the-app)
* [Features](#features)
  * [User Account Management](#user-account-management)
  * [Admin Dashboard](#admin-dashboard)
  * [Shopping Cart System](#therapist-shopping-cart-system)
  * [Live Chat Session](#live-chat-session)
* [Awards](#awards)
* [Contributing](#contributing)

## Screenshots

| ![Login Page](screenshots/login.png) | ![Home Page](screenshots/home.png) |
|:--:|:--:|
| _Login Page_ | _Home Page_ |
| ![Mentors Page](screenshots/therapists.png) | ![Checkout Page](screenshots/checkout.png) |
| _Mentors Page_ | _Checkout Page_ |
| ![Profile Page](screenshots/profile.png) | ![Live Chat Popup](screenshots/chat-session.png) |
| _Profile Page_ | _Live Chat Popup_ |


## Technologies

* HTML5
* CSS3
* Ajax
* JavaScript
* jQuery `v3.6.0`
* Node.js
* Express `v4.18.1`
* Express-Session `v1.17.2`
* MongoDB / Mongoose `v6.3.3`
* Multer `v1.4.4`
* Nodemailer `v6.7.5`
* Nodemon `v2.0.16`
* Socket.IO `v4.5.1`

## Usage

<details>
  <summary>Prerequisites</summary>

### Prerequisites

* [VSCode](https://code.visualstudio.com/download/)
* [Git](https://git-scm.com/downloads/)
* [Node.js](https://nodejs.org/en/download/)

</details>

<details>
  <summary>Installation</summary>

### Installation

1. Install the latest npm package version.

  ```sh
  npm install npm@latest -g
  ```

2. Clone the repository to your local machine.

  ```sh
  git clone https://github.com/towaquimbayo/MyMind.git
  ```

3. Installing required dependencies requires Node and npm.

  ```sh
  npm install
  ```

</details>

<details>
  <summary>Environment Variables Setup</summary>

### Environment Variables Setup

For the project to run correctly, environment variables are required. Rename the `.env.example` to `.env`.

1. Sign up for a MongoDB Atlas account at <https://www.mongodb.com/cloud/atlas/register>. Then create a database Cluster and connect your project to that Cluster by clicking on the `Connect`, selecting the `Connect To Your Application` option and copying the Database `URI` string as your `DATABASE_URL`. Finally, replace the `username` and `password` fields in the URI string with your database credentials.
2. Either enter your email account credentials for the Nodemailer transporter credentials or create a Gmail account to generate an App Password by following the instructions at <https://medium.com/@y.mehnati_49486/how-to-send-an-email-from-your-gmail-account-with-nodemailer-837bf09a7628>.

</details>

<details>
  <summary>Run The App</summary>

### Run The App

Running the application locally or in production is straightforward since both the frontend and backend are integrated into a single Node.js application running on port 8000.

Execute `npm start` to run locally in development mode or production mode.

</details>

## Features

### User Account Management

Our user account management system allows users to create and manage their accounts securely with ease. Whether they are mentors or mentees, users have control over their profile information.

* __Account Creation__: Users can create mentor or mentee accounts. Mentors are required to enter additional information regarding their session cost and professional experience.
* __Account Editing__: Users can edit their profile information, including profile picture, name, email, and phone number.
* __Account Deletion__: Users have the option to delete their accounts.

### Admin Dashboard

Our Admin Dashboard provides administrators with comprehensive tools to manage all users registered on the application. This feature ensures that administrators can maintain control over the platform's user base and perform various administrative tasks efficiently.

* __User Management__: View all users in a table format on the Admin Dashboard page. Administrators can also edit mentee and mentor information, create new users including administrators, and delete user accounts if necessary.
* __Search and Filter__: Search users by keywords and filter the table accordingly.
* __Sorting Table__: Sort the user table by clicking on headings such as email or username in ascending or descending order.

### Shopping Cart System

Our application features a mentor shopping cart system, allowing users to browse and "purchase" live chat sessions with mentors. Although a payment integration system is not yet implemented, mentees can simulate the process of adding mentors to their cart and checking out.

* __Therapist Listings__: Any user can view a list of available mentors for live chat sessions.
* __Shopping Cart__: Registered mentees can add or remove mentors to their shopping cart and proceed to the Checkout page. The Checkout cart page also displays the total price including tax for the cart items.
* __Invoice Generation__: Mentees can print an invoice PDF of their order from the Checkout page.
* __Order Confirmation__: After confirming their cart and checking out, mentees are navigated to a Thank You page and receive an email confirmation. They can start a live chat session with the ordered mentor immediately.
* __Pricing Plans__: 4 different pricing plans are available for mentor sessions: Trial, 1 Month, 3 Months, and 1 Year (mocked up to reasonable timeframes in minutes).

### Live Chat Session

We enable real-time communication between mentors and mentees using Socket.io. This feature allows for seamless live chat sessions, enhancing the user experience.

* __Real-Time Communication__: Bi-directional private communication for live mentor chat sessions.
* __Contact Information__: Both mentee and mentor can access each other’s phone numbers during the live chat session for private communication via text or phone call.
* __Session Timer__: Display of remaining session time in real-time, with the chat ending automatically when time expires.
