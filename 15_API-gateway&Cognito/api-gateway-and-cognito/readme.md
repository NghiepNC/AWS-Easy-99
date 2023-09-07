# API Gateway & Cognito

## API Gateway là gì?
Một dịch vụ API Gateway được cung cấp bởi AWS. Nó cung cấp một cách đơn giản để xây dựng, quản lý và bảo mật các RESTful API hoặc WebSocket. AWS API Gateway là một dịch vụ quan trọng trong kiến trúc dựa trên các dịch vụ của AWS (AWS-based microservices architecture) và thường được sử dụng cùng với các dịch vụ AWS khác như AWS Lambda, EC2, S3, Amazon DynamoDB.

## API Gateway là gì?
AWS API Gateway cung cấp các tính năng:
- Cho phép thiết kế và phát triển API RESTful hoặc WebSocket thông qua web GUI.
- Điều phối các yêu cầu API đến các hệ thống hoặc dịch vụ khác nhau.
- Authen/Author request tới các API.
- Quản lý và giám sát các yêu cầu API, vd số lượng request,
response time...
- AWS API Gateway cũng cung cấp các tính năng bảo mật, bao gồm chứng thực và ủy quyền các yêu cầu API và mã hóa secure communication giữa các hệ thống khác nhau.

## Đặc trưng của API Gateway
- Là một fully managed service của AWS.
- Khả năng scale và High Availablity không giới hạn.
- Zero idle cost
- Easy to setup
- Dễ dàng kết hợp với các dịch vụ khác như CloudWatch, WAF cho mục đích monitor & security.

## Hệ sinh thái API Gateway
API Gateway là một service chủ yếu có nhiệm vụ nhận request của client sau đó forward tới các service phía sau.

## Khi nào nên sử dụng API Gateway?
API Gateway phù hợp cho những bài toán sau
- Kiến trúc Micro-service sử dụng lambda làm backend
- Backend API cho hầu hết các use case (web API, IoT)
- Gateway nhận data trực tiếp từ client sau đó lưu vào DynamoDB (DB First) 
- Web Socket cho những hệ thống realtime communication.