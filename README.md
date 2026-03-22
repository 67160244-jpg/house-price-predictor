# 🏠 House Price Prediction App

เว็บแอปพลิเคชันสำหรับทำนายราคาบ้านโดยใช้ Machine Learning
ผู้ใช้สามารถกรอกข้อมูลบ้าน เช่น จำนวนห้อง พื้นที่ และทำเล เพื่อประเมินราคาบ้านได้แบบ Real-time ผ่านหน้าเว็บ

---

## 🎯 Problem Statement

การตั้งราคาบ้านเป็นปัญหาที่มีความซับซ้อน เนื่องจากราคาบ้านขึ้นอยู่กับหลายปัจจัย เช่น ทำเลที่ตั้ง ขนาดพื้นที่ จำนวนห้อง และสิ่งอำนวยความสะดวก

การประเมินราคาด้วยมนุษย์เพียงอย่างเดียวอาจมีความคลาดเคลื่อนสูง ดังนั้นจึงนำ Machine Learning มาช่วยวิเคราะห์และทำนายราคาบ้าน เพื่อช่วยให้ผู้ซื้อ ผู้ขาย และนักลงทุนสามารถตัดสินใจได้ดีขึ้น

---

## 📊 Dataset

Dataset ที่ใช้ประกอบด้วยข้อมูลเกี่ยวกับบ้าน เช่น:

* Rooms: จำนวนห้องทั้งหมด
* Bedroom2: จำนวนห้องนอน
* Bathroom: จำนวนห้องน้ำ
* Car: จำนวนที่จอดรถ
* Distance: ระยะทางจากใจกลางเมือง (CBD)
* Landsize: ขนาดที่ดิน (ตารางเมตร)
* BuildingArea: ขนาดตัวบ้าน (ตารางเมตร)
* YearBuilt: ปีที่สร้างบ้าน

รวมถึงข้อมูลเชิงหมวดหมู่ เช่น Suburb (ทำเล)

📌 แหล่งข้อมูล:

[house_price.csv](https://github.com/user-attachments/files/26170194/house.price.csv)


## 🔍 Exploratory Data Analysis (EDA)

ก่อนการสร้างโมเดล ได้มีการวิเคราะห์ข้อมูลเบื้องต้น เช่น:

* ตรวจสอบ missing values และลบข้อมูลที่ไม่สมบูรณ์
* วิเคราะห์ distribution ของราคาบ้าน
* ตรวจสอบความสัมพันธ์ของ features กับราคา (Correlation)
* ตรวจจับ outliers เช่น บ้านที่มีขนาดผิดปกติ

และใช้ One-Hot Encoding สำหรับข้อมูล categorical เช่น Suburb

---

## 🤖 Model Development

ได้ทดลองใช้โมเดลหลายแบบ ได้แก่:

* Linear Regression
* Random Forest Regressor
* XGBoost Regressor

### ⚙️ การพัฒนาโมเดล:

* แบ่งข้อมูล Train/Test (80/20)
* ใช้ Pipeline เพื่อรวม preprocessing + model
* ทำ Cross-Validation (5-Fold)
* ปรับค่า Hyperparameter ด้วย GridSearchCV

---

## 📈 Model Evaluation

ใช้ metrics ที่เหมาะสมกับ Regression:

* R² Score (ยิ่งใกล้ 1 ยิ่งดี)
* RMSE (Root Mean Squared Error)
* MAE (Mean Absolute Error)

📊 โมเดลที่ดีที่สุดถูกเลือกจากค่า R² ที่สูงที่สุด
และมีค่าความคลาดเคลื่อนต่ำ

---

## 🚀 Deployment (Web Application)

โมเดลถูกนำไปใช้งานผ่าน Streamlit Web App

### ✨ Features ของเว็บ:

* 🔮 ทำนายราคาบ้านแบบ Real-time
* 📊 แสดงกราฟแนวโน้มราคาบ้าน
* 📍 เลือกทำเล (Suburb)
* 🧠 แสดง insight ของราคาบ้าน (แพง / กลาง / ประหยัด)
* 📈 แสดงความสัมพันธ์ เช่น:

  * Price vs Building Area
  * Price vs Rooms

---

## 🖥️ Demo

👉 ((https://house-price-predictor-mswkimhpxaamdbaqqswfwa.streamlit.app/))

---

## 📂 Project Structure

```id="c2lq2b"
house_price/
│
├── app.py
├── requirements.txt
├── model_artifacts/
│   ├── house_price_pipeline.pkl
│   ├── feature_names.json
│   └── model_metadata.json
```

---

## ⚙️ Installation (Run Locally)

```id="ntp0km"
git clone https://github.com/YOUR_USERNAME/house-price-predictor.git
cd house-price-predictor

py -m venv venv
venv\Scripts\activate

py -m pip install -r requirements.txt
py -m streamlit run app.py
```

เปิดใช้งานที่:
http://localhost:8501

---

## 🛠 Tech Stack

* Python
* Streamlit
* Scikit-learn
* XGBoost
* Pandas / NumPy
* Matplotlib

---

## 💡 Example Use Cases

* ประเมินราคาบ้านก่อนซื้อ/ขาย
* วิเคราะห์อสังหาริมทรัพย์
* ใช้เป็นเครื่องมือช่วยตัดสินใจด้านการลงทุน

---

## ⚠️ Disclaimer

โมเดลนี้เป็นเพียงเครื่องมือช่วยประมาณราคา
ไม่สามารถใช้แทนการประเมินราคาจริงโดยผู้เชี่ยวชาญได้
ผลลัพธ์อาจมีความคลาดเคลื่อนขึ้นอยู่กับข้อมูลที่ป้อนเข้า

---

## 🔮 Future Improvements

* เพิ่มแผนที่ (Latitude / Longitude)
* ใช้ Plotly สำหรับ interactive graph
* เพิ่ม Feature Importance บนหน้าเว็บ
* รองรับข้อมูล real-time

---

## 👨‍💻 Author

* (Aemika Oiuphan)
* GitHub: https://github.com/67160244-jpg

---

## ⭐️ Summary

โปรเจกต์นี้แสดงให้เห็นกระบวนการ Machine Learning แบบครบวงจร:

Data → EDA → Model → Evaluation → Deployment

ซึ่งเป็น workflow ที่ใช้จริงในสายงาน Data Science และ Machine Learning Engineering
