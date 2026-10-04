# Track 1 · Day 17 — Problem Interview Practice

> Case A: **AI Tutor – Diagnostic Refresher**

## 1. Thông tin cá nhân và nhóm

| Mục | Nội dung |
|---|---|
| MHV | 2A202602421 |
| Họ tên | Nguyễn Quang Huy |
| Tên nhóm | `[TODO: tên nhóm]` |
| Thành viên | Đỗ Lê Việt Anh (2A202602491), Nguyễn Thị Minh Khánh (2A202602546), Nguyễn Quang Huy (2A202602421), Lại Bá Quân (2A202602495) |
| Case đã chọn | **A. AI Tutor – Diagnostic Refresher**: nút "Tôi vẫn chưa hiểu", AI chẩn đoán lỗ hổng rồi cho ôn lại khái niệm nền |
| Đối tượng phỏng vấn | Người từng bị kẹt khi học trên VLearn trong 7 ngày gần đây |

Cấu trúc repo:

```
├── README.md
└── interview/
    ├── notes.md          # Interview Record, lượt mình làm interviewer
    └── recording-link.md # Link bản ghi đã được người được phỏng vấn đồng ý
```

---

## 2. Problem Hypothesis Brief (Chặng 1)

Nhóm chỉ được cung cấp solution. Phần dưới là chuỗi giả thuyết nhóm dựng ngược từ solution, để đi kiểm chứng. Đây chưa phải sự thật.

| Mắt xích | Giả thuyết |
|---|---|
| **Solution** | Khi người học bấm "Tôi vẫn chưa hiểu", AI hỏi vài câu để chẩn đoán khái niệm nền đang hổng, rồi đưa phần ôn ngắn cho đúng khái niệm đó. |
| **Change** | Người học tự gỡ được chỗ kẹt trong một buổi học, thay vì bỏ qua phần đó, chép đáp án hoặc bỏ dở bài. |
| **Actor** | Người tự học online, học một mình ngoài giờ, không có người để hỏi ngay lúc đó, chịu áp lực thời gian lớn. |
| **Situation & Job** | *Khi* đã đọc hoặc xem lại một khái niệm mới mà vẫn không hiểu, *tôi muốn* biết chính xác mình đang thiếu gì, *để* học tiếp được mà không mất cả buổi tra cứu. |
| **Pain** | (1) Không biết mình thiếu kiến thức gì nên không biết tìm từ khóa nào. (2) Tự chụp màn hình đẩy vào ChatGPT thì AI trả lời lan man, mất thời gian. (3) Áp lực thời gian khiến người học dễ nản chí bỏ qua. |
| **Evidence cần tìm** | Một lần kẹt cụ thể gần đây: đang học gì, đã thử những gì (workaround thật), kết quả ra sao (AI trả lời có đúng ý không), hậu quả của việc không hiểu bài. |

**Hai cách giải thích cạnh tranh:**

- **H1, giả thuyết đứng sau solution:** Người học kẹt chủ yếu vì **thiếu kiến thức nền** (prerequisite).
- **H2, giải thích thay thế:** Nền đủ, nhưng **cách trình bày hiện tại khó hiểu** (lan man, không đúng trọng tâm) hoặc do **cách người dùng prompt AI** chưa rõ ràng.

**Giả thuyết bị bác bỏ khi:** Phần lớn người được phỏng vấn gỡ được chỗ kẹt nhờ một cách giải thích khác (đổi prompt) chứ không nhờ học lại kiến thức cũ, hoặc họ chấp nhận việc AI thỉnh thoảng trả lời lan man mà không thấy đó là pain lớn.

---

## 3. Conversation Guide — phiên bản cuối (sau khi luyện)

### Big 3 — ba điều cần học

| # | Điều cần học | Nối với giả thuyết |
|---|---|---|
| 1 | Lần kẹt gần nhất diễn ra thế nào, và người học đã thực sự làm gì để xử lý (workaround thật) | Situation & Job, Pain |
| 2 | Khó khăn khi sử dụng các workaround (ChatGPT, Google) có thực sự do hổng kiến thức không | H1 và H2 |
| 3 | Mức độ nghiêm trọng của vấn đề (áp lực thời gian, tần suất lặp lại) | Pain có đủ lớn không |

### Kịch bản (~15 phút)

**Mở đầu (1–2 phút)**
- "Chào bạn, mình đang làm một bài tập nhỏ về thói quen học tập. Mình muốn nghe về trải nghiệm học của bạn gần đây. Không có câu trả lời đúng sai, mình chỉ muốn nghe câu chuyện thực tế của bạn thôi."
- "Mình xin phép ghi âm để làm tư liệu học tập nhé." → **chờ đồng ý rồi mới bật ghi âm.**

**Sàng lọc (1 phút)**
- "Trong 7 ngày qua, có lúc nào bạn học trên VLearn mà không hiểu một phần bài không?"
- "Lúc đó bạn có làm gì để xử lý không?" *(Nếu có thì đi tiếp)*

