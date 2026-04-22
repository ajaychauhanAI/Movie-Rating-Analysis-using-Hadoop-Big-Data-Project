# 🎬 Movie Rating Analysis using Hadoop

<p align="center">
  <b>Big Data Fundamentals Project</b><br>
  <i>Implemented using Hadoop Ecosystem (HDFS, MapReduce, Hive)</i>
</p>

---

## 📌 Project Overview

This project demonstrates a **complete Big Data processing pipeline** to analyze movie rating datasets using the Hadoop ecosystem.

With the rapid growth of digital platforms, large volumes of user-generated data (ratings, reviews, etc.) are produced. Traditional systems struggle to process such data efficiently.

This project solves that problem using **distributed computing techniques** to extract meaningful insights such as:

* Average ratings of movies
* Top-performing movies

---

## 🎯 Objectives

* To store large datasets using **HDFS**
* To process data using **MapReduce (Python)**
* To perform analytical queries using **Hive**
* To understand distributed data processing
* To generate insights from raw data

---

## 🏗️ Architecture

Raw CSV Dataset
↓
HDFS (Storage Layer)
↓
MapReduce (Processing Layer)
↓
Processed Output (HDFS)
↓
Hive (Analysis Layer)
↓
Insights (Top Movies)

---

## ⚙️ Technologies & Tools Used

* HDFS (Storage Layer)
* MapReduce (Data Processing)
* Hive (Data Analysis)
* Python
* Linux / Cloudera
* ChatGPT (Generative AI Assistance)

---

## 📊 Dataset Information

The dataset contains movie-related information along with user ratings.

### 📌 Key Attributes:

* userId – Unique user ID
* movieId – Unique movie ID
* title – Movie name
* genre – Movie category
* rating – User rating (1–5)
* year – Release year
* watch_time – Duration
* device – Viewing device
* location – User location
* review_score – Detailed rating (1–10)

---

## 🔄 Workflow Explanation

* The dataset is stored in HDFS for distributed storage
* MapReduce processes the data to calculate average ratings
* Processed data is stored back in HDFS
* Hive is used to analyze and query the results
* Final insights such as top-rated movies are generated

---

## 📈 Output

* Average rating of each movie
* Identification of top-performing movies
* Structured insights from raw data

---

## 🤖 Use of Generative AI

Generative AI played an important role in this project:

* Code generation (Mapper & Reducer)
* Debugging support
* Hive query assistance
* Concept understanding of Big Data tools

---

## 🔐 Validation

All generated code and outputs were:

* Manually tested
* Verified for correctness
* Successfully executed in the Hadoop environment

---

## 🌟 Key Features

* Scalable Big Data processing
* Efficient handling of large datasets
* Distributed computing approach
* Integration of AI for enhanced productivity

---

## 🎯 Conclusion

This project successfully demonstrates how the Hadoop ecosystem can be used to process and analyze large-scale datasets efficiently.

By combining **HDFS, MapReduce, and Hive**, the system transforms raw movie data into meaningful insights, enabling better decision-making in real-world scenarios.

---

## 👨‍💻 Author

**Ajay Chauhan**
🎓 BCA (Data Science & AI)
🏫 Babu Banarasi Das University

---

## ⭐ Final Note

This project reflects a real-world Big Data solution where distributed computing is essential for handling large-scale data efficiently.
