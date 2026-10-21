

# Cập nhật Fcitx5 Lotus trên NixOS

## 1. Tìm phiên bản mới

Mở [GitHub Releases](https://github.com/LotusInputMethod/fcitx5-lotus/releases), tìm bản mới nhất và ghi lại số phiên bản, ví dụ `5.0.7`.

## 2. Lấy hash mã nguồn

Thay `X.Y.Z` bằng số phiên bản mới:

```
nix-prefetch-url --unpack https://github.com/LotusInputMethod/fcitx5-lotus/archive/refs/tags/vX.Y.Z.tar.gz
```

Ghi lại hash dạng base32 mà lệnh in ra.

## 3. Đổi hash sang định dạng SRI

Thay `HASH_BASE32` bằng hash vừa nhận:

```
nix hash convert --hash-algo sha256 --to sri HASH_BASE32
```

Ghi lại kết quả bắt đầu bằng `sha256-`.

## 4. Cập nhật gói

Mở `pkgs/fcitx5-lotus.nix`, cập nhật các giá trị:

```
version = "X.Y.Z";
tag = "vX.Y.Z";
hash = "sha256-HASH_SRI";
```

Thay giá trị mẫu bằng phiên bản và hash mới.

## 5. Cập nhật tài liệu

Trong `docs/system-guide.md`, sửa số phiên bản Lotus được ghi trong tài liệu.

## 6. Rebuild NixOS

Từ thư mục cấu hình, chạy:

```
nswitch
```

Không cần chạy `nix flake update` để cập nhật Lotus.