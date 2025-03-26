"# Sql-A7" 

# Question: 1 PostgreSQL কী?

PostgreSQL হলো একটি শক্তিশালী, ওপেন-সোর্স **অবজেক্ট-রিলেশনাল ডাটাবেজ ম্যানেজমেন্ট সিস্টেম (ORDBMS)**, যা SQL ভাষার উপর ভিত্তি করে তৈরি এবং এটিকে আরও সম্প্রসারিত করে। এটি নির্ভরযোগ্যতা, ডেটার অখণ্ডতা (data integrity) এবং উন্নত ফিচারের জন্য ব্যাপকভাবে পরিচিত।

##  ওপেন-সোর্স ও অবজেক্ট-রিলেশনাল ডাটাবেজ
- PostgreSQL সম্পূর্ণ **ফ্রি ও ওপেন-সোর্স**, যার ফলে যে কেউ এটি ব্যবহার, পরিবর্তন এবং বিতরণ করতে পারে।  
- এটি একটি **অবজেক্ট-রিলেশনাল ডাটাবেজ**, যা **রিলেশনাল মডেল** এবং **অবজেক্ট-ওরিয়েন্টেড ফিচার** একত্রিত করে আরও শক্তিশালী ডাটাবেজ ব্যবস্থাপনা প্রদান করে।  

##  SQL সমর্থন ও উন্নত ফিচার
- এটি **SQL স্ট্যান্ডার্ডের সাথে高度 (উচ্চ) সামঞ্জস্যপূর্ণ** এবং উন্নত ডেটা ম্যানেজমেন্টের জন্য প্রয়োজনীয় **কমপ্লেক্স কুয়েরি (complex queries), ফরেন কি (foreign keys), ট্রিগার (triggers), ভিউ (views)** সহ আরও অনেক ফিচার সরবরাহ করে।  
- **এন্টারপ্রাইজ-লেভেলের** (enterprise-level) অ্যাপ্লিকেশন ও ডাটাবেজ ম্যানেজমেন্টের জন্য এটি অন্যতম সেরা সমাধান।  

## কেন PostgreSQL ব্যবহার করবেন?
 **উন্নত পারফরম্যান্স ও স্কেলেবিলিটি** (large-scale data management)।  
 **ডেটার নিরাপত্তা ও অখণ্ডতা** বজায় রাখে।  
 **একাধিক প্রোগ্রামিং ভাষার সাথে কাজ করে** (Python, JavaScript, PHP, etc.)।  
 **JSON, XML, GIS (Geospatial Data)** ইত্যাদি উন্নত ডেটা টাইপ সাপোর্ট করে।  

## সংক্ষেপে
**PostgreSQL একটি অত্যন্ত শক্তিশালী ও বহুমুখী ডাটাবেজ, যা ছোট প্রকল্প থেকে শুরু করে বড় এন্টারপ্রাইজ সিস্টেম পর্যন্ত ব্যবহারের জন্য আদর্শ!** 



# Question: 2 PostgreSQL-এ ডাটাবেস স্কিমার উদ্দেশ্য

PostgreSQL-এ **স্কিমা** একটি **নেমস্পেস** হিসাবে কাজ করে, যা টেবিল, ভিউ, ফাংশনের মতো ডাটাবেজ অবজেক্টগুলোকে **লজিক্যাল গ্রুপে** সংগঠিত করতে সাহায্য করে। এটি **পরিচালনা, ব্যবস্থাপনা এবং নিরাপত্তা** উন্নত করে।

##  সংগঠন ও নেমস্পেস
স্কিমা ব্যবহার করে সম্পর্কিত ডাটাবেজ অবজেক্টগুলোকে একত্রিত করা যায়, ফলে সেগুলো সহজে পরিচালনা ও খুঁজে পাওয়া যায়।

##  অবজেক্ট নেমিং
একই ডাটাবেজের ভিন্ন স্কিমার মধ্যে একই নামে একাধিক অবজেক্ট থাকতে পারে, যা **নেমিং কনফ্লিক্ট** প্রতিরোধ করে।

**সংক্ষেপে, স্কিমা PostgreSQL ডাটাবেজকে আরও গোছালো ও কার্যকরভাবে পরিচালনা করতে সাহায্য করে!** 






# Question: 3 **Primary Key এবং Foreign Key কী? (PostgreSQL)**  

