<details>
<summary>ENG (English Version)</summary>

# ADsP - I. Understanding Data

## 1. Types of Data

### (1) Definition of Data
### (2) Quantitative and Qualitative Data
1. **Quantitative Data**
   - Numerical values or amounts
2. **Qualitative Data**
   - Characteristics or attributes
### (3) Structured, Unstructured, and Semi-structured Data
1. **Structured Data**
   - Relational databases
   - Excel
   - CSV
2. **Unstructured Data**
   - Text
   - Images
   - Social media posts
3. **Semi-structured Data**
   - XML
   - HTML
   - JSON
   - Logs
> **Schema:** Defines the structure, format, and relationships of data.  
> **Metadata:** Data that describes other data.


---

## 2. Tacit Knowledge and Explicit Knowledge

### (1) Tacit Knowledge
Knowledge acquired through personal experience and difficult to formalize or transfer.
### (2) Explicit Knowledge
Knowledge that can be documented, expressed, and easily shared.
### (3) Interaction Between Tacit and Explicit Knowledge
**Socialization → Externalization → Combination → Internalization**
(This process is repeated continuously.)


---

## 3. DIKW Pyramid

### Data
Raw facts without context.
- A Company: 10,000 KRW
- B Company: 20,000 KRW
### Information
Data organized to provide meaning and context.
- A Company's price is **lower than** B Company's price.
### Knowledge
Information used to make decisions.
- Based on the price comparison, decide whether to buy from A Company.
### Wisdom
Knowledge combined with experience, values, and judgment.
- Make a final decision by considering other factors in addition to price.

**DIKW**
**Data → Information → Knowledge → Wisdom**


---

## 4. Definition and Characteristics of a Database

### (1) Definition of a Database
An organized collection of related data.
### (2) Characteristics of a Database
- **Integrated Data**
  - Minimizes redundancy.
- **Stored Data**
  - Stored on computer-readable storage media.
- **Shared Data**
  - Can be used by multiple users or applications.
- **Operational Data**
  - Continuously updated according to organizational activities.
### Database Independence
**Physical Data Independence**
Changes in physical storage methods or structures do not affect application programs.
**Logical Data Independence**
Changes in the logical structure or schema do not affect application programs.


---

## 5. DBMS (Database Management System)

### (1) Database Management Systems
#### Relational DBMS
Examples:
- Oracle
- MySQL
- MS SQL
#### Object-Oriented DBMS
Manages data using object-oriented concepts.
### (2) Database Design Process
**Requirements Analysis → Conceptual Design → Logical Design → Physical Design → Implementation**
### (3) SQL (Structured Query Language)
#### DDL — Data Definition Language
- `CREATE`
- `ALTER`
- `DROP`
#### DML — Data Manipulation Language
- `SELECT`
- `INSERT`
- `UPDATE`
- `DELETE`
#### DCL — Data Control Language
- `GRANT`
- `REVOKE`
### (4) NoSQL
Examples:
- MongoDB
- Cassandra
- HBase
- Redis


---

## 6. Data Warehouse (DW)
A **Data Warehouse** is a database designed primarily for analysis and decision-making.

### Characteristics
- **Subject-Oriented**
- **Integrated**
- **Time-Variant**
- **Non-Volatile**
### Data Lake
Stores various forms of data, including:
- Structured data
- Unstructured data
- Semi-structured data
### Data Mart
A smaller subset of a Data Warehouse focused on a particular:
- Subject
- Department
- Business function


---

## 7. Database Applications

### (1) Internal Corporate Databases
1. **OLTP — Online Transaction Processing**
   - Processes online transactions.
2. **OLAP — Online Analytical Processing**
   - Performs multidimensional analytical processing.
3. **CRM — Customer Relationship Management**
   - Manages customer relationships.
4. **SCM — Supply Chain Management**
   - Manages supply chains.
5. **KMS — Knowledge Management System**
   - Manages organizational knowledge.
6. **ERP — Enterprise Resource Planning**
   - Integrates and manages enterprise resources.
7. **BI — Business Intelligence**
   - Supports business decision-making through data analysis.
   - Examples:
     - Tableau
     - Power BI
     - FineReport
8. **BA — Business Analytics**
   - Uses data and analytical techniques to support business decisions.
### (2) Social Infrastructure Databases
1. **ITS — Intelligent Transport System**
2. **NEIS — National Education Information System**


---

## 8. Understanding Big Data

### (1) Definition of Big Data
Big Data is commonly characterized by the **4Vs**:
1. **Volume**
2. **Variety**
3. **Velocity**
4. **Value**

