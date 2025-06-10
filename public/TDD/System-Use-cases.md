
### **Technical System Use Cases**

#### **Actors**
1. **Resident User (USER)**: A regular user of the system who interacts with community features, profile management, notifications, payments, and complaints.
2. **Admin (ADMIN)**: A privileged user responsible for managing users, payments, complaints, and dashboard statistics.
3. **System (SYSTEM)**: The backend system responsible for automated tasks such as email notifications, database backups, and activity logging.

---

### **Authentication Use Cases**
1. **Register Account (UC1)**  
   - **Description**: Allows a user to create an account in the system.  
   - **Technical Details**:  
     - Endpoint: `POST /register`  
     - Input: User details (e.g., name, email, password).  
     - Output: Success or error message.  
     - Dependencies: Database for storing user credentials.

2. **Login to System (UC2)**  
   - **Description**: Enables a user to log in using their credentials.  
   - **Technical Details**:  
     - Endpoint: `POST /login`  
     - Input: Email and password.  
     - Output: Authentication token.  
     - Dependencies: Database for verifying credentials.

3. **Reset Password (UC3)**  
   - **Description**: Allows a user to reset their password.  
   - **Technical Details**:  
     - Endpoint: `POST /reset-password`  
     - Input: Email address.  
     - Output: Password reset link sent via email.  
     - Dependencies: Email service (e.g., Nodemailer).

4. **Admin Login (UC4)**  
   - **Description**: Enables an admin to log in with elevated privileges.  
   - **Technical Details**:  
     - Endpoint: `POST /admin/login`  
     - Input: Admin credentials.  
     - Output: Admin authentication token.  
     - Dependencies: Database for verifying admin credentials.

---

### **Community Use Cases**
1. **View Community Posts (UC5)**  
   - **Description**: Allows users to view posts in the community.  
   - **Technical Details**:  
     - Endpoint: `GET /posts`  
     - Output: List of posts.  
     - Dependencies: Database for fetching posts.

2. **Create Post (UC6)**  
   - **Description**: Enables users to create a new post.  
   - **Technical Details**:  
     - Endpoint: `POST /posts`  
     - Input: Post content.  
     - Output: Success or error message.  
     - Dependencies: Database for storing posts.

3. **Edit Own Post (UC7)**  
   - **Description**: Allows users to edit their own posts.  
   - **Technical Details**:  
     - Endpoint: `PUT /posts/:id`  
     - Input: Updated post content.  
     - Output: Success or error message.  
     - Dependencies: Database for updating posts.

4. **Delete Own Post (UC8)**  
   - **Description**: Enables users to delete their own posts.  
   - **Technical Details**:  
     - Endpoint: `DELETE /posts/:id`  
     - Output: Success or error message.  
     - Dependencies: Database for deleting posts.

5. **Add Comment (UC9)**  
   - **Description**: Allows users to add comments to posts.  
   - **Technical Details**:  
     - Endpoint: `POST /comments`  
     - Input: Comment content and post ID.  
     - Output: Success or error message.  
     - Dependencies: Database for storing comments.

6. **View Comments (UC10)**  
   - **Description**: Enables users to view comments on posts.  
   - **Technical Details**:  
     - Endpoint: `GET /comments/:postId`  
     - Output: List of comments.  
     - Dependencies: Database for fetching comments.

---

### **Profile Management Use Cases**
1. **View Profile (UC11)**  
   - **Description**: Allows users to view their profile.  
   - **Technical Details**:  
     - Endpoint: `GET /profile`  
     - Output: User profile details.  
     - Dependencies: Database for fetching user data.

2. **Update Profile (UC12)**  
   - **Description**: Enables users to update their profile information.  
   - **Technical Details**:  
     - Endpoint: `PUT /profile`  
     - Input: Updated profile details.  
     - Output: Success or error message.  
     - Dependencies: Database for updating user data.

3. **View Other Profiles (UC13)**  
   - **Description**: Allows users to view other users' profiles.  
   - **Technical Details**:  
     - Endpoint: `GET /profile/:userId`  
     - Output: Profile details of the specified user.  
     - Dependencies: Database for fetching user data.

---

### **Notification System Use Cases**
1. **View Notifications (UC14)**  
   - **Description**: Enables users to view their notifications.  
   - **Technical Details**:  
     - Endpoint: `GET /notifications`  
     - Output: List of notifications.  
     - Dependencies: Database for fetching notifications.

2. **Mark as Read (UC15)**  
   - **Description**: Allows users to mark notifications as read.  
   - **Technical Details**:  
     - Endpoint: `PUT /notifications/:id`  
     - Output: Success or error message.  
     - Dependencies: Database for updating notification status.

3. **Send Reply (UC16)**  
   - **Description**: Enables users to reply to notifications.  
   - **Technical Details**:  
     - Endpoint: `POST /notifications/reply`  
     - Input: Reply content.  
     - Output: Success or error message.  
     - Dependencies: Database for storing replies.

4. **Delete Notification (UC17)**  
   - **Description**: Allows users to delete notifications.  
   - **Technical Details**:  
     - Endpoint: `DELETE /notifications/:id`  
     - Output: Success or error message.  
     - Dependencies: Database for deleting notifications.

---

### **Payment System Use Cases**
1. **View Payments (UC18)**  
   - **Description**: Enables users to view their payment details.  
   - **Technical Details**:  
     - Endpoint: `GET /payments`  
     - Output: List of payments.  
     - Dependencies: Database for fetching payment data.

2. **Process Payment (UC19)**  
   - **Description**: Allows users to process payments.  
   - **Technical Details**:  
     - Endpoint: `POST /payments`  
     - Input: Payment details.  
     - Output: Success or error message.  
     - Dependencies: Payment gateway integration.

---

### **Admin Management Use Cases**
1. **Manage Users (UC29)**  
   - **Description**: Enables admins to manage user accounts.  
   - **Technical Details**:  
     - Endpoint: `GET /admin/users`  
     - Output: List of users.  
     - Dependencies: Database for fetching user data.

