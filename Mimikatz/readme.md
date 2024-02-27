Modules:
+ crypto
+ dpapi:
+ event
+ kerberos
+ lsadump:
+ misc
+ net: hiển thị thông tin ví dụ như thông tin về users, groups, ip, share folder,.... tương ứng với các submodule của nó.
+ privilege: cung cấp 1 số chức năng để thay đổi đặc quyền cho các proc mimikatz.
+ process
+ rpc
+ sekurlsa
+ service
+ sid
+ standard: mấy command cơ bản mà không liên quan đến hoạt động chính của tool lắm.
+ token
+ ts
+ vault
ETC....

Tìm hiểu chi tiết từng submodule tại https://tools.thehacker.recipes/mimikatz/modules

Các khả năng của Mimikatz:

1. Phân tích procdump của proc lsass.exe. Đây là proc chịu trách nhiệm thực thi chính sách bảo mật trên hệ thống. Trong kịch bản ta dump được proc này của compromised user, ta có thể phân tích dump bằng mimikatz trên 1 máy khác.
-Dumping-lsass vid
2. Khả năng thao tác với Windows Event Log. Cụ thể bằng module event với 2 submodules là clear (xóa log), hoặc drop (patch event log, không cho nó bắt thêm log mới nữa).
3. 
