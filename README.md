# ProjectGroup03_63KTPM2_Version03
# Để chạy cài đặt ứng dụng cần thiết lập như sau:
1. Thiết lập cơ sở dữ liệu: tạo CSDL và các bảng như sau:
   
  create database BTLWINFORM

  create table ManagerAccount(mUser char(50), pass char(50))
  

  create table EmployeeAccount(
  		mUser char(50), 
  		password char(50), 
  		managerUser char(50),
  		idPeople char(50) primary key)

  create table EmployeeInfo( 
    	mName nvarchar(50), 
    	sex nvarchar(50), 
    	birth date, 
    	province nvarchar(50), 
    	idPeople char(50) primary key, 
    	phone char(50),
    	pathImage char(350))


  create table Support(mSupport  nvarchar(40))
  insert into Support values(N'null')
2. Vào file "ManagerTables.cs" -> tìm đến biến SQL_CONNECT_DATABASE -> đổi giá trị ở trường "Data source" thành đúng tên server của
  máy đang chạy (Dùng Sqlserver)
# Lưu ý 1: khi thực hiện thao tác thêm món ăn, thao tác chọn ảnh món ăn chỉ lấy file ảnh có tên có độ dài tối đa 30 ký tự, không có khoảng trắng, không dấu
# Lưu ý 2: để đảm bảo chạy tốt, các giá trị bằng chữ nhập vào nên nhập Tiếng Anh
