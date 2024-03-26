## 1. Password Spray.

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/237df839-12a3-4839-9c27-3fa9fa2fd637)

## 2. Password Guessing (SSH).

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/b72d87e3-a16c-4329-b132-fb985f12b25a)

## 3. Verifying Access.

Đầu tiên xem máy nào nghe ở port 445:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/907ce084-5da3-496c-81f4-da4698026d5f)

Format output, list lại ip vào 1 file:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/7a484298-8c2c-4dc4-aa13-7b54134fa2b1)

Thử dùng Cred đó xem có dùng được trên máy nào không bằng ip list trên:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/f3979b65-08a0-4bf2-b2ee-810a54935735)

## 4. Cred Breach

Breach dựa trên cred đã có:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/b4de1aed-50eb-46c9-a8a2-0145fb0b6618)

## 5. Password Spray (domain).

Đầu tiên sử dụng cred đã có để lấy userlist trên DC:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/83412e16-b21a-4d62-8721-9183f5fdef2f)

Format output thành 1 user list:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/4a689789-09b3-4eca-bd4f-3759799768b7)

Spray:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/84c00bb6-53dc-4a86-ac13-73ea6f10dd5e)

