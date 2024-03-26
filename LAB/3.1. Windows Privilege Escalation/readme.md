Tới path của tool beroot và chạy executable:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/349a8497-f96a-48fb-aeb0-43756c11fd27)


Check vuln bằng 1 tool khác.

Add new module vào PS:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/40d47f81-291d-4347-8af7-761c0a2e6067)

Run command sau khi import module:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/e937fc42-bfa9-4175-8590-e86effac9a3b)

Ta có được result về các vuln như path nào bị lỗi unquoted, dll nào hijacking được, permission.

Với vuln unquoted, có thể verify bằng service:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/191c8a01-a684-47ef-b5ef-00d4cb16f3ba)

Exploit thử:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/057b6857-64d7-4e41-b77f-652b5931d639)

Create thành công exe:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/ed05f4f3-02d8-47ff-be7f-831d3db2ea0a)

Reboot và check:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/aededb0f-afb2-4c63-9aa6-b057e54de990)
![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/e5e8fe8e-af87-4960-9b33-4fead05c345b)

