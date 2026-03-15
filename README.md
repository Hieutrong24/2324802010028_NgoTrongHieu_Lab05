# 2324802010028_NgoTrongHieu_Lab05

## Giới thiệu

Xin chào thầy,

Đây là bài **Lab 05** của em. Trong bài này em xây dựng một hệ thống gồm nhiều service theo kiến trúc **Microservices**. Các service được tách biệt để đảm bảo tính **độc lập, dễ mở rộng và dễ bảo trì**.

---

# Kiến trúc hệ thống

Hệ thống được thiết kế theo mô hình **Microservices Architecture**, trong đó mỗi service đảm nhiệm một chức năng riêng biệt:

- **auth-service**: xử lý xác thực và cấp token cho người dùng  
- **user-service**: quản lý thông tin người dùng  
- **content-service**: quản lý nội dung bài đăng  
- **chat-service**: xử lý chức năng chat  
- **notification-service**: gửi thông báo giữa các service  
- **code-judge-service**: xử lý chấm bài code  

Các service giao tiếp với nhau thông qua **RabbitMQ Message Broker** để thực hiện **giao tiếp bất đồng bộ (Asynchronous Communication)**.

---

# RabbitMQ

Trong hệ thống, em đã tích hợp **RabbitMQ** để kết nối các service.

RabbitMQ được sử dụng để:

- Gửi message giữa các service
- Giảm sự phụ thuộc trực tiếp giữa các service
- Tăng khả năng mở rộng và xử lý bất đồng bộ

Một số service có sử dụng RabbitMQ:

- **auth-service**
- **user-service**
- **code-judge-service**
- **notification-service**

---

# Clean Architecture

Trong project này, em đã áp dụng **Clean Architecture** cho các service quan trọng nhằm đảm bảo cấu trúc code rõ ràng và dễ bảo trì.

Các service áp dụng Clean Architecture gồm:

- **auth-service**
- **user-service**
- **code-judge-service**

Cấu trúc Clean Architecture gồm các layer chính:

- **Domain**
- **Application**
- **Infrastructure**
- **API**

Cách tổ chức này giúp **tách biệt logic nghiệp vụ với framework và database**.

---

# Docker

Toàn bộ hệ thống được **container hóa bằng Docker** để dễ dàng triển khai.

Project sử dụng:

- **Dockerfile** cho từng service
- **docker-compose.yml** để chạy toàn bộ hệ thống

Docker Compose giúp:

- Chạy nhiều service cùng lúc
- Quản lý container dễ dàng
- Kết nối các service với RabbitMQ và database

---

# Kết luận

Thông qua bài Lab này, em đã thực hành:

- Xây dựng hệ thống **Microservices**
- Sử dụng **RabbitMQ** để giao tiếp giữa các service
- Áp dụng **Clean Architecture**
- Triển khai hệ thống bằng **Docker và Docker Compose**

Em xin cảm ơn thầy đã xem bài của em.


## 🎥 Demo Video
https://youtu.be/COqKtYResqc
