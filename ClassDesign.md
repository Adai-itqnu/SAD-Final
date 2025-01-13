# UI Layer
## Classes:
### LoginUI
- **Attributes:** None
- **Methods:**
  - `displayLoginForm()`: Display login form to the user.
  - `submitLogin()`: Send login details to the Authentication subsystem.

### ParentUI
- **Attributes:** None
- **Methods:**
  - `viewParentDashboard()`: Show parent-specific dashboard.

### TeacherUI
- **Attributes:** None
- **Methods:**
  - `viewTeacherDashboard()`: Show teacher-specific dashboard.

### RegistrationUI
- **Attributes:** None
- **Methods:**
  - `displayRegistrationForm()`: Display the registration form to new users.
  - `submitRegistration()`: Send registration data to the system.

### CourseManagementUI
- **Attributes:** None
- **Methods:**
  - `displayCourseList()`: Show a list of courses to the user.
  - `manageCourse()`: Manage course operations like enrollment.

### NotificationUI
- **Attributes:** None
- **Methods:**
  - `viewNotifications()`: Display notifications to the user.

---

# Application Layer
## Classes:
### GroupController
- **Attributes:** None
- **Methods:**
  - `joinGroup(groupId)`: Allow a user to join a specific group.
  - `addLesson(groupId, lessonData)`: Add a lesson to a specific group.

### ServiceController
- **Attributes:** None
- **Methods:**
  - `manageServices()`: Coordinate system services (e.g., notifications, encryption).

### DatabaseService
- **Attributes:** None
- **Methods:**
  - `queryData(query)`: Execute database queries and return results.
  - `updateData(updateCommand)`: Update data in the database.

### EncryptionService
- **Attributes:** None
- **Methods:**
  - `encryptData(data)`: Encrypt sensitive information.
  - `decryptData(data)`: Decrypt sensitive information.

### NotificationController
- **Attributes:** None
- **Methods:**
  - `createNotification(notificationData)`: Create a new notification for the user.
  - `deleteNotification(notificationId)`: Remove an existing notification.

### LoginController
- **Attributes:** None
- **Methods:**
  - `authenticateUser(credentials)`: Validate user credentials during login.

### RegistrationController
- **Attributes:** None
- **Methods:**
  - `registerNewUser(userData)`: Handle new user registration.

---

# Data Layer
## Classes:
### NotificationLogStorage
- **Attributes:**
  - `logs`: Store logs of notifications.
- **Methods:**
  - `saveLog(logData)`: Save a new notification log.
  - `retrieveLog(logId)`: Retrieve a specific log by ID.

### UserStorage
- **Attributes:**
  - `userData`: Store user data.
- **Methods:**
  - `saveUser(user)`: Save user data to storage.
  - `getUser(userId)`: Retrieve user information by ID.

### Group
- **Attributes:**
  - `groupId`: Unique identifier for the group.
  - `groupName`: Name of the group.
- **Methods:**
  - `createGroup(groupData)`: Create a new group.
  - `deleteGroup(groupId)`: Delete a group.

### Course
- **Attributes:**
  - `courseId`: Unique identifier for the course.
  - `courseName`: Name of the course.
- **Methods:**
  - `addCourse(courseData)`: Add a new course.
  - `removeCourse(courseId)`: Remove a course.

### Lesson
- **Attributes:**
  - `lessonId`: Unique identifier for the lesson.
  - `lessonTitle`: Title of the lesson.
- **Methods:**
  - `addLesson(lessonData)`: Add lesson content.
  - `deleteLesson(lessonId)`: Remove a lesson.
