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

```text
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
```

---

## ⚙️ Technologies & Tools Used

| Category      | Tools                        |
| ------------- | ---------------------------- |
| Storage       | HDFS                         |
| Processing    | MapReduce (Hadoop Streaming) |
| Analysis      | Hive                         |
| Programming   | Python                       |
| Platform      | Linux / Cloudera             |
| AI Assistance | ChatGPT                      |

---

## 📊 Dataset Information

The dataset contains movie-related information along with user ratings.

### 📌 Key Columns:

* `userId` – Unique user ID
* `movieId` – Unique movie ID
* `title` – Movie name
* `genre` – Movie category
* `rating` – User rating (1–5)
* `year` – Release year
* `watch_time` – Duration
* `device` – Viewing device
* `location` – User location
* `review_score` – Detailed rating (1–10)

---

## 🔄 Workflow Explanation

1. Dataset is uploaded to **HDFS**
2. **Mapper** extracts (movie, rating)
3. **Reducer** calculates average rating
4. Output is stored in HDFS
5. **Hive** is used to query and analyze results

---

## 🧪 Implementation Steps

### 1️⃣ Upload Dataset to HDFS

```bash
hdfs dfs -mkdir /user/cloudera/ajaychauhan/movie
hdfs dfs -put movie.csv /user/cloudera/ajaychauhan/movie
```

### 2️⃣ Run MapReduce Job

```bash
hadoop jar hadoop-streaming.jar \
-files mapper.py,reducer.py \
-input /user/cloudera/ajaychauhan/movie/movie.csv \
-output /user/cloudera/ajaychauhan/movie/output \
-mapper "python mapper.py" \
-reducer "python reducer.py"
```

### 3️⃣ View Output

```bash
hdfs dfs -cat /user/cloudera/ajaychauhan/movie/output/part-00000
```

---

## 🧾 Hive Analysis

### Create Table

```sql
CREATE TABLE movie_avg (
  movie STRING,
  avg_rating FLOAT
)
ROW FORMAT DELIMITED
FIELDS TERMINATED BY '\t';
```

### Load Data

```sql
LOAD DATA INPATH '/user/cloudera/ajaychauhan/movie/output' INTO TABLE movie_avg;
```

### Queries

```sql
SELECT * FROM movie_avg;

SELECT * FROM movie_avg
ORDER BY avg_rating DESC;

SELECT * FROM movie_avg
ORDER BY avg_rating DESC
LIMIT 5;
```

---

## 📈 Output

* Average rating of each movie
* Sorted list of top-rated movies
* Top 5 movies identified

---

## 🤖 Use of Generative AI

Generative AI played a key role in this project:

* ✔ Code generation (Mapper & Reducer)
* ✔ Debugging assistance
* ✔ Hive query creation
* ✔ Concept understanding (HDFS, MapReduce, Hive)

---

## 🔐 Validation

All AI-generated code was:

* Tested manually
* Verified for correctness
* Executed successfully in Hadoop environment

---

## 🌟 Key Features

* Scalable data processing
* Efficient handling of large datasets
* SQL-like analysis using Hive
* Integration of AI for faster development

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
