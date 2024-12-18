# UMass Buy and Sell

UMass Buy and Sell is a web application that allows students to easily create listings to sell items. Built with JavaScript, HTML/CSS, PouchDB, and Express.js, this full-stack marketplace leverages Google authentication for secure access. The application uses PouchDB to ensure secure, offline-first data storage and features optimized Express.js API endpoints for faster and more efficient data processing. Additionally, Figma mockups were designed to streamline the development process and align the application with user needs.  


# Getting Started

1. Download or clone this repository to your local machine.
2. Ensure that `.env` is present. If not, email one of the team members for access.
2. Open your terminal.
3. Navigate to the project directory.
4. Run `npm install` to install dependencies.
5. After the installation is complete, run `npm run dev`.
 
## File Structure

    /src: Coding files

      *note: `client/schema.js` is used by server and client, since it contains shared information*

      /client: HTML, CSS, and javascript files related to the frontend of the application

      /docs: Folder with milestone-1 document

      /server: Javascript files relating to backend and API endpoints

    .gitignore: Git ignores

    .htmlvalidate.json: HTML validation configs

    .env: Configs for running application. Also contains sensitive information such as google API keys.

    README.md: Readme file

    package-lock.json: JSON lock file

    package.json: JSON packages
    
## .env Parameters
- `GOOGLE_CLIENT_ID`: Public Google API key
- `GOOGLE_CLIENT_SECRET`: Private Google API key
- `HOST_URI`: IP and location where the application will be hosted. ex. `http://localhost:8080`
- `SESSION_SECRET_KEY`: Key used to encode sessions
- `DEV`: Set to truthy string in order to have the server generate fake data

## API Routes

### GET Endpoints

- `/api/listings`: Retrieve all listing IDs as a list of strings
- `/api/listings/:id`: Retrieve the JSON data of a listing
- `/api/listings/:id/exists`: Returns a JSON object that represents whether the given ID corresponds to a listing in the database. Formatted as `{exists: ...}`
- `/api/listings/:id/thumbnail`: Retrieve the thumbnail of a listing
- `/api/listings/:id/carousel/:index`: Retrieve a carousel image of a listing
- `/api/profiles`: Retrieve all profile IDs as a list of strings
- `/api/profiles/:id`: Retrieve a specific profile
- `/api/profiles/:id/exists`: Returns a JSON object that represents whether the given ID corresponds to a profile in the database. Formatted as `{exists: ...}`
- `/api/profiles/:id/postedListings`: Retrieve listing IDs posted by a specific profile
- `/api/self/profile`: Retrieve logged-in user's ID
- `/api/login/callback`: Endpoint for login callback
- `/api/login`: Login endpoint

### POST Endpoints

- `/api/profiles`: Create a new profile
- `/api/listings`: Create a new listing

### PUT Endpoints

- `/api/listings`: Update a listing
- `/api/profiles`: Update a profile

### DELETE Endpoints

- `/api/listings/:id`: Delete a listing

# Using UMass Buy and Sell

## User Base

UBay is a web application create for students at UMass Amherst to buy and sell items. Imagine yourself a college student who wants to sell or buy items from/for their dorm.

## Login Page

When first opening the web application, the user is prompted to create an account with our Google Authentication system. Clicking the 'Log in with Google' button leads the user to select a Google account to proceed with.

## Main Page

The top of the page includes a navigation bar to the "Home" page, search bar, "Sell" page, and "Profile" page.

The "Home" page is where listings from other students are posted in containers detailing product picture, product title, and price representing individual listings that can be clicked on to see full details. The intention is for the page to serve as a hub for postings made.

## Product Page

The top of the page includes a navigation bar to the "Home" page, search bar, "Sell" page, and "Profile" page.

The "Product" page displays pertinent information about an item being sold that includes title, quantity, price, description, and a seller information. At the bottom, there is a contact button that directly creates an email sent to the seller to inquire further. The intention is to allow a user to learn more about an item before making a buying decision.

## Seller Page

The top of the page includes a navigation bar to the "Home" page, search bar, "Sell" page, and "Profile" page.

The "Sell" page displays fill in boxes for a user to fill in to post an item they would like to sell that includes title, quantity, price, description, and a seller information. At the bottom, user presses a "Post" button to put item on the home page/marketplace. The intention is to allow a user to make postings for other student's to view.

## Profile Page

The top of the page includes a navigation bar to the "Home" page, search bar, "Sell" page, and "Profile" page.

The "Profile" allows the user to see their account details such as displayed name, profile picture, and email, which are automatically filled in by Google. Additionally, there is an items section that dynamically adds postings made by a user, wherein clicking a listing offers a delete button to remove an item from the home page/marketplace as appropriate. The intention is to allow a user to see what others see in terms of account details when they make a post.

(If there is an issue with posting listings and the listings dynamically updating to your profile page, please close the application, delete the listings folders, and re-open the application)
