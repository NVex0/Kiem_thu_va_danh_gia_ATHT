View node info:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/b5b9702c-0668-4349-8bc0-3521b43e349a)

Marked compromised user (giả định) thành owned, sau đó tìm attack path ngắn nhất tới domain admin:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/f28ffaa9-4e92-4c94-87d6-9d47030e28f4)

Chain: Từ compromised user -> change password của node tiếp theo (node tiếp theo là 1 user thuộc domain admin).

Thử tương tự, tìm shortest path với 1 compromised user (giả định, marked as owned) khác:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/39b075f0-6c5d-4936-967a-8855ab30b146)

Chain: Compromised user (thuộc DesktopAdmin) -> DesktopAdmin lại có quyền admin ở node kế tiếp -> node này lại có 1 session, là node tiếp theo -> node này lại có quyền admin ở node kế -> node kế lại có 1 session, là node tiếp theo -> node này thuộc domain admin.

Hoặc ta có thể thử Short path mà không cố định từ 1 compromised user mà mình owned nào, tức là từ non admin tới domain admin:

![image](https://github.com/NVex0/Kiem_thu_va_danh_gia_ATHT/assets/113530029/c450abeb-2509-4e8e-b2c4-274dd67d74d3)
