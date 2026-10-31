# Kỹ Năng Vibecoding_Flow

Quy trình phát triển phần mềm có kiểm soát cho AI lập trình: phân tích nghiệp vụ, thiết kế, lập trình, kiểm thử, kiểm tra bảo mật, nghiệm thu và phát hành, triển khai, bảo trì.

---

## I. Cấu Trúc Thư Mục

```text
├── plugin.json                    # Khai báo plugin
├── README.md                      # Giới thiệu và hướng dẫn sử dụng
└── skills/
    └── Vibecoding_Flow/
        ├── SKILL.md               # Quy tắc bắt buộc, mức quy mô, chu trình công việc, các cổng
        ├── GIAI_DOAN_VA_TIEU_CHI.md
        ├── MAU_TAI_LIEU.md
        ├── KIEM_THU_VA_TRIEN_KHAI.md
        ├── SUA_LOI_KHAN_CAP.md
        ├── QUY_UOC_GIT.md
        ├── KIEM_TRA_BAO_MAT.md
        ├── THIET_KE_GIAO_DIEN.md
        ├── GIAI_PHAP_CO_SAN.md
        ├── DIEM_XEM_TRUOC.md
        └── CAU_TRUC_THU_MUC.md
```

`SKILL.md` giữ các quy tắc bắt buộc và được giữ dưới 5.000 token để không bị cắt khi Claude Code nén ngữ cảnh. Quy trình chi tiết nằm trong các tệp tham chiếu, AI mở khi thực hiện bước tương ứng.

---

## II. Nội Dung Chính

- 18 nguyên tắc bắt buộc, gồm: không đoán, không phá vỡ, tìm giải pháp có sẵn trước khi viết mã, viết mã đơn giản và dùng lại mã đã có, dọn dẹp những gì AI tạo ra, cho người dùng xem trong lúc làm, đặt tệp đúng thư mục và không rải tệp ra gốc dự án.
- 13 giai đoạn có cổng kiểm soát; ba mức quy mô Nhỏ, Vừa, Lớn quyết định giai đoạn và tài liệu phải làm.
- Chu trình 11 bước cho mỗi công việc, có điểm xem trước sau mỗi lát.
- Cổng kiểm thử, cổng bảo mật, cổng triển khai, cổng khẩn cấp.
- Quy trình sửa lỗi khẩn cấp, kiểm tra bảo mật phần A–E, ứng phó sự cố bảo mật.
- Quy ước Git, sổ dùng chung chống trùng mã, danh sách tự rà soát mã và dọn dẹp.
- Bộ 27 tài liệu đánh số, mã định danh, ma trận truy vết.

---

## III. Hướng Dẫn Cài Đặt

### 1. Claude Code

1. **Cài skill cho toàn bộ máy:**
   ```bash
   git clone https://github.com/vinhngtienmdb-ui/vibecoding_skill.git
   mkdir -p ~/.claude/skills
   cp -r vibecoding_skill/skills/Vibecoding_Flow ~/.claude/skills/Vibecoding_Flow
   ```
   Trên Windows, thư mục đích là `%USERPROFILE%\.claude\skills\Vibecoding_Flow`.
2. **Bắt buộc áp dụng cho mọi dự án (tùy chọn):** thêm vào `~/.claude/CLAUDE.md`:
   ```markdown
   - Mọi công việc lập trình chỉ áp dụng skill `Vibecoding_Flow`. Nạp skill này trước khi bắt đầu việc.
   ```
3. **Kiểm tra:** mở Claude Code và gõ `/Vibecoding_Flow`.

### 2. Google Antigravity (Gemini)

1. **Cài đặt toàn cục (Machine-local):**
   Sao chép thư mục này vào đường dẫn:
   ```text
   ~/.gemini/config/plugins/dev-lifecycle/
   ```
2. **Kích hoạt plugin trong `config.json`:**
   ```json
   {
     "plugins": {
       "dev-lifecycle": {
         "enabled": true
       }
     }
   }
   ```
