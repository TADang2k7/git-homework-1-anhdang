1
2
thay doi
- **Bản chất của Git Rebase:** Rebase dời mốc gốc (base commit) của nhánh `experiment` tới đỉnh (tip) mới nhất của nhánh `main`.
- **Quá trình diễn ra:**
  1. Git tạm thời gỡ 2 commit của nhánh `experiment` ra một vùng lưu tạm.
  2. Git cập nhật nhánh `experiment` để lấy commit mới nhất từ `main` (`main_update.txt`).
  3. Git lần lượt "phát lại" (re-apply) từng commit của nhánh `experiment` lên trên đỉnh commit mới của `main`.
  4. Hai commit của `experiment` được tạo lại với commit hash hoàn toàn mới, biến lịch sử commit từ phân nhánh song song trở thành một đường thẳng tuyến tính (linear history).
EOF
