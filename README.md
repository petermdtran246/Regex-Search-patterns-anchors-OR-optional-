# ✨ Regex Pattern Matching in Python  
### Practical NLP & Text Preprocessing Exercise

This project demonstrates how to use **Python’s `re` module** to search, filter, and manipulate text using **regular expressions**.  
It includes real examples of:

- Anchors (`^`, `$`)
- Character sets (`[aA]`)
- OR patterns (`(need|want)`)
- Optional characters (`?`)
- Text extraction
- Basic NLP-style text cleaning

---

## 📘 Dataset Used

```python
reviews = [
    "Anna helped me today!",
    "the service was awful",
    "amazing support from An",
    "He wanted a refund yesterday",
    "the item I needed arrived",
    "Absolutely loved the product",
    "I want to buy again"
]


🔎 Exercise 1 — Regex Search Tasks

Below are four regex-based pattern matching exercises in Python using re.search().

1️⃣ Find all reviews that start with “A” or “a”.

Pattern:
^[aA]

a_reviews = []
pattern_to_find = r"^[aA]"

for i in reviews:
    if re.search(pattern_to_find, i):
        a_reviews.append(i)

print(a_reviews)


Output:

['Anna helped me today!', 'amazing support from An', 'Absolutely loved the product']

2️⃣ Find all reviews that end with the letter “d”.

Pattern:
d$

d_reviews = []
pattern_to_find = r"d$"

for i in reviews:
    if re.search(pattern_to_find, i):
        d_reviews.append(i)

print(d_reviews)


Output:

['the item I needed arrived']

3️⃣ Find reviews containing “need/needed” or “want/wanted”.

Pattern:
(need|want)ed?

all_reviews = []
pattern_to_find = r"(need|want)ed?"

for i in reviews:
    if re.search(pattern_to_find, i):
        all_reviews.append(i)

print(all_reviews)


Output:

['He wanted a refund yesterday', 'the item I needed arrived', 'I want to buy again']

4️⃣ Find reviews referring to “Anna” or short form “An”.
✔ Approach 1 — OR grouping
Aa_reviews = []
pattern_to_find = r"(Anna|An)"

for i in reviews:
    if re.search(pattern_to_find, i):
        Aa_reviews.append(i)

print(Aa_reviews)

✔ Approach 2 — Optional characters

Ann?a? matches:

"An"

"Ana"

"Anna"

Aa_reviews = []
pattern_to_find = r"Ann?a?"

for i in reviews:
    if re.search(pattern_to_find, i):
        Aa_reviews.append(i)

print(Aa_reviews)


Output:

['Anna helped me today!', 'amazing support from An']

🧠 Concepts Practiced
Concept	Meaning
^	Start-of-string anchor
$	End-of-string anchor
[aA]	Match lowercase or uppercase
`(x	y)`
?	Optional character
ed?	Matches “ed” or nothing
Ann?a?	Matches An / Ana / Anna
Raw string (r"...")	Avoids escape issues
re.search()	Find whether pattern exists
🚀 How to Run This Project
pip install notebook
jupyter notebook


Open the notebook and run all cells to see outputs.

📌 About This Project

This exercise is part of my NLP fundamentals.
My goal is to gain a strong foundation in pattern matching and text processing before working with:

NLTK

spaCy

Text normalization pipelines

Word embeddings

Transformers

Vector databases

