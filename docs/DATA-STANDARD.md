# Tiêu chuẩn dữ liệu Kho Tri thức An Sơn

## 1. Mục tiêu

Tài liệu này là tiêu chuẩn dữ liệu chính thức cho toàn bộ kho tri thức của An Sơn. Mọi thông tin được ghi nhận trong repository phải có nguồn có thể kiểm chứng được. Không được suy đoán, dựng lại hoặc đưa vào dữ liệu những thông tin chưa được xác minh.

Mỗi mẩu thông tin phải có ít nhất một nguồn rõ ràng và đáng tin cậy trước khi được coi là hợp lệ.

## 2. Cấu trúc dữ liệu

Cấu trúc dữ liệu chính được tổ chức theo tầng liên kết sau:

- Brand: thương hiệu chính
- Product Family: nhóm sản phẩm thuộc một thương hiệu
- Product: sản phẩm cụ thể trong một product family
- SKU: biến thể cụ thể của sản phẩm, ví dụ theo màu sắc, kích thước hoặc cấu hình

Quan hệ giữa các tầng như sau:

- Một brand có thể có nhiều product family.
- Một product family có thể chứa nhiều product.
- Một product có thể có nhiều SKU.
- Mỗi SKU phải thuộc về một product cụ thể.

Cấu trúc này giúp đảm bảo dữ liệu được tổ chức nhất quán, dễ tra cứu và dễ cập nhật.

## 3. Quy tắc đặt ID

Mọi tài liệu hoặc đối tượng dữ liệu phải có ID rõ ràng, nhất quán và có thể đọc được bằng máy.

Các ví dụ về ID hợp lệ:

- brand-cadivi
- pf-cadivi-cv
- product-cadivi-cv-2x15
- sku-cadivi-cv-2x15-black

Quy tắc chung:

- Sử dụng chữ thường.
- Dùng dấu gạch nối cho các từ riêng biệt.
- Bắt đầu bằng tiền tố mô tả loại đối tượng: brand, pf, product, sku.
- Giữ tên ngắn gọn, súc tích và có thể truy xuất dễ dàng.

## 4. Quy tắc đặt slug

Slug dùng cho đường dẫn và tham chiếu dữ liệu phải tuân thủ các quy tắc sau:

- Viết bằng chữ thường.
- Chỉ dùng dấu gạch nối (-).
- Không dùng dấu tiếng Việt hoặc ký tự có dấu.
- Không dùng khoảng trắng.
- Không dùng ký tự đặc biệt không cần thiết.

Ví dụ:

- cadivi
- product-family-cadivi
- product-cadivi-cv-2x15

## 5. Quy tắc ghi nguồn

Mọi thông tin factual phải được ghi rõ nguồn. Nguồn được phép sử dụng bao gồm:

- Official website
- Official catalogue
- Official datasheet
- Official price list
- Government standard

Quy tắc bắt buộc:

- Không sử dụng nguồn không rõ ràng.
- Không sử dụng nguồn không xác minh được.
- Không sử dụng suy đoán hoặc thông tin từ blog, forum hoặc trang không chính thức nếu chưa có xác nhận.
- Nếu không có nguồn, phải ghi TODO thay vì đưa ra giả định.

## 6. Quy tắc TODO

Khi thông tin chưa có sẵn hoặc chưa được xác minh, cần thực hiện theo quy tắc sau:

- Viết đúng từ TODO.
- Không tự ý invent thông tin.
- Không điền dữ liệu mơ hồ khi chưa có bằng chứng.
- Khi có nguồn mới, cập nhật tài liệu để thay thế TODO bằng thông tin đã xác minh.

## 7. Quy trình cập nhật

Mọi thay đổi dữ liệu phải tuân thủ quy trình sau:

1. Research: tìm kiếm thông tin từ các nguồn chính thức và đáng tin cậy.
2. Verify: kiểm tra tính chính xác và tính nhất quán của thông tin.
3. Update: cập nhật nội dung phù hợp trong repository.
4. Commit: thực hiện commit với nội dung rõ ràng.
5. Push: đẩy thay đổi lên kho lưu trữ.

## 8. Versioning

Mọi cập nhật quan trọng phải được ghi nhận bằng Git thông qua commit. Điều này đảm bảo:

- Lịch sử thay đổi được lưu lại đầy đủ.
- Các sửa đổi có thể được kiểm tra và theo dõi.
- Tài liệu và dữ liệu trong repository luôn có tính minh bạch và có thể quản lý được.

Tài liệu này là tiêu chuẩn dữ liệu chính thức cho toàn bộ repository.
