# Kết quả phân tích của Use Case 5: Gửi thông báo đến học viên

## Lớp phân tích

### **Boundary (Ranh giới)**

#### a. **NotificationUI**  
- **Mô tả**: Giao diện cho phép giáo viên hoặc quản trị viên gửi thông báo đến học viên.  
- **Thuộc tính**: *(Chưa được liệt kê)*  
- **Phương thức**:  
  - `sendNotification()`  
  - `displayResult()`  

---

### **Control (Điều khiển)**

#### a. **NotificationController**  
- **Mô tả**: Điều phối các tác vụ liên quan đến việc gửi thông báo, xác thực người nhận, và lưu thông tin thông báo.  
- **Thuộc tính**: *(Chưa được liệt kê)*  
- **Phương thức**:  
  - `sendNotification()`  
  - `validateRecipients()`  
  - `saveNotification()`  
  - `logNotification()`  

---

### **Entity (Thực thể)**

#### a. **UserStorage**  
- **Mô tả**: Quản lý và cung cấp thông tin về các học viên đủ điều kiện nhận thông báo.  
- **Thuộc tính**: *(Chưa được liệt kê)*  
- **Phương thức**:  
  - `getValidRecipients()`  

#### b. **NotificationStorage**  
- **Mô tả**: Lưu trữ thông tin chi tiết về thông báo được gửi.  
- **Thuộc tính**:  
  - `title`  
  - `content`  
  - `createdAt`  
- **Phương thức**:  
  - `saveNotification()`  

#### c. **NotificationLogStorage**  
- **Mô tả**: Ghi lại trạng thái gửi thông báo và thời điểm gửi.  
- **Thuộc tính**:  
  - `sentAt`  
  - `status`  
- **Phương thức**:  
  - `saveLog()`  

---

## Trách nhiệm

### **NotificationUI**  
- Hiển thị giao diện nhập nội dung thông báo và kết quả gửi thông báo.  

### **NotificationController**  
- Điều phối quy trình gửi thông báo, xác minh người nhận, lưu thông tin, và ghi nhật ký.  

### **UserStorage**  
- Cung cấp danh sách người nhận hợp lệ.  

### **NotificationStorage**  
- Lưu trữ thông tin nội dung thông báo được tạo.  

### **NotificationLogStorage**  
- Ghi lại thông tin nhật ký gửi thông báo, bao gồm trạng thái và thời gian gửi.  

