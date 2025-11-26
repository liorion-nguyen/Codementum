# HTML5 & Form Mastery

---

# Khởi động

**Thời gian: 15 phút**

**Hoạt động**

- **Task 1: Warm-up Quiz (5 phút)**
  - Giáo viên đặt câu hỏi: "Các em đã biết gì về HTML5 và Form?"
  - Học sinh trả lời nhanh: Liệt kê các thẻ HTML đã biết
  - Mục tiêu: Kích hoạt kiến thức nền, tạo không khí học tập

- **Task 2: Phân tích đề thi mẫu (10 phút)**
  - Xem 2-3 câu hỏi trắc nghiệm về HTML5 Forms từ đề SEACSO mẫu
  - Học sinh thảo luận nhóm nhỏ: "Câu này hỏi gì? Các em sẽ chọn đáp án nào?"
  - Giáo viên gợi ý: "Có điều gì đặc biệt trong các câu hỏi này không?"
  - Mục tiêu: Nhận biết dạng bài sẽ gặp, tạo động lực học tập

---

# Kiến thức

**Thời gian: 60 phút**

## 📑 MỤC LỤC

1. [HTML5 Semantic Elements](#1-html5-semantic-elements-15-phút)
2. [HTML5 Forms - Cấu trúc cơ bản](#2-html5-forms---cấu-trúc-cơ-bản-10-phút)
3. [Các loại Input cơ bản](#3-các-loại-input-cơ-bản-15-phút)
4. [Input đặc biệt - Trọng tâm đề thi](#4-input-đặc-biệt---trọng-tâm-đề-thi-10-phút)
5. [Các thẻ Form khác](#5-các-thẻ-form-khác-5-phút)
6. [Validation trong HTML5](#6-validation-trong-html5-5-phút)

---

## **1. HTML5 Semantic Elements (15 phút)**

### **1.1. Giới thiệu Semantic HTML**

**Vấn đề với HTML cũ:**
- HTML cũ (HTML4) dùng nhiều `<div>` và `<span>` với `id` và `class`
- Khó hiểu cấu trúc và ý nghĩa của từng phần
- Khó bảo trì và phát triển

**Giải pháp HTML5:**
- HTML5 giới thiệu các thẻ Semantic (có ý nghĩa)
- Mỗi thẻ có ý nghĩa rõ ràng về chức năng
- Dễ hiểu, dễ bảo trì, tốt cho SEO và Accessibility

**Ví dụ so sánh:**
```html
<!-- HTML cũ -->
<div id="header">
    <div class="logo">Logo</div>
    <div class="nav">Menu</div>
</div>
<div id="content">
    <div class="article">Bài viết</div>
</div>
<div id="footer">Footer</div>

<!-- HTML5 Semantic -->
<header>
    <div class="logo">Logo</div>
    <nav>Menu</nav>
</header>
<main>
    <article>Bài viết</article>
</main>
<footer>Footer</footer>
```

### **1.2. Các thẻ Semantic quan trọng**

#### **`<header>` - Phần đầu trang**
- **Mục đích**: Phần đầu của trang hoặc section
- **Chứa**: Logo, navigation, tiêu đề
- **Ví dụ**:
  ```html
  <header>
      <h1>Trang Web của Tôi</h1>
      <nav>
          <a href="#home">Trang chủ</a>
          <a href="#about">Giới thiệu</a>
      </nav>
  </header>
  ```
- **Lưu ý**: Có thể có nhiều `<header>` trong 1 trang (mỗi section có thể có header riêng)

#### **`<nav>` - Điều hướng**
- **Mục đích**: Chứa các liên kết điều hướng
- **Chứa**: Menu, navigation links
- **Ví dụ**:
  ```html
  <nav>
      <ul>
          <li><a href="#home">Trang chủ</a></li>
          <li><a href="#products">Sản phẩm</a></li>
          <li><a href="#contact">Liên hệ</a></li>
      </ul>
  </nav>
  ```

#### **`<main>` - Nội dung chính**
- **Mục đích**: Nội dung chính, duy nhất của trang
- **Chứa**: Nội dung chính, không bao gồm header, footer, sidebar
- **Ví dụ**:
  ```html
  <main>
      <h1>Tiêu đề chính</h1>
      <p>Nội dung chính của trang...</p>
  </main>
  ```
- **QUAN TRỌNG**: Mỗi trang chỉ có **1** `<main>`

#### **`<section>` - Phần nội dung**
- **Mục đích**: Phần nội dung có chủ đề riêng
- **Chứa**: Nội dung có thể có tiêu đề riêng
- **Ví dụ**:
  ```html
  <section>
      <h2>Giới thiệu</h2>
      <p>Nội dung giới thiệu...</p>
  </section>
  <section>
      <h2>Dịch vụ</h2>
      <p>Nội dung dịch vụ...</p>
  </section>
  ```
- **Lưu ý**: Có thể có nhiều `<section>` trong 1 trang

#### **`<article>` - Bài viết độc lập**
- **Mục đích**: Nội dung độc lập, có thể tái sử dụng
- **Chứa**: Bài viết, blog post, comment
- **Ví dụ**:
  ```html
  <article>
      <header>
          <h2>Tiêu đề bài viết</h2>
          <p>Ngày đăng: 01/01/2025</p>
      </header>
      <p>Nội dung bài viết...</p>
      <footer>
          <p>Tác giả: Nguyễn Văn A</p>
      </footer>
  </article>
  ```
- **Khác với `<section>`**: `<article>` là nội dung độc lập, có thể đọc riêng

#### **`<aside>` - Nội dung phụ**
- **Mục đích**: Nội dung phụ, sidebar
- **Chứa**: Quảng cáo, links liên quan, thông tin bổ sung
- **Ví dụ**:
  ```html
  <aside>
      <h3>Quảng cáo</h3>
      <p>Nội dung quảng cáo...</p>
  </aside>
  ```

#### **`<footer>` - Phần cuối trang**
- **Mục đích**: Phần cuối của trang hoặc section
- **Chứa**: Copyright, links, thông tin liên hệ
- **Ví dụ**:
  ```html
  <footer>
      <p>&copy; 2025 Công ty ABC. All rights reserved.</p>
      <nav>
          <a href="#privacy">Chính sách</a>
          <a href="#terms">Điều khoản</a>
      </nav>
  </footer>
  ```

### **1.3. Cấu trúc trang HTML5 hoàn chỉnh**

**Ví dụ cấu trúc trang web:**
```html
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <title>Trang Web Mẫu</title>
</head>
<body>
    <header>
        <h1>Logo/Tiêu đề</h1>
        <nav>Menu điều hướng</nav>
    </header>
    
    <main>
        <section>
            <h2>Phần 1</h2>
            <article>
                <h3>Bài viết 1</h3>
                <p>Nội dung...</p>
            </article>
        </section>
        
        <aside>
            <h3>Sidebar</h3>
            <p>Nội dung phụ...</p>
        </aside>
    </main>
    
    <footer>
        <p>Copyright &copy; 2025</p>
    </footer>
</body>
</html>
```

---

## **2. HTML5 Forms - Cấu trúc cơ bản (10 phút)**

### **2.1. Thẻ `<form>` - Container chính**

**Cú pháp cơ bản:**
```html
<form action="url-xử-lý" method="GET|POST">
    <!-- Các input fields -->
</form>
```

**Các thuộc tính quan trọng:**
- `action`: URL xử lý form khi submit (ví dụ: `action="/submit"`)
- `method`: Phương thức gửi dữ liệu
  - `GET`: Dữ liệu hiển thị trên URL (ví dụ: `?name=John&age=20`)
  - `POST`: Dữ liệu gửi kèm trong request body (bảo mật hơn)
- `enctype`: Kiểu mã hóa dữ liệu
  - `application/x-www-form-urlencoded` (mặc định)
  - `multipart/form-data` (cho file upload)
  - `text/plain`
- `target`: Nơi hiển thị kết quả
  - `_self` (mặc định): Cùng tab
  - `_blank`: Tab mới
  - `_parent`: Frame cha
  - `_top`: Toàn bộ window
- `autocomplete`: Bật/tắt tự động điền (`on` hoặc `off`)
- `novalidate`: Tắt validation HTML5 (không nên dùng)

**Ví dụ:**
```html
<form action="/submit" method="POST" enctype="multipart/form-data">
    <!-- Form fields -->
</form>
```

### **2.2. Thẻ `<label>` - Gắn nhãn cho input**

**Cú pháp:**
```html
<label for="input-id">Nhãn</label>
<input type="text" id="input-id" name="input-name">
```

**Hai cách sử dụng:**

**Cách 1: Sử dụng `for` và `id` (Khuyến nghị)**
```html
<label for="username">Tên đăng nhập:</label>
<input type="text" id="username" name="username">
```

**Cách 2: Bọc input trong label**
```html
<label>
    Tên đăng nhập:
    <input type="text" name="username">
</label>
```

**Lợi ích:**
- Click vào label sẽ focus vào input
- Tốt cho Accessibility (screen readers)
- Trải nghiệm người dùng tốt hơn

**Ví dụ hoàn chỉnh:**
```html
<form>
    <div>
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
    </div>
    
    <div>
        <label>
            <input type="checkbox" name="agree">
            Tôi đồng ý với điều khoản
        </label>
    </div>
</form>
```

---

## **3. Các loại Input cơ bản (15 phút)**

### **3.1. Input Text - Văn bản thường**

**Cú pháp:**
```html
<input type="text" name="field-name" value="giá trị mặc định" placeholder="gợi ý">
```

**Các thuộc tính:**
- `name`: Tên trường (bắt buộc khi submit)
- `value`: Giá trị mặc định
- `placeholder`: Gợi ý hiển thị khi trống
- `maxlength`: Độ dài tối đa
- `minlength`: Độ dài tối thiểu
- `size`: Chiều rộng hiển thị (số ký tự)
- `readonly`: Chỉ đọc (vẫn submit được)
- `disabled`: Vô hiệu hóa (không submit được)

**Ví dụ:**
```html
<input type="text" 
       name="fullname" 
       placeholder="Nhập họ và tên" 
       maxlength="50" 
       minlength="2" 
       required>
```

**So sánh `value` vs `placeholder`:**
```html
<!-- value: Giá trị mặc định, có thể submit -->
<input type="text" name="city" value="Hà Nội">

<!-- placeholder: Chỉ là gợi ý, không submit -->
<input type="text" name="city" placeholder="Nhập thành phố">
```

### **3.2. Input Email - Email**

**Cú pháp:**
```html
<input type="email" name="email" required>
```

**Đặc điểm:**
- Tự động validation định dạng email
- Trình duyệt kiểm tra có `@` và domain hợp lệ
- Trên mobile, bàn phím tự động chuyển sang email mode

**Ví dụ:**
```html
<label for="email">Email:</label>
<input type="email" 
       id="email" 
       name="email" 
       placeholder="example@email.com" 
       required>
```

**Validation tự động:**
- ✅ `user@example.com` - Hợp lệ
- ❌ `user@` - Không hợp lệ
- ❌ `user.com` - Không hợp lệ

### **3.3. Input Password - Mật khẩu**

**Cú pháp:**
```html
<input type="password" name="password" required>
```

**Đặc điểm:**
- Ẩn ký tự khi gõ (hiển thị dấu chấm hoặc dấu sao)
- Không hiển thị giá trị trong HTML source
- Thường dùng với `minlength` để bảo mật

**Ví dụ:**
```html
<label for="password">Mật khẩu:</label>
<input type="password" 
       id="password" 
       name="password" 
       minlength="8" 
       required>
```

### **3.4. Input Number - Số**

**Cú pháp:**
```html
<input type="number" name="age" min="0" max="120" step="1">
```

**Các thuộc tính:**
- `min`: Giá trị tối thiểu
- `max`: Giá trị tối đa
- `step`: Bước nhảy (ví dụ: `step="5"` → 0, 5, 10, 15...)
- `value`: Giá trị mặc định

**Ví dụ:**
```html
<!-- Tuổi: 1-120 -->
<input type="number" name="age" min="1" max="120" step="1">

<!-- Điểm: 0-100, bước 0.5 -->
<input type="number" name="score" min="0" max="100" step="0.5">

<!-- Số lượng: 1-10, bước 1 -->
<input type="number" name="quantity" min="1" max="10" step="1">
```

**Lưu ý:**
- Trình duyệt hiển thị nút tăng/giảm
- Chỉ nhận số, không nhận chữ cái
- Có thể nhập số thập phân nếu `step` cho phép

### **3.5. Input Date - Ngày tháng**

**Cú pháp:**
```html
<input type="date" name="birthday" min="1900-01-01" max="2025-12-31">
```

**Đặc điểm:**
- Hiển thị date picker trên trình duyệt
- Format: `YYYY-MM-DD`
- Có thể giới hạn min/max

**Ví dụ:**
```html
<label for="birthday">Ngày sinh:</label>
<input type="date" 
       id="birthday" 
       name="birthday" 
       min="1900-01-01" 
       max="2025-12-31">
```

**Các loại date khác:**
```html
<!-- Chỉ thời gian -->
<input type="time" name="time">

<!-- Ngày và giờ -->
<input type="datetime-local" name="datetime">

<!-- Tháng -->
<input type="month" name="month">

<!-- Tuần -->
<input type="week" name="week">
```

### **3.6. Input URL - Địa chỉ web**

**Cú pháp:**
```html
<input type="url" name="website" placeholder="https://example.com">
```

**Đặc điểm:**
- Tự động validation định dạng URL
- Phải có protocol (`http://` hoặc `https://`)
- Trên mobile, bàn phím tự động chuyển sang URL mode

**Ví dụ:**
```html
<label for="website">Website:</label>
<input type="url" 
       id="website" 
       name="website" 
       placeholder="https://example.com">
```

### **3.7. Input Tel - Số điện thoại**

**Cú pháp:**
```html
<input type="tel" name="phone" pattern="[0-9]{10,11}">
```

**Đặc điểm:**
- Trên mobile, bàn phím tự động chuyển sang số
- Không tự động validation (cần dùng `pattern`)
- Thường kết hợp với `pattern` để validation

**Ví dụ:**
```html
<label for="phone">Số điện thoại:</label>
<input type="tel" 
       id="phone" 
       name="phone" 
       pattern="[0-9]{10,11}" 
       placeholder="0123456789">
```

---

## **4. Input đặc biệt - Trọng tâm đề thi (10 phút)**

### **4.1. Radio Buttons - Lựa chọn đơn**

**Cú pháp:**
```html
<input type="radio" name="group-name" value="value" id="id">
<label for="id">Nhãn</label>
```

**Đặc điểm:**
- Chỉ chọn được **1** option trong nhóm
- **QUAN TRỌNG**: Tất cả radio cùng nhóm phải có cùng `name`
- Mỗi radio phải có `value` riêng
- Nên dùng `id` và `label` để dễ click

**Ví dụ cơ bản:**
```html
<fieldset>
    <legend>Giới tính:</legend>
    <input type="radio" name="gender" value="male" id="male">
    <label for="male">Nam</label>
    
    <input type="radio" name="gender" value="female" id="female">
    <label for="female">Nữ</label>
    
    <input type="radio" name="gender" value="other" id="other">
    <label for="other">Khác</label>
</fieldset>
```

**Ví dụ với `checked` (mặc định chọn):**
```html
<input type="radio" name="payment" value="cash" id="cash" checked>
<label for="cash">Tiền mặt</label>

<input type="radio" name="payment" value="card" id="card">
<label for="card">Thẻ</label>
```

**Lỗi thường gặp:**
```html
<!-- ❌ SAI: Thiếu name, không nhóm được -->
<input type="radio" value="option1"> Option 1
<input type="radio" value="option2"> Option 2

<!-- ✅ ĐÚNG: Cùng name để nhóm -->
<input type="radio" name="choice" value="option1" id="opt1">
<label for="opt1">Option 1</label>
<input type="radio" name="choice" value="option2" id="opt2">
<label for="opt2">Option 2</label>
```

### **4.2. Checkbox - Lựa chọn nhiều**

**Cú pháp:**
```html
<input type="checkbox" name="field-name" value="value" id="id">
<label for="id">Nhãn</label>
```

**Đặc điểm:**
- Có thể chọn **nhiều** options
- Mỗi checkbox có thể có `name` riêng hoặc cùng `name` (sẽ là mảng)
- Có thể có nhiều checkbox được chọn cùng lúc

**Ví dụ cơ bản:**
```html
<fieldset>
    <legend>Sở thích:</legend>
    <input type="checkbox" name="hobby" value="reading" id="reading">
    <label for="reading">Đọc sách</label>
    
    <input type="checkbox" name="hobby" value="sports" id="sports">
    <label for="sports">Thể thao</label>
    
    <input type="checkbox" name="hobby" value="travel" id="travel">
    <label for="travel">Du lịch</label>
</fieldset>
```

**Ví dụ với `checked` (mặc định chọn):**
```html
<input type="checkbox" name="agree" value="yes" id="agree" checked>
<label for="agree">Tôi đồng ý với điều khoản</label>
```

**So sánh Radio vs Checkbox:**
```html
<!-- Radio: Chỉ chọn 1 -->
<input type="radio" name="size" value="S"> S
<input type="radio" name="size" value="M"> M
<input type="radio" name="size" value="L"> L

<!-- Checkbox: Chọn nhiều -->
<input type="checkbox" name="topping" value="cheese"> Phô mai
<input type="checkbox" name="topping" value="pepperoni"> Pepperoni
<input type="checkbox" name="topping" value="mushroom"> Nấm
```

### **4.3. Hidden Input - Trường ẩn**

**Cú pháp:**
```html
<input type="hidden" name="field-name" value="value">
```

**Đặc điểm:**
- Không hiển thị trên màn hình
- Vẫn được gửi khi submit form
- Dùng để truyền dữ liệu không cần người dùng nhập

**Ví dụ:**
```html
<form>
    <!-- Người dùng không thấy -->
    <input type="hidden" name="user_id" value="12345">
    <input type="hidden" name="session_id" value="abc123">
    
    <!-- Người dùng thấy và nhập -->
    <input type="text" name="comment" placeholder="Nhập bình luận">
    
    <button type="submit">Gửi</button>
</form>
```

**Ứng dụng:**
- Lưu ID người dùng
- Lưu session token
- Lưu thông tin bảo mật
- Tracking information

### **4.4. File Input - Upload file**

**Cú pháp:**
```html
<input type="file" name="file" accept="file-types" multiple>
```

**Các thuộc tính:**
- `accept`: Giới hạn loại file
  - `accept="image/*"` - Tất cả ảnh
  - `accept=".pdf,.doc,.docx"` - Chỉ PDF và Word
  - `accept="video/*"` - Tất cả video
- `multiple`: Cho phép chọn nhiều file
- `capture`: Chụp ảnh trực tiếp (mobile)

**Ví dụ:**
```html
<!-- Upload 1 ảnh -->
<label for="avatar">Ảnh đại diện:</label>
<input type="file" id="avatar" name="avatar" accept="image/*">

<!-- Upload nhiều ảnh -->
<label for="photos">Ảnh (nhiều file):</label>
<input type="file" id="photos" name="photos" accept="image/*" multiple>

<!-- Upload PDF -->
<label for="document">Tài liệu:</label>
<input type="file" id="document" name="document" accept=".pdf,.doc,.docx">
```

**Lưu ý:**
- Form phải có `enctype="multipart/form-data"` khi upload file
- Không thể set `value` cho file input (bảo mật)

**Ví dụ form upload:**
```html
<form action="/upload" method="POST" enctype="multipart/form-data">
    <label for="file">Chọn file:</label>
    <input type="file" id="file" name="file" accept="image/*" multiple>
    <button type="submit">Upload</button>
</form>
```

---

## **5. Các thẻ Form khác (5 phút)**

### **5.1. Select & Option - Dropdown**

**Cú pháp:**
```html
<select name="field-name">
    <option value="value1">Hiển thị 1</option>
    <option value="value2" selected>Hiển thị 2</option>
    <option value="value3">Hiển thị 3</option>
</select>
```

**Các thuộc tính:**
- `name`: Tên trường
- `multiple`: Cho phép chọn nhiều (giữ Ctrl/Cmd)
- `size`: Số dòng hiển thị
- `required`: Bắt buộc chọn

**Ví dụ:**
```html
<label for="country">Quốc gia:</label>
<select id="country" name="country" required>
    <option value="">-- Chọn quốc gia --</option>
    <option value="vn">Việt Nam</option>
    <option value="us">Hoa Kỳ</option>
    <option value="uk">Anh</option>
</select>
```

**Option groups:**
```html
<select name="car">
    <optgroup label="Xe hơi">
        <option value="sedan">Sedan</option>
        <option value="suv">SUV</option>
    </optgroup>
    <optgroup label="Xe máy">
        <option value="scooter">Scooter</option>
        <option value="motorcycle">Motorcycle</option>
    </optgroup>
</select>
```

### **5.2. Textarea - Vùng nhập văn bản dài**

**Cú pháp:**
```html
<textarea name="field-name" rows="4" cols="50" placeholder="Gợi ý"></textarea>
```

**Các thuộc tính:**
- `rows`: Số dòng (chiều cao)
- `cols`: Số cột (chiều rộng)
- `maxlength`: Độ dài tối đa
- `minlength`: Độ dài tối thiểu
- `readonly`: Chỉ đọc
- `disabled`: Vô hiệu hóa

**Ví dụ:**
```html
<label for="message">Tin nhắn:</label>
<textarea id="message" 
          name="message" 
          rows="5" 
          cols="40" 
          placeholder="Nhập tin nhắn của bạn..."
          maxlength="500"
          required></textarea>
```

### **5.3. Button - Nút bấm**

**Ba loại button:**
```html
<!-- Submit form -->
<button type="submit">Gửi</button>

<!-- Reset form -->
<button type="reset">Làm mới</button>

<!-- Button thường (không submit) -->
<button type="button">Click me</button>
```

**So sánh với `<input type="submit">`:**
```html
<!-- Cách 1: Button -->
<button type="submit">Gửi Form</button>

<!-- Cách 2: Input -->
<input type="submit" value="Gửi Form">
```

**Lợi ích của `<button>`:**
- Có thể chứa HTML bên trong (icon, text formatting)
- Linh hoạt hơn về styling

**Ví dụ:**
```html
<button type="submit">
    <span>Gửi</span>
    <i class="icon-send"></i>
</button>
```

---

## **6. Validation trong HTML5 (5 phút)**

### **6.1. Thuộc tính Validation cơ bản**

#### **`required` - Bắt buộc nhập**
```html
<input type="text" name="name" required>
```
- Không được để trống
- Trình duyệt tự động kiểm tra khi submit

#### **`pattern` - Regex pattern**
```html
<input type="text" name="phone" pattern="[0-9]{10,11}">
```
- Kiểm tra định dạng theo regex
- Ví dụ: Số điện thoại 10-11 chữ số

**Các pattern thường dùng:**
```html
<!-- Số điện thoại Việt Nam: 10-11 số -->
<input type="tel" pattern="[0-9]{10,11}">

<!-- Email -->
<input type="email" pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$">

<!-- Mã bưu điện: 5 số -->
<input type="text" pattern="[0-9]{5}">

<!-- Mật khẩu: ít nhất 8 ký tự, có chữ hoa, chữ thường, số -->
<input type="password" pattern="(?=.*[a-z])(?=.*[A-Z])(?=.*[0-9]).{8,}">
```

#### **`min` và `max` - Giới hạn giá trị**
```html
<!-- Số -->
<input type="number" min="0" max="100" step="5">

<!-- Ngày -->
<input type="date" min="2020-01-01" max="2025-12-31">
```

#### **`minlength` và `maxlength` - Độ dài chuỗi**
```html
<input type="text" minlength="3" maxlength="20">
```

#### **`step` - Bước nhảy**
```html
<!-- Bước 5: 0, 5, 10, 15... -->
<input type="number" step="5">

<!-- Bước 0.1: 0, 0.1, 0.2... -->
<input type="number" step="0.1">
```

### **6.2. Các lỗi sai thường gặp trong đề thi**

#### **❌ Lỗi 1: Quên thuộc tính `name` cho radio buttons**
```html
<!-- SAI -->
<input type="radio" value="male"> Nam
<input type="radio" value="female"> Nữ

<!-- ĐÚNG -->
<input type="radio" name="gender" value="male" id="male">
<label for="male">Nam</label>
<input type="radio" name="gender" value="female" id="female">
<label for="female">Nữ</label>
```

#### **❌ Lỗi 2: Nhầm lẫn `value` và `placeholder`**
```html
<!-- value: Giá trị mặc định, sẽ submit -->
<input type="text" name="city" value="Hà Nội">

<!-- placeholder: Chỉ là gợi ý, KHÔNG submit -->
<input type="text" name="city" placeholder="Nhập thành phố">
```

#### **❌ Lỗi 3: Không hiểu cách `pattern` hoạt động**
```html
<!-- SAI: pattern="email" không phải là regex hợp lệ -->
<input type="email" pattern="email">

<!-- ĐÚNG: Dùng regex -->
<input type="email" pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$">
```

#### **❌ Lỗi 4: Nhầm lẫn `required` và `readonly`**
```html
<!-- required: Bắt buộc nhập, không được để trống -->
<input type="text" name="name" required>

<!-- readonly: Chỉ đọc, KHÔNG thể sửa, NHƯNG vẫn submit được -->
<input type="text" name="id" value="123" readonly>

<!-- disabled: Vô hiệu hóa, KHÔNG submit được -->
<input type="text" name="temp" value="temp" disabled>
```

#### **❌ Lỗi 5: Nhầm lẫn `minlength` và `min`**
```html
<!-- minlength: Độ dài chuỗi (cho text) -->
<input type="text" minlength="3" maxlength="20">

<!-- min: Giá trị tối thiểu (cho number, date) -->
<input type="number" min="0" max="100">
```

### **6.3. Custom Validation Message**

**Sử dụng `setCustomValidity()`:**
```html
<input type="text" id="username" name="username" required>
<script>
    const input = document.getElementById('username');
    input.addEventListener('input', function() {
        if (input.value.length < 3) {
            input.setCustomValidity('Tên phải có ít nhất 3 ký tự');
        } else {
            input.setCustomValidity('');
        }
    });
</script>
```

---

# Thực hành

**Thời gian: 60 phút**

## **Bài tập 1: Tạo Form đăng ký cơ bản (20 phút)**

### **Yêu cầu:**
Tạo form đăng ký với các trường:
- Họ và tên (text, required, minlength 2, maxlength 50)
- Email (email, required)
- Mật khẩu (password, required, minlength 8)
- Xác nhận mật khẩu (password, required)
- Giới tính (radio: Nam/Nữ/Khác, required)
- Sở thích (checkbox: Đọc sách/Thể thao/Du lịch/Music)
- Ngày sinh (date, min="1900-01-01")
- Nút Submit và Reset

### **Code mẫu tham khảo:**
```html
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <title>Form Đăng ký</title>
</head>
<body>
    <header>
        <h1>Đăng ký tài khoản</h1>
    </header>
    
    <main>
        <form action="/register" method="POST">
            <div>
                <label for="fullname">Họ và tên:</label>
                <input type="text" 
                       id="fullname" 
                       name="fullname" 
                       required 
                       minlength="2" 
                       maxlength="50"
                       placeholder="Nhập họ và tên">
            </div>
            
            <div>
                <label for="email">Email:</label>
                <input type="email" 
                       id="email" 
                       name="email" 
                       required
                       placeholder="example@email.com">
            </div>
            
            <div>
                <label for="password">Mật khẩu:</label>
                <input type="password" 
                       id="password" 
                       name="password" 
                       required 
                       minlength="8"
                       placeholder="Ít nhất 8 ký tự">
            </div>
            
            <div>
                <label for="confirm-password">Xác nhận mật khẩu:</label>
                <input type="password" 
                       id="confirm-password" 
                       name="confirm-password" 
                       required>
            </div>
            
            <fieldset>
                <legend>Giới tính:</legend>
                <input type="radio" name="gender" value="male" id="male" required>
                <label for="male">Nam</label>
                
                <input type="radio" name="gender" value="female" id="female">
                <label for="female">Nữ</label>
                
                <input type="radio" name="gender" value="other" id="other">
                <label for="other">Khác</label>
            </fieldset>
            
            <fieldset>
                <legend>Sở thích:</legend>
                <input type="checkbox" name="hobby" value="reading" id="reading">
                <label for="reading">Đọc sách</label>
                
                <input type="checkbox" name="hobby" value="sports" id="sports">
                <label for="sports">Thể thao</label>
                
                <input type="checkbox" name="hobby" value="travel" id="travel">
                <label for="travel">Du lịch</label>
                
                <input type="checkbox" name="hobby" value="music" id="music">
                <label for="music">Âm nhạc</label>
            </fieldset>
            
            <div>
                <label for="birthday">Ngày sinh:</label>
                <input type="date" 
                       id="birthday" 
                       name="birthday" 
                       min="1900-01-01">
            </div>
            
            <div>
                <button type="submit">Đăng ký</button>
                <button type="reset">Làm mới</button>
            </div>
        </form>
    </main>
</body>
</html>
```

---

## **Bài tập 2: Form liên hệ với Validation (15 phút)**

### **Yêu cầu:**
Tạo form liên hệ với:
- Họ tên (text, required, minlength 2)
- Email (email, required, pattern validation)
- Số điện thoại (tel, required, pattern="[0-9]{10,11}")
- Chủ đề (select dropdown, required)
- Nội dung (textarea, required, minlength 10, maxlength 500)
- Nút Submit

### **Code mẫu:**
```html
<form action="/contact" method="POST">
    <div>
        <label for="name">Họ tên:</label>
        <input type="text" 
               id="name" 
               name="name" 
               required 
               minlength="2"
               placeholder="Nhập họ và tên">
    </div>
    
    <div>
        <label for="email">Email:</label>
        <input type="email" 
               id="email" 
               name="email" 
               required
               pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$"
               placeholder="example@email.com">
    </div>
    
    <div>
        <label for="phone">Số điện thoại:</label>
        <input type="tel" 
               id="phone" 
               name="phone" 
               required
               pattern="[0-9]{10,11}"
               placeholder="0123456789">
    </div>
    
    <div>
        <label for="subject">Chủ đề:</label>
        <select id="subject" name="subject" required>
            <option value="">-- Chọn chủ đề --</option>
            <option value="support">Hỗ trợ</option>
            <option value="feedback">Phản hồi</option>
            <option value="complaint">Khiếu nại</option>
            <option value="other">Khác</option>
        </select>
    </div>
    
    <div>
        <label for="message">Nội dung:</label>
        <textarea id="message" 
                  name="message" 
                  rows="5" 
                  cols="40"
                  required
                  minlength="10"
                  maxlength="500"
                  placeholder="Nhập nội dung tin nhắn (10-500 ký tự)"></textarea>
    </div>
    
    <button type="submit">Gửi tin nhắn</button>
</form>
```

---

## **Bài tập 3: Phân tích và sửa lỗi Form (10 phút)**

### **Form có lỗi:**
```html
<form>
    <input type="radio" value="option1"> Option 1
    <input type="radio" value="option2"> Option 2
    
    <input type="text" placeholder="Nhập tên" value="Tên mặc định">
    
    <input type="email" pattern="email">
    
    <input type="number" min="0" max="100" step="2">
    
    <input type="file" accept="image">
    
    <button>Submit</button>
</form>
```

### **Yêu cầu:**
1. Tìm tất cả các lỗi trong form trên
2. Sửa lại form cho đúng
3. Giải thích từng lỗi

### **Form đúng:**
```html
<form action="/submit" method="POST">
    <fieldset>
        <legend>Lựa chọn:</legend>
        <input type="radio" name="choice" value="option1" id="opt1">
        <label for="opt1">Option 1</label>
        <input type="radio" name="choice" value="option2" id="opt2">
        <label for="opt2">Option 2</label>
    </fieldset>
    
    <div>
        <label for="name">Tên:</label>
        <input type="text" 
               id="name" 
               name="name" 
               placeholder="Nhập tên">
    </div>
    
    <div>
        <label for="email">Email:</label>
        <input type="email" 
               id="email" 
               name="email" 
               pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$">
    </div>
    
    <div>
        <label for="number">Số:</label>
        <input type="number" 
               id="number" 
               name="number" 
               min="0" 
               max="100" 
               step="2">
    </div>
    
    <div>
        <label for="file">File:</label>
        <input type="file" 
               id="file" 
               name="file" 
               accept="image/*">
    </div>
    
    <button type="submit">Submit</button>
</form>
```

**Giải thích lỗi:**
1. ❌ Radio thiếu `name` → Không nhóm được
2. ❌ Radio thiếu `id` và `label` → Khó click
3. ❌ `value` và `placeholder` dùng cùng lúc → `value` sẽ hiển thị thay vì `placeholder`
4. ❌ `pattern="email"` sai → Phải dùng regex
5. ❌ `accept="image"` sai → Phải là `accept="image/*"`
6. ❌ Button thiếu `type="submit"` → Mặc định là submit nhưng nên rõ ràng

---

## **Bài tập 4: Form upload file (10 phút)**

### **Yêu cầu:**
Tạo form upload với:
- Tên file (text, required)
- Mô tả (textarea)
- Upload ảnh (file, accept="image/*", multiple)
- Upload tài liệu (file, accept=".pdf,.doc,.docx")
- Nút Submit

### **Code mẫu:**
```html
<form action="/upload" method="POST" enctype="multipart/form-data">
    <div>
        <label for="filename">Tên file:</label>
        <input type="text" 
               id="filename" 
               name="filename" 
               required
               placeholder="Nhập tên file">
    </div>
    
    <div>
        <label for="description">Mô tả:</label>
        <textarea id="description" 
                  name="description" 
                  rows="3" 
                  cols="40"
                  placeholder="Nhập mô tả"></textarea>
    </div>
    
    <div>
        <label for="images">Upload ảnh (nhiều file):</label>
        <input type="file" 
               id="images" 
               name="images" 
               accept="image/*" 
               multiple>
    </div>
    
    <div>
        <label for="document">Upload tài liệu:</label>
        <input type="file" 
               id="document" 
               name="document" 
               accept=".pdf,.doc,.docx">
    </div>
    
    <button type="submit">Upload</button>
</form>
```

---

## **Bài tập 5: Câu hỏi trắc nghiệm mẫu (5 phút)**

### **Làm 10 câu trắc nghiệm:**

1. **Radio buttons cần thuộc tính gì để nhóm lại?**
   - A. `id`  B. `class`  C. `name`  D. `value`
   - **Đáp án: C** - Tất cả radio cùng nhóm phải có cùng `name`

2. **Để upload nhiều file ảnh, cần thêm thuộc tính gì?**
   - A. `accept="image/*"`  B. `multiple`  C. Cả A và B  D. Không cần
   - **Đáp án: C** - Cần cả `accept` để giới hạn loại file và `multiple` để chọn nhiều

3. **Thuộc tính nào bắt buộc người dùng nhập?**
   - A. `readonly`  B. `required`  C. `disabled`  D. `placeholder`
   - **Đáp án: B** - `required` bắt buộc nhập

4. **`<input type="hidden">` dùng để làm gì?**
   - A. Ẩn input khỏi màn hình  B. Không cho người dùng nhập
   - C. Truyền dữ liệu ẩn  D. Cả A và C
   - **Đáp án: D** - Ẩn khỏi màn hình và truyền dữ liệu ẩn

5. **Để giới hạn độ dài chuỗi từ 5-20 ký tự, dùng thuộc tính nào?**
   - A. `length="5-20"`  B. `minlength="5" maxlength="20"`
   - C. `size="5-20"`  D. `range="5,20"`
   - **Đáp án: B** - Dùng `minlength` và `maxlength`

6. **Sự khác biệt giữa `value` và `placeholder`?**
   - A. `value` là giá trị mặc định, `placeholder` là gợi ý
   - B. `value` sẽ submit, `placeholder` không submit
   - C. Cả A và B  D. Không có khác biệt
   - **Đáp án: C** - Cả hai đều đúng

7. **Form upload file cần `enctype` gì?**
   - A. `application/x-www-form-urlencoded`  B. `multipart/form-data`
   - C. `text/plain`  D. Không cần
   - **Đáp án: B** - `multipart/form-data` cho file upload

8. **Mỗi trang HTML5 có thể có bao nhiêu thẻ `<main>`?**
   - A. 0  B. 1  C. Nhiều  D. Tùy ý
   - **Đáp án: B** - Chỉ có 1 `<main>` trong mỗi trang

9. **Checkbox khác Radio ở điểm nào?**
   - A. Checkbox chọn nhiều, Radio chọn 1
   - B. Checkbox có thể không chọn, Radio phải chọn 1
   - C. Cả A và B  D. Không khác
   - **Đáp án: A** - Checkbox chọn nhiều, Radio chỉ chọn 1

10. **Thuộc tính `pattern` dùng để làm gì?**
    - A. Validation định dạng bằng regex
    - B. Giới hạn giá trị
    - C. Bắt buộc nhập
    - D. Tất cả đều sai
    - **Đáp án: A** - Validation định dạng bằng regex

---

# Homework

**Thời gian làm bài: 45-60 phút**

## **Bài tập về nhà**

### **1. Bài tập 1: Tạo Form đăng ký hoàn chỉnh (25 phút)**

**Yêu cầu:**
- Tạo form đăng ký với đầy đủ các trường:
  - Họ và tên (text, required, minlength 2, maxlength 50)
  - Email (email, required, pattern validation)
  - Mật khẩu (password, required, minlength 8)
  - Xác nhận mật khẩu (password, required)
  - Số điện thoại (tel, required, pattern="[0-9]{10,11}")
  - Giới tính (radio: Nam/Nữ/Khác, required)
  - Ngày sinh (date, min="1900-01-01", max="2010-12-31")
  - Quốc gia (select dropdown, required)
  - Sở thích (checkbox: ít nhất 5 lựa chọn)
  - Ảnh đại diện (file, accept="image/*")
  - Đồng ý điều khoản (checkbox, required)
- Sử dụng Semantic HTML5
- Có validation đầy đủ
- Nộp file HTML

### **2. Bài tập 2: Làm 15 câu trắc nghiệm (20 phút)**

**Yêu cầu:**
- Giáo viên gửi file PDF với 15 câu hỏi về HTML5 Forms
- Học sinh làm và nộp đáp án
- Tự giải thích đáp án của mình (tại sao chọn đáp án đó)
- Nộp file Word/PDF

### **3. Bài tập 3: Phân tích đề thi mẫu SEACSO (15 phút)**

**Yêu cầu:**
- Xem 5 câu hỏi từ đề SEACSO mẫu về HTML5 Forms
- Ghi chú chi tiết:
  - Câu hỏi hỏi gì?
  - Có "bẫy" gì không?
  - Cách làm nhanh?
  - Kiến thức cần nhớ?
- Nộp file Word/PDF với phân tích

### **4. Bài tập 4: Tạo Form liên hệ với Validation nâng cao (Tùy chọn - Bonus)**

**Yêu cầu:**
- Form liên hệ với:
  - Họ tên, Email, Số điện thoại (có validation)
  - Chủ đề (select với optgroup)
  - Mức độ ưu tiên (radio: Thấp/Trung bình/Cao)
  - Nội dung (textarea, minlength 20, maxlength 1000)
  - Đính kèm file (file, accept=".pdf,.doc,.docx,.txt")
  - Checkbox "Gửi bản sao cho tôi"
- Sử dụng Semantic HTML5
- Nộp file HTML

## **Tài liệu tham khảo**

- **MDN Web Docs**: [HTML5 Forms](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)
- **W3Schools**: [HTML Form Elements](https://www.w3schools.com/html/html_form_elements.asp)
- **HTML5 Pattern**: [Common Input Patterns](https://www.html5pattern.com/)
- **Đề mẫu SEACSO**: Mock Test Category 5 & 6

## **Chuẩn bị cho buổi sau**

- ✅ Ôn lại toàn bộ kiến thức HTML5 Forms
- ✅ Làm đầy đủ bài tập về nhà
- ✅ Đọc trước về CSS Selectors (Buổi 2)
- ✅ Xem video về CSS Selectors cơ bản (nếu có)

---

**Lưu ý quan trọng**: 

- HTML5 Forms chiếm **tỷ trọng cao** trong đề thi trắc nghiệm Vòng Quốc gia (khoảng 3-4 câu/15 câu)
- Cần nắm vững: Radio/Checkbox, Validation, Input types
- Luyện tập nhiều với các dạng bài trắc nghiệm
- Chú ý các "bẫy" thường gặp: thiếu `name` cho radio, nhầm `value` và `placeholder`, sai `pattern`

**Chúc các em học tập hiệu quả! 🚀**
