# Product Schema

## Mục đích

Tài liệu này định nghĩa cấu trúc chuẩn cho các bản ghi sản phẩm trong kho tri thức Cadivi.

## Yêu cầu chung

- Sử dụng Markdown.
- Bắt đầu bằng YAML front matter.
- Chỉ ghi thông tin đã có nguồn xác thực.
- Nếu chưa xác minh được, để giá trị là `TODO` hoặc để trống.

## Front matter chuẩn

```yaml
---
id: <slug-unique>
brand: <brand-slug>
product_name: <tên sản phẩm>
product_code: <mã sản phẩm>
slug: <slug>
family: <family-slug>
status: draft
last_verified:
sources:
  - resources/<path/to/source>
---
```

## Cấu trúc nội dung

# <Tên sản phẩm>

## Tên sản phẩm

<Tên sản phẩm đầy đủ>

## Ứng dụng

<Mô tả ngắn về ứng dụng>

## Cấu trúc

1. Ruột dẫn: <loại vật liệu>
2. Cách điện: <loại vật liệu>

## Đặc tính kỹ thuật

TODO

## Tiêu chuẩn

TODO

## Bảng quy cách

TODO

## Ghi chú

<ghi chú nguồn hoặc lưu ý>

## Quy tắc ghi nhận

- Không suy diễn hoặc invent thông tin.
- Nếu không thấy rõ trong nguồn, ghi `TODO`.
- Khi có nguồn chính thức mới, cập nhật bản ghi.
