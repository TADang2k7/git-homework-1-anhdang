bài 1
touch week2.md
git add .
git commit -m “btap tuan 2”
git log –oneline
git branch week2
git checkout week2
echo “1” >  week2.md
git add .
git commit -m “working1”
echo “2” >> week2.md
git add .
git commit -m “working2”
echo “thay doi” >> week2.md
git add .
git commit -m “thay doi”
git checkout main
cat week2.md
khi chuyển về nhánh main thì ko còn chứa các dòng đã thêm ở nhánh week2 tệp trở về trạng thái bạn đầu khi vừa đc commit ở main git đã cô lập hoàn toàn ko gian làm việc của 2 nhánh
git checkout -b week2b
git merge --no-ff week2 -m "merge nhánh week2 vào week2b theo 3 - way merge"
git branch -d week2

bài 2
git checkout -b wip
echo “lam viec” > wip.txt
git add .
git commit -m “lm tren nhanh wip”
git checkout main
git merge week2
git branch –merged >> week2.md
git branch --no-merged >> week2.md
git branch -d week2b
git checkout wip 
git branch -m work-in-progress
git push -u origin work-in-progress 

bài 3
git checkout work-in-progress 
echo "Update" >> wip.txt
git add .
git commit -m “update”
git branch -vv
git push origin work-in-progress

bài 4
git checkout main 
git checkout -b experiment 
echo "Feature 1 experiment" > exp1.txt 
git add .
git commit -m “add exp1.txt”
echo "Feature 2 experiment" > exp2.txt 
git add .
git commit -m “add exp2.txt”
git checkout main 
echo "Update from main branch" > main_update.txt 
git add .
git commit -m “update”
git checkout experiment 
git rebase main
nano week2.md
git checkout main
git merge experiment
git add .
git commit -m "Finalize week2 report and rebase documentation" 
git push origin main
