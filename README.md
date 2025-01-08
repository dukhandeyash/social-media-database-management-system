# Social Media Database Management System

## Project Overview

In today's digital era, social media platforms have become integral parts of our daily lives, enabling connections, sharing of multimedia content, and interactions among users. To manage such a platform, a robust and reliable database system is crucial. Our project aims to develop such a **Database Management System** to drive social media applications.

The project develops a **Database Management System (DBMS)** tailored for social media, implementing key functionalities such as managing user profiles, sharing multimedia content, and enabling user interactions through comments and likes. The relational database schema is designed to handle various components of a social media application, including personal information storage, content management, interaction tracking, and user activity logging.

## Database Schema Overview

The database schema consists of several interconnected components, each dedicated to a specific feature of a social media platform. Below is an overview of the core database relations:

### 1. **Users**  
- **Description**: Stores user profiles along with their personal information (name, email, etc.).
- **Key Attributes**: User ID, Name, Email, Date of Birth, etc.

### 2. **Photos and Videos**  
- **Description**: Handles multimedia content such as photos and videos uploaded by users, each linked to specific posts.
- **Key Attributes**: Media ID, File Path, Type (photo/video), Associated Post ID.

### 3. **Post**  
- **Description**: Stores the content of user-generated posts, including captions and location tags.
- **Key Attributes**: Post ID, User ID (foreign key), Caption, Location, Timestamp.

### 4. **Comments, Post Likes, and Comment Likes**  
- **Description**: Allows user interaction with posts and comments. Users can comment on posts or like posts and comments.
- **Key Attributes**:
  - **Comments**: Comment ID, User ID (foreign key), Post ID (foreign key), Comment Text, Timestamp.
  - **Post Likes**: Like ID, User ID (foreign key), Post ID (foreign key).
  - **Comment Likes**: Like ID, User ID (foreign key), Comment ID (foreign key).

### 5. **Follows**  
- **Description**: Models the actual social network, allowing users to connect with one another by following other users.
- **Key Attributes**: Follower User ID, Followed User ID.

### 6. **Hashtags and Post Tags**  
- **Description**: Enhances content discoverability by linking posts and users to trending topics via hashtags.
- **Key Attributes**:
  - **Hashtags**: Hashtag ID, Name.
  - **Post Tags**: Post ID (foreign key), Hashtag ID (foreign key).

### 7. **Bookmarks**  
- **Description**: Allows users to save posts for later viewing.
- **Key Attributes**: Bookmark ID, User ID (foreign key), Post ID (foreign key), Timestamp.

### 8. **Login**  
- **Description**: Tracks user login instances to enhance security and monitor user activity.
- **Key Attributes**: Login ID, User ID (foreign key), Login Timestamp, Device Type.

## Features

- **User Profile Management**: Store and retrieve user profiles with details such as name, email, and date of birth.
- **Multimedia Content Sharing**: Handle photos and videos shared by users and link them to posts.
- **Post Interaction**: Support for liking posts, commenting on posts, and liking comments.
- **Social Network Modeling**: Enable users to follow each other and form connections.
- **Content Discoverability**: Use hashtags to categorize and link posts with trending topics.
- **Bookmarks**: Allow users to save posts they are interested in for later reference.
- **Login Tracking**: Log user login instances for enhanced security and user activity monitoring.

## Database Relations

- **Users**  
  Stores essential user information for the platform.

- **Photos and Videos**  
  Manages multimedia files associated with posts.

- **Post**  
  Represents shared content including user-generated captions and location tags.

- **Comments, Post Likes, and Comment Likes**  
  Tracks user interactions with posts and comments.

- **Follows**  
  Models the network of users following each other.

- **Hashtags and Post Tags**  
  Provides a system for linking posts to trending topics.

- **Bookmarks**  
  Allows users to bookmark their favorite posts.

- **Login**  
  Tracks login history and security.

## Setup Instructions

### Prerequisites

- **MySQL**: Ensure MySQL is installed on your machine. You can download it from [here](https://dev.mysql.com/downloads/installer/).
- **SQL Client**: A MySQL client (e.g., MySQL Workbench) to execute the SQL queries.

### Steps to Set Up

1. **Clone the Repository**
