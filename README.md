Báo cáo lần 1

Giảng viên hướng dẫn: Thầy Ngô Văn Linh
Sinh viên: Vũ Tuấn Kiệt, mssv: 20200308
Chủ đề: Music Recommendation Engine
A. Tìm hiểu bài toán
-Hệ thống gợi ý (Recommender systems hoặc Recommendation systems) là một dạng của hệ hỗ trợ ra quyết định, cung cấp giải pháp mang tính cá nhân hóa mà không phải trải qua quá trình tìm kiếm phức tạp. Hệ gợi ý học từ người dùng và gợi ý các sản phẩm tốt nhất trong số các sản phẩm phù hợp.

-Hệ thống gợi ý sử dụng các tri thức về sản phẩm, các tri thức của chuyên gia hay tri thức khai phá học được từ hành vi con người dùng để đưa ra các gợi ý về sản phẩm
mà họ thích trong hàng ngàn hàng vạn sản phẩm có trong hệ thống. Các website thương mại điện tử, ví dụ như sách, phim, nhạc, báo...
sử dụng hệ thống gợi ý để cung cấp các thông tin giúp cho người sử dụng quyết định sẽ lựa chọn sản phẩm nào. Các sản phẩm được gợi ý dựa trên số lượng sản phẩm đó đã được 
bán, dựa trên các thông tin cá nhân của người sử dụng, dựa trên sự phân tích hành vi mua hàng trước đó của người sử dụng để đưa ra các dự đoán về hành vi mua hàng trong 
tương lai của chính khách hàng đó. Các dạng gợi ý bao gồm: gợi ý các sản phẩm tới người tiêu dùng, các thông tin sản phẩm mang tính cá nhân hóa, tổng kết các ý kiến cộng 
đồng, và cung cấp các chia sẻ, các phê bình, đánh giá mang tính cộng đồng liên quan tới yêu cầu, mục đích của người sử dụng đó.
B. Các phương pháp gợi ý
Giả sử rằng I là tập các đối tượng (Item) có thể được gợi ý, U là tập người dùng, u là một người dùng cụ thể trong tập U và i là một đối tượng cụ thể trong I mà chúng ta muốn dự đoán cho u (dựa vào sở thích của u).
Phương pháp gợi ý:Dữ liệu cơ sở	Dữ liệu đầu ra	Tiến trình xử lý
-Dựa theo lọc cộng tác:	
+ Dữ liệu cơ sở: Các điểm số đánh giá của những người sử dụng trong U đối với các đối tượng trong I.	
+ Dữ liệu đầu ra: Các điểm số đánh giá của u cho các đối tượng trong I.	
+ Tiến trình xử lý: Nhận ra người sử dụng trong U tượng tự với u ( về sở thích) và sau đó ngoại suy điểm số đánh giá vủa u cho i.
- Dựa theo nội dung:
+ Dữ liệu cơ sở: Các đặc điểm của các đối tượng trong I
+ Dữ liệu đầu ra: Các điểm số đánh giá của u cho các đối tượng trong I
+ Tiến trình xử lý: Tạo ra một mô hình mô tả sở thích của người sử dụng u, sau đó sử dụng để đánh giá mức độ ưa thích của u với i
- Dựa trên cơ sở tri thức:
+ Các đặc điểm của các đối tượng trong I
+ Các tri thức (hiểu biết) về sự phù hợp giữa các đối tượng với nhu cầu của người sử dụng
+ Một sự mô tả nhu cầu và sở thích của người sử dụng u.	Suy luận sự phù hợp giữa I và nhu cầu của u.
Trong thời gian của Project 2, em sẽ tìm hiểu chủ yếu về gợi ý dựa theo nội dung và gợi ý dựa trên cơ sở tri thức

C. Hướng tiếp cận, giải quyết bài toán
Hệ thống Recommendation Music System là một hệ thống phân tích dữ liệu và máy học được thiết kế để đưa ra các khuyến nghị âm nhạc cho người dùng dựa trên lịch sử nghe nhạc của họ và hành vi truy cập trước đó. Kiến trúc chung của hệ thống Recommendation Music System có thể được mô tả như sau:

