vào metasploit dùng `msfconsole`, dùng `exploit/multi/handler` (ta launch payload ngoài metasploit, dùng cái này để bảo nó sẵn sàng nhận connection chứ không phải exploit):

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/3598159c-cfbd-4ecd-a86c-9e5213f4a8ea)

change payload từ revtcp sang revhttp:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/0f5f10d2-9cab-4e68-b39d-11e01834c6fc)

change local host và port:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/163ed72e-a457-4558-8bef-bb91d58c9e4a)

enable accept multiple connection cho con listener:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/9d37ab9e-6666-450f-8795-09e35fa648aa)

Launch connection, -j (job) và không tương tác với connection mới (-z):

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/cfba5831-0205-4026-ac90-b84064c01e6c)

Dùng msfvenom gen vbs payload xong cho vào tmp:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/125433b7-52f0-4c75-a38b-d1147b5da8b3)

Truyền sang máy victim và chạy:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/168d4e9f-ac38-472c-a751-e1a1f316f4c1)
![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/23398029-2d97-4a8f-986d-63f5c8db8e46)

Listener nhận connection:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/0a461f65-6f19-4690-b3dc-b9fc07e0a213)

interact với session này:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/7b6ec808-a5e7-4b13-987c-7845d6348e7b)

gather info:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/3f54d275-c821-4957-8397-cc22c25d9c26)

thoát:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/e5a6d328-8dfd-4250-ab80-5f669f68a149)

Tiếp tục, dùng msfvenom gen msi file:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/fe2318ad-2d77-48c8-917e-b39ea06f00cc)

Gen iso image từ msi:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/52231f1f-7560-4f3a-8bb2-c2509c52d270)

Ném sang windows và chạy, bên msf nhận connection:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/cd8918fb-0d81-41bc-ba0a-5c09b25db9fd)

interact với session này:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/794538b7-8be5-484b-826f-a8e5687c2045)

tương tự, gather được infomation và thoát.

Final - Dùng sliver, bật http listener và gen payload:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/3b2e7503-c88a-4343-9fd5-7a7c64631aa0)

Dùng smbclient.py (Impacket) ném nó sang ổ C windows của bgreen: 

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/667e01b5-21c3-40fb-b17e-5529b28e25a1)

Dùng wmiexec.py (Impacket), remote đến pc và chạy con dll kia bằng regsvr32:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/0cf85b1b-94f9-4e3f-ae76-fe0a40ba6e06)

sliver server nhận connection:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/b39e8fdd-312f-4b9d-a85e-2886dc048328)

use session và check info:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/7e74c5b0-9cfa-4c3e-beff-f2ff784cf902)
