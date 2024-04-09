## SERVICE PERSISTENCE:

Vào sliver, bật listener tại port 443, sau đó gen payload:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/8b67018b-cfb7-4b10-b425-b479e72df8e0)

Mở http server và sang windows curl payload về:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/668404ec-9105-4b5e-8ef7-a7ece0dd98c7)

Dùng service control tạo persistence:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/8bf43654-72c2-430c-9681-f12a5bee4065)

Reboot, sliver nhận session:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/dcb368b0-017c-42bc-8bb0-df8f160d46ca)

Check role:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/70166a8c-fc0e-4c57-b45e-3b4ed3b5adb8)

Sau đó xóa service đi:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/302307f2-9dfb-4468-9e3f-ac854c5c6eed)

## REGISTRY PERSISTENCE:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/c25d0bc6-6e7a-491e-b31d-51c30eb21ee6)

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/f33a6dd9-5e87-4a4c-9790-b0914b1a992b)

Reboot, sliver nhận session:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/95bc7d37-5fcb-4f16-a9b3-d3b2f65bca8f)

Check role:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/848ccfd6-13cb-4b16-9458-1f25aef0eb58)

Sau đó del key trong registry đi là xong.

## WMI PERSISTENCE:

Set persistence vào wmi:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/7937f94c-d40e-49dd-afc3-ab5f16053cab)

Fake cred:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/7732eb14-601e-467c-90e5-bfd637e9b40e)

Sliver server nhận connection:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/4cb3b018-fc85-44d6-8a05-8b4e5e0bab57)

Vào session, và check info.
