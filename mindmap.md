# Cấu Trúc Dữ Liệu Đối Tượng (Object) & Array of Objects

## 1. Khái Niệm & Khởi Tạo
- **Bản chất:** Cấu trúc dữ liệu theo cặp Key-Value (Khóa-Giá trị).
- **Khởi tạo:** Cú pháp Object Literal `{ }`.
- **Kiểu dữ liệu:** Kiểu Tham chiếu (Reference Type).
- **Ứng dụng:** Mô phỏng thực thể thực tế (Ví dụ: Hồ sơ phòng khách sạn).

## 2. Cú Pháp Truy Cập
- **Dot Notation (`obj.prop`)**
  - Cú pháp tĩnh.
  - Ngắn gọn, được IDE hỗ trợ Autocomplete.
  - Không dùng được với biến số.
- **Bracket Notation (`obj['prop']` / `obj[var]`)**
  - Cú pháp động.
  - Bắt buộc khi truy cập qua biến (Dynamic Key).
  - Bắt buộc khi Key chứa dấu cách, gạch ngang, ký tự đặc biệt.

## 3. Thao Tác CRUD
- **Create (Thêm mới):** `obj.newKey = value`
- **Read (Đọc giá trị):** Sử dụng Dot hoặc Bracket Notation.
- **Update (Cập nhật):** Gán lại giá trị `obj.key = newValue`.
- **Delete (Xóa):** Sử dụng toán tử `delete obj.key`.
  - Hủy hoàn toàn thuộc tính khỏi đối tượng.

## 4. Mảng Các Đối Tượng (Array of Objects)
- **Mô hình:** Đại diện cho Bảng dữ liệu (Table/Collection).
- **Cấu trúc:** Mảng chứa nhiều Object con `[ {id: 1}, {id: 2} ]`.
- **Duyệt danh sách:** Thường dùng `for...of`, `forEach`, `map`.
- **Tra cứu/Lọc:** Dùng `find()`, `filter()`, `findIndex()` theo định danh (ID).
- **Thao tác mảng:** Thêm (`push`), Xóa (`splice`).

## 5. Cạm Bẫy Sai Sót Thường Gặp
- **Lỗi truy cập động:** Lặp `for...in` dùng `obj.key` bị undefined (Phải dùng `obj[key]`).
- **Lỗi xóa thuộc tính:** Gán thuộc tính `= undefined` (Key vẫn tồn tại, tốn bộ nhớ).
- **Lỗi tham chiếu vùng nhớ:** Gán `objA = objB` sinh lỗi dính vùng nhớ.
  - Cần sử dụng Sao chép nông (Shallow Copy) hoặc Sao chép sâu (Deep Copy).