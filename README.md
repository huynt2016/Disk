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

##II.Phân vùng hệ thống
