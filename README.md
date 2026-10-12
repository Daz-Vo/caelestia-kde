<div align="center">

<img src="assets/logo.svg" width="64" alt="Caelestia logo" />

# Caelestia KDE (Bản Tùy Biến Của Daz_Vo)

[![Arch Linux](https://img.shields.io/badge/Arch_Linux-1793d1?logo=arch-linux&logoColor=white&style=for-the-badge&labelColor=101418)](https://archlinux.org)
[![Fedora](https://img.shields.io/badge/Fedora-51A2DA?logo=fedora&logoColor=white&style=for-the-badge&labelColor=101418)](https://fedoraproject.org)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?logo=ubuntu&logoColor=white&style=for-the-badge&labelColor=101418)](https://ubuntu.com)
[![KDE Plasma](https://img.shields.io/badge/Plasma_6-1D99F3?logo=kde&logoColor=white&style=for-the-badge&labelColor=101418)](https://kde.org/plasma-desktop)
[![License: GPL-3.0-or-later](https://img.shields.io/badge/License-GPL--3.0--or--later-9bd0cc?style=for-the-badge&labelColor=101418)](LICENSE)

</div>

<!-- markdownlint-disable-next-line MD034 -->
https://github.com/user-attachments/assets/38b24e7f-fdd9-43db-872b-8c0ac23a44fd

> [!NOTE]
> Đây là bản fork tùy biến của [`ladybug-me/caelestia-kde`](https://github.com/ladybug-me/caelestia-kde) (bản chuyển giao diện của [`caelestia-dots/shell`](https://github.com/caelestia-dots/shell) sang KDE Plasma 6 Wayland).
> Bản fork này đã được tinh chỉnh và bổ sung các tính năng nâng cao về trải nghiệm thông báo, chặn popup rác lúc khởi động cùng bộ công cụ giữ nguyên tùy biến sau mỗi lần cập nhật.

---

## ✨ Điểm Mới & Tinh Chỉnh Trong Bản Này

1. **Thông báo dính liền khối:** Khi mở ngăn tiện ích phía trên (Utilities drawer), thông báo được đẩy xuống và gắn liền khối thành một thể thống nhất, không còn khoảng hở rời rạc hay bị che khuất.
2. **Khởi động êm ái (Startup Mute Guard):** Chặn hoàn toàn các thông báo Num Lock / Caps Lock và thanh OSD (Âm lượng / Độ sáng) nhảy lên màn hình trong 1.5 giây đầu khi vừa nạp giao diện.
3. **Vị trí thông báo chuẩn:** Vị trí mặc định được đặt tại góc trên bên phải (`top-right`) tối ưu hiển thị.
4. **Bộ công cụ khôi phục tùy biến:** Đi kèm lệnh độc quyền `caelestia-apply-customizations` giúp khôi phục toàn bộ tinh chỉnh ngay lập tức sau mỗi lần cập nhật upstream.
5. **Tối ưu chuyển cửa sổ (Alt + Tab):** Phân tách rõ ràng phím tắt, `Alt + Tab` chuyển nhanh giữa các cửa sổ gọn gàng không bị bung choáng hết màn hình lớn, trong khi `Meta + Tab` (hoặc `Super + Tab`) mở giao diện Tổng quan (Overview) toàn màn hình khi cần quản lý đa không gian làm việc.
6. **Trải nghiệm Overview mượt mà:** Chuyển không gian làm việc ngay lập tức chỉ với 1 click mà không thoát Overview, và bấm vào chính không gian làm việc hiện tại để đóng Overview.
7. **Xoay vòng Workspace hai chiều:** Giữ trọn tính năng xoay vòng (wrap-around) không gian làm việc khi bấm nút chuyển trang ở hai mép màn hình.
8. **Kéo thả ứng dụng ở Thumbnail thu nhỏ:** Cho phép kéo thả trực tiếp cửa sổ/ứng dụng giữa các thumbnail màn hình nhỏ trong thanh chuyển đổi.
9. **Vuốt 2 ngón tay chuyển Quick Toggles:** Hỗ trợ cử chỉ vuốt 2 ngón tay (Touchpad horizontal swipe) sang trái/phải để chuyển đổi qua lại giữa các trang Quick Toggles tiện lợi.
10. **Bảo tồn cấu hình Shell / Terminal riêng:** Giữ nguyên cấu hình cá nhân (Fish shell, Starship prompt, Fastfetch...), không chạy đè logo Caelestia khi mở terminal (chỉ hiển thị logo khi chạy các ứng dụng như Dolphin hoặc khi gõ lệnh thủ công).
11. **Sửa lỗi Tiling chia 4 ô bằng nhau (Quarter / Grid 2x2):** Khắc phục lỗi Krohnkite tự ý dồn cửa sổ về Master-Stack (1 ô lớn bên trái, 3 ô dồn bên phải); chuẩn hóa cơ chế tắt layout bằng giá trị `0` và tự động nạp lại script KWin ngay lập tức khi lưu cài đặt, kích hoạt sẵn chế độ chia 4 góc 2x2 bằng nhau.

12. **Tối ưu phím tắt menu nguồn (`Super + Delete`):** Chuyển phím tắt kích hoạt menu nguồn (Session menu) sang tổ hợp tiện dụng **`Super + Delete`** (thay cho `Ctrl + Alt + Delete` cồng kềnh), bấm nhanh chỉ bằng một tay.

---

## Cài Đặt (Installation)

**Yêu cầu hệ thống:** Arch-based, Fedora, hoặc Debian/Ubuntu chạy **KDE Plasma 6 trên Wayland**, Qt 6.9+.

Chạy các lệnh sau trong terminal:

```bash
git clone --recurse-submodules https://github.com/Daz-Vo/caelestia-kde.git
cd caelestia-kde
./caelestia-install
```

---

## Cập Nhật & Khôi Phục Tùy Chỉnh (Updating)

Khi Caelestia có bản cập nhật mới, bạn có thể cập nhật thông qua:
* **Giao diện Nexus:** `Nexus -> Updates -> Install Updates`
* **Lệnh terminal:** `caelestia update`

### ⚠️ Khôi phục các thiết lập tùy biến sau khi cập nhật:
Sau khi cập nhật xong, các file giao diện gốc có thể bị ghi đè. Bạn chỉ cần mở terminal và chạy một lệnh duy nhất:

```bash
caelestia-apply-customizations
```

> **Lệnh trên sẽ tự động:**
> 1. Vá lại logic gắn liền khối thông báo cho `Panels.qml`.
> 2. Kích hoạt lại bộ lọc chặn popup NumLock/OSD khi khởi động trong `Kwin.qml` và `Wrapper.qml`.
> 3. Cập nhật logic Workspace / Overview: tắt kéo thả app ở màn hình nhỏ, 1 click chuyển workspace không đóng Overview, bấm workspace hiện tại để đóng.
> 4. Kiểm tra lại cấu hình phím tắt và vị trí thông báo trong `shell.json`.
> 5. Khởi động lại Caelestia Shell để áp dụng ngay lập tức mà không cần đăng xuất.

---

## Gỡ Cài Đặt (Uninstalling)

Chạy trình cài đặt và chọn *Uninstall*, hoặc gõ lệnh:

```bash
bash ./uninstall.sh
```

---

## Phím Tắt Mặc Định (Keybinds)

| Phím tắt | Thao tác |
| --- | --- |
| `Super + Delete` | Bật menu tùy chọn nguồn (Tắt máy / Khởi động lại / Khóa) |
| `Super` | Mở App Launcher |
| `Super + /` | Bảng tra cứu phím tắt |
| `Super + Enter` | Mở Terminal |
| `Super + Tab` | Tổng quan cửa sổ (Overview) |
| `Super + 1-5` | Chuyển Không gian làm việc (Workspace) |
| `Super + B` | Bảng thông báo (Sidebar) |
| `Super + V` | Lịch sử Clipboard |
| `Super + Shift + S` | Chụp ảnh màn hình |
| `Super + Shift + A` | Tìm kiếm ảnh với Google Lens |
| `Super + Shift + D` | Nhận diện chữ trong ảnh (OCR) |
| `Super + Ctrl + S` | Quay video màn hình |
| `Super + Shift + C` | Lấy mã màu màn hình (Color Picker) |
| `Super + Shift + V` | Bảng chọn Emoji |

---

## Cấu Hình Hệ Thống

Mở **Nexus** (Nhấn `Super`, sau đó gõ `>Settings`):

- **Appearance:** Hình nền, màu sắc, phông chữ và slideshow đổi hình nền.
- **Panels:** Tùy biến thanh dock, dashboard, launcher, sidebar và overview.
- **Desktop:** Window rules, menu chuột phải, Krohnkite tiling.
- **Shortcuts:** Đổi phím tắt có sẵn hoặc thêm phím tắt cho lệnh riêng.
- **Plugins:** Cài đặt tiện ích mở rộng.

File cấu hình được lưu tại: `~/.config/caelestia/shell.json`.

---

## Xử Lý Sự Cố (Troubleshooting)

| Vấn đề | Cách khắc phục |
| --- | --- |
| Widget không hiển thị | Đăng xuất rồi đăng nhập lại, hoặc chạy: `caelestia shell -d` |
| Màu sắc không đồng bộ | Chạy `caelestia scheme set -n dynamic`, hoặc `caelestia wallpaper -f <đường_dẫn_ảnh>` |
| Cài đặt bị gián đoạn giữa chừng | Chạy lại: `bash ./scripts/setup.sh` |
| Mất tùy biến sau khi update | Chạy lại: `caelestia-apply-customizations` |

Để xem log chi tiết, bật *Debug Mode* trong `Nexus -> About -> Advanced`, sau đó chạy:
```bash
caelestia shell -l
```

---

## Cấu Trúc Thư Mục (Repository Layout)

```
installer/     Trình cài đặt TUI và danh sách gói theo từng bản phân phối Linux
scripts/       Quy trình cài đặt / cập nhật hệ thống
src/           Các tệp cài vào hệ thống (scripts, bin wrappers, submodules)
shell/         Mã nguồn giao diện Caelestia QML và plugin C++
docs/          Tài liệu hướng dẫn & kiến trúc thiết kế
assets/        Logo, ảnh chụp màn hình và video minh họa
```

---

## Đóng Góp & Lời Cảm Ơn (Credits)

- [caelestia-dots/shell](https://github.com/caelestia-dots/shell) & [caelestia dotfiles](https://github.com/caelestia-dots/caelestia) bởi [@soramanew](https://github.com/soramanew)
- [ladybug-me/caelestia-kde](https://github.com/ladybug-me/caelestia-kde) - Dự án gốc port sang KDE Plasma
- [Daz_Vo](https://github.com/Daz-Vo) - Tinh chỉnh trải nghiệm thông báo, bộ đệm khởi động và công cụ khôi phục tùy biến

## Giấy Phép (License)

GPL-3.0-or-later - Xem chi tiết tại [LICENSE](LICENSE).
