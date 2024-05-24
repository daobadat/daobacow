# Kiểm thử API với Postman
# Giới thiệu
Mục tiêu của bài tập này là thực hành kiểm thử API bằng cách sử dụng Postman. Bài tập bao gồm các bước từ việc lựa chọn một API thực tế, phân tích tài liệu API, viết các trường hợp kiểm thử, thực hiện kiểm thử và ghi lại kết quả kiểm thử.
# API Được Chọn
API được lựa chọn cho bài tập này là TheCatAPI - Documentation Portal, một API cung cấp dữ liệu ảnh đẹp về những chú mèo .
# Phân tích tài liệu API
Để hiểu rõ các chức năng và điểm cuối của TheCatAPI - Documentation Portal API, tài liệu API đã được tham khảo:

•	Base URL: https://api.thecatapi.com/v1
•	Phương thức: GET
• Các endpoint chính:
  -Get images by Name/ID: /images/{name_or_id}
  -Get images Type by Name/ID: /type/{name_or_id}
  Viết các trường hợp kiểm thử
3.1. Kiểm thử thành công

1 Kiểm thử lấy thông tin Pokémon bằng tên

-Mô tả: Kiểm thử API với search ra 1 images hợp lệ.
*Phương thức: GET
Endpoint: /images/search
Mong đợi: HTTP Status 200, thông tin về random imagaes cat.
![image](https://github.com/daobadat/daobacow/assets/124127055/7a2005b2-349a-4f12-af8f-cc054a032a8b)
2 Kiểm thử lấy thông tin Pokémon bằng ID

- Mô tả: Kiểm thử API với ID hợp lệ.
Phương thức: GET
Endpoint: /images/ace
Mong đợi: HTTP Status 200, thông tin về Pikachu (vì ID của image là ace).
![image](https://github.com/daobadat/daobacow/assets/124127055/804b7166-4627-4c8c-b16a-344329352396)

3.2. Kiểm thử thất bại

1 Kiểm thử với tên Pokémon không hợp lệ

- Mô tả: Kiểm thử API với tên image không tồn tại.
Phương thức: GET
Endpoint: /image/meo
Mong đợi: HTTP Status 404, thông báo lỗi "Not Found".
![image](https://github.com/daobadat/daobacow/assets/124127055/4a220b7b-9052-4c35-9ab9-13d54ef4025a)

2 Kiểm thử với ID Pokémon không hợp lệ

-Mô tả: Kiểm thử API với ID image không tồn tại.
Phương thức: GET
Endpoint: /image/99999
Mong đợi: HTTP Status 404, thông báo lỗi "Not Found".
![image](https://github.com/daobadat/daobacow/assets/124127055/4c469c6e-1ee5-40da-8c21-eeb9ab924e89)

Ghi lại kết quả kiểm thử và xác định các lỗi hoặc vấn đề
5.1. Kết quả kiểm thử

Test 1: Thành công, nhận được dữ liệu chi tiết về search image.
Test 2: Thành công, nhận được dữ liệu chi tiết về image với ID ace.
Test 3: Thành công, nhận được thông báo lỗi hợp lệ cho tên image không tồn tại.
Test 4: Thành công, nhận được thông báo lỗi hợp lệ cho ID image không tồn tại.
5.2. Các lỗi hoặc vấn đề

Không phát hiện lỗi hoặc vấn đề bất thường nào trong quá trình kiểm thử.
Viết báo cáo kiểm thử chi tiết
6.1. Mục tiêu kiểm thử

Xác minh tính đúng đắn và hoạt động của các endpoint chính của PokeAPI.
Đảm bảo API phản hồi chính xác với các yêu cầu hợp lệ và không hợp lệ.
6.2. Phạm vi kiểm thử

Kiểm thử các chức năng chính của PokeAPI bao gồm việc lấy thông tin image bằng tên và ID.
Kiểm thử phản hồi của API với các trường hợp lỗi thông thường.
6.3. Kết quả kiểm thử

Test Case	Expected Result	Actual Result	Status
Test 1	HTTP 200, Data for Pikachu	HTTP 200, Data for Pikachu	Passed
Test 2	HTTP 200, Data for Pikachu	HTTP 200, Data for Pikachu	Passed
Test 3	HTTP 404, Error "Not Found"	HTTP 404, Error "Not Found"	Passed
Test 4	HTTP 404, Error "Not Found"	HTTP 404, Error "Not Found"	Passed
6.4. Khuyến nghị

Tiếp tục kiểm thử với nhiều trường hợp khác nhau để đảm bảo tính ổn định và tin cậy của API.
Thực hiện kiểm thử tự động hóa để tăng hiệu quả kiểm thử.
Kết luận

Quá trình kiểm thử đã xác minh rằng PokeAPI hoạt động đúng như mong đợi với các trường hợp kiểm thử đã định nghĩa. Các kết quả kiểm thử đều đúng với dự đoán và không phát hiện lỗi nào bất thường.








