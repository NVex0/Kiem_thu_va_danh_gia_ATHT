Config sliver Server:

Add new user:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/8e72ab7b-1754-4dfc-9063-c46ee0dff641)

Import file config từ user mới. Sau đấy run sliver client. 

Run xong thì mở https listener.

Gen malware:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/71d43e56-105b-4aaf-a650-108fcd70b0fc)

Transfer sang windows xong run:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/1f0ed6f4-bd83-4c22-90c2-6149ec3b421f)

Server nhận session:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/2f330f5a-ebe3-4c00-9309-f2766b2698e3)

Use session này:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/1d9a0ab8-8384-4894-b528-6f41eadfbfc1)

Lúc này trong session, ta có thể check 1 số info:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/0bc8d795-7440-490c-bc42-e8c3df2acb08)

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/5b9e1441-deaa-41f8-bc8d-2f2686dada2d)

Run shell:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/74877965-6662-40c2-9545-1be97036cb5e)

Lúc này ta đã có shell của victim:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/a12a575e-9b2a-4b04-9204-c8b60bb773b0)

Kế đến, tiến hành sử dụng SharpWMI để thực hiện cách hành động lên WMI, vì exe này compile .NET (C#), máy victim không có .NET, ta sẽ sử dụng `execute-assembly` để cung cấp runtime cho nó chạy:

+ view logged on user:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/7766ba01-cb8a-491b-b8d3-ab140c4fc0c4)

