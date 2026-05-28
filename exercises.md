# Phan 2 - Bai Tap Mo Rong

## Bai tap 2.1 - Do nhay cua Temperature

**Ban nhan thay quy luat gi qua bon phan hoi?**

Khi temperature thap nhu 0.0, cau tra loi thuong on dinh, ngan gon va it bat ngo hon. Khi tang len 0.5, 1.0 va 1.5, phan hoi co xu huong da dang, sang tao va co cach dien dat phong phu hon, nhung temperature qua cao cung de lam cau tra loi lan man hoac kem nhat quan.

**Ban se dat temperature bao nhieu cho chatbot ho tro khach hang, va tai sao?**

Toi se dat temperature khoang 0.2 den 0.4 cho chatbot ho tro khach hang. Muc nay giup chatbot van tu nhien khi tra loi, nhung uu tien do chinh xac, nhat quan va tranh dua ra thong tin qua sang tao trong tinh huong can ho tro nguoi dung.

## Bai tap 2.2 - Danh doi Chi phi

**Uoc tinh xem GPT-4o dat hon GPT-4o-mini bao nhieu lan cho workload nay:**

Workload moi ngay co 10,000 nguoi dung * 3 lan goi = 30,000 lan goi API. Moi lan trung binh 350 token, tong cong khoang 10,500,000 token/ngay. Neu gia su chia gan dung theo ty le input/output tu bang gia trong `template.py`, GPT-4o co don gia cao hon GPT-4o-mini khoang 33.33 lan cho ca input va output, vi `5.00 / 0.150 = 33.33` va `20.00 / 0.600 = 33.33`.

**Mo ta mot truong hop ma chi phi cao hon cua GPT-4o la xung dang, va mot truong hop GPT-4o-mini la lua chon tot hon:**

GPT-4o xung dang khi tac vu can lap luan phuc tap, do chinh xac cao, xu ly yeu cau mo hoac anh huong lon den trai nghiem/ket qua kinh doanh, vi chat luong phan hoi quan trong hon chi phi moi request. GPT-4o-mini phu hop hon cho tac vu lap lai, khoi luong lon, hoi-dap don gian, phan loai, tom tat ngan hoac chatbot ho tro cap mot, noi chi phi va toc do la uu tien lon.

## Bai tap 2.3 - Trai nghiem Nguoi dung voi Streaming

Streaming quan trong nhat khi cau tra loi dai, nguoi dung dang cho tuong tac truc tiep, hoac ung dung can tao cam giac phan hoi ngay lap tuc nhu chatbot, tro ly lap trinh, viet noi dung dai va giai thich tung buoc. Non-streaming phu hop hon khi cau tra loi ngan, can xu ly tron goi truoc khi hien thi, can validate/format ket qua thanh JSON, bang du lieu hoac mot ket qua ma ung dung chi nen hien thi khi da hoan tat.

## Danh sach Kiem tra Nop Bai

- [x] Tat ca tests pass: `pytest tests/ -v`
- [x] `call_openai` da trien khai va kiem thu
- [x] `call_openai_mini` da trien khai va kiem thu
- [x] `compare_models` da trien khai va kiem thu
- [x] `streaming_chatbot` da trien khai va kiem thu
- [x] `retry_with_backoff` da trien khai va kiem thu
- [x] `batch_compare` da trien khai va kiem thu
- [x] `format_comparison_table` da trien khai va kiem thu
- [x] `exercises.md` da dien day du
- [x] Sao chep bai lam vao folder `solution-code` voi file `solution.py`