PostgreSQL-এ **Primary Key** হোলো একটি টেবিলের প্রতিটি সারিকে (row) অন্যতমভাবে শনাক্ত করার জন্য ব্যবহার করা হয়, আর **Foreign Key** দুটি টেবিলের মধ্যে সম্পর্ক তৈরি করতে সাহায় এবং ডাটা ইন্টিগিরিটি নিশ্চিত করে।  

### ** Primary Key (প্রাইমারি কি)**  
📌 **উদ্দেশ্য:** প্রতিটি সারিকে অন্যমভাবে শনাক্ত করা।  

 **বিশেষত্ব:**  
- প্রতিটি মান **অন্যদের থেকে আলাদা** (ডুপ্লিকেট নয়)।  
- এটি **NULL হতে পারবে না** (খালি থেকে পারবে না)।  
- প্রতিটি টেবিলে **শুধ়মাত্র একটি Primary Key থাকতে পারবে**।  

 **উদাহরণ:**  
একটি **Customers** টেবিলে, `customer_id` কে **Primary Key** হিসেবে ব্যবহার করা যেতে পারে কারণ এটি প্রতিটি কাস্টমারকে আলাদাভাবে শনাক্ত করবে।  

```sql
CREATE TABLE Customers (
    customer_id SERIAL PRIMARY KEY,
    name TEXT NOT NULL,
    email TEXT UNIQUE
);
```

---

### ** Foreign Key (ফরেন কি)**  
 **উদ্দেশ্য:** এক টেবিলের ডাটা অন্য টেবিলের সাথে সংক্ষোক করা এবং সম্পর্ক নির্ধারণ করা।  

 **বিশেষত্ব:**  
- এটি অন্য একটি টেবিলের **Primary Key** কে রেফারেন্স করে।  
- **রেফারেন্সিযাল ইন্টিগিরিটি নিশ্চিত করে**।  
- এক টেবিলে **একাধিক তেকে Foreign Key থাকতে পারে**।  

 **উদাহরণ:**  
```sql
CREATE TABLE Orders (
    order_id SERIAL PRIMARY KEY,
    customer_id INT REFERENCES Customers(customer_id),
    order_date DATE NOT NULL
);
```
---



# Question: 4 CHAR এবং VARCHAR ডেটা টাইপের মধ্যে পার্থক্য

CHAR এবং VARCHAR ডেটা টাইপের মধ্যে প্রধান পার্থক্য হল তাদের স্টোরেজ ক্ষমতা। CHAR হলো ফিক্সড-লেংথ স্ট্রিং স্টোর করে, যেখানে VARCHAR হলো ভ্যারিয়েবল-লেংথ স্ট্রিং, যা শুধুমাত্র প্রয়োজনীয় জায়গা ব্যবহার করে। এখানে বিস্তারিত ব্যাখ্যা দেওয়া হলো:

## CHAR (ফিক্সড-লেংথ):

- **ফিক্সড স্টোরেজ:** CHAR ডেটা টাইপ একটি নির্দিষ্ট স্টোরেজ স্পেস বরাদ্দ করে, ডেটার প্রকৃত দৈর্ঘ্য যাই হোক না কেন।
- **প্যাডিং:** যদি স্টোর করা ডেটা নির্ধারিত দৈর্ঘ্যের চেয়ে ছোট হয়, তবে CHAR স্ট্রিংটির শেষে স্পেস দিয়ে প্যাড করে, যাতে এটি পূর্ণ দৈর্ঘ্য গ্রহণ করে।
- **ব্যবহার:** কোড, আইডেন্টিফায়ার, বা ছোট স্ট্রিং স্টোর করার জন্য উপযুক্ত যেখানে প্যাডিং গ্রহণযোগ্য।
- **উদাহরণ:** যদি আপনি একটি `CHAR(10)` কলাম ডিফাইন করেন, তবে এটি সর্বদা 10টি ক্যারেক্টারের জায়গা বরাদ্দ করবে, যেভাবেই স্টোর করা হোক, যেমন `"abc"` স্টোর করলে বাকি 7টি স্পেস দিয়ে পূর্ণ হবে।

## VARCHAR (ভ্যারিয়েবল-লেংথ):

