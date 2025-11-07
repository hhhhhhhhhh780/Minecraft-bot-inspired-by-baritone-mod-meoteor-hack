# Minecraft-bot-inspired-by-baritone-mod-meoteor-hack
🧩 Hướng Dẫn Cài Đặt Bot Minecraft Trên Termux

Tệp: README-Termux-Bot.txt


---

⚙️ 1. Cập Nhật Termux và Cài NodeJS

pkg update -y
pkg upgrade -y
pkg install -y nodejs git

Giải thích:

Cập nhật Termux và cài Node.js, Git.



---

🗃️ 2. Tạo Thư Mục Bot

mkdir -p ~/mc-bot-ui
cd ~/mc-bot-ui

Giải thích:

Tạo thư mục mc-bot-ui và đi vào đó.



---

🧠 3. Tạo File Chính bot-ui.js

nano bot-ui.js

Dán code bot vào (phần code mình gửi trước), rồi nhấn CTRL + X, Y, Enter để lưu.


---

📦 4. Tạo File Cấu Hình package.json

nano package.json

Dán nội dung sau:

{
  "name": "mc-bot-ui",
  "version": "1.0.0",
  "type": "module",
  "main": "bot-ui.js",
  "dependencies": {
    "chalk": "^5.3.0",
    "inquirer": "^9.2.15",
    "ora": "^7.0.1",
    "mineflayer": "^4.11.0",
    "mineflayer-pathfinder": "^2.4.1",
    "mineflayer-pvp": "^1.6.1",
    "mineflayer-armor-manager": "^2.0.0",
    "mineflayer-auto-eat": "^2.3.2",
    "minecraft-data": "^3.51.0",
    "vec3": "^0.1.8"
  }
}


---

🔧 5. Cài Thư Viện

npm install

Giải thích:

Tải tất cả các gói thư viện cần thiết cho bot.



---

🚀 6. Chạy Bot

node bot-ui.js

Menu hiện ra:

==============================
🤖  BOT MINECRAFT TERMUX
==============================

Tên bot: BotTermux
Server: 127.0.0.1:25565
Phiên bản: 1.20.1
Chế độ: None
Trạng thái: 🔴 Đã dừng

? Chọn hành động ›

Tùy chọn:

1. Nhập IP & Port (vd: play.example.com:25565)


2. Nhập tên bot


3. Nhập phiên bản Minecraft


4. Chọn chế độ (Auto Mine, Auto PvP, v.v.)


5. Run Bot – Bot vào server


6. Stop Bot – Dừng bot




---

🔎 7. Cách Hoạt Động

Bot sử dụng mineflayer để giả làm người chơi.

Kết nối đến server theo IP, Port.

Dùng các module auto để di chuyển, PvP, farm, ăn, v.v.

Giao diện dễ hiểu nhờ inquirer.



---

🔄 8. Thêm Tính Năng Tự Kết Nối Lại

Thêm vào cuối code:

bot.on('end', () => {
  console.log("\u26a0\ufe0f Bị ngắt kết nối, thử vào lại sau 10s...");
  setTimeout(connectBot, 10000);
});


---

✅ 9. Kết Luận

Bot sử dụng được trên Termux.

Có giao diện gọn gàng.

Kết nối thực tế đến server Minecraft.

Phù hợp để test, quan sát, auto farm, PvP cơ bản.



---

Tóm tắt lệnh:

pkg update -y && pkg upgrade -y
pkg install -y nodejs git
mkdir -p ~/mc-bot-ui && cd ~/mc-bot-ui
nano bot-ui.js
nano package.json
npm install
node bot-ui.js