- Dữ liệu đầu vào: Dữ liệu đầu vào bao gồm thông tin về người dùng, bao gồm lịch sử nghe nhạc và hành vi truy cập trước đó, và thông tin về các bản nhạc, bao gồm thể loại, 
nghệ sĩ, album, lời bài hát, đánh giá của người dùng và các thông tin khác.
- Tiền xử lý dữ liệu: Dữ liệu đầu vào được tiền xử lý để chuẩn hóa và biểu diễn một cách thích hợp, bao gồm việc loại bỏ các giá trị thiếu và chuẩn hóa các giá trị số.
- Mô hình hóa: Dữ liệu được đưa vào các mô hình học máy để phân tích và dự đoán các mối quan hệ giữa các bản nhạc và người dùng
- Đánh giá và tinh chỉnh: Hệ thống được đánh giá dựa trên độ chính xác của các khuyến nghị được đưa ra, và được điều chỉnh dựa trên phản hồi của người dùng để cải 
thiện chất lượng các khuyến nghị được đưa ra.
- Đầu ra: Hệ thống đưa ra các khuyến nghị âm nhạc cho người dùng dựa trên các mô hình học máy và các thông tin về lịch sử nghe nhạc và hành vi truy cập trước đó của 
người dùng. Khuyến nghị có thể được đưa ra thông qua giao diện người dùng, email, hoặc các kênh khác.

Cụ thể hơn:
- Dữ liệu đầu vào: Em sẽ sử dụng hàm spotipy để lấy API từ Spotify, crawl dữ liệu từ Spotify về. Các bài hát sẽ bao gồm tên bài hát, nghệ sĩ, album, và có thể có thêm 
1 số thông tin về audio features, genres và lời bài hát
Sẽ có 1 hệ thống rating cho người dùng, dự kiến sẽ gồm 2 phần: Theo audio features và lời bài hát
- Mô hình hóa, ở đây mình sẽ có 2 phương thức gợi ý cùng là content-based: Đó là gợi ý theo audio features và lời bài hát
+ Gợi ý theo audio features: Gợi ý theo audio features sử dụng cosine similarity là một cách thực hiện Content-based Filtering (CBF) trong hệ thống. Trong đó, cosine 
similarity được sử dụng để đo độ tương đồng giữa các bản nhạc dựa trên các đặc trưng âm thanh của chúng
+ Cosine similarity là một phương pháp đo độ tương đồng giữa hai vector trong không gian nhiều chiều (multidimensional space). Nó được tính bằng cách tính cosin của góc
giữa hai vector.
Giá trị của cosine similarity nằm trong khoảng [-1, 1]. Nếu cosine similarity bằng 1 thì hai vector giống nhau hoàn toàn, nếu bằng 0 thì hai vector không tương đồng 
với nhau, và nếu bằng -1 thì hai vector tương đối đối nghịch nhau.
+ Để gợi ý các bài hát dựa trên lời bài hát, ta có thể sử dụng kỹ thuật xử lý ngôn ngữ tự nhiên và phân tích tần suất từ sử dụng trong các bài hát. 
Một trong những phương pháp thông dụng là sử dụng TF-IDF (Term Frequency-Inverse Document Frequency).
TF-IDF được sử dụng để xác định tầm quan trọng của một từ trong một tài liệu hoặc một tập hợp các tài liệu. 
Đầu tiên, ta tính toán tần suất của từ đó trong văn bản (TF). Sau đó, ta tính toán trọng số IDFs (Inverse Document Frequencies) để đánh giá
tầm quan trọng của từ đó trong toàn bộ tập hợp các văn bản. Công thức tính toán TF-IDF như sau:
TF(t) = (Số lần từ t xuất hiện trong một bài hát) / (Tổng số từ trong bài hát)
IDF(t) = log_e(Tổng số bài hát / Số bài hát chứa từ t)
TF-IDF(t) = TF(t) * IDF(t)
Với TF-IDF, ta có thể tính toán trọng số của từng từ trong lời bài hát và lưu trữ chúng trong một ma trận. Sau đó, ta có thể sử dụng các kỹ thuật như cosine similarity
để tìm kiếm các bài hát có lời tương tự nhau và đưa ra các gợi ý dựa trên độ tương đồng của lời bài hát.

D. Lựa chọn công nghệ, cài đặt và kết quả
- Công nghệ: Spotipy, Cosine Similarity, TFIDF
- Kết quả: hiện tại em đang trong quá trình triển khai và đã hoàn toàn sơ bộ phần gợi ý theo audio features

D. Hướng phát triển:
- Sẽ phát triển thêm gợi ý theo lời bài hát
- Phát triển hệ thống có thêm gợi ý lọc cộng tác và gợi ý dựa trên cơ sở tri thức


