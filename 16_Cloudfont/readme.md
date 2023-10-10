# 16 Tìm hiểu về Cloudfont
## 1. What is CloudFront
Là một CDN service của AWS.
Vậy CDN là gì?
=>Viết tắt của Content Delivery Network, một mạng lưới giúp delivery nội dung tới người dùng cuối một cách nhanh chóng nhờ vào việc điều hướng request của họ tới các máy chủ chứa tài nguyên gần nhất.

## 2 Tác dụng Content Delivery Network

Khi không có CDN, tài nguyên của server sẽ được deliver tới client một cách trực tiếp. =>Tuỳ vào khoảng cách địa lý mà tốc độ truy cập sẽ nhanh hay chậm.
Khi có CDN, tài nguyên của server sẽ được cache trên các máy chủ Edge, request của user tới một tài nguyên trên CloudFront sẽ được redirect tới máy chủ Edge gần nhất.

Các khái niệm Cloudfont
	-Cache: AWS CloudFront lưu trữ các tài nguyên tại edge location để giảm thời gian phản hồi và tăng tốc độ tải trang web. Các tài nguyên này bao gồm hình ảnh, tập tin CSS và JavaScript.
	- Logging and Reporting: AWS CloudFront cung cấp các báo cáo về hoạt động của distribution, bao gồm lưu lượng và số lần truy cập.
	- Security: AWS CloudFront hỗ trợ nhiều tính năng bảo mật, bao gồm kết nối HTTPS, chữ ký số (Certificate) và xác thực người dùng.
	- Customize at the Edge: thông qua cơ chế Lambda@Edge, cho phép bạn thực thi các function trên các sự kiện CloudFront. Lợi thế về tốc độ và hiệu suất so với thực thi ở Origin. Một số use-case có thể kể đến như: Authen/Author, xử lý tính toán đơn giản, SEO, Intelligent routing, Anti Bot, Realtime image transformation, A/B Testing, User prioritilization.