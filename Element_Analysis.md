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



![markdown](https://www.planttext.com/plantuml/png/d5PBRjmm3Dth54GsMUK2NXIP9aKnG58KJNC0LUOuGZoI8T8J14LFraMFr2iKakLOjgoCqQN9nuyU7md__VtdcbWwxe-jwAHwbWt2nRskwnPVfCEgUjnNrQxd9pIibMHjpGNy5000gfL4S6SRRHxtYUKRDfhO1UpZNlmIK-9TrxKn2msfRspl2E5U6jdW4GtFim_koJihD3ZJNf38cZCLlwDKJ-YA9QF_RETVfKF3nJI3Uv5bIUmNo_gmIclgURULpyxsNR6BuCtequRH7QH2sAy3ak2K6IVLipRDh9kFFMc3HF20xgGLHdRYLx6nwCyRcXplq4_lpCyxTqhPtd2H-ssyYqLhMtqtrh2pROkksC03MoSRhm92b_SVtSiYgUjivbl9yeSad6SVhP7cPOMbkrW5LUyqlswu3ONBi27r9wFSQvUddUo5L-I0CuhTgDQ2LdtsIxZ5WpO8DNPeQZHA8ubu7E7gwiD01bJG4vAOtyZWJqqZR7u50YmrZR1iYGDok0mL78EZX1gNsWEjqMmTYRST38YHd2bJic81aUWIAY2s3aaif1I0Itr11VhOjQ4V4jdOXfZSF8kQ4H82YXGDxfo7AiqdBc6IuyeuLruifnr0ylNSVC8X97_wG5J0GorPva_9OnooqtX20fE0Xv6C3HMOxj2H9gQXrjfurfZ6mHQZ_cj4G76bD-YPqDJBjubBsDKrrg2iCQY24TW26keTWhA-4gFVwJDgc2xpfEP5iKaegSezyQrah86jYFyiOQd37mTKlZMMsf28bZo19DAD6JAyBLswf-oD15AnFdcoPg05JUnqqtYPpSQGpDhPawwHuD2RG9XiVSeKdGj4AeL464UT_tg5iFZuYJuL32J67vwrTXqgr5wqVLVx7H5lFrcm1Js_HmKg5dESnwmhsyidKUUqtgKIRK3WAHoARCDNfVo2hR97N7HtZQRslzp_0000__y30000)
