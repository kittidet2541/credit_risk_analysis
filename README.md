![image](https://github.com/user-attachments/assets/cbeee98b-113e-4a6e-b4d1-390fb91951f7)![image](https://github.com/user-attachments/assets/8f717124-73ea-4898-8a68-5ddd4746f741)
---

# Credit Risk Analysis Prediction

## Overview
ในยุคปัจจุบัน ปัญหาการเป็นหนี้กำลังกลายเป็นเรื่องที่มีแนวโน้มเพิ่มสูงขึ้น ซึ่งทำให้เกิดคำถามมากมายในใจของเรา ว่าใครคือกลุ่มคนที่มีแนวโน้มจะเป็นหนี้? อายุเฉลี่ยของผู้กู้เงินอยู่ในช่วงไหน? และมีกลุ่มฐานเงินเดือนใดบ้างที่เข้าข่ายเสี่ยง? 

โปรเจคนี้เริ่มต้นจากความสงสัยเหล่านี้ โดยมีจุดมุ่งหมายเพื่อวิเคราะห์และทำความเข้าใจว่าผู้ที่เป็นหนี้มีพฤติกรรมและปัจจัยใดบ้างที่ส่งผลต่อความสามารถในการชำระหนี้ รวมถึงการคาดการณ์ว่าใครจะมีโอกาสไม่ชำระหนี้มากที่สุด โดยการใช้ข้อมูลและเทคนิคการวิเคราะห์เชิงลึก

### ลำดับขั้นตอนในการทำงาน

1. **Understanding the Problem & Data Preparation**
   - ทำความเข้าใจปัญหาและรวบรวมข้อมูลที่เกี่ยวข้อง เพื่อตั้งคำถามและกำหนดวัตถุประสงค์ในการศึกษา

2. **EDA and Clean Data**
   - ใช้การวิเคราะห์เชิงสำรวจ (EDA) เพื่อทำความเข้าใจข้อมูลในเชิงลึก ตรวจสอบคุณภาพข้อมูล และทำความสะอาดข้อมูลให้พร้อมสำหรับการวิเคราะห์

3. **Preprocess & Visualization**
   - ดำเนินการแปลงข้อมูลและสร้างการแสดงผลเพื่อช่วยในการวิเคราะห์และสื่อสารผลลัพธ์ได้อย่างชัดเจน

4. **Feature Engineering**
   - สร้างฟีเจอร์ใหม่ที่มีความสำคัญและเลือกฟีเจอร์ที่มีผลต่อการคาดการณ์ เพื่อเพิ่มประสิทธิภาพของโมเดล

5. **Model Building**
   - สร้างโมเดลการคาดการณ์ความเสี่ยงในการชำระหนี้ โดยใช้เทคนิคต่าง ๆ เช่น การจำแนกประเภท และทำการประเมินผลเพื่อปรับปรุงโมเดลให้มีความแม่นยำสูงสุด

### เป้าหมาย
โปรเจคนี้ไม่เพียงแต่จะช่วยให้เราเข้าใจปัจจัยที่ส่งผลต่อความเสี่ยงในการเป็นหนี้ แต่ยังสามารถให้ข้อมูลเชิงลึกที่เป็นประโยชน์สำหรับการวางแผนการเงินและการตัดสินใจในอนาคต โดยเฉพาะในกลุ่มผู้ให้บริการทางการเงินและผู้บริโภค


เริ่มเเรก ผมเริ่มจากการสงสัยว่า ถ้าช่วงปัจจุบัน มีภาวะเศรษฐกิจที่เเย่ลง สิ่งที่จะตามมาคือ ภาวะคนเป็นหนี้เสีย( ไม่จ่ายหนี้ ) ผมเลยเริ่มหาข้อมูลเกี่ยวกับ credit risk (bussiness understanding) ผ่านทาง kaggle เพราะว่าถือว่าเป็นข้อมูลที่มีความน่าเชื่อถือสูงนั่นเอง หลังจากที่ผมได้ข้อมูลมา ผมเริ่มทำการทำความเข้าใจข้อมูลในเเต่ละคอลัมน์เเละข้อมูลด้านใน (data understanding) ทั้งหมด

หลังจากที่สำรวจในเบื้องต้น ผมก็เริ่มมองว่า ปัญานี้สามารถแก้ไขด้วย data ได้มั้ย? ดาต้าที่รับมา สามารถนำไปแก้ไขปัญหาได้มั้ย? ซึ่งมันน่าจะสามารถตอบโจทย์ เเละแก้ไขปัญหาได้ ผมก็เริ่มสำรวจข้อมูลเชิงลึกเลย
ซึ่งการสำรวจจะเริ่มจากการตรวจสอบข้อมูล

![image](https://github.com/user-attachments/assets/a07ffbe0-c48d-4a4d-99f5-6beace690803)

ผลลัพท์ที่ได้
![image](https://github.com/user-attachments/assets/9ee6e3f2-218b-41a3-9341-d726d6c9a220)


จะเห็นได้ว่า คอลัมน์ person_emp_length และ loan_int_rate มีข้อมูลไม่เท่าตัวอื่นๆ ข้อมูล null ผมเลยทำการคลีนข้อมูลโดยผมไปดูค่าเฉลี่ย กับ มัธยฐาน มีค่าใกล้เคียงกัน จึงทำการเติมค่า null ด้วย average 
จากนั้นผมทำการสร้างข้อมูลเพิ่มโดยจัดกลุ่มของอายุ รายได้ เเละทำการ visualization ผลออกมาดังนี้

![image](https://github.com/user-attachments/assets/62003e79-29f2-4827-98ce-86bc66f29119)

นี่คือการกระจายตัวของอายุ จะเห็นว่า ช่วงอายุที่ 20-30 มีปริมาณมากที่สุด

จากนั้นผมนำ age กับ income มาทำการเปรียบเทียบเพื่อดูความสัมพันธ์

![image](https://github.com/user-attachments/assets/1bd4562c-d068-4a81-8212-dbbacb004c53)

จะเห็นว่า เงินเดือนกับอายุในชุดข้อมูลนี้ แทบจะไม่มีความสัมพันธ์กัน อาจจะเพราะว่า เป็นข้อมูลที่เฉพาะทาง (ข้อมูลนี้มีเเค่คนที่มีสินเชื่อ)

จากนั้นมาดูกลุ่มของเงินเดือน โดยจัดกลุ่มของเงินเดือนได้ดังนี้

![image](https://github.com/user-attachments/assets/3a3c2550-a9ab-40fd-bb8b-4a3d1d912772)

จากกราฟนี้สรุปได้ว่า คนที่มากู้ส่วนใหญ่คือ กลุ่มคนเงินเดือน 40k - 60k

เรามาดูเกรดการปล่อยสินเชื่อเทียบกับดอกเบี้ยดังนี้

![image](https://github.com/user-attachments/assets/f7b0d7fa-c5ef-45f9-acdc-53cce832ae6e)

จะเห็นว่า ข้อมูลมีความสัมพันธ์กันโดยยิ่งเกรดดี ค่าดอกเบี้ยยิ่งต่ำ ยิ่งเกรดเเย่ ค่าดอกเบี้ยยิ่งสูงขึ้น

เรามาดูประเภทของคนที่ขอสินเชื่อ ว่ามีที่อยู่อาศัยรูปแบบใด้บ้าง

![image](https://github.com/user-attachments/assets/b26fad56-6602-4408-a965-00783c13ffc3)

จะเห็นได้ว่า กลุ่มที่มาขอสินเชื่อเยอะที่สุดคือกลุ่มคนที่มาเช่าบ้าน (Rent) เเละ ผ่อนบ้าน เป็นเจ้าของบ้าน ตามลำดับ

เรามากันต่อที่ ประเภทที่คนมาขอสินเชื่อ จะมีอะไรบ้าง เเละดูว่าเเต่ละประเภทมีการผิดชำระหนี้ขนาดไหน

![image](https://github.com/user-attachments/assets/089ee630-1f2b-4cef-9ce5-33e4512c124d)

จะเห็นได้ว่า ประเภทที่มีการขอสินเชื่อเยอะที่สุดคือ การศึกษา (Education) เเละประเภทที่รวมหนี้สิน เป็นประเภทที่จ่ายคืนน้อยที่สุด อาจเพราะคนที่ขอรวมหนี้สินไว้ที่เดียวส่วนใหญ่เป็นผู้ที่มีปัญหาทางด้านการเงินสูงนั่นเอง

ต่อไปมาดูอัตราการชำระคืนระหว่างกลุ่ม ผู้เช่าบ้าน ผู้ผ่อนบ้าน เเละคนที่เป็นเจ้าของบ้านกัน

![image](https://github.com/user-attachments/assets/d19c4812-36ef-49d9-8376-92aece279a18)

จะเห็นว่ากลุ่มคนที่เช่าบ้าน มีเยอะมาก และมีอัตราการผิดชำระหนี้มากทีเดียวอาจเพราะว่า เป็นกลุ่มที่มีการเงินไม่มั่นคง

















---





   

      


