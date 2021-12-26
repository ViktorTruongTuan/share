# share
Qui trình sử dụng git


1.	Clone repository
git clone <http://………>
cd <project_>
2.	Switch branch
git checkout <branch_name>
3.	Push Code
git add .
git commit -m “<message>”
git push -u origin <branch_name>
4.	Pull Code
git pull
5.	Merge Code
•	Để merge một branch bất kì vào branch hiện tại :
o	$   git merge <branch_name>
•	Giả sử đang ở branch master, muốn merge branch task1 vào branch master thì làm như sau:
o	$ git checkout task1
o	$ git pull
o	$ git checkout master
o	$ git merge task1
•	Giả sử đang ở branch task1, muốn merge branch task2 vào branch master thì làm như sau.
o	$ git checkout master
o	$ git merge task2
•	Xử lý conflict:
o	Vào Visual Studio → Git change → Unmerged change
o	Nhấp đúp vào những file conflict
o	Nếu biết rõ cần phần nào thì chọn không thì chọn cả 2 sau đó command lại những phần bị trùng
•	Sau khi xử lí conflict:
o	Chạy thử xem mọi thứ oke không? Nếu oke thì push code lên nhánh hiện tại
6.	Git Tags
Trong Git có hai kiểu tag chính đó là:
•	Lightweight Tag: Các tag này chỉ đơn thuần là đánh dấu snapshot của commit.
•	Annotated Tag: Với tag này, bạn có thể đặt tiêu đề cho tag, và khi xem nó sẽ có thông tin về người tag, ngày tag,….
	Create Lightweight Tag
		git tag <Tên tag>
	Create Annotated Tag
		git tag -a <Tên tag> -m “nội dung commit”
	Xem danh sách tag
		git tag
	Xem thông tin Tag
		shit show <Tên tag>
	Thêm tag cho các commit cũ
		git log –pretty=oneline (xem log)
		git tag -a <Tên tag> <Mã checksum trong log> -m “Nội dung commit”
	Push tag
		git push –tags 
	Nhập tag vào branch( chuyển từ tag thành branch)
		git checkout -b <Tên branch> <Tên tag>

