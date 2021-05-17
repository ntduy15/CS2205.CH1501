Bài báo: https://openaccess.thecvf.com/content_cvpr_2018/papers_backup/Zhao_HSA-RNN_Hierarchical_Structure-Adaptive_CVPR_2018_paper.pdf
1. Bài toán mà bài báo giải quyết là gì? Minh hoạ input/output (tìm hình ảnh có trong bài báo để minh hoạ)

- Input: một đoạn video.
- Output: tóm tắc phân đoạn các cảnh quay.
- Đánh giá cách tiếp cận được đề xuất trên bốn tập dữ liệu phổ biến, tức là SumMe, TVum, CoSum và VTW.

![image](https://user-images.githubusercontent.com/80680544/118486219-8d861a80-b743-11eb-9dd3-21c23eb206c1.png)

2. Các câu hỏi đặt ra là gì? Đã giải quyết được đến đâu?
- Các câu hỏi đặt ra:
    - Làm cách nào để biết mà phân cảnh quay?
    - Nó có làm mất hay làm giảm chất lượng của video kết quả không?
    - Nó có nhanh không?
 
- Đã giải quyết: Trong khi một số phương pháp tóm tắt hiện có chú ý đến quy trình phân đoạn cảnh quay. Chúng tạo ra các cảnh quay bằng một số chiến lược tầm thường, chẳng hạn như phân đoạn độ dài cố định, có thể phá hủy cấu trúc phân cấp cơ bản của dữ liệu video và làm giảm hơn nữa chất lượng của các bản tóm tắt đã tạo.

3. Ý tưởng giải quyết là gì? Minh hoạ trực quan
- Để giải quyết vấn đề này trên, chúng tôi đề xuất phương pháp tóm tắt video có cấu trúc tích hợp phân đoạn cảnh quay và tóm tắt video thành Structure-Adaptive RNN, ký hiệu là HSA-RNN.
