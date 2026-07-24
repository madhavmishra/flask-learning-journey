# Lesson 02

# Topic

Python Module

---

# Goal

Understand what a Python Module is, why it is needed, and how Python imports modules.

---

# Difficulty

🟢 Beginner

---

# Estimated Time

45 Minutes

---

# Prerequisite

Lesson 01 - Python Script

---

# Theory

हामीले Lesson 01 मा Python Script सिक्यौं।

तर एउटा समस्या थियो।

यदि एउटा Program ठूलो हुँदै गयो भने एउटै File मा हजारौं Line Code हुन्छ।

उदाहरण

hospital.py

५००० लाइन

यो Maintain गर्न गाह्रो हुन्छ।

त्यसैले Python ले Code लाई साना भागमा विभाजन गर्ने सुविधा दिएको छ।

यसलाई Module भनिन्छ.

---

# Module भनेको के हो?

Module भनेको

एकवटा Python File (.py)

जसलाई अर्को Program ले Import गरेर प्रयोग गर्न सक्छ।

---

# Real World Example

कल्पना गर्नुहोस्

तपाईंको Office मा

यी Department छन्।

Accounting

HR

Store

Administration

सबैको काम अलग हुन्छ।

तर आवश्यक पर्दा

Accounting ले HR सँग Information लिन्छ।

त्यसरी नै

Python मा एउटा Module ले अर्को Module बाट Function प्रयोग गर्न सक्छ।

---

# एउटा उदाहरण

calculator.py

```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b
```

अब

main.py

```python
import calculator

print(calculator.add(10,5))
```

Output

```
15
```

---

# यहाँ के भयो?

Python ले

calculator.py

लाई Run गरेन।

त्यो File बाट

केवल Function प्रयोग गर्यो।

यही Module हो।

---

# अर्को उदाहरण

utils.py

```python
def welcome(name):
    return f"Welcome {name}"
```

main.py

```python
import utils

print(utils.welcome("Madhav"))
```

Output

```
Welcome Madhav
```

---

# अर्को Import तरीका

```python
from calculator import add

print(add(20,30))
```

Output

```
50
```

---

# किन Module बनाउने?

१.

Code Reuse

---

२.

Large Project Manage गर्न

---

३.

Debug सजिलो

---

४.

Team Work सजिलो

---

५.

Professional Structure

---

# एउटा खराब उदाहरण

project.py

१०,००० लाइन

सबै Code

❌

---

# राम्रो उदाहरण

```
project/

main.py

database.py

auth.py

routes.py

config.py

utils.py
```

हरेक File को काम छुट्टाछुट्टै।

---

# Real World

Flask आफैं

यस्तै Structure मा बनेको छ।

```
flask/

app.py

cli.py

config.py

helpers.py

sessions.py

templating.py
```

यी सबै Module हुन्।

---

# हाम्रो FlaskGen पनि

यस्तै हुनेछ।

```
flaskgen/

cli.py

creator.py

structures.py

utils.py
```

हरेक File एउटा Module हुनेछ।

---

# Best Practice

एक Module

एक Responsibility.

---

# Common Mistakes

❌ सबै Code एउटै File मा लेख्ने।

❌ Module Name

test.py

abc.py

new.py

जस्ता अर्थ नबुझिने नाम राख्ने।

---

# राम्रो Naming

database.py

auth.py

users.py

reports.py

notifications.py

---

# Exercise

१.

calculator.py बनाउनुहोस्।

२.

त्यसमा

add()

subtract()

लेख्नुहोस्।

३.

main.py बनाएर Import गर्नुहोस्।

---

# Homework

यस्ता ५ वटा Module बनाउनुहोस्।

```
project/

main.py

calculator.py

employee.py

student.py

utils.py
```

हरेकमा कम्तीमा एउटा Function राख्नुहोस्।

---

# Summary

आज मैले सिकेँ

Module भनेको एउटा Python File हो।

यसलाई अर्को File बाट Import गर्न सकिन्छ।

ठूलो Project Module बिना बनाउन हुँदैन।

Flask र FlaskGen दुवै धेरै Module मिलेर बनेका हुन्छन्.
