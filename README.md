# การวิเคราะห์ความรู้สึกจากข่าวเพื่อทำนายผลตอบแทนหุ้นรายตัวในหมวดธุรกิจธนาคารของตลาดหลักทรัพย์แห่งประเทศไทย
(NEWS SENTIMENT ANALYSIS FOR PREDICTING INDIVIDUAL STOCK RETURNS: EVIDENCE FROM THE BANKING SECTOR OF 
THE STOCK EXCHANGE OF THAILAND
)

**ผู้วิจัย:** เจตนิพิฐ จิรถาวรอนันต์  

พื้นที่จัดเก็บนี้รวบรวมซอร์สโค้ดทั้งหมดที่ใช้ในการค้นคว้าอิสระ ซึ่งครอบคลุมตั้งแต่กระบวนการรวบรวมข้อมูลข่าวสาร การประมวลผลภาษาธรรมชาติ (NLP) ไปจนถึงการวิเคราะห์ทางเศรษฐมิติ

## 📊 ภาพรวมของงานวิจัย (Project Overview)
งานวิจัยนี้นำเสนอการใช้ข้อมูลทางเลือก (Alternative Data) จากข่าวสารทางการเงิน เพื่อประเมินทิศทางและทำนายผลตอบแทนของหุ้นในกลุ่มธนาคาร (Banking Sector) ของตลาดหลักทรัพย์แห่งประเทศไทย (SET) โดยใช้แบบจำลองภาษาขนาดใหญ่ (Transformer-based models) ในการวิเคราะห์ความรู้สึก (Sentiment Analysis) ร่วมกับการทดสอบด้วยแบบจำลอง Regression

## 🛠️ เครื่องมือและเทคโนโลยีที่ใช้ (Tech Stack)
* **ภาษาโปรแกรม:** Python
* **การประมวลผลภาษาธรรมชาติ (NLP):** WangchanBERTa
* **การวิเคราะห์ทางการเงินและเศรษฐมิติ:** Regression

## 📂 แหล่งข้อมูล (Data Sources)
* ข้อมูลราคาหุ้นและงบการเงิน: ตลาดหลักทรัพย์แห่งประเทศไทย (SET)
* ข้อมูลข่าวสารการเงิน: ข่าวจากสำนักข่าวที่ SETTRADE เลือกมาเผยแพร่ ในช่วงปี 2023 - 2025

## 📁 โครงสร้างของพื้นที่จัดเก็บ (Repository Structure)

```text
├── README.md                          # รายละเอียดของโปรเจกต์
├── data/                              # โฟลเดอร์สำหรับตัวอย่างชุดข้อมูล (Sample Data)
│   ├── sample_news_data.csv           
│   └── sample_stock_data.csv          
└── src/                               # โฟลเดอร์หลักสำหรับซอร์สโค้ด
    ├── 01_news_scraping.ipynb         # สคริปต์ Selenium/Scrapy สำหรับดึงข้อมูลข่าว
    ├── 02_text_preprocessing.ipynb    # การทำความสะอาดข้อความภาษาไทย
    ├── 03_sentiment_model.ipynb       # การปรับแต่ง (Fine-tuning) WangchanBERTa และ ModernBERT
    ├── 04_event_study.ipynb           # การวิเคราะห์ Event Studies เมื่อมีข่าวเชิงบวก/ลบ
    ├── 05_panel_regression.ipynb      # การทดสอบสมมติฐานด้วย Panel Data Regression
    └── 06_portfolio_optimization.R    # การทดสอบกลยุทธ์การลงทุน (MVO, Risk Parity)
