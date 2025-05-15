# Contributing Guidelines

## Git Commit Rules

### Commit Message Format
Mỗi commit message phải tuân theo format sau:

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Type
Phải là một trong các loại sau:
- `feat`: Thêm tính năng mới
- `fix`: Sửa lỗi
- `docs`: Thay đổi tài liệu
- `style`: Thay đổi format, không ảnh hưởng đến logic
- `refactor`: Tái cấu trúc code, không thêm tính năng mới
- `test`: Thêm hoặc sửa test
- `chore`: Cập nhật build process, package manager, etc.

### Scope
Phạm vi của commit, ví dụ:
- `section-01`: Thay đổi trong Section 01
- `section-02`: Thay đổi trong Section 02
- `docs`: Thay đổi tài liệu
- `ci`: Thay đổi CI/CD
- `all`: Thay đổi toàn bộ dự án

### Subject
- Ngắn gọn, mô tả thay đổi
- Bắt đầu bằng động từ
- Không viết hoa chữ cái đầu
- Không kết thúc bằng dấu chấm

### Body
- Mô tả chi tiết thay đổi
- Giải thích lý do thay đổi
- Có thể liệt kê các thay đổi cụ thể

### Footer
- Liên kết đến issue (nếu có)
- Breaking changes (nếu có)

### Ví dụ Commit Messages

1. **Thêm tính năng mới**
```
feat(section-01): add docker installation guide

- Add step-by-step installation guide for Docker
- Include system requirements
- Add troubleshooting section

Closes #123
```

2. **Sửa lỗi**
```
fix(section-02): correct docker run command syntax

- Fix incorrect port mapping syntax in docker run command
- Update examples to use correct format
- Add explanation for port mapping

Fixes #45
```

3. **Cập nhật tài liệu**
```
docs(all): update contributing guidelines

- Add more examples for commit messages
- Improve formatting of guidelines
- Add section about code review process
```

4. **Tái cấu trúc code**
```
refactor(section-03): improve volume management examples

- Split large examples into smaller, focused ones
- Add more comments explaining each step
- Improve error handling in examples
```

5. **Cập nhật cấu hình**
```
chore(ci): update GitHub Actions workflow

- Add caching for dependencies
- Update Node.js version to 18
- Add automated testing step
```

## Quy tắc đóng góp

1. **Fork repository**
   - Fork repository này về tài khoản GitHub của bạn
   - Clone repository đã fork về máy local

2. **Tạo branch mới**
   ```bash
   # Ví dụ tạo branch cho tính năng mới
   git checkout -b feature/add-docker-compose-examples
   
   # Ví dụ tạo branch để sửa lỗi
   git checkout -b fix/correct-port-mapping
   ```

3. **Commit changes**
   - Tuân thủ quy tắc commit message
   - Commit thường xuyên với message rõ ràng

4. **Push changes**
   ```bash
   # Ví dụ push branch mới
   git push origin feature/add-docker-compose-examples
   ```

5. **Tạo Pull Request**
   - Tạo Pull Request từ branch của bạn vào branch main
   - Mô tả rõ ràng thay đổi trong PR
   - Liên kết đến issue (nếu có)

## Code Style

1. **Format code**
   - Sử dụng 2 spaces cho indent
   - Không có trailing whitespace
   - Kết thúc file bằng newline

2. **Documentation**
   - Thêm comments cho code phức tạp
   - Cập nhật README khi cần thiết
   - Sử dụng markdown cho tài liệu

3. **Testing**
   - Thêm test cho code mới
   - Đảm bảo tất cả test pass

## Review Process

1. **Code Review**
   - PR sẽ được review bởi maintainer
   - Có thể yêu cầu thay đổi
   - Cần giải quyết tất cả comments

2. **Merge**
   - PR sẽ được merge sau khi approved
   - Squash merge được khuyến khích

## Liên hệ

Nếu có thắc mắc, vui lòng:
- Mở issue trên GitHub
- Liên hệ qua email
- Tham gia discussion 