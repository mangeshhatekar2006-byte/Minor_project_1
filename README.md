# Minor_project_1
# 🧬 GroupDNA — WhatsApp Group Chat Analyzer

> **Your WhatsApp group chat, decoded.**

GroupDNA is a Python-based WhatsApp chat analytics project that analyzes an exported WhatsApp `.txt` chat file and generates a detailed, terminal-style report about group activity, messaging patterns, frequently used words, response behavior, silent streaks, and personality archetypes.

The project is developed as a **Minor Project using Python and NumPy**, with a focus on implementing data analysis using fundamental programming concepts rather than high-level data-analysis libraries.

---

## 📌 Project Overview

WhatsApp group chats contain a lot of useful information about communication patterns. GroupDNA converts raw chat data into meaningful statistics and behavioral insights.

The analyzer reads a WhatsApp exported chat file, processes the messages, and produces a formatted report containing:

* 📊 Group statistics
* 👥 Participant activity
* 📅 Busiest day
* ⏰ Busiest hour
* 🔥 Activity heatmap
* 📝 Most frequently used words
* ⚡ Response-time analysis
* 👻 Silent-streak analysis
* 🧠 Personality archetypes
* 📋 Final formatted report

The notebook currently analyzes the **Hostel Bois 4ever** dataset covering **01 April 2024 to 30 May 2024**.

---

## ✨ Features

### 1. 💬 WhatsApp Chat Parser

The parser reads the exported WhatsApp `.txt` file and extracts:

* Timestamp
* Sender
* Message text

It also handles several real-world WhatsApp chat cases:

* Normal messages
* System messages
* `<Media omitted>`
* Deleted messages
* Multi-line messages
* Empty lines

The notebook successfully processes the provided dataset and identifies message, media, deleted, and system entries separately.

---

### 2. 📊 Group Overview

Provides a summary of the complete conversation, including:

* Chat period
* Number of analyzed messages
* Number of participants
* Messages sent by each participant
* Percentage contribution of each participant

Example output from the notebook:

```text
GROUPDNA REPORT — GROUP OVERVIEW

Period       : 01 April 2024 to 30 May 2024
Analyzed msgs: 3,127
Participants : 6
Chat period  : 60 days

MESSAGES PER PERSON
Rahul        940 (30.1%)
Priya        712 (22.8%)
Neha         624 (20.0%)
Aman         484 (15.5%)
Karan        345 (11.0%)
Vikas        22  (0.7%)
```

---

### 3. 📅 Most Active Day & Hour

The project identifies:

* The day with the highest number of messages
* The hour with the highest overall message activity

Current notebook output:

```text
Busiest day : 04 May 2024 (74 messages)
Busiest hour: 18:00 - 19:00 (244 messages)
```

---

### 4. 🔥 NumPy Activity Heatmap

GroupDNA creates a **Participant × 24-hour NumPy matrix**.

Each row represents a participant and each column represents an hour of the day.

The matrix is then converted into a text-based heatmap using different intensity symbols.

```text
ACTIVITY HEATMAP (messages by hour)

       00 01 02 03 04 05 06 07 08 09 10 11 12 13 14 15 16 17 18 19 20 21 22 23

Rahul   ░ ░ ░ ░ ░ ░ ░ ░ ░ ░ ░ ░ █ ▒ ▒ █ █ ▒ █ █ ▒ █ █ █
Priya   . . . . . . ░ ▒ █ █ █ █ █ █ █ ▒ ▒ █ █ █ █ ▒ ▒ ░
Neha    . . . . . ▒ ░ ░ █ █ █ ▒ █ █ ▒ ░ █ █ █ █ █ ▒ ▒ ▒
Aman    █ █ █ █ █ . . . . . . . . . ░ ░ ░ ░ ░ ░ ░ ░ . █
```

The implementation uses NumPy for the actual matrix rather than Python lists.

---

### 5. 📝 Top Words

The analyzer identifies the group's most frequently used words.

The processing includes:

* Lowercase conversion
* Punctuation removal
* Tokenization
* Stop-word filtering
* Dictionary-based frequency counting
* Sorted frequency ranking

Example:

```text
THIS GROUP'S FAVOURITE WORDS

how             ████████████████████ 321
guys            ████████████████████ 318
about           █████████████████    274
hai             █████████████████    268
today           ████████████████     257
just            █████████████        208
which           █████████████        202
everyone        ████████████         187
telling         ███████████          179
up              ███████████          172
```

---

### 6. ⚡ Response Speed & Silent Streaks

The project calculates:

**Response Speed**

* Average response time for each participant
* Fastest replier
* Slowest replier

**Silent Streak**

* Longest consecutive period during which a participant sent no messages

Example:

```text
RESPONSE PATTERNS

Fastest replier : Vikas (avg 34.9 minutes)
Slowest replier : Aman (avg 54.9 minutes)

LONGEST SILENT STREAKS

Vikas       : 11 days (23 Apr - 03 May)
Karan       : 0 days
Rahul       : 0 days
Aman        : 0 days
Neha        : 0 days
Priya       : 0 days
```

---

### 7. 🧠 Personality Archetype Detection

GroupDNA assigns each participant a personality archetype based on quantitative messaging behavior.

The implemented archetypes are:

1. **THE SPAMMER**
2. **THE GROUP MOM**
3. **THE NIGHT OWL**
4. **THE STORYTELLER**
5. **THE DRAMA QUEEN**
6. **THE GHOST**
7. **THE COMEDIAN**
8. **THE QUESTION MASTER**

