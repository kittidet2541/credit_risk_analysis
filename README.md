
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


---





   

      


