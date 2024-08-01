# **Video Uploading Platform**

This is a backend project for a video-uploading platform, utilizing Node.js, Express, MongoDB Atlas, and Cloudinary for file uploads. The platform supports user registration, login, video uploads, and other related functionalities.

## **Features**

- User Registration and Authentication
- Video Uploading and Management
- User Profile Management
- Subscription Management
- Playlist Management
- Commenting System
- Like System
- Watch History
- Health Check

## **Technologies Used**

- **Backend:** Node.js, Express.js
- **Database:** MongoDB Atlas
- **File Uploads:** Cloudinary, Multer
- **Authentication:** JWT (JSON Web Tokens)

## **Installation**

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/video-uploading-platform.git
   cd video-uploading-platform
   Install dependencies and create .env file:

bash
Copy code
npm install


 ## **env**
 Create a .env file in the root directory and add the following environment variables:
 ```bash
- MONGO_URI=your_mongodb_atlas_uri
- CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
- CLOUDINARY_API_KEY=your_cloudinary_api_key
- CLOUDINARY_API_SECRET=your_cloudinary_api_secret
- ACCESS_TOKEN_SECRET=your_access_token_secret
- REFRESH_TOKEN_SECRET=your_refresh_token_secret
bash
Start the server:


Copy code
npm start
API Endpoints
User Routes

 ## **Register User**
Register User

URL: /api/users/register
Method: POST
Body:
json
Copy code
{
  "fullName": "shivendra",
  "email": "abc.com",
  "username": "tsrshiv",
  "password": "password123"
}
Login User

URL: /api/users/login
Method: POST
Body:
json
Copy code
{
  "email": "abc.com",
  "password": "password123"
}
Logout User

URL: /api/users/logout
Method: POST
Refresh Access Token

URL: /api/users/refresh-token
Method: POST
Change Password

URL: /api/users/change-password
Method: PUT
Body:
json
Copy code
{
  "oldPassword": "oldpassword123",
  "newPassword": "newpassword123"
}
Get Current User

URL: /api/users/me
Method: GET
Update Account Details

URL: /api/users/update
Method: PUT
Body:
json
Copy code
{
  "fullName": "John Doe",
  "email": "john@example.com"
}
Update User Avatar

URL: /api/users/update-avatar
Method: PUT
Form Data: avatar (file)
Update User Cover Image

URL: /api/users/update-cover-image
Method: PUT
Form Data: coverImage (file)
Get User Channel Profile

URL: /api/users/channel/:username
Method: GET
Get Watch History

URL: /api/users/watch-history
Method: GET
Other Routes
Health Check
URL: /api/healthcheck
Method: GET
Controllers
Comment Controller
Dashboard Controller
Healthcheck Controller
Like Controller
Playlist Controller
Subscription Controller
Tweet Controller
User Controller
Video Controller
Utilities
ApiError
ApiResponse
asyncHandler
cloudinary
