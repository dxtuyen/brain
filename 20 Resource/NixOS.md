# NixOs
---
## Command Etc
- Câu lệnh tải thông tin mới nhất từ máy chủ Nixos : 
	```bash
	# Bước 1: Cập nhật file khóa
	 nix flake update 
	# Bước 2: Dựng thử 
	nixos-rebuild dry-build --flake . 
	# Bước 3: Xem danh sách thay đổi dạng trực quan 
	nix-shell -p nvd --run "nvd diff /run/current-system ./result" 
	# Bước 4: Chuyển sang hệ thống mới (nếu bước 3 thấy hợp lý) 
	sudo nixos-rebuild switch --flake .
	```
- Cách update lotus
	- 