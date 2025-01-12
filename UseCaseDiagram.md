## 5. Gửi thông báo đến học viên

## 1. Boundary: **NotificationUI**
### Attributes:

### Methods:
- **sendNotification()**  

- **displayResult()**  


---

## 2. Control: **NotificationController**
### Attributes:
### Methods:
- **sendNotification()**  

- **validateRecipients()**

- **saveNotification()**  

- **logNotification()**  


---

## 3. Entity: **UserStorage**
### Attributes:

### Methods:
- **getValidRecipients()**  

---

## 4. Entity: **NotificationStorage**
### Attributes:
- **title**  

- **content**  
  
- **createdAt**  
  
### Methods:
- **saveNotification()**  
  
---

## 5. Entity: **NotificationLogStorage**
### Attributes:
- **sentAt**  
- **status**  

### Methods:
- **saveLog()**  

![markdown](https://www.planttext.com/plantuml/png/j5JBQjj05DtFLnoyiY4YUrDC-g1fgHieRZvWB4qrG-GxZcOKoBgBBahN9Oj2HEWc4CWYK90MMGZo7_C5_OKoikME4-Eqb2xlp3b7vzovkZ_hsprZUMwBMSPuR7MEthl2LHS4cxlwCqvKSqcxs5TDgHT53zpWQJ9Jz5xmM8gSJNL12SzFqJlGLdrGCRTAq-7h5lbiUSbYJJRNsJhe-U8m4taBNfPCa5Ns5Br38t9ChCvvAbg0FrZMAr2ejmOEBxQHnZfD5QKjPwpJ3ih2a8X6goWOua2wwceESlMPGb9G2YkR6qenRKgzWrYw-WlXgBaaYPFc79JUNRlwcm9v8h6LL3JgGcC88oW9ZVLdmXYU2eyGPBqk9nAPsK4kOZLNWgmPi4uW6eNzmH1lbAi_pc1ptjcpYkvxGJ_K2WMYDNClE4cOfepb0mNfweivCbT_Og6P3Vt74EExwoAq4pIECPvPxBlwIeN7E2uun8ohZ05OMLf_aSTOOST_Fx8dIeLCftxUgtBnaAL2sihr9qKS2sDsNtALYMJ0H6O4ngx-sY4ssXflqiyUi0Gbsn9Ftax-Ec_7-KzfDrXwDAldR4bAxIyqTVNPbh2l_23xKV4hwS_O_v3Qcrrz_4aKhMsx-swEN7LhSUnt9lfMDkSa4RS6fNRLZzZ3gkyMKrULQi3Odg34BzjV0000__y30000)

---
![markdown](https://www.planttext.com/plantuml/png/b5AzQiCm4Dxr54ScP_0BX602dG8cWqkwNwsh42Ww8vq39kJ9ElIH-Wf5BgLsek9qbExxFUdp_MCN1OFq9wTQXp72wi1YtsoBOjaVzolORb-vznh3K5LmKG1bgG008daznHRh3Om3RMFdS6WezawAzKPTLKxxYRq4Tev2ycY_JmzQdD5PZK8DjRQpv2Kcdv62PyfI79kx-zzWnqZXMJYWePI6l5YvwMj8NfBjt3FVRK4g6pAlLBDvGAncywDnztvbMVsz-3byEXbfixKiOBFz_y6PD5KxyZfzoIy0003__mC0)

---

![markdown](https://www.planttext.com/plantuml/png/h9D1Rjim44NtFCM7LkqY5_0Y26m5HXVnHie1nkJO9a2H1ZboexDbqIFr2WKfAX5Gjvjs8q2SDt_-V4e_ttyy9Q4eu-0KQGaHFPE-S0GbzFMeaz6mbtpKgMCOlQ4ueTd7C5vtaKbiyA_VcbpVxrwL3bvYS0imlpcE5L3inSg4fYMX8oKkv-rsfNm8OazM5-6Euytg6JfqIlLuUCnZi477ZhMWAHuOPLoZSktX4JqsQ6swEffmpXMSGXpMxSzUEDQQOI7hqjAyts63Abk0B-NPpjHNjTzbgjrc4tIh32J0r9rKk_tGARwGwCO6QTIQKpgDparLvT2LLRo1zJSh3B_QFcNHWOSZnwGENUOpNWAQGCSmIXrUcajFvVfFhWgdV8bt7CnnB65L00EdH6TUvzbTmlUF-jgcKkG4pp66Y0jvuwm_Bujx6XWsmOnNbt5M078od_UOPRaqBqDdvBUBdA5c9KmkCfa9_6QJf4QnD_VDl9GGmGDPbxtZb3-tV_ToN_SlHfRF7Zfupph7XnDPn__1p9-rPqDFx4t-rNy1003__mC0)

![markdown](https://www.planttext.com/plantuml/png/T5D1JiCm4Bpd5JcQGtw0K2K2g1BqKdZ0DbvI2yUErfjK5U9b77WINq2sapHEGow9PtTdTcVZt--VZMCWxXgTPPK6v_8dibsRVsQvV_PCojHvxR5jUOtjeC44hGY1BOsvpyhnxGis1wIxl0bl3yLW2OonG5dZ3n6kaKCF9J8exSHDX47AI2GYpxOS0eIDxV4gzZKE52EBYSQy1CG6b4uGivpFCN3dfaOZzwBJhfN0k0-Pmk0fViqw2kFT3uE_RSVMf7AjXdE8FbfgHhuAMku8rqnnHtlQMLRlgWfauah56YQhzSM0O7Wa4_MCSc1KfbSykEd4PML3-0X6QdmWikG4-jVhkSMPQWaC1t0uoZde_nSZP5AO94nhzON9KgVIIMi--HwfLzL55erCZ969C1DK7qbvt5OWZpUWA8O_9vvdHXR5tNA5gpcZ5Ql1bTwpoRj98OM6VjR6deMp3HhfB_GV0000__y30000)
