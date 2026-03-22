# 🏠 House Price Prediction App

เว็บแอปพลิเคชันสำหรับทำนายราคาบ้านโดยใช้ Machine Learning และแสดงผลผ่าน Streamlit
ผู้ใช้สามารถกรอกข้อมูลบ้าน เช่น จำนวนห้อง พื้นที่ และทำเล เพื่อประเมินราคาบ้านได้ทันที

---

## 🚀 Demo

👉 (https://house-price-predictor-mswkimhpxaamdbaqqswfwa.streamlit.app/)

---

## 📌 Features

* 🔮 ทำนายราคาบ้านแบบ Real-time
* 📊 แสดงกราฟแนวโน้มราคาบ้าน
* 🧠 ใช้ Machine Learning (Random Forest / XGBoost)
* 📍 รองรับข้อมูลทำเล (Suburb)
* 🎯 แสดง Insight ของราคาบ้าน (แพง / กลาง / ประหยัด)

---

## 🧠 Model Details

โมเดลที่ใช้:

* Random Forest Regressor
* XGBoost Regressor
* Linear Regression

เลือกโมเดลที่ดีที่สุดโดยใช้:

* R² Score
* RMSE
* MAE

และทำการ:

* Train/Test Split (80/20)
* Cross Validation
* Hyperparameter Tuning (GridSearchCV)

---

## 📂 Project Structure

```
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

### 1. Clone repository

```
git clone https://github.com/YOUR_USERNAME/house-price-predictor.git
cd house-price-predictor
```

### 2. Create virtual environment

```
py -m venv venv
venv\Scripts\activate
```

### 3. Install dependencies

```
py -m pip install -r requirements.txt
```

### 4. Run app

```
py -m streamlit run app.py
```

เปิดใน browser:

```
http://localhost:8501
```

---

## 📊 Input Features

โมเดลใช้ข้อมูลหลัก 8 ตัว:

* Rooms
* Bedrooms
* Bathrooms
* Car Parking
* Distance to CBD
* Land Size
* Building Area
* Year Built

---

## 📈 Visualization

ในเว็บมีการแสดงกราฟ:

* 📊 Price vs Building Area
* 📊 Price vs Rooms

เพื่อช่วยให้ผู้ใช้เข้าใจแนวโน้มราคาบ้าน

---

## 💡 Example Use Case

* ประเมินราคาบ้านก่อนซื้อ/ขาย
* วิเคราะห์อสังหาริมทรัพย์
* ใช้เป็นเครื่องมือช่วยตัดสินใจ

---

## 🛠 Tech Stack

* Python
* Streamlit
* Scikit-learn
* XGBoost
* Pandas / NumPy
* Matplotlib

---

## 📌 Future Improvements

* เพิ่มแผนที่ (Latitude / Longitude)
* ใช้ Plotly สำหรับ interactive graph
* เพิ่ม feature importance ในหน้าเว็บ
* รองรับข้อมูล real-time

---

## 👨‍💻 Author

* Aemika Oiuphan
* GitHub: https://github.com/67160244-jpg

---

## ⭐️ Acknowledgements

โปรเจกต์นี้พัฒนาขึ้นเพื่อฝึกทักษะด้าน Machine Learning และ Deployment
โดยใช้ workflow จริงแบบ ML Engineer:

Pipeline → Model → Save → Web App → Deploy

---
