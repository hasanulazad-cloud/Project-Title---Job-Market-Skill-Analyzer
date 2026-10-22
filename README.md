🔍 Job Market Skill Analyzer

Show Image Show Image Show Image Show Image

A pure-Python tool that cleans job-posting data, counts which skills employers ask for most, and lets you search postings by skill, built with nothing but dictionaries, lists, sets, functions and file handling.

📌 Project Overview

Which skills should an aspiring data professional learn first? This project analyses a small set of job postings (Data Analyst, Data Scientist, Business Analyst, Data Engineer, ML Engineer) and answers that question using core Python data structures only: no pandas required.

What it does

📋 Displays job postings in a readable format
➕ Accepts new postings from user input, with an auto-incrementing Job_ID
🧹 Cleans and normalises messy skill text (case, commas, punctuation, spacing)
📊 Extracts skills and ranks them by frequency
🔎 Searches jobs by skill with a reusable function
💾 Saves results to job_skills.csv and top_skills.txt
📂 Repository Contents
File	Description
Project_Title_Job_Market_Skill_Analyzer.ipynb	Main notebook with all nine tasks
job_skills.csv	Cleaned job postings (output of Task 9)
top_skills.txt	Skills ranked by frequency (output of Task 9)
🧰 Concepts Demonstrated

dictionaries · lists · sets · loops · functions · list comprehensions · string cleaning · regular expressions (re) · user input · file I/O · try / except / else / finally

🧩 Tasks Covered
#	Task	Technique
1	Data setup and display	Dictionary of lists, formatted printing
2	Add new job postings	input(), auto-incremented IDs
3	Clean and normalise skills	lower(), replace(), re.sub(), split() / join()
4	Skill extraction and frequency	Counting with a dictionary, sorting by value
5	Basic statistics	Totals, filtering roles that mention Python
6	Skill search function	find_jobs_by_skill()
7	Comprehension filtering	Roles with skills that appear 2+ times
8	Unique skill set	set of all skills
9	Save to files	CSV and text output with error handling
📊 Results

Analysed 6 postings (5 original plus 1 added through user input: Junior Data Analyst at BrightData).

Top skills by frequency
Rank	Skill	Postings
1	python	5
2	sql	4
3	excel	3
4	ml	2
5	statistics, powerbi, spark, deeplearning	1 each
Key insights
🐍 Python appears in 5 of 6 postings, making it the most in-demand skill in this dataset.
🗄️ SQL (4) and Excel (3) complete the core toolkit for analyst roles.
🤖 ML and Deep Learning appear only in data science and ML roles.
🧮 There are 8 unique skills in total: deeplearning, excel, ml, powerbi, python, spark, sql, statistics.
Example search
python
find_jobs_by_skill('sql')
# [(1, 'Data Analyst', 'ABC Corp'), (3, 'Business Analyst', 'DataWorks'),
#  (4, 'Data Engineer', 'InfraTech'), (6, 'Junior Data Analyst', 'BrightData')]
🚀 How to Run
bash
# 1. Clone the repository
git clone https://github.com/hasanulazad-cloud/Project-Title---Job-Market-Skill-Analyzer.git
cd Project-Title---Job-Market-Skill-Analyzer

# 2. Install Jupyter (the project uses only the Python standard library)
pip install jupyter

# 3. Open the notebook
jupyter notebook Project_Title_Job_Market_Skill_Analyzer.ipynb

ℹ️ Task 2 asks for input. Enter the number of postings to add, then a role, company and skills for each (commas are fine; Task 3 cleans them).

⚠️ Known Limitations
Sample size: Six postings is too small to generalise from; the pipeline is the point, not the numbers.
Substring search: find_jobs_by_skill() matches text inside the skills string, so a query like sql would also match a skill such as mysql. Matching on whole skills would be stricter.
Task 5 unique-skill count: The notebook prints Unique skills: 16, but that line counts the characters of the last user-entered string. The correct figure is 8, as shown in Task 8.
🔮 Future Improvements
Load postings from a CSV file or job-board API instead of hardcoded data
Handle multi-word skills (for example "Power BI") as single tokens
Visualise top skills with a bar chart
Add a skill-gap checker that compares a candidate's skills with a target role

👤 Author

Hasanul H Azad Medical billing / RCM professional upskilling in Data Science, AI and Machine Learning GitHub: @hasanulazad-cloud

⭐ If you found this useful, consider starring the repo.
