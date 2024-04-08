Run empire server và client:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/da66bdea-df58-44ee-9d01-ae89a849b2e1)

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/39cab22f-708d-410e-af37-29525e33dde6)

Mở http listener bên client:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/78601cb9-c164-453b-a9fd-c73171a74107)

Bind param cho listener:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/ef188dd7-5002-4641-a029-950d48c6e037)

Drop Agent:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/5ac417c1-d010-4e9d-9386-001fd7436613)

Set listener để agent connect tới:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/de399185-75a1-47d8-95af-da4f49d03adb)

Generate bat, sau đó transfer sang máy victim:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/66815a2e-7a0e-42c5-8a45-d7e93ca99c11)

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/0812cef2-1798-4485-adf8-2e181bbc525e)

rename agent:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/d829b5f8-29d1-4464-ad99-75c91d6cfb76)

Tương tác với agent:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/af52adf1-680d-46e8-aca3-bc75c6e7cdda)

Use module:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/4650d628-29e8-49a4-93fc-e8f01bd67c58)

exec module:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/f4e5b209-86cb-4fab-afa0-dd7cf412b076)

Sử dụng 1 module khác để check privilege escalation:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/0f57155d-d028-4bec-aa1a-0a15594e4743)

exec module:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/0e4ddd00-adf1-48ed-a69c-171bdbf7d7f8)

Sử dụng 1 module khác để dump cred:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/24d52848-6369-4565-8403-51c7ba41e51e)

Trước khi dùng module này phải ask for priv mới execute được:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/5426d727-907a-4bd9-8067-ceefc1452cca)

Chạy module để ask priv xong thì quay lại module dump cred kia:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/25988afc-bb74-44ce-8d13-65ece330f922)

Dump cred thành công.

Tiếp tục với module để scan port:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/4ba9de17-51f3-48d8-ac6e-090bc3bed739)

Result cho các port đang mở:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/f28006f0-64ce-4a09-8044-1c2b74754417)

Cuối cùng, để kết thúc, kill hết agents và listeners:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/bbef7631-18f8-469a-83d5-7f72400828b3)

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/e1ae0910-301d-480e-8a6c-6449d3ed9613)

Exit.
