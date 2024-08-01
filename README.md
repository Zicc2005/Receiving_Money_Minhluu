  <!DOCTYPE html>
  <html lang="vi">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Thông Tin Người Dùng</title>
      <style>
          body {
              font-family: Arial, sans-serif;
              background-color: #1a1a2e;
              color: white;
              text-align: center;
              overflow-y: auto; /* Cho phép cuộn dọc */
              height: 100vh; /* Chiều cao toàn bộ trang */
              animation: fadeIn 1s; /* Hiệu ứng xuất hiện */
          }
          @keyframes fadeIn {
              from { opacity: 0; }
              to { opacity: 1; }
          }
          .container {
              margin: 20px auto;
              padding: 20px;
              border-radius: 10px;
              background-color: #162447;
              width: 300px;
              position: relative;
              box-shadow: 0 4px 20px rgba(0, 0, 0, 0.5); /* Đổ bóng cho container */
              transition: transform 0.3s; /* Hiệu ứng phóng to */
          }
          .container:hover {
              transform: scale(1.05); /* Phóng to khi hover */
          }
          .profile-pic {
              border-radius: 10px; /* Đổi từ hình tròn thành hình chữ nhật */
              width: 100%; /* Đặt kích thước 100% để phù hợp với container */
              height: auto; /* Tự động điều chỉnh chiều cao */
              margin: 0 auto;
              animation: slideIn 1s; /* Hiệu ứng trượt vào */
          }
          @keyframes slideIn {
              from { transform: translateY(-20px); opacity: 0; }
              to { transform: translateY(0); opacity: 1; }
          }
          .button {
              background-color: #0f3460;
              color: white;
              border: none;
              padding: 10px;
              border-radius: 5px;
              cursor: pointer;
              margin: 5px;
              transition: background-color 0.3s; /* Hiệu ứng chuyển màu */
          }
          .button:hover {
              background-color: #1a1a2e; /* Đổi màu khi hover */
              transform: scale(1.1); /* Phóng to khi hover */
          }
          .payment-info {
              margin-top: 20px;
              animation: bounceIn 1s; /* Hiệu ứng nhảy vào */
          }
          @keyframes bounceIn {
              from { transform: scale(0.5); opacity: 0; }
              to { transform: scale(1); opacity: 1; }
          }
          .qr-code {
              width: 100px; /* Kích thước QR code */
              height: 100px;
              margin: 10px auto;
              animation: float 3s infinite; /* Hiệu ứng nổi */
          }
          @keyframes float {
              0%, 100% { transform: translateY(0); }
              50% { transform: translateY(-10px); }
          }
          .money {
              position: absolute;
              top: 0;
              width: 100%;
              height: 100%;
              pointer-events: none; /* Không cho phép tương tác */
              opacity: 0; /* Bắt đầu với độ mờ 0 */
              animation: fall 4s forwards; /* Tăng thời gian rơi */
          }
          @keyframes fall {
              0% { top: -100px; opacity: 0.8; }
              100% { top: 100%; opacity: 0; }
          }
          .bank-icon {
              width: 20px; /* Kích thước biểu tượng ngân hàng */
              vertical-align: middle; /* Căn giữa với văn bản */
              margin-right: 5px; /* Khoảng cách giữa biểu tượng và văn bản */
          }
          .social-icon {
              width: 20px; /* Kích thước biểu tượng Facebook */
              vertical-align: middle; /* Căn giữa với văn bản */
              margin-right: 5px; /* Khoảng cách giữa biểu tượng và văn bản */
          }
      </style>
  </head>
  <body>
      
      <div class="money">
          <img src="https://phongvu.vn/cong-nghe/wp-content/uploads/2020/05/Icon-thuong-thuong-phong-vu-9.jpg" alt="Money" style="width: 50px; position: absolute; left: 5%; animation: move 5s infinite;">
          <img src="https://phongvu.vn/cong-nghe/wp-content/uploads/2020/05/Icon-thuong-thuong-phong-vu-9.jpg" alt="Money" style="width: 50px; position: absolute; left: 20%; animation: move 5s infinite;">
          <img src="https://phongvu.vn/cong-nghe/wp-content/uploads/2020/05/Icon-thuong-thuong-phong-vu-9.jpg" alt="Money" style="width: 50px; position: absolute; left: 35%; animation: move 5s infinite;">
          <img src="https://phongvu.vn/cong-nghe/wp-content/uploads/2020/05/Icon-thuong-thuong-phong-vu-9.jpg" alt="Money" style="width: 50px; position: absolute; left: 50%; animation: move 5s infinite;">
          <img src="https://phongvu.vn/cong-nghe/wp-content/uploads/2020/05/Icon-thuong-thuong-phong-vu-9.jpg" alt="Money" style="width: 50px; position: absolute; left: 65%; animation: move 5s infinite;">
          <img src="https://phongvu.vn/cong-nghe/wp-content/uploads/2020/05/Icon-thuong-thuong-phong-vu-9.jpg" alt="Money" style="width: 50px; position: absolute; left: 80%; animation: move 5s infinite;">
      </div>
      <div class="container">
          <img src="https://scontent.fhan14-1.fna.fbcdn.net/v/t39.30808-6/453183725_1044125787101328_8006280582240292975_n.jpg?_nc_cat=101&ccb=1-7&_nc_sid=cc71e4&_nc_ohc=zio5NO2G4zsQ7kNvgHkDiak&_nc_ht=scontent.fhan14-1.fna&oh=00_AYD3k7rGxo4d-nauYjKIhgfCQuBeMWUvxDEKqSu2qX1tHw&oe=66B0EE43" alt="Profile Picture" class="profile-pic">
          <h2>Lưu Nguyễn Nhật Minh </h2>
          <p>Mãi love khách của em :3 </p>
          <button class="button" onclick="window.location.href='https://www.facebook.com/ZiCzIc2005'">
              <img src="https://upload.wikimedia.org/wikipedia/commons/5/51/Facebook_f_logo_%282019%29.svg" alt="Facebook" class="social-icon">Facebook
          </button>
          <div class="payment-info">
              <h3>Thông Tin Thanh Toán</h3>
              <p>
                  <img src="https://play-lh.googleusercontent.com/M9OvPTmGRRtq40m0WtVRC7v5Rc4bNxj_IliowQSOm-oi2bLmnxsQcgqO-6ajUIQ2f-U" alt="MBBank" class="bank-icon">MBBANK
              </p>
              <p>Số Tài Khoản: 0562855347 </p>
              <p>Chủ Tài Khoản: LUU NGUYEN NHAT MINH </p>
              <img src="https://scontent.fhan19-1.fna.fbcdn.net/v/t1.15752-9/452835094_1018969663225315_9199216074795106771_n.jpg?_nc_cat=110&ccb=1-7&_nc_sid=9f807c&_nc_ohc=K4L3AvNnm2EQ7kNvgG3uOZK&_nc_ht=scontent.fhan19-1.fna&oh=03_Q7cD1QFfPWH2rWuXa2lTbYJeFJ4NbKqqI-H2w-99R5yTcQLKhg&oe=66D2CC6A" alt="QR Code MBBank " class="qr-code">
              <p>
                  <img src="https://upload.wikimedia.org/wikipedia/vi/f/fe/MoMo_Logo.png" alt="Momo" class="bank-icon">Momo Payment
              </p>
              <p>Số Tài Khoản: 0562855347 </p>
              <p>Chủ Tài Khoản: LUU NGUYEN NHAT MINH </p>
              <img src="https://scontent.fhan14-5.fna.fbcdn.net/v/t1.15752-9/453297347_3653378608325759_8591539277886646745_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=9f807c&_nc_ohc=Lp_OPC1D-SkQ7kNvgHJ8UvO&_nc_ht=scontent.fhan14-5.fna&oh=03_Q7cD1QH3ew8McVuITpcPBupOn0yUMlY9oNZnWtQDhaO97IMzQw&oe=66D2870E" alt="QR Code Momo" class="qr-code">
          </div>
      </div>

      <script>
          // Hiệu ứng tiền rơi từ bên trái và bên phải
          const moneyImages = document.querySelectorAll('.money img');    
          moneyImages.forEach((img, index) => {
              img.style.animationDelay = `${index * 1.5}s`; // Thay đổi thời gian bắt đầu cho mỗi hình ảnh
          });
      </script>
  </body>
  </html>
