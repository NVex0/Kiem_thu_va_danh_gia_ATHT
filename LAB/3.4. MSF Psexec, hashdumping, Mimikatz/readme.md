## MSF Psexec.

Vào metasploit và chọn module psexec:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/fcae110f-36aa-4f4e-a3cd-183675cdcdaa)

Truyền param:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/9d7dda59-b262-4eae-aa40-422ed80202fd)

Get info từ meterpreter:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/bf3dcacb-e04e-4bd0-836d-b0499df76934)

## Hash dumping.

Từ meterpreter, dùng module `post\windows\gather\smart_hashdump` để dump hash từ SAM:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/33196644-7714-4f6b-8d56-6dd35ec92fb4)

như ta thấy NT Hash nó giống nhau (ở đây là NULL), module này ngon cho DC, còn không phải DC thì dùng `post\windows\gather\hashdump`:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/b3c2f009-89a6-4092-a95a-3a5e1a446999)

## Mimikatz.

exit meterpreter, bind param mới:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/ba297e2b-297a-4f7f-b098-c87272d0b83e)

Run exploit, sau đó check info:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/5f696ebb-9908-44ad-b3a9-ff34c780b6af)

Proc meterpreter 32 bit, còn architecture của máy là 64 bit, vì thế ta cần phải vào sys proc 64 bit. Tiến hành tìm các proc 64 bit quyền system:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/788e685d-d768-4468-a9f7-6d2a6a31bf3f)

Migrate vào 1 trong các proc trên:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/6405b77e-f30b-4f63-921d-75bfa5158c3b)

Check lại, proc meterpreter đã là 64 bit:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/1a3b05f0-071e-438e-b1c1-b6a521fe150b)

Load mimikatz:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/51286fa9-d5c3-43ad-b3ad-2c38f088d606)

Run `creds_all` để lấy plaintext password:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/7e8239ff-19ca-40e2-a16d-54e8aee2e83b)
