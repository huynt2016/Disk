# Cấu trúc ổ đĩa
##I.Cấu trúc
###1.Khái niệm cơ bản:

- Ổ cứng là nơi lưu trữ dữ liệu của máy tính.

###2.Cấu trúc ổ đĩa cứng:

- Cấu trúc của ổ cứng bao gồm nhiều đĩa từ (Plalters) được xếp song song và đồng trục với nhau, như hình sau:

<img src="http://i.imgur.com/jAkjtyK.png">

- Chú thích:
<ul>
  <li>Plalters: Các đĩa từ</li>
  <li>Spindle: Trục quay</li>
  <li>Heads: Các đầu đọc/ghi đĩa</li>
  <li>Head actuator arm: Cần đi chuyển đầu đọc</li>
</ul>

###3.Đơn vị tổ chức dữ liệu ổ đĩa:
####a.Sector:
- Sector là đơn vị lưu trữ nhỏ nhất trong ổ đĩa.
- Dung lượng của 1 sector là 512 bytes.

<img src="http://i.imgur.com/2PyeueX.png">

- Ngoài Sectors thì ổ đĩa còn có Blocks là một loại đơn vị tổ chức dữ liệu
<ul>
  <li>Thông thường thì 1 Block = 2 Sector = 1024 bytes.</li>
</ul>

####b.Track:
- Tracks là tập hợp của các sector đồng tâm có trên Plalter.

<img src="http://i.imgur.com/vskO8IM.png">

- Dung lượng của Track tùy thuộc vào bán kính của nó.
- **Như vậy:**
*Dung lượng của ổ đĩa = Số Plalter * Số Track * Giá trị trung bình Track ở giữa*

####c.Cylinder
- Cylinder là tập hợp của các Track có cùng bán kính trên các Plalter

<img src="http://i.imgur.com/Dy4qSGd.png">

##II.Các câu lệnh hay dùng
- `fdisk`: Hiển thị các phân vùng và các chi tiết như kiểu hệ thống tập tin. Tuy nhiên nó không báo cáo kích thước của mỗi phân vùng.
- `sfdisk`: Sfdisk là một tiện ích với một mục đích tương tự như fdisk, nhưng với nhiều tính năng hơn. Nó có thể hiển thị kích thước của mỗi phân vùng.
- `cfdisk`: Cfdisk là một trình soạn thảo phân vùng linux với một giao diện người dùng tương tác dựa trên kernel. Nó có thể được sử dụng để ra khỏi danh sách các phân vùng hiện có cũng như tạo ra hoặc chỉnh sửa chúng.
- `parted`: Hiển thị danh sách các phân vùng và thay đổi chúng nếu cần thiết. 
- `df`: Hiển thị thông tin chi tiết về hệ thống tập tin.
- `pydf`: Phiên bản cải tiến của df, viết bằng python. In ra tất cả các phân vùng đĩa cứng một cách dễ đọc hơn.
- `lsblk`: Liệt kê ra tất cả các khối lưu trữ, trong đó bao gồm các phân vùng đĩa và ổ đĩa.
- `blkid`: In các thiết bị khối (phân vùng và phương tiện lưu trữ) các thuộc tính như kiểu uuid và tập tin hệ thống.
- `HWiNFO`: Là một công cụ thông tin phần cứng nói chung có thể được sử dụng để in ra ổ đĩa và danh sách phân vùng.

##III.Tham khảo
- http://www.binarytides.com/linux-command-check-disk-partitions/