**Kể chuyện — Big 3 #1 (5–6 phút)**
- "Kể lại lần gần nhất bạn không hiểu bài: hôm nào, bài gì, đang học ở đâu?"
- "Chính xác thì phần nào khiến bạn không hiểu? Bạn nhận ra mình không hiểu từ lúc nào?"
- "Ngay sau đó bạn đã làm gì? Kể từng bước một (Ví dụ: Tra ChatGPT, ném raw text hay chụp slide?)."

**Đào nguyên nhân — Big 3 #2 (3–4 phút)**
- "Cách dùng công cụ đó có giúp bạn hiểu bài hơn không? Mất bao lâu thì bạn hiểu ra?"
- "Nhìn lại, bạn nghĩ việc mình không hiểu (hoặc AI trả lời không đúng ý) là do mình thiếu kiến thức nền, hay do AI khó hiểu/trình bày kém?"

**Chi phí — Big 3 #3 (2 phút)**
- "Lúc đó bạn có đang chịu áp lực gì không? (Ví dụ: khối lượng bài dài, phải học cả ngày sáng chiều)."
- "Chuyện này xảy ra thường xuyên đến mức nào?"

**Kết (1 phút)**
- "Cảm ơn bạn đã chia sẻ."

### Những câu đã bỏ / viết lại sau khi luyện

| Bản trước | Bản cuối | Vì sao sửa |
|---|---|---|
| "Giả sử có một nút để hỏi trợ giúp... Bạn cảm thấy thế nào?" | (Đã lược bỏ hoàn toàn) | Câu cũ vi phạm nguyên tắc Mom Test vì làm lộ (Pitch) solution, khiến user dự đoán tương lai thay vì kể sự thật quá khứ. |
| "Anh có ý thức được là do mình thiếu kiến thức hay là con chat nó trả lời bị khó hiểu không?" | "Nhìn lại, bạn nghĩ việc AI trả lời không đúng ý là vì nguyên nhân gì?" | Câu cũ mang tính mớm lời/dẫn dắt nguyên nhân (gợi ý H1). Câu mới mở hơn để user tự đánh giá. |

---

## 4. Practice Reflection (Chặng 4)

**1. Câu hỏi nào đã giúp user kể một tình huống cụ thể?**

Câu hỏi đào sâu về thao tác thực tế: *"Anh giải quyết vấn đề này như thế nào?"* đã giúp người dùng kể chi tiết hành động: *"copy content đấy vào chatgpt, có lúc cắt cái hình minh họa vào, chụp lại cả slide vào chatgpt"*.

**2. Chỗ nào mình cần làm tốt hơn ở lần phỏng vấn thật?**

Mình có xu hướng dẫn dắt nguyên nhân (mớm lời) thay vì để user tự nói. Ví dụ câu: *"Anh có ý thức được là do mình thiếu kiến thức hay là con chat nó trả lời bị khó hiểu không"* mang tính mớm lời khá rõ. Thay vào đó ở lần thật mình sẽ hỏi mở hơn: *"Theo anh, vì sao con chat lại trả lời không đúng ý anh lúc đó?"*.

**3. Sau khi luyện, nhóm đã sửa Conversation Guide ở đâu và vì sao?**

Nhóm đã lược bỏ hẳn phần (E) "Phản ứng với ý tưởng" (hỏi về nút trợ giúp AI) ra khỏi kịch bản phỏng vấn. Bài lab yêu cầu làm Problem Interview, nếu đưa ý tưởng giải pháp (Pitch solution) vào sẽ vi phạm nguyên tắc "The Mom Test" và làm người dùng đưa ra dự đoán thay vì sự thật. Đồng thời, sửa câu hỏi dẫn dắt nguyên nhân thành câu hỏi mở (đã liệt kê ở phần 3).

---

## 5. AI Support Log

| Bước | AI đã giúp gì | Điểm sai / hời hợt | Mình đã tự sửa thế nào |
|---|---|---|---|
| Chặng 1 | Gợi ý khung chuỗi Solution → Evidence và cấu trúc thư mục repo | Chưa bám sát được chính xác format bảng biểu chi tiết mà nhóm đã thống nhất | Lấy format bảng của nhóm làm chuẩn để đồng bộ |
| Chặng 2 & 3 | Gợi ý cách đặt câu hỏi theo Mom Test, bỏ đi câu Pitch Solution | - | Đã áp dụng để lược bỏ câu hỏi về "Nút trợ giúp" |
| Chặng 4 | Rút trích insights và exact quotes từ raw transcript phỏng vấn của mình | Không nghe được giọng điệu cảm xúc của user nên đánh giá có thể khô khan | Đã tự rà soát và bổ sung thêm context thực tế (áp lực thời gian học 2 buổi/ngày) vào notes |