# Hướng dẫn sử dụng GitHub

## Quy trình làm việc cơ bản

1. **Branching Strategy**

   - `master`: Branch này chỉ nên chứa các phiên bản ổn định của dự án. Không code trực tiếp vào branch này.  

   - `develop`: Branch này chứa các thay đổi mới nhất từ mỗi thành viên trong nhóm. Tất cả mọi người nên tạo branch cá nhân từ `develop`.

2. **Tạo Branch Cá Nhân**

   - Mỗi người tạo branch riêng từ `develop` để thực hiện công việc của mình. Đặt tên branch theo công việc hoặc tính năng mà bạn đang phát triển.

     ```
     git checkout -b feature/ten_tinh_nang develop
     ```

3. **Code và Commit**

   - Hoàn thiện công việc của mình trong branch cá nhân. Khi bạn đã hoàn thành một phần, hãy commit thay đổi của bạn:

     ```
     git add .
     git commit -m "Mô tả thay đổi"
     ```

4. **Push Branch Cá Nhân Lên GitHub**

## Quy trình làm việc chi tiết

1. Clone project về máy nếu chưa có: 

    ```
    git clone <Đường link github của project>
    ```
2. Tạo branch cá nhân từ branch `develop`:

    ### * Chú ý:
    Cần phải `pull` code để đảm bảo branch `develop` là mới nhất trước khi tạo branch cá nhân. Nếu không, có thể xảy ra xung đột khi merge code.
    ```
    git pull origin develop
    ``` 

    Tiến hành tạo branch cá nhân:
    ```
    git checkout -b feature/ten_tinh_nang develop
    ```
3. Thực hiện code vào triển khai các chức năng:
 

4. Commit code lên branch cá nhân:
    ```
    git add .
    git commit -m "Mô tả thay đổi"
    git push origin feature/ten_tinh_nang
    ```
5. Tạo Pull Request (PR) từ branch cá nhân lên branch `develop`:
    - Truy cập vào tab `Pull requests` của repo đang code trên GitHub.
    - Click vào `New pull request`.
    - Chọn branch `develop` làm base branch và branch cá nhân làm compare branch. (develop <- feature/ten_tinh_nang)
    - Điền thông tin vào các trường còn lại và click `Create pull request`.
    - Chờ quản trị viên merge code (Báo cho anh Thịnh để anh Thịnh duyệt nhá).