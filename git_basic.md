# Tổng quan về GIT

- nó như là kho dùng để lưu trữ code
- GIT có thể quản lý rất nhiều thứ trong 1 dự án
- git flow - nhánh `mater` là nhánh tổng, là nhánh cao nhất thường là để các leader quản lý - từ nhánh đó sẽ tạo ra những kho con là nhánh `develop` dùng để phát triển sản phẩm - từ `develop` sẽ tạo ra các nhánh con nữa là `feature` - chúng ta sau khi làm xong những đoạn code của các thành viên thì sẽ gửi `pull requeust` để có thể `merge` là trong nhánh khác và cuối cùng là để merge vào nhánh `mater` và sau đó tạo ra chương trình - nhánh `hotfix` là nhánh fix nhanh 1 bug trong code
  ![](https://image.slidesharecdn.com/git-intro-141228110455-conversion-gate01/95/gii-thiu-git-5-638.jpg?cb=1419813026)

# Các thuật ngữ thường dùng trong GIT

- git flow: nó là 1 luồn đi trong dự án
- branch: nó là những nhánh trong dự án
- pull request (pr): là lệnh merge code
- review: xem cái trong nhánh pr
- merge: liên kết code
- release: triển khai code lên 1 môn trường để test
- deploy: giống relase là triển khai code

# cách lệnh cơ bản dùng trong git bash

- y hệt linux

# cấu hình git

- git config --global user.name "tên bạn"
- git config --global user.email "tên email bạn"
- git config

(dùng vs r thì thôi ko cần vì đăng nhập git vào r)

# GIT repository

- `repository` là kho lưu dữ của 1 dự án, gọi tắt là `repo`
- chia thành 2 loại
  - local - là máy của mình
  - remote - là lưu trữ đám mây
- lệnh
  - git init là để tạo ra repo (đâu là điều luôn phải làm trước khi làm 1 cái gfi )
  - khi sử dụng câu lệnh thì sẽ báo hiệu cho git là đây là 1 địa chỉ dành cho git và có thể clone hoặc pull code từ git
  -
-

# Git structures:

- Clone: Nếu muốn có một bản sao của một kho chứa Git có sẵn thì phải thực hiện clone.
- Push: Lệnh push được sử dụng để đưa nội dung kho lưu trữ cục bộ lên server. Push là cách bạn chuyển giao các commit từ kho lưu trữ cục bộ của bạn lên server.
- Fetch: Khi ta thực hiện fetch, lệnh này sẽ truy cập vào repository trên server và kéo toàn bộ dữ liệu mà bạn chưa có từ repository trên server về. Sau đó, bạn có thể tích hợp dữ liệu vào branch bất kỳ lúc nào.
- Pull: Lệnh này sẽ tự động lấy toàn bộ dữ liệu từ repository trên server và gộp vào cái branch hiện tại bạn đang làm việc.
- Commit: là thao tác báo cho hệ thống biết muốn lưu lại trạng thái hiện hành, ghi nhận lại lịch sử các xử lý như đã thêm, xóa, cập nhật các file hay thư mục nào đó trên repository. Khi thực hiện commit, trong repository sẽ ghi lại sự khác biệt từ lần commit trước với trạng thái hiện tại. Các commit ghi nối tiếp với nhau theo thứ tự thời gian do đó chỉ cần theo vết các commit thì có thể biết được lịch sử thay đổi trong quá khứ.
- Branch: sau khi push lên 1 cái branch nào đó, nó chứa toàn bộ các mã nguồn chính trong repository.
  Merge: nếu muốn ghép hoặc tích hợp branch vào 1 branch khác thì phải mesge nó vào (bt thì sẽ tạo ra 1 cái pull request cho chắc kèo check)

# Một số lưu ý khi dùng git

1. Nhiều tài khoản github trên dùng một máy:

- Bạn có nhiều tài khoản github trên cùng một máy, và một số dự án yêu cầu quyền truy cập. Để có thể clone có thể sử dụng `token` của github.
  - Truy cập: [Link](https://github.com/settings/tokens) để tạo token.
  - Copy link dự án của bạn. ví dụ: `https://github.com/Tran-Duc-Duy/DivSTeam`
  - Thêm `yourToken` vào như thế này: VD: `https://yourToken@github.com/Tran-Duc-Duy/DivSTeam`  
     _=> Khi đó bạn có thể clone được dự án._

2. Đặt tên commit có ý nghĩa.
3. Nên chia dự án thành nhiều commit nhỏ để dễ quản lý.
4. Không nên đặt tên thư mục, tên file có chứa khoảng trắng.
5. Khi bắt đầu một chức năng mới, nên thành nhánh khác để phát triển.
