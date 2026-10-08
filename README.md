```markdown
<div align="center">

# 🌱 Code for Green School: Eco Survival

### *"CÙNG THPT BÌNH CHÁNH SỐNG XANH"*

**Trò chơi 2D pixel art giáo dục về bảo vệ môi trường**

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Made with JavaScript](https://img.shields.io/badge/Made%20with-JavaScript-yellow.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Firebase](https://img.shields.io/badge/Backend-Firebase-orange.svg)](https://firebase.google.com/)
[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-green.svg)](https://pages.github.com/)
[![GitHub stars](https://img.shields.io/github/stars/hihiquan2010/GreenProject?style=social)](https://github.com/hihiquan2010/GreenProject/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/hihiquan2010/GreenProject?style=social)](https://github.com/hihiquan2010/GreenProject/network)
[![GitHub issues](https://img.shields.io/github/issues/hihiquan2010/GreenProject)](https://github.com/hihiquan2010/GreenProject/issues)

### 🎮 [**BẤM VÀO ĐÂY ĐỂ CHƠI NGAY**](<a>https://hihiquan2010.github.io/GreenProject/</a>)

*Hoặc copy link: `https://hihiquan2010.github.io/GreenProject/`*

---

*Dự án tham gia **Hội thi CLB Tin Học 2026–2027** với chủ đề **"Lập Trình Vì Ngôi Trường Xanh"***

</div>

---

## 📑 Mục lục

