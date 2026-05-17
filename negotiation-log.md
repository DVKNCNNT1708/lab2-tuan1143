# Negotiation Log — Pair 03 Core Business ↔ Access Gate

## Participants

- Provider: Access Gate Service (A3/B3)
- Consumer: Core Business Service (A6/B6)

---

# Issue 1 — Gate Status Enum

## Problem
Consumer muốn biết trạng thái realtime của cổng.

## Discussion
Hai bên thảo luận các trạng thái cần hỗ trợ.

## Decision
Sử dụng:
- OPEN
- CLOSED
- LOCKED

## Rationale
Đủ cho use case hiện tại.

---

# Issue 2 — RFID Format

## Problem
Cần thống nhất format cardId.

## Decision
Format:
RFID-YYYY-NNN

Ví dụ:
RFID-2026-001

## Rationale
Dễ validate và đồng bộ hệ thống.

---

# Issue 3 — Access Log Retention

## Problem
Consumer cần lịch sử truy cập.

## Decision
Provider lưu log tối thiểu 30 ngày.

## Rationale
Phục vụ audit và security review.

---

# Issue 4 — Unauthorized Handling

## Problem
Thiếu JWT token xử lý thế nào.

## Decision
Trả HTTP 401 theo Problem Details.

## Rationale
Tuân thủ REST API standard.

---

# Issue 5 — Pagination Strategy

## Problem
Danh sách log có thể rất lớn.

## Decision
Sử dụng cursor-based pagination.

## Rationale
Hiệu quả hơn offset pagination.

---

# Issue 6 — Core Business Timeout

## Problem
Nếu Core Business không phản hồi policy check.

## Decision
Access Gate mặc định DENY access.

## Rationale
Ưu tiên an toàn hệ thống.

---

# Final Agreement

Hai bên đồng ý sử dụng OpenAPI 3.1 contract-first trước khi implementation backend.