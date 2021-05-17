Bài báo: https://openaccess.thecvf.com/content_cvpr_2018/papers_backup/Zhao_HSA-RNN_Hierarchical_Structure-Adaptive_CVPR_2018_paper.pdf

**1. Bài toán mà bài báo giải quyết là gì? Minh hoạ input/output (tìm hình ảnh có trong bài báo để minh hoạ)**

- Input: một đoạn video.
- Output: tóm tắc phân đoạn các cảnh quay.
- Đánh giá cách tiếp cận được đề xuất trên bốn tập dữ liệu phổ biến, tức là SumMe, TVum, CoSum và VTW.

![image](https://user-images.githubusercontent.com/80680544/118486219-8d861a80-b743-11eb-9dd3-21c23eb206c1.png)

**2. Các câu hỏi đặt ra là gì? Đã giải quyết được đến đâu?**
- Các câu hỏi đặt ra:
    - Làm cách nào để biết mà phân cảnh quay?
    - Nó có làm mất hay làm giảm chất lượng của video kết quả không?
    - Nó có nhanh không?
 
- Đã giải quyết: Trong khi một số phương pháp tóm tắt hiện có chú ý đến quy trình phân đoạn cảnh quay. Chúng tạo ra các cảnh quay bằng một số chiến lược tầm thường, chẳng hạn như phân đoạn độ dài cố định, có thể phá hủy cấu trúc phân cấp cơ bản của dữ liệu video và làm giảm hơn nữa chất lượng của các bản tóm tắt đã tạo.

**3. Ý tưởng giải quyết là gì? Minh hoạ trực quan**
- Để giải quyết vấn đề này trên, chúng tôi đề xuất phương pháp tóm tắt video có cấu trúc tích hợp phân đoạn cảnh quay và tóm tắt video thành Structure-Adaptive RNN, ký hiệu là HSA-RNN.

**Hình 1:**

![image](https://user-images.githubusercontent.com/80680544/118486219-8d861a80-b743-11eb-9dd3-21c23eb206c1.png)

Figure 1. The diagram of the proposed HSA-RNN, where Layer 1
and Layer 2 are designed to exploit the video structure and generate the video summary, respectively. Specifically, the blue and red
boxes represent the bidirectional LSTM unit in each layer. The
dashed boxes indicate the locations of detected shot boundaries.
The bidirectional LSTM in Layer 1 operates in a sliding manner,
and the stride at each step is equal to the length of previous detected shot.

**Hình 2:**

![image](https://user-images.githubusercontent.com/80680544/118488118-9d9ef980-b745-11eb-9bc6-26efc1aaeb68.png)

Figure 2. The comparison between the long single LSTM and sliding bidirectional LSTM on shot boundary detection. Compared to  the long single LSTM, the sliding bidirectional LSTM is much shorter, which can mitigate the vanishing gradient problem by avoiding  extremely long temporal dependency exploitation. Moreover, it can capture both the forward and backward information. Note that the blue  boxes denote the LSTM units, and the dashed boxes indicate the locations of detected shot boundaries.
