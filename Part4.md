### Quản lý người dùng


## CLass Diagram
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
