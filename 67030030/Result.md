## 🔍 คำถามทบทวน LAB06_1

1. **Docker vs Native Setup**: อธิบายข้อดีของการใช้ Docker เปรียบเทียบกับการติดตั้ง ESP-IDF บน host system <br>
ตอบ Docker เหมาะกับความสะดวก, portability, และความเป็นมาตรฐานในทีม Native เหมาะกับความเร็วและความสามารถในการ debug ได้ง่ายกว่า
2. **Build Process**: อธิบายขั้นตอนการ build ของ ESP-IDF ใน Docker container ตั้งแต่ source code จนได้ binary<br>
ตอบ 1.เตรียม Source Code : โฟลเดอร์โปรเจกต์จะต้องมีไฟล์ CMakeLists.txt, main/, และไฟล์ config อื่น ๆ 2.เข้า Docker Container 3.ตั้งค่า ESP-IDF : โหลด environment 4.กำหนดค่าโปรเจกต์: สร้างไฟล์ config 5.Build โปรเจกต์ : สร้าง binary และไฟล์ output 6.ได้ binary เช่น firmware.bin, bootloader.bin, และ partition_table.bin ในโฟลเดอร์ build/
3. **CMake Files**: บทบาทของไฟล์ CMakeLists.txt แต่ละไฟล์คืออะไร และทำงานอย่างไรใน Docker environment?<br>
ตอบ การทำงานของ CMake ไม่ต่างจาก native เพราะ Docker ใช้เครื่องมือเดียวกัน เพียงแต่ทำงานใน container ที่แยกจากระบบหลัก
4. **Git Ignore**: ไฟล์ .gitignore มีความสำคัญอย่างไรสำหรับ ESP32 project development?<br>
ตอบ ช่วยให้ repo สะอาด ไม่ต้องแชร์ไฟล์ที่สร้างขึ้นหรือเฉพาะเครื่อง
5. **Container Persistence**: ข้อมูลใดบ้างที่จะหายไปเมื่อ restart container และข้อมูลใดที่จะอยู่ต่อ?<br>
ตอบ เมื่อปิดหรือรีสตาร์ท Docker container ข้อมูลที่อยู่ภายใน container จะหายไปเว้นแต่ว่าจะมีการ mount โฟลเดอร์จาก host เข้ามาซึ่งจะทำให้ไฟล์ต่าง ๆ ในโฟลเดอร์นั้นยังคงอยู่แม้ container ถูกปิด
6. **Development Workflow**: เปรียบเทียบ workflow การพัฒนาระหว่างการใช้ Docker กับการทำงานบน native system<br>
ตอบ Docker คือ ใช้งานง่าย ไม่ต้องติดตั้ง ESP-IDF เอง,เหมาะกับการทำงานร่วมกันในทีม,ต้องเข้า container เพื่อ build,flash Debug ยุ่งยากกว่าเล็กน้อย
Native คือ ต้องติดตั้งเครื่องมือและตั้งค่าเอง,Build/Flash ได้สะดวกผ่าน terminal โดยตรง,Debug ง่าย ใช้เครื่องมือบนเครื่องได้เต็มที่,เหมาะกับการพัฒนาแบบลุยๆ และเร็ว
