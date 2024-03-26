Grep module icecast và dùng 1 module trong mớ grep được:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/d4cfecad-3edc-4b8b-9de6-8669fab4f514)

Change default payload sang reverse http:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/d95c2fc3-05c1-428a-b938-b18d6a47c70e)

Change remote host sang ip windows chạy vuln icecast service:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/8f01c67a-41f2-48be-94fe-584a99063621)

Và local host sang ip máy attacker:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/10b4fa09-011d-42c6-a178-62540f1bd7e4)

Run exploit và mở được session meterpreter:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/e0edc1c7-b32b-41c3-bb9d-dd30922e1973)

Có thể để meterpreter chạy background để làm việc khác:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/467e2d49-8ce5-4e97-a620-1ce034972584)

Có thể đổi tên session:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/6a570341-a316-4078-81ea-73c5c043c561)

Đi vào đấm tiếp session đang chạy background:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/c1a44ce2-1a0d-40d5-b25b-9e9285a0e1c1)

Info:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/ade183ff-e2d4-43c6-8c58-9ef7a782cf05)
![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/40f3c3e8-3923-4f88-8d4e-be45d6f4be56)

Process info:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/850300ba-3652-4c4d-8950-73342abdc85b)

Find icecast trong proclist:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/09711d4b-6ff0-47e3-b1a5-cdec3ba803e4)

Gain shell bằng `shell` trên meterpreter, sau đó dùng mấy command check info: `net user`, `hostname`, `ipconfig`.

Thêm user làm backdoor vào:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/d9ef4998-a8f4-45a2-a024-a1d3926c3ecb)

Nâng quyền backdoor user bằng cách Add user vào local admin group:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/c00a74af-9b83-4e82-bb60-1b313d9c906e)

del acc:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/a35d8e72-2512-438b-82ab-ce4fa019eb69)

chụp màn hình máy victim:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/23f4cc5b-e89c-494f-9211-c81044945c61)
![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/34bb266a-fa2e-47d8-b8a4-e3831979942c)

Search và sử dụng proc explorer.exe:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/c8b241a9-8d7d-438f-8e1d-6610d6342dad)

Keylogging:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/7d935e3b-50f5-4c03-840b-455407b572eb)


