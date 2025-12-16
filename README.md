# 🍜 Feed Me - Trang Donate Cá Nhân

Một trang web đơn giản và đẹp mắt để nhận donate thông qua MoMo. Dễ dàng tùy chỉnh mà **không cần biết code**!

![Preview](https://img.shields.io/badge/Status-Ready-green) ![License](https://img.shields.io/badge/License-Free-blue)

### 🌐 Demo: [https://nuoitoi.click](https://nuoitoi.click)

---

## 📦 Cài Đặt Nhanh

1. **Tải file** `index.html` về máy
2. Mở file bằng **bất kỳ trình soạn thảo văn bản nào** (Notepad, TextEdit, VS Code...)
3. Tìm đến phần `const CONFIG = {` và chỉnh sửa theo hướng dẫn bên dưới
4. Lưu file và upload lên hosting của bạn (hoặc mở trực tiếp trên trình duyệt để xem trước)

---

## 🎨 Hướng Dẫn Tùy Chỉnh Chi Tiết

### 📍 Vị Trí Cần Sửa

Mở file `index.html`, kéo xuống tìm dòng:

```javascript
const CONFIG = {
```

Tất cả những gì bạn cần chỉnh sửa đều nằm trong phần `CONFIG` này.

---

### 1️⃣ Thông Tin Cơ Bản

```javascript
pageTitle: "Nuôi Tôi 🍜",              // Tiêu đề trang (hiển thị trên tab trình duyệt)
```

**Cách sửa:** Thay `"Nuôi Tôi 🍜"` bằng tiêu đề bạn muốn.

**Ví dụ:**
```javascript
pageTitle: "Buy Me A Coffee ☕",
```

---

### 2️⃣ Avatar & Trạng Thái

```javascript
avatar: "🧑‍💻",                         // Avatar (emoji hoặc link ảnh)
statusBadge: "😢",                     // Badge trạng thái bên cạnh avatar
authorName: "Tôi",                    // Tên hiển thị ở footer
authorLink: "",                       // Link tới profile (để trống nếu không có)
```

**Cách sửa:**

| Thuộc tính | Mô tả | Ví dụ |
|------------|-------|-------|
| `avatar` | Emoji hoặc link ảnh | `"👨‍💻"` hoặc `"https://i.imgur.com/abc.jpg"` |
| `statusBadge` | Emoji hiển thị bên avatar | `"🔥"`, `"💪"`, `"😴"` |
| `authorName` | Tên của bạn | `"Nguyễn Văn A"` |
| `authorLink` | Link đến Facebook/GitHub | `"https://github.com/username"` |

**Ví dụ dùng ảnh:**
```javascript
avatar: "https://avatars.githubusercontent.com/u/123456",
```

---

### 3️⃣ Câu Chuyện Của Bạn

```javascript
storyTitle: "📖 Câu chuyện của tôi",
storyContent: `
    <p>Nội dung...</p>
`,
```

**Cách sửa:** Thay đổi nội dung bên trong. Bạn có thể dùng HTML cơ bản:

| Tag HTML | Công dụng | Ví dụ |
|----------|-----------|-------|
| `<p>...</p>` | Đoạn văn | `<p>Xin chào!</p>` |
| `<span class="highlight">...</span>` | Tô sáng chữ | `<span class="highlight">quan trọng</span>` |
| `<ul><li>...</li></ul>` | Danh sách | `<ul><li>Item 1</li><li>Item 2</li></ul>` |
| `<br>` | Xuống dòng | `Dòng 1<br>Dòng 2` |
| `<strong>...</strong>` | In đậm | `<strong>Chú ý</strong>` |

**Ví dụ:**
```javascript
storyContent: `
    <p>Xin chào! Mình là <span class="highlight">Hùng</span>, một freelancer đang cố gắng mỗi ngày! 🚀</p>
    <p>Mỗi ly cà phê từ bạn sẽ giúp mình:</p>
    <ul style="margin-top: 10px; margin-left: 20px;">
        <li>☕ Thức đêm code project</li>
        <li>📚 Mua sách học thêm</li>
        <li>🎮 Giải trí sau giờ làm</li>
    </ul>
`,
```

---

### 4️⃣ Dòng Chữ Chạy (Marquee)

```javascript
marqueeItems: [
    "🔥 BREAKING: Dev bỏ ăn trưa 7 ngày...",
    "🎮 Fun fact: 99% donate sẽ đi vào game...",
    // Thêm nhiều dòng khác...
],
```

**Cách sửa:** 
- Mỗi dòng được bọc trong `"..."` và cách nhau bởi dấu `,`
- Dòng cuối **KHÔNG** cần dấu `,`

**Ví dụ:**
```javascript
marqueeItems: [
    "🎯 Đang làm dự án siêu hay, donate để xem nha!",
    "💡 1 donate = 1 feature mới",
    "🙏 Cảm ơn mọi người đã ủng hộ!"
],
```

---

### 5️⃣ Emoji Nổi (Background Animation)

```javascript
floatingEmojis: ["🍜", "💰", "🎮", "☕", "🍕", "💻", "🎵", "🌙", "⭐"],
```

**Cách sửa:** Thay đổi các emoji trong danh sách.

**Ví dụ:**
```javascript
floatingEmojis: ["☕", "🎮", "💻", "🎵", "💖", "🌟"],
```

---

### 6️⃣ ⭐ Các Mức Donate (QUAN TRỌNG!)

Đây là phần quan trọng nhất - cấu hình link MoMo của bạn:

```javascript
donationOptions: [
    {
        amount: 10000,                    // Số tiền (không có dấu phẩy)
        emoji: "🥤",                      // Emoji hiển thị
        description: "1 ly trà đá",       // Mô tả ngắn
        momoLink: "https://me.momo.vn/..." // Link MoMo của bạn
    },
    // ... các mức khác
],
```

#### 🔧 Cách Tạo Link MoMo:

1. Mở app **MoMo** trên điện thoại
2. Vào **"Nhận tiền"** → **"Yêu cầu thanh toán"**
3. Nhập số tiền muốn nhận (ví dụ: 10,000đ)
4. Nhấn **"Tạo link"** hoặc **"Chia sẻ"**
5. Copy link và dán vào `momoLink`

#### 📝 Ví dụ Đầy Đủ:

```javascript
donationOptions: [
    {
        amount: 10000,
        emoji: "🥤",
        description: "1 ly trà đá",
        momoLink: "https://me.momo.vn/yourname/abc123"
    },
    {
        amount: 25000,
        emoji: "☕",
        description: "1 ly cà phê",
        momoLink: "https://me.momo.vn/yourname/def456"
    },
    {
        amount: 50000,
        emoji: "🍜",
        description: "1 tô phở",
        momoLink: "https://me.momo.vn/yourname/ghi789",
        isDefault: true  // ← Thêm dòng này để đặt làm mức mặc định được chọn sẵn
    },
    {
        amount: 100000,
        emoji: "🎮",
        description: "Game mới",
        momoLink: "https://me.momo.vn/yourname/jkl012"
    }
],
```

#### ⚠️ Lưu Ý Quan Trọng:

- `amount`: Viết số **KHÔNG** có dấu phẩy (10000, không phải 10,000)
- `isDefault: true`: Chỉ **MỘT** mức được đánh dấu mặc định
- Có thể thêm/bớt mức donate tùy ý

---

### 7️⃣ Link MoMo Dự Phòng

```javascript
momoFallback: "https://me.momo.vn/yourname",
```

**Cách sửa:** Thay bằng link MoMo profile của bạn (link không có số tiền cố định).

---

### 8️⃣ Danh Sách Người Đã Donate

```javascript
recentDonations: [
    {
        avatar: "😇",                              // Emoji avatar
        name: "Nguyễn Văn A",                     // Tên người donate
        message: "Ủng hộ bạn nha! 💪",            // Lời nhắn
        amount: 50000,                            // Số tiền
        time: "2025-12-10 14:30:00"               // Thời gian (YYYY-MM-DD HH:MM:SS)
    },
    // Thêm người khác...
],
```

**Cách thêm người donate mới:**

1. Copy mẫu bên trên
2. Dán vào trong `recentDonations: [ ... ]`
3. Sửa thông tin tương ứng
4. **NHỚ** thêm dấu `,` sau mỗi người (trừ người cuối cùng)

**Ví dụ với nhiều người:**
```javascript
recentDonations: [
    {
        avatar: "🎮",
        name: "Gamer Pro",
        message: "Mua game đi bro!",
        amount: 200000,
        time: "2025-12-11 10:00:00"
    },
    {
        avatar: "👩",
        name: "Mẹ",
        message: "Con ăn cơm nhà đi 😤",
        amount: 50000,
        time: "2025-12-10 18:30:00"
    }
],
```

**Nếu chưa có ai donate:** Để mảng rỗng
```javascript
recentDonations: [],
```

---

### 9️⃣ Footer & Thông Tin Khác

```javascript
footerText: "Nếu bạn thấy vui, hãy share cho bạn bè cùng cười! 😂",
disclaimer: `
    ⚠️ Đây là trang web parody/troll.<br>
    Mọi donate đều được sử dụng để mua phở và cà phê (thật sự) 🍜 ☕
`,
```

**Cách sửa:** Thay đổi nội dung tùy thích.

---

### 🔟 Tùy Chỉnh Text (Nâng Cao)

```javascript
sectionTitleDonate: "💝 Nuôi Tôi Ngay!",
sectionTitleDonors: "🎉 Những người tốt bụng",
donateButtonText: "Nuôi Tôi",
emptyDonationTitle: "Chưa có ai nuôi tôi...",
emptyDonationQuote: '"Một đồng cũng là tình thương, hai đồng cũng là yêu mến" 💝',
```

---

## 🚀 Deploy (Đưa Lên Internet)

### Cách 1: GitHub Pages (Miễn phí)

1. Tạo tài khoản [GitHub](https://github.com)
2. Tạo repository mới tên `donate` (hoặc tên bất kỳ)
3. Upload file `index.html`
4. Vào **Settings** → **Pages** → Source chọn `main` branch
5. Website sẽ có địa chỉ: `https://username.github.io/donate`

### Cách 2: Netlify (Miễn phí, dễ hơn)

1. Vào [netlify.com](https://netlify.com)
2. Kéo thả file `index.html` vào trang
3. Xong! Bạn sẽ có link ngay lập tức

### Cách 3: Vercel (Miễn phí)

1. Vào [vercel.com](https://vercel.com)
2. Tạo project mới và upload file
3. Deploy với 1 click

---

## ❓ FAQ - Câu Hỏi Thường Gặp

### Q: Làm sao để thêm ảnh avatar thay vì emoji?
**A:** Thay emoji bằng link ảnh:
```javascript
avatar: "https://i.imgur.com/your-image.jpg",
```

### Q: Trang không hiển thị đúng?
**A:** Kiểm tra:
- Có thiếu dấu `"` hoặc `,` không?
- Có dấu `,` thừa ở cuối danh sách không?
- Mở Console (F12) để xem lỗi

### Q: Link MoMo không hoạt động?
**A:** 
- Kiểm tra link có đúng format `https://me.momo.vn/...`
- Test link trên trình duyệt trước
- Đảm bảo link còn hiệu lực

### Q: Muốn thay đổi màu sắc?
**A:** Tìm phần `:root { ... }` trong CSS và sửa các giá trị màu:
```css
:root {
    --primary: #ff6b6b;      /* Màu chính */
    --secondary: #4ecdc4;    /* Màu phụ */
    --accent: #ffe66d;       /* Màu nhấn */
}
```

---

## 🎉 Easter Egg

Nhấn tổ hợp phím: `↑ ↑ ↓ ↓ ← → ← → B A` để kích hoạt Rainbow Mode! 🌈

---

## 📄 License

Miễn phí sử dụng cho mục đích cá nhân. Nếu thấy hữu ích, hãy ⭐ star repo nhé!

---

Made with 💔 and ☕ by a hungry developer
