| **Lớp Phân Tích**         | **Phần Tử Thiết Kế**                         |
|----------------------------|----------------------------------------------|
| LoginController            | Login                             |
| EncryptionService          | EncryptionService Subsystem<br>IEncryptionService Interface |
| RegistrationController     | Registration                      |
| NotificationController     | Notification Subsystem<br>INotificationController Interface |
| GroupController<br> JoinGroup <br> AddLesson          | Group Subsystem<br>IGroupController Interface |
| ProgressController         | Tracking                         |
| ServiceController          | Service Subsystem<br>IService Interface |


### Design-Element-to-Owning-Package Map

| Design Element                        | Owning Package                           |
|---------------------------------------|------------------------------------------|
| LoginUI                               | Middleware::UI::Authentication           |
| RegistrationUI                        | Middleware::UI::Authentication           |
| CourseManagementUI                    | Applications::UI::Course Management      |
| TeacherUI                             | Applications::UI::Teacher Management     |
| ParentUI                              | Applications::UI::Parent Management      |
| NotificationUI                        | Middleware::UI::Notification             |
| GroupManagementUI SubSystem           | Applications::Group Management           |
| IGroupManagementUI Interface          | Applications::Group Management           |
| ServiceUI Subsystem                   | Business Services::UI::Service Management|
| IServiceUI Interface                  | Business Services::UI::Service Management|
| UserAccount                           | Applications::User Management            |
| Group                                 | Applications::Group Management           |
| Course                                | Applications::Course Management          |
| Lesson                                | Applications::Course Management          |
| Notification Subsystem                | Middleware::Notification                 |
| INotification Interface               | Middleware::Notification                 |
| UserStorage Subsystem                 | Middleware::Storage::User                |
| IUserStorage Interface                | Middleware::Storage::User                |
| DatabaseService Subsystem             | Middleware::Storage::Database            |
| IDatabaseService Interface            | Middleware::Storage::Database            |
| Login                                 | Middleware::Security::Authentication     |
| EncryptionService Subsystem           | Middleware::Security::Encryption         |
| IEncryptionService Interface          | Middleware::Security::Encryption         |
| Registration                          | Middleware::Security::Authentication     |
| Notification Subsystem                | Middleware::Notification                 |
| INotificationController Interface     | Middleware::Notification                 |
| Group Subsystem                       | Applications::Group Management           |
| IGroupController Interface            | Applications::Group Management           |
| Tracking                              | Applications::Tracking                   |
| Service Subsystem                     | Business Services::Service Management    |
| IService Interface                    | Business Services::Service Management    |


