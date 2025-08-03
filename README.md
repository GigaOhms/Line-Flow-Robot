# Line Flow Bot

**Line Flow Bot** là một robot dò line mini được thiết kế để học tập và nghiên cứu về RTOS, PID, điều khiển nhúng, cảm biến, thuật toán. Dự án này được tham khảo và chỉnh sửa từ project gốc: [Mini Line Flow Robot – MQCR Excel](https://bitbucket.org/mqcrexcel/mini-line-flow-robot/).

![](/.github/draw.png)
![](/.github/img.png)

---

## 🧠 Vi điều khiển (MCU)

- **STM32F103C8T6**: ARM Cortex-M3 phổ biến
- Tốc độ xung nhịp: 72 MHz
- Bộ nhớ Flash: 64 KB
- SRAM: 20 KB

---

## 🔋 Cấp nguồn

- Điện áp hoạt động: **5–9V**, từ pin Li-ion/LiPo hoặc nguồn ngoài.
- Mạch cấp nguồn gồm:
  - **2 x AMS1117**: chuyển từ 5V hoặc 9V xuống 5V và 3.3V 
  - **CH224K (USB Type-C PD Sink)**: cấu hình lấy ra 9V từ cổng USB PD thông qua thiết lập cấu hình điện trở.
  - Công tắc nguồn

---

## ⚙️ Phần cứng chính

### 🚗 Động cơ

- **2 x GA12 N20 500 RPM**
  - Điện áp hoạt động: 5-9V
  - Kết nối qua mạch **2 cầu H** sử dụng **L9110S**

### 🔍 Cảm biến dò line

- **8 x TCRT5000**
  - 7 cảm biến dùng để dò line đen-trắng
  - 1 cảm biến riêng để nhận tín hiệu bắt đầu

### 📦 Cảm biến gia tốc

- **GY-521 (MPU6050)**
  - Gia tốc kế + con quay hồi chuyển (6 DOF)
  - Giao tiếp I2C

### 📟 Hiển thị

- **LED 7 đoạn**
- **LED trạng thái rời**
- **LED nguồn 9V PD decoy**

### 🔘 Nút nhấn

- 2 nút nhấn dùng để cấu hình chế độ chạy hoặc hiệu chỉnh cảm biến

---

## 🧩 Giao tiếp và kết nối

- **SWD**: giao tiếp nạp chương trình và debug cho STM32
- **I2C**: giao tiếp với MPU6050

---
