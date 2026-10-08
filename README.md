```markdown
# 🌱 Code for Green School: Eco Survival

> **"CÙNG THPT Bình Chánh SỐNG XANH"** — Trò chơi 2D pixel art giáo dục về bảo vệ môi trường, được phát triển bởi **CLB Tin Học - Trường THPT Bình Chánh** cho Hội thi năm học 2026–2027.

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Made with JavaScript](https://img.shields.io/badge/Made%20with-JavaScript-yellow.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Firebase](https://img.shields.io/badge/Backend-Firebase-orange.svg)](https://firebase.google.com/)
[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-green.svg)](https://pages.github.com/)
[![GitHub stars](https://img.shields.io/github/stars/hihiquan2010/GreenProject?style=social)](https://github.com/hihiquan2010/GreenProject/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/hihiquan2010/GreenProject?style=social)](https://github.com/hihiquan2010/GreenProject/network)
[![GitHub issues](https://img.shields.io/github/issues/hihiquan2010/GreenProject)](https://github.com/hihiquan2010/GreenProject/issues)

---

## 🎮 Chơi ngay

👉 **[BẤM VÀO ĐÂY ĐỂ CHƠI GAME](https://hihiquan2010.github.io/GreenProject/)**

Hoặc copy link này vào trình duyệt:
```
https://hihiquan2010.github.io/GreenProject/
```

---

## 📖 Giới thiệu

**Code for Green School: Eco Survival** là một trò chơi **web 2D top-down pixel art** mô phỏng một ngày học tập tại **Trường THPT Bình Chánh**. Người chơi vào vai một học sinh phải:

- 🎒 **Sinh tồn** qua nhiều ngày học tập khắc nghiệt
- ☀️ **Đối phó** với 3 loại thời tiết: **Oi bức**, **Ô nhiễm**, **Mưa phùn**
- ♻️ **Dọn rác** để bảo vệ môi trường và **hồi máu**
- 🪑 **Ngồi ghế** đúng giờ học, **tắt điện/quạt** đúng lúc
- 🔇 **Tập trung** trong lớp bằng minigame giữ im lặng
- 👥 **Chơi nhóm online** cùng bạn bè qua Firebase

Game được lấy cảm hứng từ **bản đồ trường THPT Bình Chánh thật** (dãy nhà 2 tầng mái đỏ, sân trước rộng, cột cờ Tổ quốc, cây xanh 2 bên).

---

## 🎮 Gameplay

### ⏰ Thời khóa biểu 1 ngày

```
GIỜ RA CHƠI SÁNG → TIẾT 1 → TIẾT 2 → RA CHƠI → TIẾT 3 → TIẾT 4
→ RA CHƠI → TIẾT 5 → TIẾT 6 → RA CHƠI → TIẾT 7 → KẾT THÚC NGÀY
```

- Mỗi tiết: **60 giây**
- Mỗi giờ ra chơi: **30 giây**
- Chuyển tiết: **3 giây**

### 🌤️ Ba loại thời tiết

| Thời tiết | Hiệu ứng | Cách đối phó |
|---|---|---|
| ☀️ **OI BỨC** | Nhiệt độ cơ thể tăng khi ở lớp không quạt | Tắt điện khi ra chơi, bật quạt khi vào lớp |
| ☣️ **Ô NHIỄM** | Rác vương vãi bốc mùi hôi | Nhặt rác bỏ vào Thùng Xanh |
| 🌧️ **MƯA PHÙN** | Vũng nước gây trượt té, cống tắc | Tắt quạt, tránh vũng, thông cống |

**1 ngày = 1 thời tiết duy nhất**, được random từ ngày 4 trở đi.

### 🌡️ Cơ chế nhiệt độ cơ thể

- Nhiệt độ chuẩn: **50°**
- **Trời nóng**: quạt chỉ làm mát **về 50°** (không thể xuống dưới)
- **Trời mưa**: quạt làm mát **xuống dưới 50°** → nguy cơ **hạ thân nhiệt**
- Nhiệt độ > 85° hoặc < 15° → **mất HP liên tục**

### ♻️ Cơ chế nhặt rác hồi máu

| Số rác | HP hồi (nhân vật thường) | HP hồi (Bảo Ngọc - regen) |
|---|---|---|
| 1 rác | +4 HP | +6 HP |
| 5 rác (đầy túi) | +25 HP (bonus +5) | +38 HP |
| **Dọn càng nhiều** | → **giảm tỉ lệ ô nhiễm ngày mai** (tối đa -60%) | |

### 🔇 Minigame "Giữ im lặng"

- Trong mỗi tiết, cứ **10 giây có 80% cơ hội** xuất hiện
- Nhấn **SPACE/CLICK/TAP** khi kim trượt vào **vùng xanh**
- Trượt **3 lần** = mất 10 HP + cô giáo khiển trách
- Nhân vật **Gia Uy** có vùng xanh rộng hơn (40%)

### 🎭 4 nhân vật với kỹ năng riêng

| Nhân vật | Kỹ năng | Đặc điểm tạo hình |
|---|---|---|
| **Gia Hưng** | 🏃 Tốc độ +20% | Cao, cân đối, tóc ngắn |
| **Bảo Ngọc** | ♻️ Hồi +8 HP mỗi ngày | Nữ, thấp, mảnh mai, **tóc dài** |
| **Minh Thái** | 🛡️ Chống chịu thời tiết tốt | **Cao nhất, to con** |
| **Gia Uy** | 💻 Quạt tay x2 + Minigame dễ | Cao, **đeo kính** |

---

## 👥 Chơi nhóm Online

Game hỗ trợ **multiplayer realtime** qua **Firebase Realtime Database** — không cần server riêng.

### Cách chơi nhóm

1. **Chủ phòng**: Bấm **👥 Online** → **🎮 Tạo phòng** → Nhận **mã 6 ký tự**
2. **Chia sẻ** mã phòng cho bạn bè qua Zalo/Messenger
3. **Bạn bè**: Bấm **👥 Online** → **🔗 Vào phòng** → Nhập mã → **Tham gia**
4. **Chủ phòng**: Bấm **▶ Bắt đầu** → cả nhóm vào game cùng nhau

### Tính năng đồng bộ

- ✅ Vị trí, hướng nhìn, animation của mọi người chơi
- ✅ Trạng thái quạt tay, ngồi ghế, cầm rác
- ✅ Hành động: tắt đèn, bật quạt, mở cửa, nhặt rác, sửa điện
- ✅ Nhiệt độ cơ thể của đồng đội
- ✅ Thời tiết + tiến trình thời khóa biểu

---

## 🎨 Đồ họa Pixel Art

### Bản đồ

Bản đồ được thiết kế dựa trên **ảnh thật của trường THPT Bình Chánh**:

- 🏫 **Dãy nhà 2 tầng mái ngói đỏ** với 12 cửa sổ và hàng hiên 12 cột
- 🚩 **Cột cờ Tổ quốc** ở giữa sân với **cờ đỏ sao vàng** bay theo gió
- 🌳 **6 cây xanh** 2 bên sân trường
- 🌸 **2 bồn hoa** trước sân
- 🛡️ **Bốt bảo vệ** góc dưới trái
- ♻️ **Thùng rác xanh** góc dưới phải
- 🚰 **2 cống thoát nước** trên sân

### Nhân vật pixel

Mỗi nhân vật có **tạo hình riêng biệt**:

- **Chiều cao** (`height`): 0.92 → 1.28
- **Vóc dáng** (`width`): 0.92 → 1.22
- **Tóc dài** (`hasLongHair`): chỉ Bảo Ngọc
- **Kính** (`hasGlasses`): chỉ Gia Uy
- **Màu sắc**: da, tóc, áo, quần riêng theo nhân vật

---

## 🚀 Cài đặt và chạy

### Yêu cầu

- Trình duyệt hiện đại hỗ trợ **ES6+**, **Canvas 2D**
- **Kết nối Internet** (để load Firebase SDK)

### Bước 1: Clone repository

```bash
git clone https://github.com/hihiquan2010/GreenProject.git
cd GreenProject
```

### Bước 2: Tạo Firebase Project

1. Truy cập [Firebase Console](https://console.firebase.google.com/)
2. **Add project** → Đặt tên (VD: `cfg-eco-thptbc`) → Create
3. Menu **Build** → **Realtime Database** → **Create Database**
4. Chọn location **Singapore** → Start in **Test mode** → Enable
5. Vào tab **Rules** → Paste:
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
6. **Publish**

### Bước 3: Lấy Firebase Config

1. **Project Settings** (icon ⚙️) → **General**
2. Kéo xuống **Your apps** → **Web** (icon `</>`)
3. Đặt nickname → **Register app**
4. Copy đoạn `firebaseConfig`:
   ```js
   const firebaseConfig = {
     apiKey: "AIzaSy...",
     authDomain: "your-project.firebaseapp.com",
     databaseURL: "https://your-project-default-rtdb.asia-southeast1.firebasedatabase.app",
     projectId: "your-project",
     storageBucket: "your-project.appspot.com",
     messagingSenderId: "123456789",
     appId: "1:123456789:web:abcdef"
   };
   ```

### Bước 4: Thay vào file `index.html`

Tìm dòng:
```js
// ⚠️ THAY CONFIG FIREBASE CỦA BẠN VÀO ĐÂY
const firebaseConfig = { ... };
```

Thay bằng config của bạn.

### Bước 5: Deploy lên GitHub Pages

```bash
git add index.html
git commit -m "Setup Firebase config"
git push origin main
```

Sau đó vào **Settings → Pages → Source: main → Save**.

Truy cập: `https://hihiquan2010.github.io/GreenProject/`

