# Provider Analysis — Access Gate Service

## Service Name
Access Gate Service

## Responsibilities
Access Gate Service chịu trách nhiệm:

- Quản lý trạng thái cổng ra vào
- Ghi nhận log quẹt thẻ RFID
- Cung cấp lịch sử truy cập cho Core Business
- Hỗ trợ kiểm tra trạng thái cổng realtime

## Main APIs

### GET /gates
Trả danh sách cổng trong hệ thống.

### GET /gates/{gateId}/status
Lấy trạng thái realtime của cổng.

### GET /access-logs/recent
Lấy access log gần đây.

### POST /access-logs
Ghi nhận access log mới từ thiết bị cổng.

## Validation Rules

- gateId phải có dạng `GATE-XX`
- cardId phải có dạng `RFID-YYYY-NNN`
- status chỉ gồm:
  - OPEN
  - CLOSED
  - LOCKED

## Possible Errors

- Gate not found
- Invalid RFID format
- Unauthorized request
- Internal server error

## Non-functional Requirements

- Response realtime dưới 2 giây
- API sử dụng Bearer JWT
- Log retention tối thiểu 30 ngày