The notebook calculates scores for the archetypes and assigns the highest-scoring category to each participant.

---

### 8. 📋 Final Report

All analytics are combined into a single terminal-style report.

The final output includes:

* Group overview
* Message distribution
* Busiest day and hour
* Activity heatmap
* Favourite words
* Response patterns
* Silent streaks
* Special message counts
* Personality archetypes

The report is designed to be clean and screenshot-friendly without using plotting libraries.

---

## 🛠️ Technologies Used

| Technology       | Purpose                                          |
| ---------------- | ------------------------------------------------ |
| Python           | Core programming and data processing             |
| NumPy            | Activity heatmap matrix and numerical operations |
| Jupyter Notebook | Project development                              |
| Google Colab     | Notebook execution                               |
| GitHub           | Project hosting and version control              |

---

## 🧩 Python Concepts Used

This project demonstrates:

* Variables and data types
* Strings
* Lists
* Tuples
* Sets
* Dictionaries
* Loops
* Conditional statements
* Functions
* File handling
* String manipulation
* Sorting
* Lambda functions
* List/dictionary operations
* `datetime`
* NumPy arrays
* NumPy indexing and aggregation

---

## 🚫 Project Constraints

A major objective of this project is to perform the analysis using Python fundamentals.

### Allowed

* Python fundamentals
* Lists, tuples, sets and dictionaries
* NumPy
* `open()` / file reading
* `datetime`
* String methods
* List and dictionary comprehensions
* `sorted()`

### Not Used

* ❌ Pandas
* ❌ Matplotlib
* ❌ Seaborn
* ❌ Plotly
* ❌ `collections.Counter`
* ❌ `collections.defaultdict`
* ❌ Regular expressions (`re`)
* ❌ WhatsApp analyzer libraries
* ❌ Machine-learning libraries

These restrictions are part of the original project requirements.

---

## 📁 Project Structure

```text
GroupDNA/
│
├── Mangesh_Minor_Project_1.ipynb
├── hostel_bois.txt
├── README.md
└── output/
    └── screenshots/
```

### Files

**`Mangesh_Minor_Project_1.ipynb`**
Main Jupyter/Google Colab notebook containing the complete analysis.

**`hostel_bois.txt`**
Synthetic WhatsApp chat dataset used for the project.

**`README.md`**
Project documentation and setup instructions.

---

## ▶️ How to Run

### Option 1 — Google Colab

1. Open the `.ipynb` file in Google Colab.
2. Upload `hostel_bois.txt` to the Colab session.
3. Make sure the dataset is available in the same working directory.
4. Run the notebook cells from top to bottom.
5. View the generated GroupDNA report.

The notebook also checks whether the dataset exists and displays an upload instruction if it is missing.

---

### Option 2 — Jupyter Notebook

Install Python and NumPy:

```bash
pip install numpy jupyter
```

Then start Jupyter:

```bash
jupyter notebook
```

Open:

```text
Mangesh_Minor_Project_1.ipynb
```

Place:

```text
hostel_bois.txt
```

in the same folder and run the notebook.

---

## 📊 Dataset

The provided dataset is a **synthetic WhatsApp chat export** representing a fictional engineering college hostel group called:

> **Hostel Bois 4ever**

Dataset information:

* **Date range:** 01 April 2024 – 30 May 2024
* **Duration:** 60 days
* **Participants:** 6
* **Original lines:** 3,177
* **Real message entries:** 3,174
* **Media entries:** approximately 30
* **Deleted messages:** approximately 15
* **System messages:** 4

The dataset is synthetic and was created specifically for this project.

---

## 🔐 Privacy

The project can be used with a personal WhatsApp chat export as an optional extension.

**Do not upload or publish your personal WhatsApp chat on GitHub.**

If you analyze your own chat:

* Keep the original `.txt` file private.
* Do not commit personal conversations to GitHub.
* Share only an appropriate screenshot of the generated analysis.
* Obtain consent from group members before publicly sharing analysis results.

The project brief specifically recommends keeping personal chat data private.

---

## 🎯 Learning Objectives

Through this project, I learned how to:

* Process raw text files
* Build a custom WhatsApp parser
* Handle messy real-world data
* Extract structured information from unstructured text
* Perform frequency analysis
* Work with timestamps
* Calculate response-time statistics
* Detect silent periods
* Build a NumPy-based activity matrix
* Design rule-based behavioral classifications
* Format analytical results into a readable report

---

## 🚀 Future Improvements

Possible future enhancements include:

* 📈 Interactive visualizations
* 🌐 Web-based dashboard
* 📱 Streamlit application
* 😊 Emoji analysis
* 🔤 Sentiment analysis
* 🔎 Advanced keyword analysis
* 📊 Monthly activity comparison
* 🏆 Additional personality archetypes
* 📤 Export reports to PDF
* 🎨 Graphical heatmaps

---

## 👨‍💻 Author

**Mangesh Shankar Hatekar**

**Minor Project — Python + NumPy**

**Batch:** August

---

## 📜 Project Note

This project was developed as an educational minor project focused on Python fundamentals, file handling, text processing, NumPy, and basic behavioral analytics.

The notebook contains an AI-assisted disclosure comment indicating that AI was used as a learning aid for structuring and debugging.

---

## ⭐ If You Like This Project

If you find this project useful or interesting:

⭐ Star the repository
🍴 Fork the project
💡 Suggest improvements
📢 Share the project

---

**Built with 🐍 Python + 🔢 NumPy**

> **GroupDNA — Decode the group. Discover the patterns.**
