# 🎓 Program Transfer Planner

## 📌 Description

This project is a web-based application built using **HTML, CSS, and JavaScript (all embedded in a single file)**.

The purpose of this application is to help students plan transferring from one academic program to another by showing:

- All courses in a selected program  
- Whether each course is passed or not  
- Which courses can be transferred (equivalency)  

The application dynamically updates based on the selected academic program.

---

## ⚙️ Features

- Displays course list automatically on page load  
- Shows pass status (Yes / No) with color indicators  
- Dropdown menu to select academic program  
- Dynamic UI updates when program changes  
- Transfer button generates equivalency table  
- Only passed courses are considered for transfer  
- Includes 5 additional fixed courses (always marked as passed)  

---

## 🧩 How the Application Works

### 1. Program-Based Course Storage

Courses are stored in a JavaScript object where each program has its own set of courses:

```
programCourses = {
    "Computer Engineering": [...],
    "Computer Science": [...],
    "Civil Engineering": [...],
    "Electrical and Electronics Engineering": [...]
}
```


Each course includes:
- Course name  
- Pass status ("Yes" or "No")  

---

### 2. Dynamic Course Loading

When a user selects a program from the dropdown:

- The function `loadCourses()` is triggered  
- The course table is cleared  
- New courses for the selected program are loaded  
- The 5 additional courses are appended at the bottom  

This ensures:
- Each program shows different courses  
- Extra courses remain consistent across all programs  

---

### 3. UI Update (Title Change)

When the dropdown value changes:

- The page title updates dynamically  
- The course table refreshes  

Example:
```
🎓 Civil Engineering Transfer Planner
```

This improves user experience and keeps the interface consistent.

---

### 4. Transfer Function

When the **Transfer button** is clicked:

- The system loops through all courses  
- Filters only courses where `passed = Yes`  
- Displays them in the equivalency table  

Courses marked `"No"` are not included, as required.

---

## 🧠 Equivalency Algorithm

The application uses a **keyword-based matching approach** to determine course equivalency.

| Keyword in Course Name | Equivalent Course |
|------------------------|------------------|
| Math                   | Engineering Mathematics |
| Physics                | Applied Physics |
| Programming            | Intro to Programming |
| Data Structures        | Data Structures |
| Artificial Intelligence | Artificial Intelligence |
| Machine Learning       | Machine Learning |
| Networks               | Computer Networks |
| Operating Systems      | Operating Systems |

If no match is found → **"N/A"**

---

## 🚀 Improvement Plan (Future Work)

### 🤖 Automatic Syllabus Comparison

The current system uses simple keyword matching. This can be significantly improved using Artificial Intelligence.

---

### 🔁 Proposed Algorithm

1. Load syllabus text for each course  
2. Preprocess text (remove stopwords, normalize data)  
3. Convert text into numerical vectors using NLP models  
4. Compare courses using similarity measures  
5. Match courses with the highest similarity score  

---

### 🧠 AI Techniques

- Natural Language Processing (NLP)  
- Sentence Embeddings (e.g., BERT, Sentence Transformers)  
- Cosine Similarity  

---

### 💡 Benefits

- More accurate course equivalency  
- Reduces manual matching  
- Scalable across universities  
- Handles complex syllabus descriptions  

---

## ✅ Conclusion

This project demonstrates:

- Dynamic web application development using JavaScript  
- Logical handling of course and program data  
- Interactive UI updates based on user selection  

It also highlights how Artificial Intelligence can enhance course transfer systems in the future by enabling automated and accurate syllabus comparison.