- **ভ্যারিয়েবল স্টোরেজ:** VARCHAR ডেটা টাইপ শুধুমাত্র ডেটার প্রকৃত দৈর্ঘ্য অনুযায়ী স্টোরেজ স্পেস ব্যবহার করে।
- **কোনো প্যাডিং নেই:** VARCHAR স্ট্রিংয়ে অতিরিক্ত স্পেস প্যাড করে না; এটি শুধুমাত্র প্রকৃত ডেটা স্টোর করে।
- **ব্যবহার:** পরিবর্তনশীল দৈর্ঘ্যের ডেটা যেমন নাম, বর্ণনা বা অন্যান্য টেক্সট ফিল্ডের জন্য উপযুক্ত, যেখানে স্পেস সাশ্রয়ী হতে হবে।




# Question: 5 **WHERE ক্লজ কী? (SQL)**  

SQL-এ **WHERE ক্লজ** ব্যবহার করে নির্দিষ্ট শর্ত অনুযায়ী ডাটাবেজ থেকে নির্দিষ্ট তথ্য বের করা যায়। এটি মূলত **সারিগুলো ফিল্টার করতে** সাহায্য করে, যেন কেবল প্রয়োজনীয় ডাটাগুলোই রিটার্ন হয়।  

### ** WHERE ক্লজের উদ্দেশ্য**  
 নির্দিষ্ট শর্ত অনুযায়ী কেবল প্রয়োজনীয় সারিগুলোকে **ফিল্টার করা**।  
 শুধুমাত্র **যে সারিগুলো শর্ত পূরণ করে, সেগুলোই** রিটার্ন করা।  
 ডাটাবেজ কুয়েরির পারফরম্যান্স **বাড়াতে সাহায্য করে**।  

---
### ** WHERE ক্লজের সাধারণ গঠন (Syntax)**  
```sql
SELECT column_name FROM table_name WHERE শর্ত;
```

---
### ** শর্তের ধরণ**  
 **সরল তুলনা (Comparison):**  
```sql
SELECT * FROM employees WHERE department = 'Sales';
```
উপরের কুয়েরিটি **employees** টেবিল থেকে কেবল সেই সারিগুলো বের করবে, যেখানে **department = 'Sales'**।  

 **যুক্তিবাদী অপারেটর (AND, OR, NOT):**  
```sql
SELECT * FROM employees WHERE department = 'Sales' AND salary > 50000;
```
এই কুয়েরিটি কেবল সেই কর্মচারীদের তথ্য রিটার্ন করবে, যাদের **বিভাগ 'Sales' এবং বেতন ৫০,০০০-এর বেশি**।  

 **আরও জটিল শর্ত (LIKE, IN, BETWEEN, IS NULL, ইত্যাদি):**  
```sql
SELECT * FROM products WHERE price BETWEEN 100 AND 500;
```
এই কুয়েরিটি **১০০ থেকে ৫০০ টাকার মধ্যে থাকা সকল প্রোডাক্ট দেখাবে**।  

---
### ** WHERE ক্লজের অন্যান্য ব্যবহার**  
 **UPDATE**: নির্দিষ্ট সারি আপডেট করতে।  
```sql
UPDATE employees SET salary = 60000 WHERE department = 'Sales';
```
 **DELETE**: নির্দিষ্ট সারি ডিলিট করতে।  
```sql
DELETE FROM employees WHERE department = 'Sales';
```

---
### ** সংক্ষেপে**  
- **WHERE ক্লজ** নির্দিষ্ট শর্ত অনুযায়ী ডাটা ফিল্টার করতে ব্যবহার হয়।  
- এটি **SELECT, UPDATE, DELETE** স্টেটমেন্টের সাথে কাজ করে।  
- **AND, OR, NOT, LIKE, IN, BETWEEN, IS NULL** ইত্যাদি শর্ত প্রয়োগ করা যায়।  

 **WHERE ক্লজ ব্যবহার করে ডাটাবেজ থেকে সঠিক তথ্য সহজেই বের করা যায়!** 



# Question: 6 **LIMIT এবং OFFSET কী? (SQL)**  

SQL-এ **LIMIT** এবং **OFFSET** ক্লজ ব্যবহার করা হয় ডাটাবেজ কুয়েরির **ফলাফলের সংখ্যা নিয়ন্ত্রণ** করতে এবং **পেজিনেশন পরিচালনা** করতে।

---
### ** LIMIT ক্লজ**  
✅ **উদ্দেশ্য:** কুয়েরির ফলাফলের **সর্বোচ্চ কতটি সারি (row) দেখানো হবে**, তা নির্ধারণ করা।  
✅ **কখন ব্যবহার হয়?**  
- যখন **নির্দিষ্ট সংখ্যক রেকর্ড রিটার্ন করতে হয়**।  
- **বড় ডাটাবেজ থেকে লোড কমাতে** চাইলে।  
- **ORDER BY** এর সাথে ব্যবহার করে **সুনির্দিষ্ট অংশের ডাটা** বের করতে।  

