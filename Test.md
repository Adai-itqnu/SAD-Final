@startuml
interface IUser {
    + CreateUser(username: string, password: string): bool
    + GetUserDetails(userId: int): UserAccount
    + UpdateUser(userId: int, newUsername: string): bool
    + DeleteUser(userId: int): bool
}

class UserAccount {
    - Id: int
    - Username: string
    - Password: string
    - Email: string
    - CreatedDate: DateTime
    + GetProfile(): string
    + SetPassword(newPassword: string): void
}

IUser <|-- UserAccount

interface IGroupController {
    + CreateGroup(groupName: string): bool
    + AssignUserToGroup(userId: int, groupId: int): bool
    + RemoveUserFromGroup(userId: int, groupId: int): bool
    + GetGroupDetails(groupId: int): Group
}

class Group {
    - Id: int
    - Name: string
    - Members: List<UserAccount>
    - CreatedDate: DateTime
    + AddMember(user: UserAccount): bool
    + RemoveMember(userId: int): bool
    + GetMemberList(): List<UserAccount>
}

IGroupController <|-- Group

interface IService {
    + AddCourse(course: Course): bool
    + RemoveCourse(courseId: int): bool
    + AddLessonToCourse(lesson: Lesson, courseId: int): bool
    + GetCourseDetails(courseId: int): Course
    + ListCourses(): List<Course>
}

class Course {
    - Id: int
    - Title: string
    - Description: string
    - Lessons: List<Lesson>
    + AddLesson(lesson: Lesson): bool
    + RemoveLesson(lessonId: int): bool
    + GetLessonList(): List<Lesson>
}

class Lesson {
    - Id: int
    - Title: string
    - Content: string
    - Duration: int
    + GetSummary(): string
    + SetContent(newContent: string): void
}

IService <|-- Course
IService <|-- Lesson

interface IStorage {
    + SaveData(data: object, key: string): bool
    + LoadData(key: string): object
    + DeleteData(key: string): bool
    + ListKeys(): List<string>
}

class Storage {
    - DatabaseFile: string
    + SaveData(data: object, key: string): bool
    + LoadData(key: string): object
    + DeleteData(key: string): bool
    + ListKeys(): List<string
}

IStorage <|-- Storage

interface IAuthentication {
    + Login(username: string, password: string): string
    + Logout(token: string): bool
    + ValidateToken(token: string): bool
    + ResetPassword(userId: int, email: string): bool
}

class Authentication {
    - Token: string
    + Login(username: string, password: string): string
    + Logout(token: string): bool
    + ValidateToken(token: string): bool
    + ResetPassword(userId: int, email: string): bool
}

IAuthentication <|-- Authentication

' Relationships
UserAccount --> IGroupController : "Belongs to Group"
Group --> IService : "Manages Courses & Lessons"
IStorage --> UserAccount : "Persists Data"
IStorage --> Group : "Persists Data"
IStorage --> Course : "Persists Data"
IStorage --> Lesson : "Persists Data"
IAuthentication --> IUser : "Authenticates"
@enduml
