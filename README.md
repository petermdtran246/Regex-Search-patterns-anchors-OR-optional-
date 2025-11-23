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

**1️⃣ Reviews starting with “A” or “a”**

Pattern:
^[aA] → match strings that begin with A/a.
a_reviews = []
pattern_to_find = r"^[aA]"

for i in reviews:
    if re.search(pattern_to_find, i):
        a_reviews.append(i)

print(a_reviews)

**Output:**

['Anna helped me today!', 'amazing support from An', 'Absolutely loved the product']


