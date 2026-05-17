# API Versioning Strategy

## Current Version
v1.0.0

## Versioning Rules

### Major Version
Tăng major version khi:

- Breaking API changes
- Xóa field cũ
- Đổi response format

Ví dụ:
v1 → v2

### Minor Version
Tăng minor version khi:

- Thêm field mới
- Thêm endpoint mới
- Không phá vỡ compatibility

Ví dụ:
v1.0 → v1.1

### Patch Version
Tăng patch version khi:

- Sửa lỗi documentation
- Fix typo
- Không đổi behavior API

Ví dụ:
v1.0.0 → v1.0.1

## Backward Compatibility

- Không xóa field đang dùng
- Không đổi kiểu dữ liệu field cũ
- Deprecated endpoint phải giữ ít nhất 1 version