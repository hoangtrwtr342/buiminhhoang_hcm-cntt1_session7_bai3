Bài 3 : Tự động hóa Phân tích File Log


I. Phân tích

Pipeline đưa dữ liệu từ lệnh này sang lệnh tiếp theo. Trong PowerShell, dữ liệu được truyền giữa các lệnh qua pipeline:

Get-Content ──|──> Select-String ──|──> Measure-Object
 (đọc log)          (lọc TIMEOUT)          (đếm dòng khớp)


 II. Câu lệnh

 Viết câu lệnh PowerShell nối 3 bước (**Đọc file | Lọc chữ | Đếm dòng**) hoàn chỉnh, cho ra một con số duy nhất.

 -> Get-Content .\ **access.log** | Select-String "TIMEOUT" | Measure-Object -Line
