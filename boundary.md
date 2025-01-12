| Lớp Phân Tích      | Phần Tử Thiết Kế        |
|---------------|---------------|
| LoginUI | LoginUI |
| RegistrationUI    | RegistrationUI  |
|CourseManagementUI  |  CourseManagementUI  |
| TeacherUI | TeacherUI   |
| ParentUI | ParentUI |
|NotificationUI | NotificationUI |
|GroupCreationUI <br> GroupJoinUI | GroupManagementUI SubSystem <br> IGroupManagementUI Interface|
|ServiceUI | ServiceUI Subsystem <br> IServiceUI Interface|
| Parent <br> Teacher<br>Student<br>Member<br>UserAccount| UserAccount |
| Group  | Group  |
|Course  |  Course  |
| Lesson | Lesson  |
|NotificationLogStorage <br> NotificationStorage| Notification Subsystem <br>  INotification Interface |
|UserStorage | UserStorage Subsystem <br> IUserStorage Interface |
|DatabaseService | DatabaseService Subsystem <br> IDatabaseService Interface |
| LoginController            | Login                             |
| EncryptionService          | Encryption Subsystem<br>IEncryptionService Interface |
| RegistrationController     | Registration                      |
| NotificationController     | Notification Subsystem<br>INotificationController Interface |
| GroupController<br> JoinGroup <br> AddLesson          | Group Subsystem<br>IGroupController Interface <br>IAddLesson <br> IJoinGroup|
| ProgressController         | Tracking                         |
| ServiceController          | Service Subsystem<br>IServiceController Interface |
