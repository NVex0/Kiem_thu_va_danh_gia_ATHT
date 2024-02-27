Modules:
+ crypto: Các thao tác liên quan tới Cryptography như Hash, các mã hóa dùng Crypto API của windows, Certificate...
  
+ dpapi: Data Protect API. DPAPI là mã hóa dựa trên tài khoản Windows: CurrentUser hoặc Local Machine, được Microsoft giới thiệu từ năm 2000. Ví dụ cho file path tương ứng với các DPAPI section:
 ![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/7bcc0e94-96eb-4db0-8c1f-3294dbe77ddc)

+ event: thao tác với windows event log.
  
+ kerberos: Các hoạt động liên quan tới Kerberos ticket.

+ lsadump: Dùng để dump hash NT, NTLM, LSA default password,... hoặc thực hiện 1 số attack như DCSync, DCShadow.

+ misc: linh tinh.
  
+ net: hiển thị thông tin ví dụ như thông tin về users, groups, ip, share folder,.... tương ứng với các submodule của nó.
  
+ privilege: cung cấp 1 số chức năng để thay đổi đặc quyền cho các proc mimikatz.
  
+ process: cho phép tương tác với proc (listed, khởi tạo hay dừng proc)
  
+ rpc: các thao tác liên quan tới rpc server.
  
+ sekurlsa: là module được dùng nhiều nhất của mimikatz, nó giúp ta lấy được pass bản rõ, pass dạng hash ntlm, kerberos ticket,.... từ LSASS.
  
+ service: các thao tác liên quan tới dịch vụ của Windows.
  
+ sid: các thao tác liên quan tới sid.
  
+ standard: mấy command cơ bản mà không liên quan đến hoạt động chính của tool lắm.
  
+ token: các thao tác lên Windows token.

+ ts: Terminal Service....
  
+ vault: cho phép lấy cred như password từ Windows Vault.
ETC....

> Tìm hiểu chi tiết từng submodule tại https://tools.thehacker.recipes/mimikatz/modules

Các khả năng của Mimikatz:

1. Phân tích procdump của proc lsass.exe. Đây là proc chịu trách nhiệm thực thi chính sách bảo mật trên hệ thống. Trong kịch bản ta dump được proc này của compromised user, ta có thể phân tích dump bằng mimikatz trên 1 máy khác.
   
> Dumping-lsass vid.

2. Khả năng thao tác với Windows Event Log. Cụ thể bằng module event với 2 submodules là clear (xóa log), hoặc drop (patch event log, không cho nó bắt thêm log mới nữa).

3. Perform 1 số tấn công:
   
- Pass the hash.
  
> Pass the hash vid.

- Pass the ticket.
  
- AD Tampering:
  
  + DCSync.

  > DCSync attack vid.
    
  + DCshadow. eg: `lsadump::dcshadow /object=lowprivuser /attribute=primaryGroupID /value=512`
    
- Privilege Escalation : Module `privilege`.
  
- misc:
  
  + skeleton : tạo 1 backdoor dựa trên tấn công skeleton key attack. Nó sẽ inject vào lsass.exe để tạo 1 masterkey để hijack mọi xác thực trên AD. Sau đó nó có thể logon vào bất cứ user nào trong domain chỉ với cùng 1 password.
    
- Credentials Dumping:
  
  + Hiển thị cred của các user đã log: `sekurlsa::logonpasswords`
    
  + Export Kerberos tickets (Có thể phục vụ cho tấn công pass the ticket): `sekurlsa::tickets /export`
    
- Thay đổi SID, Token:
  
  + Thay đổi SID: `sid::add /user:targetUser /sid:newSid`
    
  + Mạo danh Token: `token::elevate /domainadmin`
    
- Terminal Service (cái module ts đó):
  
  + Cho phép chạy đa phiên RDP: `ts::multirdp`
    
  + Liệt kê phiên rdp: `ts::sessions`
  
  