---

## 🎯 Điều khiển

### Trên máy tính

| Phím | Chức năng |
|---|---|
| `WASD` / `↑↓←→` | Di chuyển |
| `E` | Tương tác (nhặt rác, công tắc, mở cửa) |
| `F` / `Space` | Quạt tay / Ngồi ghế |
| `SPACE` | Nhấn trong minigame |

### Trên điện thoại

- **Joystick ảo** (góc trái) — Di chuyển
- **Nút E** (góc phải) — Tương tác
- **Nút F** (góc phải) — Quạt tay
- **Nút 🪑** (góc phải) — Ngồi/đứng dậy

---

## 🛠️ Công nghệ sử dụng

| Thành phần | Công nghệ |
|---|---|
| **Frontend** | HTML5, CSS3, Vanilla JavaScript |
| **Đồ họa** | Canvas 2D API |
| **Âm thanh** | Web Audio API (procedural synthesis) |
| **Multiplayer** | Firebase Realtime Database 10.12.0 |
| **Fonts** | Press Start 2P, Lexend |
| **Hosting** | GitHub Pages |

Không sử dụng framework nặng — game chạy mượt ngay cả trên điện thoại tầm trung.

---

## 📁 Cấu trúc dự án

```
GreenProject/
├── index.html          # Toàn bộ game (single-file)
├── README.md           # File này
├── LICENSE             # GNU GPL v3.0
└── assets/             # (không cần — mọi thứ inline)
```

