```markdown
<div align="center">

# 🌱 Code for Green School: Eco Survival

### 🏫 *"CÙNG THPT BÌNH CHÁNH SỐNG XANH"*

**Trò chơi 2D Pixel Art giáo dục về bảo vệ môi trường & sinh tồn học đường**

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg?style=for-the-badge&logo=gnu)](https://www.gnu.org/licenses/gpl-3.0)
[![Made with JavaScript](https://img.shields.io/badge/Made%20with-JavaScript-F7DF1E.svg?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Backend Firebase](https://img.shields.io/badge/Backend-Firebase-FFCA28.svg?style=for-the-badge&logo=firebase&logoColor=black)](https://firebase.google.com/)
[![Deploy GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-22C55E.svg?style=for-the-badge&logo=githubpages&logoColor=white)](https://pages.github.com/)

[![GitHub stars](https://img.shields.io/github/stars/hihiquan2010/GreenProject?style=social)](https://github.com/hihiquan2010/GreenProject/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/hihiquan2010/GreenProject?style=social)](https://github.com/hihiquan2010/GreenProject/network)
[![GitHub issues](https://img.shields.io/github/issues/hihiquan2010/GreenProject)](https://github.com/hihiquan2010/GreenProject/issues)

---

### 🎮 [**👉 BẤM VÀO ĐÂY ĐỂ CHƠI NGAY TRÊN BROWSER 👈**](https://hihiquan2010.github.io/GreenProject/)

*Đường dẫn truy cập trực tiếp:* `https://hihiquan2010.github.io/GreenProject/`

---

*🏆 Dự án tham gia **Hội thi CLB Tin Học 2026–2027** với chủ đề **"Lập Trình Vì Ngôi Trường Xanh"***

</div>

---

## 📑 Mục lục

