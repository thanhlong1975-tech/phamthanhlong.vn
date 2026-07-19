# Kiến trúc Kho Tri thức An Sơn

## Mục đích

Tài liệu này mô tả cấu trúc kiến trúc của Kho Tri thức An Sơn, nhằm tổ chức dữ liệu một cách nhất quán, có thể dùng lại và dễ duy trì.

## Cấu trúc phân cấp

```text
Brand
├── Product Family
│   ├── Product
│   │   ├── SKU
│   │   ├── Datasheet
│   │   ├── Images
│   │   ├── FAQ
│   │   └── Standards
```

## Mỗi cấp có vai trò gì

### Brand

Brand là mức cao nhất, đại diện cho thương hiệu hoặc nhãn hiệu chính. Mức này tập trung mô tả thông tin chung của thương hiệu, bao gồm bản sắc, phạm vi hoạt động và các nhóm sản phẩm liên quan.

### Product Family

Product Family là nhóm sản phẩm thuộc cùng một hướng hoặc cùng một dòng sản phẩm trong một brand. Mức này giúp gom các sản phẩm có đặc điểm, mục đích sử dụng hoặc cấu trúc tương đồng lại với nhau.

### Product

Product là sản phẩm cụ thể nằm trong một product family. Mức này chứa thông tin chung về sản phẩm, bao gồm mô tả, ứng dụng và các tài liệu liên quan.

### SKU

SKU là biến thể cụ thể của một product. Mức này dùng để biểu thị phiên bản riêng biệt của sản phẩm, như màu sắc, kích thước hoặc cấu hình khác nhau.

### Datasheet

Datasheet là tài liệu kỹ thuật hoặc thông tin tham khảo liên quan đến sản phẩm. Mức này lưu trữ dữ liệu mô tả kỹ thuật, đặc tính và tài liệu hỗ trợ tra cứu.

### Images

Images là kho hình ảnh liên quan đến sản phẩm hoặc SKU. Mức này giúp lưu trữ và tái sử dụng hình ảnh một cách có tổ chức.

### FAQ

FAQ là tập hợp các câu hỏi thường gặp liên quan đến sản phẩm hoặc thương hiệu. Mức này hỗ trợ lưu trữ các câu hỏi và câu trả lời đã được chuẩn hóa.

### Standards

Standards là các tiêu chuẩn hoặc yêu cầu liên quan đến sản phẩm, có thể dùng để liên kết với dữ liệu kỹ thuật hoặc quy chuẩn.

## Quan hệ giữa các mức

Mỗi mức có mối liên hệ với các mức khác theo cấu trúc phân cấp:

- Một brand có thể chứa nhiều product family.
- Một product family có thể chứa nhiều product.
- Một product có thể có nhiều SKU.
- Một product có thể có nhiều datasheet, images, FAQ và standards liên quan.

Quan hệ này cho phép dữ liệu được tổ chức theo tầng, giúp phân biệt thông tin chung và thông tin chi tiết.

## Vì sao thông tin chỉ nên tồn tại một lần

Thông tin nên chỉ tồn tại ở một vị trí duy nhất trong kho tri thức để tránh sự mâu thuẫn và trùng lặp. Nếu cùng một dữ liệu được lưu ở nhiều nơi, rất dễ xảy ra tình trạng không thống nhất giữa các bản ghi.

Giữ một bản chính duy nhất giúp:

- giảm nguy cơ sai lệch thông tin;
- dễ kiểm soát cập nhật;
- giảm công sức duy trì;
- tăng độ nhất quán cho toàn bộ hệ thống.

## Vì sao mỗi đối tượng nên có ID duy nhất

Mỗi đối tượng trong kho tri thức nên có một ID duy nhất để có thể được nhận diện rõ ràng và tham chiếu một cách chính xác.

ID duy nhất giúp:

- phân biệt các đối tượng có tên tương tự;
- tránh nhầm lẫn giữa các bản ghi;
- hỗ trợ liên kết dữ liệu giữa các tầng;
- làm việc tốt hơn với tự động hóa và AI.

## Vì sao AI nên tái sử dụng dữ liệu thay vì sao chép

AI nên tận dụng dữ liệu có sẵn trong kho tri thức thay vì tạo ra bản sao riêng cho từng ứng dụng. Điều này giúp dữ liệu được dùng lại một cách nhất quán và giảm nguy cơ phát sinh nhiều phiên bản khác nhau.

Tái sử dụng dữ liệu mang lại lợi ích:

- dữ liệu luôn được cập nhật từ một nguồn thống nhất;
- giảm việc chỉnh sửa nhiều chỗ khi thông tin thay đổi;
- giúp các ứng dụng khác nhau dựa trên cùng một nền tảng dữ liệu;
- nâng cao tính nhất quán và độ tin cậy của kết quả đầu ra.

## Single Source of Truth

Single Source of Truth có nghĩa là mọi ứng dụng phải sử dụng dữ liệu từ cùng một kho tri thức chung. Không nên duy trì các bản sao dữ liệu riêng trong từng công cụ hoặc quy trình khác nhau.

Khi tất cả hệ thống đều tiêu thụ dữ liệu từ cùng một nguồn, thông tin sẽ được quản lý tập trung, dễ kiểm tra và dễ đồng bộ. Đây là nền tảng để hệ thống kiến thức có thể phát triển một cách bền vững và nhất quán.