![markdown](https://www.planttext.com/plantuml/png/j5JBQjj05DtFLnoyiY4YUrDC-g1fgHieRZvWB4qrG-GxZcOKoBgBBahN9Oj2HEWc4CWYK90MMGZo7_C5_OKoikME4-Eqb2xlp3b7vzovkZ_hsprZUMwBMSPuR7MEthl2LHS4cxlwCqvKSqcxs5TDgHT53zpWQJ9Jz5xmM8gSJNL12SzFqJlGLdrGCRTAq-7h5lbiUSbYJJRNsJhe-U8m4taBNfPCa5Ns5Br38t9ChCvvAbg0FrZMAr2ejmOEBxQHnZfD5QKjPwpJ3ih2a8X6goWOua2wwceESlMPGb9G2YkR6qenRKgzWrYw-WlXgBaaYPFc79JUNRlwcm9v8h6LL3JgGcC88oW9ZVLdmXYU2eyGPBqk9nAPsK4kOZLNWgmPi4uW6eNzmH1lbAi_pc1ptjcpYkvxGJ_K2WMYDNClE4cOfepb0mNfweivCbT_Og6P3Vt74EExwoAq4pIECPvPxBlwIeN7E2uun8ohZ05OMLf_aSTOOST_Fx8dIeLCftxUgtBnaAL2sihr9qKS2sDsNtALYMJ0H6O4ngx-sY4ssXflqiyUi0Gbsn9Ftax-Ec_7-KzfDrXwDAldR4bAxIyqTVNPbh2l_23xKV4hwS_O_v3Qcrrz_4aKhMsx-swEN7LhSUnt9lfMDkSa4RS6fNRLZzZ3gkyMKrULQi3Odg34BzjV0000__y30000)

---
![markdown](https://www.planttext.com/plantuml/png/b5AzQiCm4Dxr54ScP_0BX602dG8cWqkwNwsh42Ww8vq39kJ9ElIH-Wf5BgLsek9qbExxFUdp_MCN1OFq9wTQXp72wi1YtsoBOjaVzolORb-vznh3K5LmKG1bgG008daznHRh3Om3RMFdS6WezawAzKPTLKxxYRq4Tev2ycY_JmzQdD5PZK8DjRQpv2Kcdv62PyfI79kx-zzWnqZXMJYWePI6l5YvwMj8NfBjt3FVRK4g6pAlLBDvGAncywDnztvbMVsz-3byEXbfixKiOBFz_y6PD5KxyZfzoIy0003__mC0)

---

# Kết quả phân tích của Use Case 6: Tạo nhóm học tập

## Lớp phân tích

### **Entity (Thực thể)**

#### a. **Group (Nhóm)**  
- **Mô tả**: Đại diện cho một nhóm học tập được tạo trên hệ thống.  
- **Thuộc tính**:  
  - `groupID`  
  - `groupName`  
  - `creatorID`  
  - `memberList`  
  - `creationDate`  
- **Phương thức**:  
  - `getGroupDetails()`  
  - `addMember(memberID)`  
  - `removeMember(memberID)`  

#### b. **Member (Thành viên)**  
- **Mô tả**: Đại diện cho người dùng trong nhóm học tập.  
- **Thuộc tính**:  
  - `memberID`  
  - `email`  
  - `name`  
  - `status`  
- **Phương thức**:  
  - `getMemberDetails()`  
  - `updateStatus(newStatus)`  

---

### **Boundary (Ranh giới)**

#### a. **GroupCreationUI**  
- **Mô tả**: Cung cấp giao diện để giáo viên hoặc học sinh tạo nhóm học tập.  
- **Thuộc tính**: *(Chưa được liệt kê)*  
- **Phương thức**:  
  - `displayGroupForm()`  
  - `captureGroupDetails()`  
  - `showNotification()`  

---

### **Control (Điều khiển)**

#### a. **GroupController**  
- **Mô tả**: Điều phối các tương tác giữa giáo viên, hệ thống iLearn, cơ sở dữ liệu và các dịch vụ thông báo.  
- **Thuộc tính**: *(Chưa được liệt kê)*  
- **Phương thức**:  
  - `createGroup(groupDetails)`  
  - `inviteMembers(memberList)`  
  - `handleErrors(errorType)`  

---

### **Utility (Tiện ích)**

#### a. **NotificationService**  
- **Mô tả**: Gửi thông báo đến các thành viên được mời tham gia nhóm học tập.  
- **Thuộc tính**:  
  - `notifications`  
  - `recipientList`  
- **Phương thức**:  
  - `sendNotification(details)`  
  - `trackNotificationStatus()`  

---

## Trách nhiệm

### **GroupCreationUI**  
- Xử lý tương tác của người dùng để nhập thông tin và tạo nhóm học tập.  

### **GroupController**  
- Điều phối các quy trình tạo nhóm, mời thành viên, và xử lý lỗi.  

### **Group**  
- Đại diện và lưu trữ thông tin về nhóm học tập.  

### **Member**  
- Đại diện và lưu trữ thông tin về các thành viên trong nhóm.  

### **NotificationService**  
- Gửi thông báo đến các thành viên được mời tham gia nhóm học tập.  


![markdown](https://www.planttext.com/plantuml/png/h9D1Rjim44NtFCM7LkqY5_0Y26m5HXVnHie1nkJO9a2H1ZboexDbqIFr2WKfAX5Gjvjs8q2SDt_-V4e_ttyy9Q4eu-0KQGaHFPE-S0GbzFMeaz6mbtpKgMCOlQ4ueTd7C5vtaKbiyA_VcbpVxrwL3bvYS0imlpcE5L3inSg4fYMX8oKkv-rsfNm8OazM5-6Euytg6JfqIlLuUCnZi477ZhMWAHuOPLoZSktX4JqsQ6swEffmpXMSGXpMxSzUEDQQOI7hqjAyts63Abk0B-NPpjHNjTzbgjrc4tIh32J0r9rKk_tGARwGwCO6QTIQKpgDparLvT2LLRo1zJSh3B_QFcNHWOSZnwGENUOpNWAQGCSmIXrUcajFvVfFhWgdV8bt7CnnB65L00EdH6TUvzbTmlUF-jgcKkG4pp66Y0jvuwm_Bujx6XWsmOnNbt5M078od_UOPRaqBqDdvBUBdA5c9KmkCfa9_6QJf4QnD_VDl9GGmGDPbxtZb3-tV_ToN_SlHfRF7Zfupph7XnDPn__1p9-rPqDFx4t-rNy1003__mC0)

![markdown](https://www.planttext.com/plantuml/png/T5D1ReGm3BppYXpfWHz4QANILYkrUq5zW9Uukr53WXp3QbNrPJtqIVr2HG8KMCe5F7PcF3Rv-VhUUGRYjZP9KXdmNZoHQniX9LhMVCrpyP68_YcPj3s9Kv_U5xVO0MfSe1KXiAEnzbbxbYzO7v5oKOTt3yLa0OpnW7Qs3o9yGWxj5CYWZK_l8WnAHQ8qykoB8K5OkmvlSf-ZjvZvtznuP05Y3Tei4BkswXcuzLFFKMRLTDieO2n3PMhn4hzcpGMdzyCCNlT2ogDhhGAQzQcqRmnSG-cZeteahw3Xbd1hMFxiBWV7-arNWJczaNIMoHaJ1bF5u4ynB2KIZupQTfg7AKyoPx3Au0EH2zWaKG334JmAALlMPZ5r3zsIcP19umhiguQLpdZdbagaJbVR4cZLodt0cQ1wNt34nGI5U0MoRFXVOZmRKvRbwsrjrepUDvCR1f9fM9F24XhwsV8-IoSxjAg_qRy0003__mC0)
