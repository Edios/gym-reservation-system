# Gym Reservation System
A complete gym reservation system that allows users to view available classes, sign up or cancel class reservations, and manage their gym activities through a calendar interface. This project is divided into two main parts:

- **Cient (Frontend)**: Built with React and Tailwind CSS.
- **Server (Backend)**: Built with Node.js, Express, and MongoDB for API services and user authentication.

-----------------
## Features
- **User Authentication**: Simple login system to manage registered accounts.
- **Calendar View**: Displays available gym classes in a calendar format.
- **Class Details**: View details for each class, including the coach, location, and available seats.
- **Reservations**: Sign up or cancel reservations for gym classes. The class entry updates automatically in the calendar view.

-----------------
## Project Structure
gym-reservation-system/

├── gym-reservation-server/          # Backend submodule (API and database)  
├── gym-reservation-client/         # Frontend submodule (React app for user interface)  
├── .gitmodules       # Configuration file for Git submodules  
└── README.md         # Project documentation  

-----------------
## Installation
1. **Clone the Repository**  
Clone the main repository, including both frontend and backend submodules:
```
git clone --recurse-submodules https://github.com/Edios/gym-reservation-system
```
Or, if you’ve already cloned the repo without submodules, initialize and update them:
```
git submodule init
git submodule update
```
2. **Install Dependencies**
### Backend  
Navigate to the `gym-reservation-server` directory and install dependencies:
```
cd gym-reservation-server
npm install
```
### Frontend  
Navigate to the `gym-reservation-client` directory and install dependencies:
```
cd gym-reservation-client
npm install
```
3. **Setup mongo db server**
Run local mongo server or use already existing one
For more details about running self hosted db visit this tutorial: https://www.mongodb.com/docs/manual/tutorial/manage-mongodb-processes/

4. **Setup Environment Variables*
Each part of the project requires environment variables. Create `.env` files in both `gym-reservation-server` and `gym-reservation-client` directories.

### Backend gym-reservation-server `.env` File
JWT Secret can be generated here: https://jwtsecret.com/generate
```
MONGO_URI=<your_mongodb_connection_string> 
JWT_SECRET=<your_jwt_secret> 
PORT=5000
```
### Frontend gym-reservation-client `.env` File
Create .env file with address to your backend
```
REACT_APP_API_URL=http://localhost:5000/api
```
5. **Running the Application**

Navigate to the `gym-reservation-server` and start server:
```
cd gym-reservation-server
npm start
```
Navigate to the `gym-reservation-client` and start server:
```
cd gym-reservation-client
npm start
```
