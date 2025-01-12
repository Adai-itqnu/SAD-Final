## Các lớp phân tích  

### 1. Thực thể (Entity)  
- **Service**: Đại diện cho các dịch vụ được cấu hình.  
  - **Thuộc tính**:  
    - `serviceID`  
    - `name`  
    - `configurationOptions`  
  - **Phương thức**:  
    - `configure(options)`  

### 2. Biên (Boundary)  
- **ServiceUI**: Giao diện cấu hình dịch vụ.  
  - **Phương thức**:  
    - `displayServices()`  
    - `updateConfiguration()`  

### 3. Điều khiển (Control)  
- **ServiceController**: Quản lý các yêu cầu cấu hình dịch vụ.  
  - **Phương thức**:  
    - `getServiceList()`  
    - `updateServiceConfiguration(serviceID, options)`  

---

## Biểu đồ Sequence Diagram  
![Cấu hình dịch vụ](
https://www.planttext.com/plantuml/png/b92nIWCn6CVtFCNt0ds13bAee0vEMgZZDHSkWUkNaaiEEtVeK0IT7UmDHH2xEJM3G_eYtnFu2dAMzb8ugOu9-Vt_-V--_6Uli8cnRfopX5jjO508mqRQOPgOATm8Koek1bUCQxH6v_kR_kwO2yC4McKFJnch4w1prh1Ts3vkPvW1Ijgi9r26fGP9VWvMad_2h0sv9ly2cKeqf8hy787JPkL0XdUKa99VS0ab-HKxC550yxikt8KtLyEl3j849HIXugq93HGbTU7Mk2dSEzgiR1ImXw3Jtdh-vwhZsPUA_0n_n2pYkXP3VKd-0UFuscmzTJtPgRQnj9EYBiYlrP7cCVbdTK9F_qJTRuA6eU8xh5uRbYY1Xm_C_gd8oXg2KQZqSKnFOEh6-JS0003__mC0)


---

## Biểu đồ Class Diagram  

![Cấu hình dịch vụ](
https://www.planttext.com/plantuml/png/R8rD2i8m48NtESKixQ8t2ALGDmN1XVG0CHbB84rACX6AU38N7iahIF-jkXbctdlplTVZcGSIdc9Zc3GY13YXlsg9m7aaRJHrMNPZ001XDChzS5dHuB18Po-wZbwGTlROzZDi3DmbxCwszAe4piykAk4NljAXDQAR4c6N36fibI0iFal-y0fdoJjZq0FdSZncReqqfGuwq0QxVd_JVxcGfXdCVRDVbRs-o6kSvMXLRCmR003__mC0).
