# Phiếu QC 1 — Road v1.0

Lô được kiểm (học viên): nguyenvandai        Người kiểm (học viên): nguyenquocvuong  
Ngày: 2026-11-20                              Phiên bản guideline: Road v1.0  
File được kiểm (tên + `revision` trong manifest): nguyenvandai-front.zip, nguyenvandai-fisheye.zip (revision 1)  
Số ảnh kiểm: 20 ảnh bắt buộc (A01–A12, B01–B08) (+ 8 ảnh thêm A13–A16, B09–B12, ghi riêng, không tính vào bảng dưới)   Số nhãn đã kiểm (shape + tag): 201 (121 shape + 80 tag)  

## Tổng hợp theo mã
| Mã | Loại lỗi | Số mục kiểm | Số lỗi | Mức |
| --- | --- | ---: | ---: | --- |
| QC1-01 tag camera | sai thuộc tính / bỏ sót | 20 | 0 | nặng |
| QC1-02 đủ L1, R1 | bỏ sót | 40 | 0 | nặng |
| QC1-03 position | sai thuộc tính / thừa | 34 | 0 | nặng |
| QC1-04 tâm vạch, chiều, điểm dừng | sai phạm vi / bỏ sót | 34 | 0 | chính |
| QC1-05 vạch đứt, che | sai phạm vi / sai thuộc tính | 34 | 0 | chính |
| QC1-06 style, color, kind | sai thuộc tính | 34 | 0 | chính |
| QC1-07 vùng lái | sai phạm vi / bỏ sót / thừa | 53 | 0 | chính |
| QC1-08 đèn, màu | bỏ sót / sai phạm vi / sai thuộc tính | 17 | 0 | nặng / chính |
| QC1-09 facing, type, group, biển phụ | sai thuộc tính | 34 | 0 | chính |
| QC1-10 hình in, đủ biển | bỏ sót / sai phạm vi | 17 | 0 | chính |
| QC1-11 fisheye | sai phạm vi / sai thuộc tính | 20 | 0 | chính |
| QC1-12 file | lỗi file | 2 | 0 | nhẹ / nặng |

Cách đếm số mục kiểm (đếm từ file của Đại, chỉ 20 ảnh bắt buộc): QC1-01 = số tag camera; QC1-02 = 20 ảnh × 2 vạch (L1, R1); QC1-03/04/05/06 = 34 lane; QC1-07 = 24 drivable + 11 crosswalk + 18 road_curb; QC1-08 = 17 đèn; QC1-09 = 17 đèn + 17 biển; QC1-10 = 17 biển; QC1-11 = 20 shape trên ảnh fisheye; QC1-12 = 2 file.

## Danh sách lỗi (mỗi lỗi một dòng)
| # | Mã | Ảnh | Nhãn (label, id) | Mức | Mô tả ngắn |
| --- | --- | --- | --- | --- | --- |
| — | — | — | — | — | Không ghi nhận lỗi nào. |

Cảnh báo của `road_check lint` đã xem xét và xác định là báo nhầm (người kiểm đã mở ảnh đối chiếu):
- QC1-04 (điểm đầu cao hơn điểm cuối): A06, A08, A11 (2 lane).
- QC1-05 (2 polyline cùng `position`): A01 (L1 và L2), A04, A09, A11.
- QC1-02 (thiếu L1/R1): xem mục "Ca mơ hồ" bên dưới.

## Ca mơ hồ
| Ảnh | Câu hỏi cho lead | Lời đáp (nếu có) |
| --- | --- | --- |
| A05 | Ảnh không có vạch sơn, không có L1 và R1. Xác nhận được miễn QC1-02? | Người kiểm đã xem ảnh: không có vạch ở phía đó, nên không phải lỗi bỏ sót. Chưa có xác nhận của coach. |
| A06 | Không thấy vạch ở phía L1. Xác nhận được miễn QC1-02? | Người kiểm đã xem ảnh: không có vạch ở phía đó, nên không phải lỗi bỏ sót. Chưa có xác nhận của coach. |
| A07 | Không thấy vạch ở phía L1. Xác nhận được miễn QC1-02? | Người kiểm đã xem ảnh: không có vạch ở phía đó, nên không phải lỗi bỏ sót. Chưa có xác nhận của coach. |
| A10 | Không thấy vạch ở phía R1. Xác nhận được miễn QC1-02? | Người kiểm đã xem ảnh: không có vạch ở phía đó, nên không phải lỗi bỏ sót. Chưa có xác nhận của coach. |

## Quyết định
Lỗi nặng: 0   Lỗi chính: 0 / 201 nhãn = 0 %   Lỗi nhẹ: 0   Ca chờ lead: 0 (4 ca QC1-02 ở A05, A06, A07, A10 đã được người kiểm xem ảnh và xác định là không có vạch; chưa có xác nhận của coach)  
Quyết định (Release / Hold / Rework): Release  
Lý do (theo luật của phiếu): không có lỗi nặng, tỉ lệ lỗi chính 0 % (≤ 5 %). Người kiểm đã mở ảnh đối chiếu: các cảnh báo QC1-04 và QC1-05 là báo nhầm, và 4 cảnh báo QC1-02 (A05, A06, A07, A10) là do ảnh không có vạch kẻ làn ở phía đó, nên không phải lỗi bỏ sót. Lưu ý: đặc tả bàn giao yêu cầu coach xác nhận các ảnh này; hiện chưa có xác nhận. Nếu coach cho rằng có vạch thì quyết định đổi thành Rework.  

Loại lỗi: bỏ sót = thiếu nhãn phải có; thừa = gán cái không phải đối tượng; sai phạm vi = hình lệch, sai chiều, dừng sai chỗ, tràn vùng. Ba loại này theo cách chia lỗi gán nhãn của ISO/IEC 5259-4 (mục 8.4.2); "sai thuộc tính" và "lỗi file" là khóa học thêm. Cách xếp mức: thang mức lỗi QC 1 Road v1.0 (docs/qc_severity_road_v1.0.md trong repo của lab).