Game được thiết kế theo kiểu **single-file** để dễ deploy và chia sẻ.

---

## 🎓 Mục đích giáo dục

Game hướng đến việc **giáo dục ý thức bảo vệ môi trường** cho học sinh:

- ♻️ **Phân loại rác** và tái chế
- ⚡ **Tiết kiệm điện** — tắt thiết bị khi ra khỏi lớp
- 🌿 **Giảm ô nhiễm** — dọn rác để ngày mai trời trong xanh hơn
- 💧 **Giữ vệ sinh** — thông cống, tránh vũng nước
- 🧘 **Tập trung học tập** — minigame giữ im lặng

Mỗi hành động nhỏ đều có **tác động đến ngày mai** — đây là bài học về **trách nhiệm với môi trường**.

---

## 🤝 Đóng góp

Mọi đóng góp đều được hoan nghênh! Vui lòng:

1. **Fork** repository
2. Tạo branch mới: `git checkout -b feature/tinh-nang-moi`
3. Commit: `git commit -m "Thêm tính năng X"`
4. Push: `git push origin feature/tinh-nang-moi`
5. Mở **Pull Request**

### Ý tưởng phát triển

- [ ] Thêm nhiều lớp học hơn (10A1, 11A2, 12A3)
- [ ] Minigame phụ: trồng cây, tưới hoa
- [ ] Boss cuối tuần: "Ngày hội môi trường"
- [ ] Hệ thống thành tích (achievements)
- [ ] Chế độ co-op nhiều đội
- [ ] Bảng xếp hạng online

