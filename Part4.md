### Quản lý Người Dùng

---

#### **Class Diagram**
![UserManagementSubSystem](https://www.planttext.com/plantuml/png/V5JFQzH05BxFN_6OYrbf2rvpa69N4BIBnQ7qEYOX6PfCscHIkeW7sMDFnRDWNFPGeQ3MYncAXrdwVynVuByWcz-JZUQov7tVuttlUz_cZ_ozdmgQY2mA4Ne41o5DKvWowYSqGaxvDlCVlcdvYKtLB-x3EmJbSwYM1c03uwB6daUKXJQa8c7SR_Ywk1Kl0rtSPC_MYsY07bD64lLZK2M9BdBkaq3bR03DVFLvJdIHnpQuL7Y2HLuVEj35xTais0pT8bogt261bjyTA-fKDGCcDhoDuz2Z7Br7jGMrlFxohU9kRQA-yl553jLFeelbeEghd1zbSoq_SEky-hMXBanik8YPsqcewtq9TQalOLpOLCih9pZMSaMIhBAcbT8Ew4WdhJ_jjFNrUi7zqiypo-kVTmV6FJGshTfFCbsiX2NYKu_tcEMU5U-KQRc8I4B9XhF5tBhBKQQB9N-bxbze-V7DGpuUrL0Ngxa1MSmj_PdOPhhh1gSBZzd6pSGReBd9fRgZ_nff7lPreBuqCMWbjqOq-RWmSxK3RdkkSODcXXNu2ORTNS2FSPjb6x2ZxZ1gtdkKHeqDUFDVWVMrbbSym6Wq8tjxJmVVYAPFb0IC_d-cqVxpiWL2TO-HuT26tLkXCWhIMEK28xJlSJUBmhy0003__mC0)

@startuml

' Class Diagram
class NgườiDùng {
    + MãNgườiDùng: int
    + Email: string
    + MậtKhẩuBăm: string
    + VaiTrò: string
    + TrạngThái: string
    + NgàyTạo: datetime
    + NgàyCậpNhật: datetime
    + xácThực(mậtKhẩu: string): boolean
}

class VaiTrò {
    + MãVaiTrò: int
    + TênVaiTrò: string
    + MôTả: string
    + gánQuyền(quyền: Quyền): void
}

class Quyền {
    + MãQuyền: int
    + MãVaiTrò: int
    + DịchVụTruyCập: string
}

class DịchVụXácThực {
    + đăngNhập(email: string, mậtKhẩu: string): string
    + đăngXuất(token: string): void
    + kiểmTraToken(token: string): boolean
}

class QuảnLýHồSơNgườiDùng {
    + lấyNgườiDùng(id: int): NgườiDùng
    + cậpNhậtNgườiDùng(ngườiDùng: NgườiDùng): void
    + xóaNgườiDùng(id: int): void
}

class PhânQuyền {
    + kiểmTraQuyền(vaiTrò: string, dịchVụ: string): boolean
}

NgườiDùng "1" -- "*" VaiTrò : "có"
VaiTrò "1" -- "*" Quyền : "xác định"
DịchVụXácThực ..> NgườiDùng : "xác thực"
QuảnLýHồSơNgườiDùng ..> NgườiDùng : "quản lý"
PhânQuyền ..> VaiTrò : "kiểm soát"

@enduml


## Sequence Diagram
![CourseManagementSubsystem](https://www.planttext.com/plantuml/png/Z9FDIWCn58NtUOgpKy7YlWkfq9MWY3-uJgTn9dJcZarl1cOfVG8VG6YL8We54JTc5bsC-1vv0bz1AbOxE5Lt8Ravvxlt96_5h3LWQTWciH1hE59zgoXGQ6iP6fa86N1gi1--FlZYIhVBPmf59xNKbIR7ZkL84Uj0iaxfI9bC1qe4AR59OvmCb3amwPcErPua6IhpTNIOVk_D1JX7MxBio84IecA6ndQzJHEXBwOQ79LF588ruUNoPKWXAF9kUevrbKWTRoBnRiheHTxTsGrHgpKtMVWtqTE-62PW8vV5wPCAtOyPBChHM0t8nhiRPBwu-4Le9T3IZ2fCcTHWKpuYAqVeszmN5oIMYlycwdatO_Jjn_fRUA6rWgYnNNq6bVvsJu-npb4veWZ1lDKjSEJTXD7nRgmtQbBz-JoQoCjxYy2xMulOkqc-FBUW78EYyfh4pvlL0DdO79bt4_flW7Ki_qgl3kNNGTKs95gAklCV-0u00F__0m00)

@startuml

' Sequence Diagram
actor NgườiDùng
boundary AuthenticationService
control UserProfileManager
control RoleManager
entity Database

NgườiDùng -> AuthenticationService: gửi thông tin đăng nhập (email, mật khẩu)
AuthenticationService -> Database: kiểm tra thông tin người dùng
Database --> AuthenticationService: trả về thông tin người dùng
AuthenticationService -> RoleManager: kiểm tra vai trò và quyền
RoleManager --> AuthenticationService: trả kết quả kiểm tra quyền
AuthenticationService --> NgườiDùng: trả về JWT (thành công/ thất bại)

NgườiDùng -> UserProfileManager: yêu cầu lấy thông tin cá nhân
UserProfileManager -> Database: truy vấn thông tin người dùng
Database --> UserProfileManager: trả về thông tin người dùng
UserProfileManager --> NgườiDùng: trả về thông tin cá nhân

@enduml