** উদাহরণ:**
```sql
SELECT * FROM employees ORDER BY salary DESC LIMIT 5;
```
 এই কুয়েরিটি **বেতন অনুযায়ী সাজানো (DESC) টপ ৫ জন কর্মচারীর তথ্য** দেখাবে।  

---
### ** OFFSET ক্লজ**  
 **উদ্দেশ্য:** নির্দিষ্ট সংখ্যক সারি **এড়িয়ে (skip)** তারপর ফলাফল দেখানো।  
**কখন ব্যবহার হয়?**  
- **পেজিনেশন (Pagination) করতে।**  
- প্রথম X সংখ্যক রেকর্ড **স্কিপ** করে **পরবর্তী রেকর্ড ফেচ** করতে।  

** উদাহরণ:**
```sql
SELECT * FROM employees ORDER BY salary DESC LIMIT 5 OFFSET 5;
```
 এই কুয়েরিটি **বেতন অনুযায়ী সাজানো ৫ জন কর্মচারী বাদ দিয়ে পরবর্তী ৫ জনের তথ্য** দেখাবে।  

---
### ** LIMIT + OFFSET = Pagination **  
 **প্রথম পেজ:**
```sql
SELECT * FROM products ORDER BY price ASC LIMIT 10 OFFSET 0;
```
 **দ্বিতীয় পেজ:**
```sql
SELECT * FROM products ORDER BY price ASC LIMIT 10 OFFSET 10;
```
 **তৃতীয় পেজ:**
```sql
SELECT * FROM products ORDER BY price ASC LIMIT 10 OFFSET 20;
```
✅ এইভাবে **LIMIT এবং OFFSET ব্যবহার করে পেজওয়াইজ ডাটা লোড করা যায়!**  

---
### ** সংক্ষেপে:**  
- **LIMIT** → কতো সংখ্যক রেকর্ড দেখানো হবে সেটি নির্ধারণ করে।  
- **OFFSET** → কতগুলো রেকর্ড **স্কিপ** করে দেখানো হবে সেটি নির্ধারণ করে।  
- **Pagination-এর জন্য LIMIT ও OFFSET একসঙ্গে ব্যবহার করা হয়**।  

 **বড় ডাটাসেট থেকে ডাটা লোড করার সময় পারফরম্যান্স বাড়াতে LIMIT এবং OFFSET ব্যবহার করা হয়!** 



# Question: 7 **UPDATE স্টেটমেন্ট দিয়ে ডাটা পরিবর্তন (SQL)**

SQL-এ **UPDATE** স্টেটমেন্ট ব্যবহার করে বিদ্যমান ডাটা **পরিবর্তন** করা হয়।

---
### ** UPDATE স্টেটমেন্ট কীভাবে কাজ করে?**
 **SET ক্লজ:** যে কলামের মান পরিবর্তন করতে হবে, তা নির্ধারণ করে।
 **WHERE ক্লজ:** নির্দিষ্ট রেকর্ড নির্বাচন করতে ব্যবহার হয়। **WHERE ক্লজ না দিলে পুরো টেবিলের ডাটা পরিবর্তন হয়ে যাবে!**

---
### ** UPDATE স্টেটমেন্টের সাধারণ গঠন:**
```sql
UPDATE table_name
SET column_name = 'new_value'
WHERE condition;
```

---
### ** উদাহরণ ১: নির্দিষ্ট একটি রেকর্ড আপডেট করা**
```sql
UPDATE students
SET name = 'Rahim'
WHERE student_id = 101;
```
 এটি **student_id = 101** রেকর্ডের `name` কলামের মান **'Rahim'** এ পরিবর্তন করবে।

---
### ** উদাহরণ ২: একাধিক কলাম আপডেট করা**
```sql
UPDATE employees
SET salary = 50000, department = 'HR'
WHERE emp_id = 5;
```
 এটি **emp_id = 5** রেকর্ডের `salary` এবং `department` আপডেট করবে।

---
### ** উদাহরণ ৩: একসাথে একাধিক রেকর্ড আপডেট করা**
```sql
UPDATE products
SET price = price * 1.10
WHERE category = 'Electronics';
```
✅ এটি **Electronics ক্যাটাগরির সব প্রোডাক্টের** দাম **১০% বৃদ্ধি করবে**।


