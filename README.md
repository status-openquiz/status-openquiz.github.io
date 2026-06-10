# status-openquiz.github.io

{
            "id": "20260603-api-down",
            "title": "API không phản hồi",
            "status": "resolved",
            "severity": "critical",
            "message": "Backend API bị quá tải do lưu lượng tăng đột biến. Đã scale lại hạ tầng và khôi phục dịch vụ.",
            "started_at": "2026-06-03T14:20:00+07:00",
            "resolved_at": "2026-06-03T15:45:00+07:00"
        },
        {
            "id": "20260520-slow-quiz",
            "title": "Tạo quiz chậm bất thường",
            "status": "resolved",
            "severity": "minor",
            "message": "Provider AI phản hồi chậm khiến thời gian tạo quiz kéo dài. Đã chuyển sang provider dự phòng.",
            "started_at": "2026-05-20T09:00:00+07:00",
            "resolved_at": "2026-05-20T11:30:00+07:00"
        }


Field	Bình thường	Đang có lỗi
status (root)	"operational"	"outage" hoặc "degraded"
incidents[].status	"resolved"	"investigating" / "identified" / "monitoring"
incidents[].resolved_at	timestamp	null
Các giá trị status root:

operational — hoạt động bình thường
degraded — một số dịch vụ bị ảnh hưởng
outage — sự cố nghiêm trọng, không truy cập được
Các giá trị incidents[].status:

investigating — đang điều tra
identified — đã xác định nguyên nhân
monitoring — đã vá, đang theo dõi
resolved — đã giải quyết


Có 3 mức severity:

Value	Màu hiển thị	Ý nghĩa
"minor"	Xám	Sự cố nhỏ, ít ảnh hưởng
"major"	Vàng	Sự cố đáng kể, một số tính năng bị ảnh hưởng
"critical"	Đỏ	Sự cố nghiêm trọng, toàn bộ hệ thống bị ảnh hưởng
Trong status.json hiện tại chưa dùng "major" lần nào cả.