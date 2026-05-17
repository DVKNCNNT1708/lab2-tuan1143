# Consumer Analysis — Access Gate → Core Business

## Consumer Service
Access Gate Service

## Required Provider
Core Business Service

## Purpose
Access Gate cần gọi Core Business để kiểm tra policy ra/vào realtime.

## Required Information

Access Gate cần nhận:

- allowAccess
- policyReason
- userRole
- expiryTime

## Performance Requirement

- Policy response dưới 1 giây
- API phải hỗ trợ realtime decision

## Error Handling

Nếu Core Business không phản hồi:

- mặc định deny access
- ghi log lỗi vào hệ thống

## Security

- JWT Bearer Authentication
- TLS required