### Data Size Units
**K → M → G → T → P → E → Z → Y**
- KB — Kilobyte
- MB — Megabyte
- GB — Gigabyte
- TB — Terabyte
- PB — Petabyte
- EB — Exabyte
- ZB — Zettabyte
- YB — Yottabyte
### (2) Background of Big Data
Factors contributing to the emergence of Big Data:
- Google Flu Trends
- NASA climate simulations
- Rapid progress in digitalization
- Mobile revolution
  - Social media emotional data
  - GPS
  - Accelerometers
- Development of cloud computing technologies
### (3) Functions of Big Data
Big Data can function as a **platform**, including social media platforms.
### (4) Fundamental Changes Created by Big Data
1. **Post-processing**
2. **Full population analysis**
3. **Quantity over precision**
4. **Correlation over causality**
### (5) Difficulty in Measuring the Value of Big Data
The value of Big Data is difficult to determine in advance.


---

## 9. Applications of Big Data

### (1) Big Data Application Areas
Big Data can be utilized by:
- Companies
- Governments
- Individuals
### (2) Technologies Used for Big Data
- Association Rule Learning
- Classification Analysis
- Genetic Algorithms
- Machine Learning
- Regression Analysis
- Sentiment Analysis
- Social Network Analysis


---

## 10. Challenges and Countermeasures of Big Data

### (1) Challenges and Countermeasures in the Big Data Era
1. **Invasion of Privacy**
   - Shift from consent-based responsibility to accountability.
2. **Erosion of the Principle of Responsibility**
   - Emphasize result-based responsibility.
3. **Data Misuse**
   - Requires algorithmic transparency and specialized knowledge.
### (2) Privacy Protection Technologies
1. **Anonymization**
2. **Aggregation**
3. **Data Deletion**
4. **Data Categorization**
5. **Data Masking**


---

## 11. Three Essential Elements for Big Data Utilization

1. **Data**
   - IoT is an important source of data.
2. **Technology**
3. **People**


---

## 12. Big Data Analysis and Strategic Insights

### (1) Skepticism About Big Data
Big Data itself does not automatically produce valuable insights.
### (2) Big Data Analysis Is Not Simply About "Big"
The size of data is not the core issue.
Important considerations include:
- Cost-effectiveness
- Appropriate analytical methods
- Understanding analytical performance
### (3) Limitations of Analysis Without Strategic Alignment
Analysis without connection to business strategy has limited value.
### (4) Practical Analysis vs. Strategic Value-Based Analysis
1. **Practical Analysis**
   - Focuses on solving immediate problems.
2. **Strategic Value-Based Analysis**
   - Focuses on deriving long-term strategic value.


---

## 13. Data Science

### (1) Meaning and Role of Data Science
Data Science uses a **holistic approach** that combines multiple disciplines.
### (2) Key Components of Data Science
1. **IT / Data Management Domain**
2. **Analytical Domain**
3. **Business Consulting Domain**
### (3) Roles and Required Capabilities of Data Scientists
Data scientists require both:
- **Hard Skills**
- **Soft Skills**


---

## 14. Strategic Insight and the Role of Humanities
### (1) External Environmental Factors
1. **Divergence**
2. **Service**
3. **Market Creation**
### (2) Internal Situational Factors
Internal organizational conditions should also be considered when deriving strategic insights.
### (3) Limitations of Data Science and the Role of Humanities
Data Science alone cannot explain every business or social phenomenon.
Humanities can provide:
- Context
- Interpretation
- Human-centered perspectives
- Strategic judgment


---

## 15. Changes in Value Paradigms

### Stage 1 — Digitalization
Physical or analog information is converted into digital form.
### Stage 2 — Connection
Digital technologies connect people, devices, organizations, and information.
### Stage 3 — Agency
Connected systems increasingly act autonomously and make decisions.
**Digitalization → Connection → Agency**

</details>
<details>
<summary>KOR (한국어 버전)</summary>
# ADsP - I 과목. 데이터 이해

<img width="1885" height="2633" alt="image" src="https://github.com/user-attachments/assets/015b3497-1516-4a63-a262-948e0f629949" />
<img width="1989" height="2771" alt="image" src="https://github.com/user-attachments/assets/6eb73dae-f3b6-4f4d-b359-ba5c7874a4ff" />
<img width="2011" height="2826" alt="image" src="https://github.com/user-attachments/assets/fda2ca0a-a48a-4410-85c6-770e6c5c0065" />
<img width="1958" height="2725" alt="image" src="https://github.com/user-attachments/assets/3f8a7465-9704-4424-a20d-53e4281013ed" />
<img width="1887" height="2641" alt="image" src="https://github.com/user-attachments/assets/39948cb9-0978-4b14-a938-13584e6820a4" />

</details>