- [📖 Giới thiệu](#-giới-thiệu)
- [🎮 Gameplay & Cơ chế](#-gameplay--cơ-chế)
  - [⏰ Thời khóa biểu một ngày](#-thời-khóa-biểu-một-ngày)
  - [🌤️ Hệ thống thời tiết](#️-hệ-thống-thời-tiết)
  - [🌡️ Cơ chế nhiệt độ cơ thể](#️-cơ-chế-nhiệt-độ-cơ-thể)
  - [♻️ Dọn rác & Giảm ô nhiễm](#️-dọn-rác--giảm-ô-nhiễm)
  - [🔇 Minigame "Giữ im lặng"](#-minigame-giữ-im-lặng)
  - [🎭 Hệ thống nhân vật](#-hệ-thống-nhân-vật)
- [👥 Chơi nhóm Online (Multiplayer)](#-chơi-nhóm-online-multiplayer)
- [🎨 Đồ họa & Thiết kế](#-đồ-họa--thiết-kế)
- [🎯 Hướng dẫn điều khiển](#-hướng-dẫn-điều-khiển)
- [🛠️ Công nghệ sử dụng](#️-công-nghệ-sử-dụng)
- [🚀 Cài đặt & Triển khai](#-cài-đặt--triển-khai)
- [📁 Cấu trúc dự án](#-cấu-trúc-dự-án)
- [🎓 Giá trị giáo dục](#-giá-trị-giáo-dục)
- [🤝 Đóng góp phát triển](#-đóng-góp-phát-triển)
- [👨‍💻 Tác giả](#-tác-giả)
- [📜 Giấy phép](#-giấy-phép)
- [🙏 Lời cảm ơn](#-lời-cảm-ơn)

---

## 📖 Giới thiệu

**Code for Green School: Eco Survival** là một trò chơi **Web 2D Top-down Pixel Art** mô phỏng sinh động một ngày học tập tại **Trường THPT Bình Chánh**. 

Người chơi hóa thân thành một học sinh, thực hiện các nhiệm vụ sinh tồn qua từng tiết học, ứng phó với điều kiện thời tiết khắc nghiệt, giữ gìn vệ sinh chung và chung tay xây dựng môi trường học đường xanh - sạch - đẹp.

### 🎯 Nhiệm vụ chính trong game

| Nhiệm vụ | Biểu tượng | Mô tả chi tiết |
| :--- | :---: | :--- |
| **Sinh tồn** | 🎒 | Duy trì chỉ số sinh mệnh ($HP > 0$) xuyên suốt các ngày học |
| **Ứng phó thời tiết** | 🌤️ | Linh hoạt thích nghi với Oi bức, Ô nhiễm và Mưa phùn |
| **Bảo vệ môi trường** | ♻️ | Thu gom rác thải, dọn dẹp sân trường để hồi HP và giảm ô nhiễm |
| **Kỷ luật lớp học** | 🪑 | Tuân thủ giờ giấc, ngồi đúng vị trí khi vào tiết |
| **Tiết kiệm năng lượng** | ⚡ | Tắt quạt và thiết bị điện khi ra khỏi phòng học |
| **Rèn luyện tập trung** | 🔇 | Chinh phục minigame "Giữ im lặng" trong giờ giảng |
| **Hợp tác đồng đội** | 👥 | Kết nối multiplayer realtime cùng bạn bè qua Firebase |

### 💡 Nguồn cảm hứng thiết kế

Bản đồ trò chơi được tái hiện tỉ mỉ từ **ảnh chụp thực tế của Trường THPT Bình Chánh**:
- Dãy nhà lớp học 2 tầng mái ngói đỏ đặc trưng
- Sân trường rộng lớn với cột cờ Tổ quốc trung tâm
- Hàng cây xanh rợp bóng mát và các bồn hoa hai bên sân

---

## 🎮 Gameplay & Cơ chế

### ⏰ Thời khóa biểu một ngày

Một ngày học trong game trải qua **7 tiết học** xen kẽ các giờ ra chơi:


```

┌──────────────────┐    ┌────────┐    ┌────────┐    ┌──────────┐
│ RA CHƠI SÁNG 30s │ ➔ │ TIẾT 1 │ ➔ │ TIẾT 2 │ ➔ │ RA CHƠI  │
└──────────────────┘    │  60s   │    │  60s   │    │   30s    │
└────────┘    └────────┘    └──────────┘
│
┌──────────┐    ┌────────┐    ┌────────┐    ┌────────┐   │
│  TIẾT 7  │ ◄─ │ TIẾT 6 │ ◄─ │ TIẾT 5 │ ◄─ │ RA CHƠI │ ◄┘
│   60s    │    │  60s   │    │  60s   │    │  30s   │ ◄─ ┌────────┐
└──────────┘    └────────┘    └────────┘    └────────┘    │ TIẾT 3 │
│ TIẾT 4 │
└────────┘

```

* **Thời gian mỗi tiết học:** 60 giây
* **Thời gian giờ ra chơi:** 30 giây
* **Thời gian chuyển tiết:** 3 giây *(kèm hiệu ứng tiếng chuông 🔔)*

---

### 🌤️ Hệ thống thời tiết

Mỗi ngày học chỉ xuất hiện **DUY NHẤT MỘT** loại thời tiết. Từ **Ngày 4 trở đi**, thời tiết sẽ thay đổi ngẫu nhiên *(không lặp lại thời tiết của ngày liền trước)*.

| Loại thời tiết | Biểu tượng | Hiệu ứng môi trường | Cách ứng phó hiệu quả |
| :--- | :---: | :--- | :--- |
| **OI BỨC** | ☀️ | Nhiệt độ tăng cao liên tục khi ở trong lớp không bật quạt | Tắt điện khi ra chơi, bật quạt khi vào tiết |
| **Ô NHIỄM** | ☣️ | Rác thải bốc mùi, chất lượng không khí suy giảm | Tích cực nhặt rác bỏ vào Thùng Rác Xanh |
| **MƯA PHÙN** | 🌧️ | Vũng nước gây trơn trượt, hệ thống cống tắc nghẽn | Tắt quạt tránh lạnh, né vũng nước, thông cống |

---

### 🌡️ Cơ chế nhiệt độ cơ thể

Thanh nhiệt độ hiển thị trong khoảng **0°C → 100°C** *(mức nhiệt độ chuẩn là **50°C**)*:

| Trạng thái | Ngưỡng nhiệt độ | Tác động lên nhân vật |
| :--- | :---: | :--- |
| 🔥 **Sốc nhiệt** | $> 85^\circ\text{C}$ | Mất **4 HP / giây** |
| ♨️ **Nóng** | $> 70^\circ\text{C}$ | Mất **1 HP / giây** |
| ✅ **Bình thường** | $30^\circ\text{C} \le T \le 70^\circ\text{C}$ | Cơ thể ổn định, không mất HP |
| 🧊 **Mát** | $< 30^\circ\text{C}$ | Mất **1 HP / giây** |
| ❄️ **Hạ thân nhiệt** | $< 15^\circ\text{C}$ | Mất **3 HP / giây** |

> [!IMPORTANT]
> **Quy tắc vàng về nhiệt độ:**
> * ☀️ **Trời nắng nóng:** Bật quạt giúp hạ nhiệt độ cơ thể **về mức chuẩn 50°C** *(không giảm xuống thấp hơn)*.
> * 🌧️ **Trời mưa lạnh:** Bật quạt sẽ tiếp tục hạ nhiệt độ **xuống dưới 50°C**, dễ dẫn đến nguy cơ hạ thân nhiệt!

---

### ♻️ Dọn rác & Giảm ô nhiễm

Thu gom và bỏ rác vào **Thùng Rác Xanh** *(góc dưới bên phải sân trường)* để phục hồi HP:

#### 1. Cơ chế hồi phục sinh mệnh (HP)
| Số lượng rác | HP hồi phục thường | HP hồi phục (Bảo Ngọc - Nội tại $\times 1.5$) |
| :---: | :---: | :---: |
| **1 rác** | +4 HP | +6 HP |
| **3 rác** | +12 HP | +18 HP |
| **5 rác (Túi đầy)** | **+25 HP** *(Bonus +5 HP)* | **+38 HP** |

#### 2. Cơ chế giảm tỷ lệ ô nhiễm ngày tiếp theo
| Số rác dọn hôm nay | Mức độ giảm ô nhiễm | Tỷ lệ xuất hiện Ô nhiễm ngày mai |
| :---: | :---: | :---: |
| **0 rác** | 0% | 35% |
| **5 rác** | 25% | 26% |
| **10 rác** | 50% | 17% |
| **12+ rác** | **60% (Tối đa)** | **14% (Thấp nhất)** |

---

### 🔇 Minigame "Giữ im lặng"

Trong giờ học, giáo viên sẽ ngẫu nhiên kiểm tra độ tập trung của lớp:

* ⏱️ Mỗi **10 giây**, có **80% xác suất** xuất hiện minigame.
* 🎯 Nhấn **SPACE / CLICK / TAP** chính xác khi kim trượt vào **Vùng Xanh**.
* ✅ Nhân vật **Gia Uy** sở hữu vùng xanh rộng hơn (**40%**), giúp thao tác dễ dàng hơn.
* ❌ Thất bại **3 lần**: Mất **10 HP** và bị giáo viên khiển trách.

---

### 🎭 Hệ thống nhân vật

| Nhân vật | Vai trò | Kỹ năng đặc biệt | Đặc điểm tạo hình Pixel |
| :---: | :---: | :--- | :--- |
| **Gia Hưng** | 🏃 Năng động | Tốc độ di chuyển **+20%** | Dáng cao, cân đối, tóc ngắn |
| **Bảo Ngọc** | ♻️ Lớp xanh | Hồi thêm **+8 HP/ngày**, x1.5 HP từ rác | Nữ, nhỏ nhắn, **tóc dài** |
| **Minh Thái** | 🛡️ Cờ đỏ | Giảm sát thương nhận vào, chống chịu tốt | **Cao nhất, vóc dáng to khỏe** |
| **Gia Uy** | 💻 CLB Tin Học | Tốc độ quạt **x2**, minigame dễ hơn | Dáng cao, **đeo kính tri thức** |

---

## 👥 Chơi nhóm Online (Multiplayer)

Tích hợp tính năng **Multiplayer Realtime** qua **Firebase Realtime Database** — giúp trải nghiệm mượt mà cùng bạn bè trên trình duyệt mà không cần cài đặt server.

### 📋 Sơ đồ kết nối phòng chơi


```

┌───────────────────────────┐                 ┌───────────────────────────┐
│        CHỦ PHÒNG          │                 │          BẠN BÈ           │
├───────────────────────────┤                 ├───────────────────────────┤
│ 1. Chọn chế độ Online     │                 │ 1. Chọn chế độ Online     │
│ 2. Bấm "Tạo phòng"        │ ── Gửi mã ───►  │ 2. Bấm "Vào phòng"        │
│ 3. Nhận mã Phòng (6 ký tự)│   (Zalo/Mess)   │ 3. Nhập mã phòng          │
│ 4. Bấm "Bắt đầu"          │ ◄─ Khách vào ── │ 4. Chờ chủ phòng bắt đầu  │
└───────────────────────────┘                 └───────────────────────────┘

```

### 🔄 Các dữ liệu được đồng bộ Realtime

- 📍 **Vị trí & Hướng nhìn:** Tọa độ $(x, y)$ và hướng mặt (Trái/Phải/Lên/Xuống)
- 🏃 **Animation:** Chuỗi khung hình đi bộ, thao tác quạt tay
- 🎒 **Trạng thái:** Ngồi ghế, cầm rác, quạt mát, mở cửa
- ⚡ **Tương tác môi trường:** Bật/tắt đèn quạt, thông cống, nhặt rác
- 🌡️ **Chỉ số sinh tồn:** Thanh nhiệt độ và lượng HP của đồng đội
- ⏰ **Thời gian hệ thống:** Đồng bộ tiến trình tiết học và giờ ra chơi

---

## 🎨 Đồ họa & Thiết kế

### 🏫 Bản đồ trường học Pixel Art

Bản đồ trò chơi được dựng tỉ mỉ theo cấu trúc thực tế của **Trường THPT Bình Chánh**:

* 🏫 **Dãy nhà chính:** 2 tầng, mái ngói đỏ, 12 cửa sổ, hàng hiên 12 cột.
* 🚩 **Cột cờ trung tâm:** Đặt tại giữa sân, lá cờ đỏ sao vàng tung bay.
* 🌳 **Cảnh quan:** 6 cây xanh rợp bóng, 2 bồn hoa phía trước sân.
* 🛡️ **Khu vực chức năng:** Bốt bảo vệ (góc dưới trái), Thùng rác xanh (góc dưới phải), Hệ thống cống thoát nước.
* 🚪 **Các phòng học:** Phòng 10A3, 11A3, 12A3 được trang bị đầy đủ bàn ghế, bảng đen, quạt và công tắc.

### 👤 Thông số khởi tạo nhân vật Pixel

```json
{
  "GiaHung":  { "height": 1.10, "width": 1.00, "hasGlasses": false, "hasLongHair": false },
  "BaoNgoc":  { "height": 0.92, "width": 0.92, "hasGlasses": false, "hasLongHair": true  },
  "MinhThai": { "height": 1.28, "width": 1.22, "hasGlasses": false, "hasLongHair": false },
  "GiaUy":    { "height": 1.15, "width": 1.00, "hasGlasses": true,  "hasLongHair": false }
}

```

---

## 🎯 Hướng dẫn điều khiển

### 💻 Trên Máy tính (PC / Laptop)

| Phím bấm | Thao tác tương ứng |
| --- | --- |
| W A S D / ↑ ↓ ← → | Di chuyển nhân vật |
| E | Tương tác *(Nhặt rác, bật/tắt công tắc, mở cửa, nói chuyện)* |
| F hoặc Space | Quạt tay / Ngồi vào ghế học |
| Space | Thực hiện canh nhịp trong minigame "Giữ im lặng" |

### 📱 Trên Điện thoại / Máy tính bảng

Giao diện cảm ứng tối ưu hóa cho màn hình di động:

* 🕹️ **Joystick ảo (Góc trái):** Điều khiển di chuyển linh hoạt 360°.
* 🅴 **Nút E (Góc phải):** Tương tác với vật thể gần nhất.
* 🅵 **Nút F (Góc phải):** Thực hiện quạt tay làm mát.
* 🪑 **Nút Ghế (Góc phải):** Ngồi xuống / Đứng dậy.
* ⚙️ **Nút Menu (Góc trên):** Tạm dừng và xem hướng dẫn.

---

## 🛠️ Công nghệ sử dụng

```
+-----------------------------------------------------------------------+
|                           FRONTEND & CORE                             |
|  HTML5 Canvas 2D API  |  Vanilla JavaScript (ES6+)  |  CSS3 Flex/Grid  |
+-----------------------------------------------------------------------+
                                   │
                  ┌────────────────┴────────────────┐
                  ▼                                 ▼
+-----------------------------------+ +-----------------------------------+
|       BACKEND & MULTIPLAYER       | |         AUDIO & ASSETS          |
|  Firebase Realtime Database 10.x  | | Web Audio API (Procedural Synthes)|
|  GitHub Pages (Static Hosting)    | | Google Fonts (Press Start 2P)   |
+-----------------------------------+ +-----------------------------------+

```

* ⚡ **Không phụ thuộc Framework nặng:** Giúp trò chơi đạt tốc độ tải cực nhanh và hoạt động mượt mà trên các thiết bị cấu hình trung bình.
* 🎨 **Procedural Canvas Rendering:** Toàn bộ đồ họa và hiệu ứng âm thanh được tổng hợp trực tiếp bằng mã nguồn, tối ưu dung lượng lưu trữ.

---

## 🚀 Cài đặt & Triển khai

### 📋 Yêu cầu môi trường

* Trình duyệt web hiện đại *(Chrome, Firefox, Edge, Safari)* hỗ trợ **HTML5 Canvas** và **ES6+**.
* Kết nối Internet *(để tải Firebase SDK và Font chữ)*.

### 🔧 Các bước thực hiện

#### 1. Clone Repository

```bash
git clone [https://github.com/hihiquan2010/GreenProject.git](https://github.com/hihiquan2010/GreenProject.git)
cd GreenProject

```

#### 2. Cấu hình Firebase Realtime Database

1. Truy cập [Firebase Console](https://console.firebase.google.com/) và tạo dự án mới.
2. Vào mục **Build ➔ Realtime Database ➔ Create Database** *(Chọn khu vực Singapore)*.
3. Chuyển sang tab **Rules**, thiết lập quyền truy cập và bấm **Publish**:

```json
{
  "rules": {
    "rooms": {
      "$roomCode": {
        ".read": true,
        ".write": true
      }
    }
  }
}

```

#### 3. Cập nhật mã nguồn `index.html`

Sao chép mã cấu hình Firebase Web App của bạn và dán vào vị trí tương ứng trong file `index.html`:

```javascript
// ⚠️ CẤU HÌNH FIREBASE REALTIME DATABASE
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  databaseURL: "https://YOUR_PROJECT-default-rtdb.asia-southeast1.firebasedatabase.app",
  projectId: "YOUR_PROJECT",
  storageBucket: "YOUR_PROJECT.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};

```

#### 4. Deploy lên GitHub Pages

```bash
git add index.html
git commit -m "feat: Configure Firebase credentials"
git push origin main

```

> Bật tính năng **GitHub Pages** tại: `Settings -> Pages -> Branch: main -> Save`.

---

## 📁 Cấu trúc dự án

```
GreenProject/
├── 📄 index.html        # Single-file chứa toàn bộ HTML, CSS, JS Logic, Audio & Graphics
├── 📄 README.md         # Tài liệu hướng dẫn chi tiết dự án
├── 📜 LICENSE           # Giấy phép mã nguồn mở GNU GPL v3.0
└── 🙈 .gitignore        # Cấu hình bỏ qua các tệp không cần thiết

```

---

## 🎓 Giá trị giáo dục

Trò chơi lồng ghép khéo léo các bài học thực tiễn về ý thức bảo vệ môi trường dành cho học sinh:

| Ý niệm giáo dục | Hành động tương ứng trong game |
| --- | --- |
| ♻️ **Ý thức phân loại rác** | Thu gom rác thải đúng nơi quy định để phục hồi thể lực |
| ⚡ **Tiết kiệm năng lượng** | Tắt quạt và đèn khi rời phòng học để giảm tiêu thụ điện |
| 🌿 **Trách nhiệm môi trường** | Giữ gìn vệ sinh chung giúp bầu trời ngày hôm sau trong xanh hơn |
| 💧 **Vệ sinh trường lớp** | Khơi thông cống rãnh, tránh đọng nước phát sinh mầm bệnh |
| 🧘 **Kỷ luật & Tập trung** | Mân mê chú ý bài giảng, rèn luyện tính tự giác trong giờ học |

> [!NOTE]
> **Thông điệp cốt lõi:** *"Mỗi hành động nhỏ của cá nhân hôm nay đều trực tiếp quyết định chất lượng môi trường sống của tập thể vào ngày mai."*

---

## 🤝 Đóng góp phát triển

Mọi ý tưởng đóng góp và Pull Request cải tiến dự án đều được trân trọng!

```bash
# 1. Fork Repository về tài khoản của bạn
# 2. Clone project về máy local
git clone [https://github.com/YOUR_USERNAME/GreenProject.git](https://github.com/YOUR_USERNAME/GreenProject.git)

# 3. Tạo Branch cho tính năng mới
git checkout -b feature/AmazingFeature

# 4. Commit các thay đổi
git commit -m "feat: Add some AmazingFeature"

# 5. Push lên GitHub Branch
git push origin feature/AmazingFeature

# 6. Mở một Pull Request trên GitHub

```

### 💡 Hướng phát triển tiếp theo

* [ ] 🏫 Mở rộng thêm các phòng học (10A1, 11A2, 12A3) và khu vực Căn tin.
* [ ] 🌱 Thêm minigame chăm sóc vườn cây thanh niên.
* [ ] 🏆 Bảng xếp hạng điểm số sinh tồn Online.
* [ ] 🎵 Nhạc nền sống động thay đổi theo thời tiết và thời gian trong ngày.

---

## 👨‍💻 Tác giả

### 🍪 Cookie

**Thành viên CLB Tin Học — Trường THPT Bình Chánh**

*Dự án hoàn thiện trong khuôn khổ **Hội thi CLB Tin Học 2026–2027***

*Chủ đề: **"Lập Trình Vì Ngôi Trường Xanh"***

---

## 📜 Giấy phép

### GNU General Public License v3.0

```text
Code for Green School: Eco Survival
Copyright (C) 2026  Cookie & CLB Tin Học THPT Bình Chánh

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

```

* 📖 Xem toàn văn giấy phép tại: [https://www.gnu.org/licenses/gpl-3.0.txt](https://www.gnu.org/licenses/gpl-3.0.txt)

---

## 🙏 Lời cảm ơn

Xin chân thành cảm ơn sự hỗ trợ và đồng hành từ:

| Đối tác / Tổ chức | Nội dung hỗ trợ |
| --- | --- |
| 🌱 **Ban Giám Hiệu THPT Bình Chánh** | Tậo điều kiện và là nguồn cảm hứng phát triển dự án |
| 💚 **Thầy Cô CLB Tin Học** | Đóng góp ý kiến chuyên môn và định hướng kỹ thuật |
| 👥 **Học sinh THPT Bình Chánh** | Tham gia thử nghiệm (Playtest) và góp ý trải nghiệm |
| 🔥 **Google Firebase & GitHub** | Cung cấp nền tảng hạ tầng Backend & Hosting miễn phí |

---

### 🌱 HÃY CHƠI, HỌC VÀ LAN TỎA TINH THẦN SỐNG XANH! 🌱

**CLB TIN HỌC THPT BÌNH CHÁNH — NĂM HỌC 2026–2027**

*Made with 💚 in Vietnam*