```sql
UPDATE employees
SET salary = 50000; -- ⚠️ এটি সব কর্মচারীর বেতন ৫০,০০০ সেট করে দেবে!
```
✅ **সবসময় WHERE ক্লজ ব্যবহার করে নির্দিষ্ট রেকর্ড আপডেট করা উচিত।**




# Question: 8 PostgreSQL-এ JOIN অপারেশনের গুরুত্ব এবং এটি কিভাবে কাজ করে

PostgreSQL-এ, JOIN অপারেশনের মাধ্যমে দুটি বা তার বেশি টেবিলের রেকর্ডগুলোকে সম্পর্কিত কলামের ভিত্তিতে একত্রিত করা হয়, যা একক কুয়েরি দিয়ে একাধিক টেবিল থেকে ডেটা বের করার সুযোগ দেয়। এটি রিলেশনাল ডেটাবেসের জন্য অত্যন্ত গুরুত্বপূর্ণ, কারণ এতে তথ্য বিভিন্ন টেবিলে ভাগ করা থাকে এবং JOIN অপারেশন এর মাধ্যমে সেই তথ্য একসাথে নিয়ে আসা হয়।

### JOIN অপারেশনের গুরুত্ব:

1. **ডেটা ইন্টিগ্রেশন**:
   JOIN অপারেশন আপনাকে সম্পর্কিত টেবিলগুলো থেকে ডেটা একত্রিত করার সুযোগ দেয়, যা আপনাকে ডেটার একটি পূর্ণাঙ্গ দৃষ্টিভঙ্গি প্রদান করে। উদাহরণস্বরূপ, একটি টেবিলের ব্যবহারকারীর তথ্য এবং অন্য টেবিলের অর্ডার তথ্য একসাথে পেতে JOIN করা হয়।

2. **ডেটা রিডান্ডেন্সি এড়ানো**:
   ডেটাকে আলাদা টেবিলে সংরক্ষণ করা এবং JOIN ব্যবহার করে তাদের একত্রিত করা, একই তথ্য একাধিকবার স্টোর করার প্রয়োজনীয়তা কমিয়ে দেয়। এর ফলে ডেটার নির্ভুলতা এবং কার্যকারিতা বৃদ্ধি পায়। এর মাধ্যমে আপনার ডেটাবেসে অপ্রয়োজনীয় তথ্যের পুনরাবৃত্তি কমে আসে।

JOIN অপারেশন একটি শক্তিশালী টুল, যা রিলেশনাল ডেটাবেসে তথ্যের মধ্যে সম্পর্ক স্থাপন করে এবং আরও ভালোভাবে ডেটা বিশ্লেষণ করার সুযোগ দেয়।



# Question: 9 **GROUP BY ক্লজ এবং এটি সংক্ষেপক (aggregation) অপারেশনে কী ভূমিকা রাখে তা ব্যাখ্যা করুন।**

SQL-এ **GROUP BY** ক্লজ ব্যবহার করে **একই ধরনের মানবিশিষ্ট সারিগুলো (rows) একত্রিত করা হয়** এবং **সংক্ষিপ্ত তথ্য বের করতে** অ্যাগ্রিগেট ফাংশন (SUM, COUNT, AVG ইত্যাদি) প্রয়োগ করা হয়।

---
### ** GROUP BY ক্লজের উদ্দেশ্য**
✅ একই মানবিশিষ্ট ডাটা গ্রুপ করে।
✅ অ্যাগ্রিগেট ফাংশনের মাধ্যমে প্রতিটি গ্রুপের উপর ভিত্তি করে ডাটা বিশ্লেষণ করা যায়।
✅ রিপোর্টিং এবং ডাটা সামারাইজেশনের জন্য ব্যবহৃত হয়।

---
### ** GROUP BY ক্লজের সাধারণ গঠন**
```sql
SELECT column_name, AGGREGATE_FUNCTION(column_name)
FROM table_name
GROUP BY column_name;
```

---
### ** উদাহরণ ১: প্রতিটি বিভাগের মোট কর্মচারী সংখ্যা বের করা**
```sql
SELECT department, COUNT(*) AS total_employees
FROM employees
GROUP BY department;
```
এটি **প্রতিটি বিভাগে কতজন কর্মচারী আছে তা দেখাবে**।

