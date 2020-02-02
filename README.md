OOP Review

1. Lập trình hướng đối tượng có 4 tính chất quan trọng sau :
- Tính kế thừa : là khả năng xây dựng lớp mới dựa trên những lớp có sẵn ( quan hệ cha con ). Lớp ban đầu được gọi là lớp cha, lớp kế thừa lớp ban đầu là lớp con. Lớp con có thể bổ sung thêm các chức năng ( phương thức ) và các thành phần ( thuộc tính ) mới .
VD : từ đối tượng "xe" bạn có thêm phát triển thêm các lớp khác như "xe đạp" , "xe máy",....
- Tính đóng gói và che giấu dữ liệu : tính chất này thể hiện ở chỗ không cho người sử dụng các đối tượng thay đổi các thuộc tính nội tại của các đối tượng. Chỉ các phương thức nội tại ( trong code ) mới thay đổi được nó . 
- Tính trừu tượng hóa : là bỏ qua các đặc điểm chung của các đối tượng để làm nổi bật nên các đặc điểm riêng của từng đối tượng.
-  Tính đa hình : bạn có thể hiểu khi 1 đối tượng kế thừa ( extend ) hay thực hiện 1 hành vi của 1 interface ( implement ) thì đối tượng đó của chính là class mà ta kế thừa và cũng chính là interface mà đối tượng đó thực hiện.
Ví dụ:
Tạo abstract class Animal có phương thức sayHello. abstract class này thể hiện tính trừu tượng, có nghĩa ta định ra rằng dù là con vật gì đi nữa thì nó cũng có phương thức sayHello.
Tạo 2 lớp Cat và Dog kế thừa từ Animal. Khi khởi tạo chúng sẽ có tên. Chúng override lại phương thức sayHello để chào hỏi theo cách riêng của chúng. Điều này thể hiện tính đóng gói (đóng gói biến tên và phương thức sayHello với nhau) và tính thừa kế (Cat và Dog mang đặc điểm chung là có sayHello từ Animal).
Tạo lớp Zoo để quản lí nhiều Animal, có (1) phương thức add, remove để thêm, bớt các Animal (các đối tượng của các lớp thừa kế từ Animal), (2) phương thức showListAnimal để gọi sayHello của tất cả đối tượng nó quản lí. Điều này thể hiện tính đa hình, Zoo gọi chỉ gọi một phương thức sayHello, nhưng tùy con vật mà lời chào hỏi sẽ khác nhau.

2. Lợi ích của việc sử dụng đối tượng:
Để làm nổi bật được lợi thế của lập trình hướng đối tượng tớ sẽ so sánh nó với "lập trình thủ tục".
- Lập trình hướng đối tượng là 1 khái niệm mới nên hầu hết chúng ta ai cũng sẽ đi qua lập trình hướng thủ tục trước sau đó mới học lập trình hướng đối tượng.
- Lập trình hướng thủ tục : hướng theo các chức năng.Lập trình hướng thủ tục chia 1 chương trình ( 1 chức năng lớn ) thành các hàm chức năng nhỏ hơn.Các hàm là độc lập với nhau.
-> Việc phát triển 1 chương trình hướng thủ tục rất khó cũng như việc làm theo teamwork cũng thế do không có đối tượng cụ thể nếu muốn sử dụng từng hàm chức năng riêng biệt giữa các file dữ liệu trong chương trình khó khăn, không dễ hình dung trực quan -> nếu có 1 khái niệm mới đưa những thứ trực quan như đời thường vào trong code thì lập trình viên sẽ dễ dàng cho lập trình viên hơn rất nhiều.

3. Sử dụng interface
- Interface : Khi bạn muốn tạo dựng một bộ khung chuẩn gồm các chức năng mà những module hay project cần phải có. Giống như sau khi nhận requirement của khách hàng về team ngồi với nhau và phân tích các đầu mục các tính năng của từng module, sau đó triển khai vào code viết các interface như đã phân tích,để các bạn dev có thể nhìn vào đó để thực hiện đủ các tính năng (khi đã implement rồi thì không sót một tính năng nào).

4. Sử dụng abstract class:
- Abstract class: Giống như demo trên bạn có thể hiểu khi định nghĩa một đối tượng có những chức năng A,B,C trong đó tính năng A,B chắc chắn sẽ thực thi theo cách nào đó, còn tính năng C phải tùy thuộc vào đối tượng cụ thể là gì, như đối tượng Dog, Cat tuy chúng đều có thể phát ra âm thanh nhưng âm thanh là khác nhau. Vì vậy method Speak() là abstract method để chỉ ra rằng tính năng này còn dang dở chưa rõ thực thi, các lớp extend phải hoàn thành nốt tính năng này, còn những tính năng đã hoàn thành vẫn sử dụng như bình thường đây là những tính năng.

5. Nạp chồng (Overloading): Đây là khả năng cho phép một lớp có nhiều thuộc tính, phương thức cùng tên nhưng với các tham số khác nhau về loại cũng như về số lượng. Khi được gọi, dựa vào tham số truyền vào, phương thức tương ứng sẽ được thực hiện.

6. Ghi đè (Overriding): là hai phương thức cùng tên, cùng tham số, cùng kiểu trả về nhưng thằng con viết lại và dùng theo cách của nó, và xuất hiện ở lớp cha và tiếp tục xuất hiện ở lớp con. Khi dùng override, lúc thực thi, nếu lớp Con không có phương thức riêng, phương thức của lớp Cha sẽ được gọi, ngược lại nếu có, phương thức của lớp Con được gọi.
Giả sử chúng ta có một lớp định nghĩa phương thức Cộng:
 public class Demo{
  public int Cong(int x, int y) {
    return x + y;
  }

  public string Cong(string s1, string s2) {
    return s1.Concat(s2);
  }
}
   Hai phương thức Cong định nghĩa trong cùng lớp là đặc điểm khác biệt thứ hai giữa Overloading và Overriding.

7. Các access modifier trong java: public, private, protected.
- Public: có thể truy cập ở mọi nơi-trong class, class con, các class ngoài package.
- Private: Chỉ trong class đó mới truy cập được.
- Protected: Truy cập trong class của nó và trong 1 package. Ngoài ra, các class con ở ngoài package cũng có thể truy cập được.
