<div id="tieu-de">
  <h1>SA BÀN SỐ LỊCH SỬ VIỆT BẮC</h1>
  <p>Nhấp vào các điểm đánh dấu đỏ trên bản đồ để xem thông tin lịch sử</p>
</div>

<!-- Khung chứa bản đồ -->
<div id="ban-do"></div>
body {
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
}

#tieu-de {
  background-color: #8b0000; /* Màu đỏ sẫm lịch sử */
  color: white;
  text-align: center;
  padding: 10px;
}

#tieu-de h1 {
  margin: 0;
  font-size: 20px;
}

#tieu-de p {
  margin: 5px 0 0 0;
  font-size: 14px;
}

/* Chỉnh kích thước cho khung bản đồ */
#ban-do {
  height: 500px;
  width: 100%;
}
// 1. Khởi tạo bản đồ và đặt góc nhìn trung tâm tại khu vực Việt Bắc (Thái Nguyên - Bắc Kạn)
var banDo = L.map('ban-do').setView([21.8, 105.8], 8);

// 2. Lấy lớp hình ảnh bản đồ từ OpenStreetMap
L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
  attribution: 'Bản đồ lịch sử'
}).addTo(banDo);

// 3. Tạo điểm mốc 1: An toàn khu (ATK) Định Hóa - Thái Nguyên
var diem1 = L.marker([21.9114, 105.6311]).addTo(banDo);
diem1.bindPopup(
  "<b>ATK Định Hóa (Thái Nguyên)</b><br>" +
  "<i>Giai đoạn: 1947 - 1954</i><br>" +
  "Nơi ở và làm việc của Chủ tịch Hồ Chí Minh cùng Trung ương Đảng trong kháng chiến chống Pháp."
);

// 4. Tạo điểm mốc 2: Khu di tích lịch sử Nà Tu - Bắc Kạn
var diem2 = L.marker([22.2536, 105.8239]).addTo(banDo);
diem2.bindPopup(
  "<b>Di tích lịch sử Nà Tu (Bắc Kạn)</b><br>" +
  "<i>Năm 1951</i><br>" +
  "Nơi Bác Hồ tặng 4 câu thơ nổi tiếng cho lực lượng Thanh niên xung phong."
);
