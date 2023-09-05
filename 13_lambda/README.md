# 13 _ Lambda
Hôm nay mình sẽ cùng tìm hiểu về dịch vụ serverless trên AWS là Lambda

## What is Lambda?
Một service serverless của AWS cho phép người dùng thực thi code mà không cần quan tâm tới hạ tầng phía sau.
Lamda hỗ trợ các ngôn ngữ (runtime) sau: 
* Java
* Python 
* .NET
* GO
* Ruby
* Custom Runtime 

## Đặc trưng của Lambda
* Khi tạo 1 lambda function, bạn quyết định cấu hình thông qua thông số Memory. Min = 128MB, Max = 10GB. Memory càng cao, CPU được allocate càng lớn.
* Lambda khi khởi chạy được cấp phát 1 vùng nhớ tạm min = 512MB max =10GB, sẽ bị xoá khi lambda thực thi xong.
* Timeout tối đa 15 phút (quá thời gian này nếu execute chưa xong vẫn tính là failed và bị thu hồi resource).
* Lambda có thể được trigger từ nhiều nguồn: Trigger trực tiếp (Console or CLI), API Gateway, event từ các service khác (S3, SQS, DynamoDB, Kinesis, IoT...), hoặc chạy theo lịch (trigger từ EventBridge).

* Lambda có 2 mode chạy là chạy ngoài VPC và chạy trong VPC. Thông thường nếu lambda cần kết nối với RDS Database thì nên để trong VPC. *Lưu ý đến số lượng IP của subnet chứa lambda.
* Lambda sau khi chạy xong sẽ không lưu lại bất cứ gì
	- Log -> CloudWatch log
	- File output -> S3 hoặc EFS
	- Data output -> RDS Database hoặc DynamoDB.
* Lambda cũng cần được cấp IAM Role để có thể tương tác với các resource khác. Mặc định Lambda khi tạo ra sẽ được gán Role có các quyền cơ bản (vd write log to CloudWatch).

* Lambda không chỉ chứa 1 file code mà có thể chứa các file library, file common,... Để tiện dụng ta có thể gom nhóm chúng lại thành các **layer** và tái sử dụng ở nhiều function, tránh duplicate code.
* Khi có nhiều request từ client, Lambda scale horizontal bằng cách gia tăng số lượng concurent execute. Giới hạn này mặc định khi tạo account AWS là **10 concurent executions**. Cần request tăng số này lên trước khi release production.
* Lambda có thể được set một số **reserve concurent** để tránh bị ảnh hưởng bởi các lambda khác.
