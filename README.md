# Start .Net Project from command line

```dotnetcli
dotnet new sln --output <Solution_Name>
cd <Solution_Name>
dotnet new <Project_Type> -o <Project_Name>
dotnet sln add <Project_Name>
```

[Reference1](https://learn.microsoft.com/en-us/dotnet/core/tools/dotnet-sln)\
[Reference2](https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-web-api?view=aspnetcore-7.0&tabs=visual-studio-code)

---

# Docker

## Setup docker on ubuntu 22.04 WSL

- Follow this document at: <https://docs.docker.com/engine/install/ubuntu/>
- If you got error: _"Cannot connect to the Docker daemon at unix:/var/run/docker.sock. Is the docker daemon running?"_
  - Download and install: <https://github.com/microsoft/WSL/releases/download/1.0.3/Microsoft.WSL_1.0.3.0_x64_ARM64.msixbundle>
  - Run command: `sudo systemctl start docker`
  - [Reference](https://stackoverflow.com/questions/44678725/cannot-connect-to-the-docker-daemon-at-unix-var-run-docker-sock-is-the-docker)

---

# Interview

## Media Step

### Questions

1. SOAP và REST Full Api khác nhau như nào
1. Làm sao tối ưu 1 API chạy chậm
1. Các bước tạo 2 table Teacher & Student many to many dùng code first
1. Có bao nhiêu table sinh ra dưới database
1. Làm sao query tất cả teacher cùng student của teacher đó dùng LINQ
1. Làm sao query tất cả teacher mà có student tên có chứa "Messi"
1. Làm sao insert 1000 teacher vào database
1. Làm sao insert 1 triệu teacher vào database

### Test project (làm trong 1 ngày)

FE (web có thể dùng reactjs / javascript / mvc / angular/ vuejs.., ưu tiên reactjs): cho phép người dùng nhập vào danh sách Customer (Full Name, Date of Birth - DOB, Email), Shop (Name, Location) và Product (Name, Price). Một Customer có thể mua nhiều Product ở nhiều Shop. Một Shop có nhiều Product. Cần nhập ít nhất là 30 Customer, 3 Shop, và 3003 Product. Cho phép người dùng thực hiện tìm kiếm Product.

BE (.net hoặc .netcore): lưu trữ Customer/Shop/Product vào database. Load dữ liệu từ database và tiến hành sắp xếp theo qui luật: Customer.Email theo thứ tự alphabet tăng dần, Shop.Location theo thứ tự alphabet giảm dần, Product.Price theo thứ tự giảm dần. Lưu ý số lượng Customer/Shop/Product trước và sau khi sắp xếp là không thay đổi. => Kết quả sắp xếp sẽ được trả về FE để hiện thị lên UI (Nếu không đủ 30 Customer, 3 Shop, và 3003 Product, UI sẽ hiển thị thông báo lỗi Không Đủ Dữ Liệu).

--> FE OUTPUT:

```html
Table Headers
------------------------------------------------------------------------
Customer (Name - Email) | Shop (Name - Location)| Product (Name - Price)
------------------------------------------------------------------------
Customer (Name - Email) | Shop (Name - Location)| Product (Name - Price)
------------------------------------------------------------------------
Customer (Name - Email) | Shop (Name - Location)| Product (Name - Price)
------------------------------------------------------------------------
Customer (Name - Email) | Shop (Name - Location)| Product (Name - Price)
------------------------------------------------------------------------
Customer (Name - Email) | Shop (Name - Location)| Product (Name - Price)
------------------------------------------------------------------------
Customer (Name - Email) | Shop (Name - Location)| Product (Name - Price)
------------------------------------------------------------------------
```

Làm video ngắn giải thích code flow và demo chạy tính năng trên UI
