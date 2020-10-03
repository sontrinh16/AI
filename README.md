# search

1. Bài 1
Sử sụng DFS
    - Khởi tạo result lưu kết quả 
    - visited lưu những node đã thăm 
    - stack là một hàng xếp lưu những node sẽ duyệt
- Lấy trạng thái ban đầu đưa vào stack
    - start = (problem.getStartState(), [])
    - stack.push(start)

- Duyết cho đến khi stack rỗng
    - Pop một node ra khỏi stack để xét
    - Kiểm tra xem có phải trạng thái đích không nếu có thì lưu vào result.
    - Không thì duyệt các node con của node đang xét nếu chưa có trong visited, push các node này vào stack
- Trả về kết quả

2. Bài 2
- Sử sụng BFS
    - Khởi tạo result lưu kết quả 
    - visited lưu những node đã thăm 
    - queue là một hàng đợi lưu những node sẽ duyệt
- Lấy trạng thái ban đầu đưa vào queue
    - start = (problem.getStartState(), [])
    - queue.update(start)

- Duyết cho đến khi queue rỗng
    - Pop một node ra khỏi queue để xét
    - Kiểm tra xem có phải trạng thái đích không nếu có thì lưu vào result.
    - Không thì duyệt các node con của node đang xét nếu chưa có trong visited, update các node này vào queue
- Trả về kết quả

3. Bài 3
Sử dụng uniform cost search. Tương tự với bài 2 nhưng sử dụng priority queue để lưu các node sẽ xét. Và priority queue này xét độ ưu tiên trên cost để đi đến các node đó, hàm cost được tính dựa trên cost trên node hiện tại cộng với cost tới node kế nó. Sau đó ta vẫn update p_queue như bài 2 chỉ khác là thêm thuộc tính cost vào trong node

4. Bài 4
Sử dụng A*. Cũng tương tự Uniform cost search nhưng chỉ khác ở phần tính cost bằng cách sử dụng kết quả của hàm heuristic đã định nghĩa cộng thêm vào cost để tối ưu hơn so với UCS

5. Bài 5
Setting cho bài toán cách phát hiện pacman liệu đã đi đến 4 góc hay chưa

6. Bài 6
Tối ưu hóa A* cho bài toán đi đến 4 góc nhanh nhất. Ta tối ưu nó bằng cách thiết kế hàm heuristic tính toán khoảng cách mahattan giữa các node trong path với vị trí các góc và trả về giá trị khoảng cách mahattan lớn nhất