- [Giới thiệu](#-giới-thiệu)
- [Gameplay](#-gameplay)
- [Chơi nhóm Online](#-chơi-nhóm-online)
- [Đồ họa Pixel Art](#-đồ-họa-pixel-art)
- [Cài đặt và chạy](#-cài-đặt-và-chạy)
- [Điều khiển](#-điều-khiển)
- [Công nghệ sử dụng](#-công-nghệ-sử-dụng)
- [Cấu trúc dự án](#-cấu-trúc-dự-án)
- [Mục đích giáo dục](#-mục-đích-giáo-dục)
- [Đóng góp](#-đóng-góp)
- [Tác giả](#-tác-giả)
- [Giấy phép](#-giấy-phép)
- [Lời cảm ơn](#-lời-cảm-ơn)

---

## 📖 Giới thiệu

**Code for Green School: Eco Survival** là một trò chơi **web 2D top-down pixel art** mô phỏng một ngày học tập tại **Trường THPT Bình Chánh**. Người chơi hóa thân thành một học sinh, phải vượt qua những ngày học tập với thời tiết khắc nghiệt, bảo vệ môi trường và sinh tồn qua từng tiết học.

### 🎯 Nhiệm vụ chính của người chơi

| Nhiệm vụ | Mô tả |
|---|---|
| 🎒 **Sinh tồn** | Sống sót qua nhiều ngày, giữ HP > 0 |
| ☀️ **Đối phó thời tiết** | Thích nghi với Oi bức, Ô nhiễm, Mưa phùn |
| ♻️ **Dọn rác** | Bảo vệ môi trường, hồi máu, giảm ô nhiễm |
| 🪑 **Ngồi ghế** | Tuân thủ giờ học, không bị khiển trách |
| ⚡ **Tiết kiệm điện** | Tắt thiết bị khi ra chơi |
| 🔇 **Tập trung** | Vượt minigame "Giữ im lặng" trong tiết |
| 👥 **Chơi nhóm** | Cùng bạn bè sinh tồn qua Firebase |

### 💡 Nguồn cảm hứng

Bản đồ game được thiết kế dựa trên **ảnh chụp thực tế của trường THPT Bình Chánh**: dãy nhà 2 tầng mái ngói đỏ, sân trước rộng lớn, cột cờ Tổ quốc, hàng cây xanh hai bên.

---

## 🎮 Gameplay

### ⏰ Thời khóa biểu một ngày

```
┌──────────────────┐   ┌────────┐   ┌────────┐   ┌──────────┐
│ RA CHƠI SÁNG 30s │ → │ TIẾT 1 │ → │ TIẾT 2 │ → │ RA CHƠI  │
└──────────────────┘   │  60s   │   │  60s   │   │   30s    │
                       └────────┘   └────────┘   └──────────┘
                                                        ↓
┌──────────┐   ┌────────┐   ┌────────┐   ┌────────┐   ┌────────┐
│ TIẾT 7   │ ← │ TIẾT 6 │ ← │ TIẾT 5 │ ← │ RA CHƠI │ ← │ TIẾT 3 │
│  60s     │   │  60s   │   │  60s   │   │   30s  │   │  TIẾT 4│
└──────────┘   └────────┘   └────────┘   └────────┘   └────────┘
```

- **Mỗi tiết**: 60 giây
- **Mỗi giờ ra chơi**: 30 giây
- **Chuyển tiết**: 3 giây (có tiếng chuông 🔔)

### 🌤️ Ba loại thời tiết

Mỗi ngày chỉ có **DUY NHẤT MỘT** loại thời tiết. Từ **ngày 4 trở đi** mới random (không lặp lại ngày trước).

| Loại | Biểu tượng | Hiệu ứng | Cách đối phó |
|---|---|---|---|
| **OI BỨC** | ☀️ | Nhiệt độ tăng khi ở lớp không có quạt | Tắt điện khi ra chơi, quạt khi vào lớp |
| **Ô NHIỄM** | ☣️ | Rác bốc mùi hôi, không khí ô nhiễm | Nhặt rác bỏ vào Thùng Xanh |
| **MƯA PHÙN** | 🌧️ | Vũng nước trơn trượt, cống tắc | Tắt quạt, tránh vũng, thông cống |

### 🌡️ Cơ chế nhiệt độ cơ thể

Thanh nhiệt độ hiển thị **0° → 100°**, mức chuẩn là **50°**.

| Trạng thái | Điều kiện | Tác động |
|---|---|---|
| 🔥 **Sốc nhiệt** | Nhiệt độ > 85° | Mất **4 HP/giây** |
| ♨️ **Nóng** | Nhiệt độ > 70° | Mất **1 HP/giây** |
| ✅ **Bình thường** | 30° ≤ Nhiệt độ ≤ 70° | Không ảnh hưởng |
| 🧊 **Mát** | Nhiệt độ < 30° | Mất **1 HP/giây** |
| ❄️ **Hạ thân nhiệt** | Nhiệt độ < 15° | Mất **3 HP/giây** |

**Quy tắc vàng**:
- ☀️ **Trời nóng**: quạt chỉ làm mát **VỀ 50°** — không thể xuống dưới
- 🌧️ **Trời mưa**: quạt làm mát **XUỐNG DƯỚI 50°** — nguy cơ hạ thân nhiệt!

### ♻️ Cơ chế nhặt rác hồi máu

Bỏ rác vào **Thùng Rác Xanh** (góc dưới phải sân) sẽ **hồi HP**:

| Số rác | HP hồi thường | HP hồi (Bảo Ngọc ×1.5) |
|---|---|---|
| 1 rác | +4 HP | +6 HP |
| 3 rác | +12 HP | +18 HP |
| **5 rác (đầy túi)** | **+25 HP** (bonus +5) | **+38 HP** |

### 🌿 Cơ chế giảm ô nhiễm

Càng dọn nhiều rác → ngày mai càng **ít khả năng có thời tiết Ô nhiễm**:

| Rác dọn hôm qua | Giảm ô nhiễm | Xác suất Ô nhiễm ngày mai |
|---|---|---|
| 0 rác | 0% | 35% |
| 5 rác | 25% | 26% |
| 10 rác | 50% | 17% |
| **12+ rác** | **60% (tối đa)** | **14% (thấp nhất)** |

### 🔇 Minigame "Giữ im lặng"

Trong mỗi tiết học, cô giáo nhắc nhở học sinh tập trung:

- ⏱️ Cứ **10 giây**, có **80% cơ hội** minigame xuất hiện
- 🎯 Nhấn **SPACE / CLICK / TAP** khi kim trượt vào **vùng xanh**
- ✅ Vùng xanh rộng: nhân vật **Gia Uy** (40%) — dễ hơn
- ❌ Trượt 3 lần: mất **10 HP** + cô giáo khiển trách

### 🎭 Bốn nhân vật với kỹ năng riêng

| Nhân vật | Vai trò | Kỹ năng | Tạo hình |
|---|---|---|---|
| **Gia Hưng** | 🏃 Năng động | Tốc độ +20% | Cao, cân đối, tóc ngắn |
| **Bảo Ngọc** | ♻️ Lớp xanh | Hồi +8 HP/ngày | Nữ, thấp, mảnh mai, **tóc dài** |
| **Minh Thái** | 🛡️ Cờ đỏ | Chống chịu tốt | **Cao nhất, to con** |
| **Gia Uy** | 💻 CLB Tin Học | Quạt x2, minigame dễ | Cao, **đeo kính** |

---

## 👥 Chơi nhóm Online

Game hỗ trợ **multiplayer realtime** qua **Firebase Realtime Database** — không cần tự dựng server, chơi được với bạn bè ở bất kỳ đâu.

### 📋 Các bước chơi nhóm

```
┌─────────────────┐                              ┌─────────────────┐
│   CHỦ PHÒNG     │                              │    BẠN BÈ       │
├─────────────────┤                              ├─────────────────┤
│ 1. 👥 Online    │                              │ 1. 👥 Online    │
│ 2. 🎮 Tạo phòng │ ──── Chia sẻ mã ────→        │ 2. 🔗 Vào phòng │
│ 3. Nhận mã 6 KT │      (Zalo/Mess)              │ 3. Nhập mã      │
│ 4. ▶ Bắt đầu    │ ←───── Tham gia ─────         │ 4. Chờ bắt đầu  │
└─────────────────┘                              └─────────────────┘
```

### 🔄 Tính năng đồng bộ

| Đồng bộ | Chi tiết |
|---|---|
| ✅ **Vị trí** | Tọa độ x, y của mọi người chơi |
| ✅ **Hướng nhìn** | Facing: trái/phải/lên/xuống |
| ✅ **Animation** | Frame đi bộ, animation quạt tay |
| ✅ **Trạng thái** | Ngồi ghế, cầm rác, quạt tay |
| ✅ **Hành động** | Tắt đèn, bật quạt, mở cửa, nhặt rác |
| ✅ **Nhiệt độ** | Thanh nhiệt của đồng đội |
| ✅ **Thời gian** | Tiến trình tiết học/ra chơi |

---

## 🎨 Đồ họa Pixel Art

### 🏫 Bản đồ trường học

Bản đồ được **tái hiện từ ảnh chụp thật** của trường THPT Bình Chánh:

| Vị trí | Chi tiết |
|---|---|
| 🏫 **Dãy nhà chính** | 2 tầng, mái ngói đỏ, 12 cửa sổ, hàng hiên 12 cột |
| 🚩 **Cột cờ** | Ở giữa sân, cờ đỏ sao vàng bay theo gió |
| 🌳 **Cây xanh** | 6 cây 2 bên sân trường |
| 🌸 **Bồn hoa** | 2 bồn hoa trước sân |
| 🛡️ **Bốt bảo vệ** | Góc dưới trái |
| ♻️ **Thùng rác xanh** | Góc dưới phải |
| 🚰 **Cống thoát nước** | 2 cống trên sân |
| 🏫 **3 lớp học** | 10A3, 11A3, 12A3 với bàn ghế |

### 👤 Nhân vật pixel

Mỗi nhân vật có **bộ thông số tạo hình riêng**:

| Thuộc tính | Giá trị | Ý nghĩa |
|---|---|---|
| `height` | 0.92 → 1.28 | Chiều cao (thấp → cao) |
| `width` | 0.92 → 1.22 | Vóc dáng (mảnh → to) |
| `hasLongHair` | `true/false` | Có tóc dài không (chỉ Bảo Ngọc) |
| `hasGlasses` | `true/false` | Có đeo kính không (chỉ Gia Uy) |
| `skin`, `hair`, `shirt`, `pants` | Hex colors | Màu da, tóc, áo, quần |

---

## 🚀 Cài đặt và chạy

### 📋 Yêu cầu hệ thống

- ✅ Trình duyệt hiện đại hỗ trợ **ES6+**, **Canvas 2D**
- ✅ **Kết nối Internet** (để load Firebase SDK và Google Fonts)

### 🔧 Các bước cài đặt

#### Bước 1 — Clone repository

```bash
git clone https://github.com/hihiquan2010/GreenProject.git
cd GreenProject
```

#### Bước 2 — Tạo Firebase Project

1. Truy cập [Firebase Console](https://console.firebase.google.com/)
2. Bấm **Add project** → Đặt tên (VD: `cfg-eco-thptbc`) → **Create**
3. Menu trái: **Build** → **Realtime Database** → **Create Database**
4. Chọn location **Singapore** → **Start in Test mode** → **Enable**
5. Vào tab **Rules**, paste đoạn JSON sau rồi **Publish**:

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

#### Bước 3 — Lấy Firebase Config

1. **Project Settings** (icon ⚙️) → tab **General**
2. Kéo xuống **Your apps** → chọn **Web** (icon `</>`)
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

#### Bước 4 — Thay config vào `index.html`

Mở file `index.html`, tìm dòng có chú thích:

```js
// ⚠️ THAY CONFIG FIREBASE CỦA BẠN VÀO ĐÂY
const firebaseConfig = { ... };
```

Thay bằng config vừa copy ở Bước 3.

#### Bước 5 — Deploy lên GitHub Pages

```bash
git add index.html
git commit -m "Setup Firebase config"
git push origin main
```

Vào **Settings → Pages → Source: `main` → Save**.

Sau 1-2 phút, truy cập: `https://hihiquan2010.github.io/GreenProject/`

---

## 🎯 Điều khiển

### 💻 Trên máy tính

| Phím | Chức năng |
|---|---|
| `WASD` hoặc `↑ ↓ ← →` | Di chuyển nhân vật |
| `E` | Tương tác (nhặt rác, công tắc, mở cửa, nói chuyện) |
| `F` hoặc `Space` | Quạt tay / Ngồi ghế |
| `SPACE` | Nhấn trong minigame "Giữ im lặng" |

### 📱 Trên điện thoại

Game hỗ trợ **cảm ứng đa điểm** với giao diện được thiết kế riêng:

| Nút | Vị trí | Chức năng |
|---|---|---|
| 🕹️ **Joystick ảo** | Góc trái | Di chuyển 360° |
| 🅴 **Nút E** | Góc phải | Tương tác |
| 🅵 **Nút F** | Góc phải | Quạt tay |
| 🪑 **Nút ghế** | Góc phải | Ngồi / Đứng dậy |
| ⚙️ **Nút menu** | Góc phải | Mở hướng dẫn |

---

## 🛠️ Công nghệ sử dụng

| Thành phần | Công nghệ | Ghi chú |
|---|---|---|
| **Frontend** | HTML5, CSS3, Vanilla JS | Không dùng framework |
| **Đồ họa** | Canvas 2D API | `image-rendering: pixelated` |
| **Âm thanh** | Web Audio API | Procedural synthesis (không cần file MP3) |
| **Multiplayer** | Firebase Realtime DB 10.12.0 | Sync realtime, free tier |
| **Fonts** | Press Start 2P, Lexend | Google Fonts |
| **Hosting** | GitHub Pages | Miễn phí, HTTPS sẵn |

**Ưu điểm thiết kế**: Game chạy **mượt trên điện thoại tầm trung** vì không dùng framework nặng, mọi asset đều được **vẽ bằng Canvas procedural**.

---

## 📁 Cấu trúc dự án

```
GreenProject/
│
├── index.html          # ⭐ Toàn bộ game (single-file)
├── README.md           # 📄 File này
├── LICENSE             # 📜 GNU GPL v3.0
└── .gitignore          # (tuỳ chọn)
```

Game được thiết kế theo kiểu **single-file** để dễ deploy, chia sẻ và bảo trì. Mọi thứ — từ logic, đồ họa, âm thanh — đều nằm trong **một file `index.html` duy nhất**.

---

## 🎓 Mục đích giáo dục

Đây là một dự án game có **giá trị giáo dục cao**, hướng đến việc nâng cao ý thức bảo vệ môi trường cho học sinh THPT:

| Bài học | Thể hiện trong game |
|---|---|
| ♻️ **Phân loại rác** | Nhặt rác và bỏ đúng vào Thùng Xanh |
| ⚡ **Tiết kiệm điện** | Tắt đèn, quạt khi ra khỏi lớp |
| 🌿 **Giảm ô nhiễm** | Dọn rác để ngày mai bầu trời trong xanh |
| 💧 **Giữ vệ sinh** | Thông cống, tránh vũng nước |
| 🧘 **Tập trung** | Minigame giữ im lặng trong giờ học |
| 👥 **Trách nhiệm tập thể** | Chơi nhóm, cùng sinh tồn |

> **Triết lý thiết kế**: Mỗi hành động nhỏ đều có **tác động đến ngày mai** — đây là bài học về **trách nhiệm cá nhân với môi trường tập thể**.

---

## 🤝 Đóng góp

Mọi đóng góp — dù nhỏ — đều được hoan nghênh!

### Quy trình đóng góp

```bash
# 1. Fork repository trên GitHub
# 2. Clone bản fork của bạn
git clone https://github.com/YOUR_USERNAME/GreenProject.git
cd GreenProject

# 3. Tạo branch mới
git checkout -b feature/tinh-nang-moi

# 4. Commit thay đổi
git add .
git commit -m "feat: thêm tính năng X"

# 5. Push lên fork của bạn
git push origin feature/tinh-nang-moi

# 6. Mở Pull Request trên GitHub
```

### 💡 Ý tưởng phát triển

- [ ] 🏫 Thêm nhiều lớp học hơn (10A1, 11A2, 12A3)
- [ ] 🌱 Minigame phụ: trồng cây, tưới hoa
- [ ] 🎉 Boss cuối tuần: "Ngày hội môi trường"
- [ ] 🏆 Hệ thống thành tích (achievements)
- [ ] 👥 Chế độ co-op nhiều đội thi đua
- [ ] 📊 Bảng xếp hạng online
- [ ] 🌍 Thêm bản đồ các trường khác
- [ ] 🎵 Nhạc nền theo ngày/đêm

---

## 👨‍💻 Tác giả

<div align="center">

### 🍪 Cookie

**Thành viên CLB Tin Học — Trường THPT Bình Chánh**

[![Email](https://img.shields.io/badge/Email-uyp079658@gmail.com-red?style=flat&logo=gmail)](mailto:uyp079658@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-hihiquan2010-black?style=flat&logo=github)](https://github.com/hihiquan2010)

</div>

> Dự án được thực hiện trong khuôn khổ **Hội thi CLB Tin Học 2026–2027**  
> Chủ đề: ***"Lập Trình Vì Ngôi Trường Xanh"***

---

## 📜 Giấy phép

<div align="center">

### GNU General Public License v3.0

[![GPL v3](https://www.gnu.org/graphics/gplv3-127x51.png)](https://www.gnu.org/licenses/gpl-3.0)

</div>

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

### ✅ Quyền lợi

| Quyền | Mô tả |
|---|---|
| ✅ **Sử dụng** | Cho mục đích cá nhân, giáo dục, thương mại |
| ✅ **Nghiên cứu** | Đọc, tìm hiểu mã nguồn |
| ✅ **Sửa đổi** | Chỉnh sửa, tùy biến theo nhu cầu |
| ✅ **Phân phối** | Chia sẻ bản gốc hoặc bản sửa đổi |

### ⚠️ Điều kiện bắt buộc

| Điều kiện | Mô tả |
|---|---|
| 📢 **Ghi nguồn** | Nêu rõ tác giả gốc (Cookie + CLB Tin Học THPT Bình Chánh) |
| 📄 **Giữ giấy phép** | Không được đổi giấy phép GPL v3.0 khi phân phối lại |
| 🔓 **Mở mã nguồn** | Nếu phát hành bản sửa đổi, phải công khai source code |
| ⚠️ **Không bảo hành** | Tác giả không chịu trách nhiệm nếu có lỗi |

### 🔗 Liên kết

- 🌐 **Website**: [https://www.gnu.org/licenses/gpl-3.0](https://www.gnu.org/licenses/gpl-3.0)
- 📖 **Toàn văn**: [https://www.gnu.org/licenses/gpl-3.0.txt](https://www.gnu.org/licenses/gpl-3.0.txt)

> 💡 **Lưu ý**: Tạo file `LICENSE` riêng bằng cách copy toàn văn từ [đây](https://www.gnu.org/licenses/gpl-3.0.txt) và lưu vào thư mục gốc dự án.

---

## 🙏 Lời cảm ơn

<div align="center">

Dự án này không thể hoàn thành nếu thiếu sự hỗ trợ của:

| Đóng góp | Người/Tổ chức |
|---|---|
| 🌱 **Nguồn cảm hứng** | Ban giám hiệu THPT Bình Chánh |
| 💚 **Hướng dẫn, hỗ trợ** | Thầy cô CLB Tin Học |
| 👥 **Testing & feedback** | Các bạn học sinh |
| 🎨 **Cảm hứng đồ họa** | Cộng đồng pixel art Việt Nam |
| 🔥 **Backend miễn phí** | Firebase (Google) |
| 📚 **Kiến thức chia sẻ** | Cộng đồng mã nguồn mở |
| 💻 **Công cụ phát triển** | VS Code, Git, GitHub |

</div>

---

<div align="center">

## 🌱 HÃY CHƠI, HỌC VÀ LAN TỎA TINH THẦN SỐNG XANH! 🌱

### *"Lập Trình Vì Ngôi Trường Xanh"*

**CLB Tin Học THPT Bình Chánh — Năm học 2026–2027**

---

⭐ **Nếu bạn thấy dự án hữu ích, hãy [star repository này](https://github.com/hihiquan2010/GreenProject) nhé!** ⭐

[![Star](https://img.shields.io/github/stars/hihiquan2010/GreenProject?style=for-the-badge&logo=github&color=yellow)](https://github.com/hihiquan2010/GreenProject/stargazers)

*Made with 💚 in Vietnam*

</div>
