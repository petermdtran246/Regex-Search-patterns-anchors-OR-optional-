✨ Regex Pattern Matching Exercise – Python NLP Practice

This project showcases several practical regex techniques used in text processing, NLP preprocessing, and information extraction.
Each task demonstrates how to use different regex concepts such as anchors, optional characters, character sets, and grouping.

📌 Dataset
reviews = [
    "Anna helped me today!",
    "the service was awful",
    "amazing support from An",
    "He wanted a refund yesterday",
    "the item I needed arrived",
    "Absolutely loved the product",
    "I want to buy again"
]

🔎 Exercise 1 — Regex Search (patterns, anchors, OR, optional)

Below are four regex tasks and their solutions.

1️⃣ Find all reviews that start with the letter “A” or “a”.
Solution
a_reviews = []
pattern_to_find = r"^[aA]"

for i in reviews:
    if re.search(pattern_to_find, i):
        a_reviews.append(i)

print(a_reviews)

Output
['Anna helped me today!', 'amazing support from An', 'Absolutely loved the product']


2️⃣ Find all reviews that end with the letter “d”.
Solution
d_reviews = []
pattern_to_find = r"d$"

for i in reviews:
    if re.search(pattern_to_find, i):
        d_reviews.append(i)

print(d_reviews)

Output
['the item I needed arrived']

3️⃣ Find all reviews that contain “need/needed” or “want/wanted”.
Solution
all_reviews = []
pattern_to_find = r"(need|want)ed?"

for i in reviews:
    if re.search(pattern_to_find, i):
        all_reviews.append(i)

print(all_reviews)


Output
['He wanted a refund yesterday', 'the item I needed arrived', 'I want to buy again']


4️⃣ Find all reviews that refer to Anna — both “Anna” and short form “An”.
Approach 1 — OR group
Aa_reviews = []
pattern_to_find = r"(Anna|An)"

for i in reviews:
    if re.search(pattern_to_find, i):
        Aa_reviews.append(i)

print(Aa_reviews)

Approach 2 — Optional characters (regex pattern logic)
Aa_reviews = []
pattern_to_find = r"Ann?a?"

for i in reviews:
    if re.search(pattern_to_find, i):
        Aa_reviews.append(i)

print(Aa_reviews)

Output
['Anna helped me today!', 'amazing support from An']


🧠 What This Project Demonstrates

✔ Using regex anchors:

^ for beginning of string

$ for end of string

✔ Using character sets [aA]
✔ Using OR operator (need|want)
✔ Using optional characters ?
✔ Combining regex with Python loops and list building
✔ Practical NLP-style text filtering

🚀 How to Run

Clone the repo

Open the .ipynb file in Jupyter Notebook or VS Code

Run all cells to see results

Modify patterns to experiment with regex behavior

