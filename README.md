# TalentLens – Resume Analyzer & Career Recommender 🎯  

TalentLens is an AI-powered **resume analysis and recommendation system** built with **Streamlit**. It allows users to upload resumes in PDF format, analyzes their skills and experience, and provides:  
- **Smart career path suggestions**  
- **Skill gap recommendations**  
- **Personalized courses & certifications**  
- **Resume improvement tips**  
- **Admin dashboard with insights & visualizations**  

---

## 🚀 Features  
### 👨‍💻 User Side
- Upload resumes in **PDF format**  
- Extracts information (Name, Email, Contact, Skills, Experience Level, etc.) using **PyResparser & PDFMiner**  
- Predicts candidate level (Fresher, Intermediate, Experienced)  
- Provides **recommended skills** and **career path suggestions** (Data Science, Web Development, Android, iOS, UI/UX)  
- Suggests **courses & certifications** to upskill  
- Evaluates **resume quality** with a scoring system  
- Provides **resume improvement tips**  

### 🛠 Admin Side
- Secure login for admin (`username: mohd`, `password: zaid123`)  
- View user data stored in **MySQL database**  
- Download reports as CSV  
- Visualize candidate statistics using **Plotly Pie Charts**:  
  - Predicted Career Field distribution  
  - User Level distribution  

---

## 📂 Project Structure  
```
TalentLens/
│
├── Logo/                   # Project logos
├── Uploaded_Resumes/       # Folder where user resumes are stored
├── Courses.py              # Course recommendation data
├── app2.py                  # Main Streamlit app
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```

---

## ⚙️ Installation & Setup  

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/mohdzaid72/TalentLens-by-NLP-Project-.git
cd TalentLens-by-NLP-Project-
```

### 2️⃣ Create Virtual Environment (optional but recommended)
```bash
python -m venv venv
source venv/bin/activate   # for Linux/Mac
venv\Scripts\activate      # for Windows
```

### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

**requirements.txt (sample)**  
```txt
streamlit
pandas
pyresparser
pdfminer3
streamlit-tags
pillow
pymysql
plotly
nltk
pafy
youtube-dl
```

### 4️⃣ Setup Database (MySQL)
- Create database:
```sql
CREATE DATABASE CV;
```
- The table is auto-created by the script  

Update credentials in `app.py` if needed:
```python
connection = pymysql.connect(
    host='localhost',
    user='root',
    password='root',
    db='cv'
)
```

### 5️⃣ Run the App
```bash
streamlit run app.py
```

---

## 🎯 Usage
1. Launch the app → Upload resume (PDF)  
2. View: Resume parsing results, skill analysis, resume tips, recommended courses  
3. Admins → Login to analyze candidate statistics and export data  

---

## 📊 Visualizations (Admin Side)
- **Pie Chart for Predicted Career Fields**  
- **Pie Chart for User Levels (Fresher / Intermediate / Experienced)**  

---

## 🔑 Admin Credentials
```
Username: mohd
Password: zaid123
```

---

## 📌 Future Improvements
- Add **ML/NLP models** for advanced resume parsing & job role prediction  
- Integrate **LinkedIn API** to auto-fetch candidate data  
- Deploy on **Streamlit Cloud / AWS / GCP** for public access  
- Support multiple file formats (DOCX, TXT)  

---

## 👨‍💻 Author
**Mohd Zaid**  
[LinkedIn](https://www.linkedin.com/in/mohd-zaid-5b6452233/)  