---
### ** উদাহরণ ২: প্রতিটি বিভাগের গড় বেতন নির্ণয় করা**
```sql
SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department;
```
 এটি **প্রতিটি বিভাগের গড় বেতন দেখাবে**।

---
### ** উদাহরণ ৩: প্রতিটি ক্যাটাগরির সর্বোচ্চ ও সর্বনিম্ন দামের প্রোডাক্ট বের করা**
```sql
SELECT category, MAX(price) AS highest_price, MIN(price) AS lowest_price
FROM products
GROUP BY category;
```
✅ এটি **প্রতিটি ক্যাটাগরির সবচেয়ে দামী ও সবচেয়ে সস্তা প্রোডাক্ট দেখাবে**।

---
### ** গুরুত্বপূর্ণ সতর্কতা!**
 **GROUP BY ছাড়া অ্যাগ্রিগেট ফাংশন ব্যবহার করলে ত্রুটি হতে পারে।**
```sql
SELECT department, salary FROM employees GROUP BY department;
-- এটি কাজ করবে না কারণ salary কলামটি GROUP BY তে নেই!
```
**যে কলামের উপর গ্রুপিং করা হবে, সেটিকে অবশ্যই GROUP BY-তে উল্লেখ করতে হবে।**



# Question: 10 PostgreSQL-এ COUNT(), SUM(), এবং AVG() এর মতো অ্যাগ্রিগেট ফাংশন কিভাবে হিসাব করা যায়

PostgreSQL-এ COUNT(), SUM(), এবং AVG() এর মতো অ্যাগ্রিগেট ফাংশন SQL কুয়েরি ব্যবহার করে হিসাব করা যায়, যা সাধারণত GROUP BY ক্লজের সাথে ব্যবহার করা হয় ডেটা গ্রুপ করার জন্য, তার পর অ্যাগ্রিগেট ক্যলকুলেশন করা হয়।

### COUNT():
COUNT() ফাংশন নির্দিষ্ট শর্ত পূর্ণ করা সারির সংখ্যা প্রদান করে।

**উদাহরণ**:
```sql
SELECT COUNT(*) FROM employees; 
-- এটি employees টেবিলের সমস্ত সারি গননা করবে।

SELECT COUNT(DISTINCT customer_id) FROM orders;
-- এটি orders টেবিল থেকে ইউনিক customer_id গননা করবে, অর্থাৎ কতজন গ্রাহক অর্ডার করেছে।

SUM():
SUM() ফাংশন একটি সংখ্যাগত কলামের মোট যোগফল প্রদান করে।

উদাহরণ:
SELECT SUM(salary) FROM employees;
-- এটি employees টেবিল থেকে সমস্ত কর্মচারীর বেতন যোগফল করবে।

SELECT SUM(quantity * price) FROM order_items;
-- এটি order_items টেবিল থেকে মোট আয়ের হিসাব করবে (quantity * price)।

AVG():
AVG() ফাংশন একটি সংখ্যাগত কলামের গড় মান প্রদান করে।

উদাহরণ:

SELECT AVG(salary) FROM employees;
-- এটি employees টেবিল থেকে সমস্ত কর্মচারীর গড় বেতন বের করবে।

SELECT AVG(price) FROM products;
-- এটি products টেবিল থেকে সমস্ত পণ্যের গড় দাম বের করবে।

GROUP BY:
GROUP BY ক্লজ ব্যবহার করে আপনি ডেটা গ্রুপ করতে পারেন একটি বা একাধিক কলামের ভিত্তিতে, তারপর প্রতিটি গ্রুপের জন্য অ্যাগ্রিগেট ফাংশন প্রয়োগ করতে পারেন।

উদাহরণ:

SELECT department, AVG(salary) FROM employees GROUP BY department;
-- এটি employees টেবিল থেকে প্রতিটি বিভাগের গড় বেতন বের করবে।


HAVING:
HAVING ক্লজ GROUP BY এর পর গ্রুপকৃত ডেটা ফিল্টার করতে ব্যবহৃত হয়, যা WHERE এর মতো, তবে এটি অ্যাগ্রিগেট ফাংশনের জন্য ব্যবহৃত হয়।

উদাহরণ:

SELECT department, AVG(salary) FROM employees GROUP BY department HAVING AVG(salary) > 50000;
-- এটি শুধুমাত্র এমন বিভাগগুলির গড় বেতন দেখাবে যেগুলির গড় বেতন ৫০,০০০ এর বেশি।