---

## 👨‍💻 Tác giả

**Cookie** 🍪  
Thành viên **CLB Tin Học — Trường THPT Bình Chánh**

- 📧 Email: [uyp079658@gmail.com](mailto:uyp079658@gmail.com)
- 🐙 GitHub: [@hihiquan2010](https://github.com/hihiquan2010)

> Dự án được thực hiện trong khuôn khổ **Hội thi CLB Tin Học 2026–2027** với chủ đề **"Lập Trình Vì Ngôi Trường Xanh"**.

---

## 📜 Giấy phép — GNU General Public License v3.0

```
Code for Green School: Eco Survival
Copyright (C) 2026  Cookie & CLB Tin Học THPT Bình Chánh

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```

### Quyền lợi

- ✅ **Sử dụng** cho mục đích cá nhân, giáo dục, thương mại
- ✅ **Nghiên cứu** và **sửa đổi** mã nguồn
- ✅ **Phân phối** bản sao cho người khác

### Điều kiện

- 📢 **Ghi nguồn** tác giả gốc (Cookie + CLB Tin Học THPT Bình Chánh)
- 📄 **Giữ nguyên** giấy phép GPL v3.0 trong mọi bản phân phối
- 🔓 **Mở mã nguồn** nếu bạn phát hành bản sửa đổi
- ⚠️ **Không bảo hành** — tác giả không chịu trách nhiệm nếu có lỗi

### Liên kết

- 🌐 Website: [https://www.gnu.org/licenses/gpl-3.0](https://www.gnu.org/licenses/gpl-3.0)
- 📖 Toàn văn: [https://www.gnu.org/licenses/gpl-3.0.txt](https://www.gnu.org/licenses/gpl-3.0.txt)

Để có toàn văn giấy phép GPL v3.0, hãy tạo file `LICENSE` riêng bằng cách copy nội dung từ [đây](https://www.gnu.org/licenses/gpl-3.0.txt).

---

## 🙏 Cảm ơn

- 🌱 **Ban giám hiệu THPT Bình Chánh** — đã tạo cảm hứng từ ngôi trường thật
- 💚 **Thầy cô CLB Tin Học** — hướng dẫn và hỗ trợ
- 👥 **Các bạn học sinh** — người chơi và tester nhiệt tình
- 🎨 **Cộng đồng pixel art Việt Nam** — nguồn cảm hứng đồ họa
- 🔥 **Firebase** — backend miễn phí cho multiplayer
- 📚 **Cộng đồng mã nguồn mở** — đã chia sẻ kiến thức vô giá

---

<div align="center">

**🌱 HÃY CHƠI, HỌC VÀ LAN TỎA TINH THẦN SỐNG XANH! 🌱**

*"Lập Trình Vì Ngôi Trường Xanh"* — CLB Tin Học THPT Bình Chánh 2026–2027

⭐ Nếu bạn thấy dự án hữu ích, hãy **star** repository này! ⭐

</div>
```
