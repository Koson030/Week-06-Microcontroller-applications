## 🔍 คำถามทบทวน LAB06_1

1. **Docker vs Native Setup**: อธิบายข้อดีของการใช้ Docker เปรียบเทียบกับการติดตั้ง ESP-IDF บน host system <br>
ตอบ Docker เหมาะกับความสะดวก, portability, และความเป็นมาตรฐานในทีม Native เหมาะกับความเร็วและความสามารถในการ debug ได้ง่ายกว่า
2. **Build Process**: อธิบายขั้นตอนการ build ของ ESP-IDF ใน Docker container ตั้งแต่ source code จนได้ binary<br>
ตอบ 1.เตรียม Source Code : โฟลเดอร์โปรเจกต์จะต้องมีไฟล์ CMakeLists.txt, main/, และไฟล์ config อื่น ๆ 2.เข้า Docker Container 3.ตั้งค่า ESP-IDF : โหลด environment 4.กำหนดค่าโปรเจกต์: สร้างไฟล์ config 5.Build โปรเจกต์ : สร้าง binary และไฟล์ output 6.ได้ binary เช่น firmware.bin, bootloader.bin, และ partition_table.bin ในโฟลเดอร์ build/
3. **CMake Files**: บทบาทของไฟล์ CMakeLists.txt แต่ละไฟล์คืออะไร และทำงานอย่างไรใน Docker environment?<br>
ตอบ
4. **Git Ignore**: ไฟล์ .gitignore มีความสำคัญอย่างไรสำหรับ ESP32 project development?<br>
ตอบ
5. **Container Persistence**: ข้อมูลใดบ้างที่จะหายไปเมื่อ restart container และข้อมูลใดที่จะอยู่ต่อ?<br>
ตอบ
6. **Development Workflow**: เปรียบเทียบ workflow การพัฒนาระหว่างการใช้ Docker กับการทำงานบน native system<br>
ตอบ
