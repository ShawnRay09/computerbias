---
toc: true
layout: base
title: Computing Bias Lesson
description: By Shawn Ray, Jonah Luo, Tarun Rayavarapu, Arya Savlani
---
<style>
header {
  display: none;
}
</style>

# Computing Bias Lesson 🧠

## Introduction 📌

Computing bias occurs when computer systems systematically and unfairly discriminate against certain groups. Bias in computing can reinforce social inequalities, create unfair advantages, and lead to real-world harm. This lesson explores how bias emerges, real-world examples, and strategies for mitigation.

---

## What is Computing Bias? 

> "We can say that a computer system is biased if it both unfairly and systematically discriminates against one group in favor of another." – *Nissenbaum et al.* ([Cornell Paper](https://nissenbaum.tech.cornell.edu/papers/Discerning%20Bias%20in%20Computer%20Systems.pdf))


<img src="{{site.baseurl}}/images/compbi.png" height="250" wdith="375">

<a>
</a>

---

<a>
</a>

<h3>Doctor or Nurse Drawings 🎨</h3> 

<a>
</a>



<button id="roleButton">Get Role</button>
<p id="result"></p>

---

<style>
    button {
        background-color: #4CAF50;
        color: white;
        border: none;
        padding: 10px 20px;
        font-size: 18px;
        cursor: pointer;
        border-radius: 5px;
        transition: background-color 0.3s ease;
    }
    button:hover {
        background-color: #45a049;
    }
    #result {
        margin-top: 20px;
        font-size: 22px;
        font-weight: bold;
        color: #333;
    }
</style>

<script>
    document.getElementById("roleButton").addEventListener("click", function() {
        let role = Math.random() < 0.5 ? "Doctor" : "Nurse";
        document.getElementById("result").innerText = "Draw a: " + role;
    });
</script>

## **Types of Bias in Computing** 🔍

<a>
</a>


<a>
</a>


 **Pre-existing Social Bias**

   - Originates from societal norms, stereotypes, or historical inequalities.
   - Embedded into technology due to biased data, biased creators, or societal influence.
   - **Examples:**
     - Hiring algorithms favoring men over women.
     - Facial recognition systems performing poorly on non-white faces.

<img src="{{site.baseurl}}/images/faca.png" height="250">

<a>
</a>

---

<a>
</a>

 **Technical Bias**

   - Stems from design, implementation, or structural limitations in technology.
   - Even systems built with good intentions may introduce bias through their function.
   - **Examples:**
     - Google Translate assigning gendered pronouns based on stereotypes.
     - Default settings not representing all user demographics.

<img src="{{site.baseurl}}/images/gender.png" height="250" width="375">

---

 **Emergent Social Bias**

   - Develops over time as a system interacts with users or adapts to real-world data.
   - AI models may evolve in a biased manner based on user interactions.
   - **Examples:**
     - AI chatbots learning harmful language from users.
     - Search engines amplifying biased content over time.


<img src="{{site.baseurl}}/images/ai.png" height="250" width="375">

<a>
</a>

---

<a>
</a>

#### **Question 1:**  ❓
A company implements an AI hiring system that unintentionally prefers male candidates over female candidates because it was trained on past hiring data from a male-dominated industry. What type of bias is this an example of?  

- A) Pre-existing Social Bias  
- B) Technical Bias  
- C) Emergent Social Bias  
- D) No Bias Present  

<details>  
<summary>Reveal Answer</summary>  

Answer: A) Pre-existing Social Bias  

This bias originates from societal inequalities reflected in historical hiring data.  
</details>  

<a>
</a>

---  

<a>
</a>

#### **Question 2:**  ❓
An AI-powered chatbot gradually starts using offensive language after interacting with online users who repeatedly expose it to toxic content. What type of bias does this represent?  

- A) Pre-existing Social Bias  
- B) Technical Bias  
- C) Emergent Social Bias  
- D) Algorithmic Efficiency Bias  

<details>  
<summary>Reveal Answer</summary>  

Answer: C) Emergent Social Bias  

The chatbot learns bias over time from user interactions, rather than being biased from the start.  
</details>

<a>
</a>

---

<a>
</a>

### **Popcorn Hack #1:**  

Think of a real-world example where a computer system has shown bias. It could be something you've read about, experienced, or imagined.  

#### Question: 
Describe the biased system, explain what type of bias it represents (**Pre-existing Social Bias, Technical Bias, or Emergent Social Bias**), and suggest one way to reduce or fix the bias.  

<details>  
<summary>Example Response</summary>  

"A facial recognition system fails to accurately recognize darker-skinned individuals. This is an example of **Technical Bias** because the training data lacked enough diversity. A way to fix this could be to ensure the dataset includes a wide range of skin tones before training the model."*  

</details>

<a>
</a>

---

<a>
</a>

## Real-World Examples of Computing Bias 🌍

### **Amazon's AI Hiring Tool**
- **Bias Type:** Pre-existing Social Bias  
- Amazon's AI recruitment system favored male candidates due to past hiring data.
- The system penalized resumes with words like "women" (e.g., *“Women’s Chess Club”*).
- **Impact:** Women were unfairly ranked lower for job opportunities.  
🔗 [Read More](https://www.ml.cmu.edu/news/news-archive/2016-2020/2018/october/amazon-scraps-secret-artificial-intelligence-recruiting-engine-that-showed-biases-against-women.html)

### **Google Translate Gender Bias**
- **Bias Type:** Technical Bias  
- When translating from gender-neutral languages, it introduced gender assumptions.
- Example:
  - Turkish: *O bir doktor* → English: *He is a doctor*  
  - Turkish: *O bir hemşire* → English: *She is a nurse*  
- **Impact:** Reinforced stereotypes about professions.  
🔗 [Read More](https://qz.com/1141122/google-translates-gender-bias-pairs-he-with-hardworking-and-she-with-lazy-and-other-examples)

### **Microsoft’s AI Chatbot Tay**
- **Bias Type:** Emergent Social Bias  
- Tay learned from Twitter interactions but was manipulated into tweeting racist and offensive content within 24 hours.
- **Impact:** AI can absorb and amplify human biases without proper safeguards.  
🔗 [Read More](https://fortune.com/longform/ai-bias-problem)

<img src="{{site.baseurl}}/images/tay.png" height="250" width="375">

<a>
</a>

---

## How to Mitigate these Biases?

<a>
</a>

### Pre-existing Social Biases

- **Bias Awareness Training**: Educate developers to recognize and address social biases in design and data collection.
- **Inclusive Design**: Involve diverse perspectives in algorithm design to reflect multiple viewpoints.
- **Bias Mitigation in Data Collection**: Regularly audit and balance data to avoid harmful stereotypes.

### Technical Bias

- **Transparent Algorithms**: Ensure algorithms are explainable and understandable to identify bias.
- **Bias Testing and Auditing**: Continuously test for fairness across demographics.
- **Improved Evaluation Metrics**: Use fairness-aware metrics to evaluate models and prevent group disadvantages.

### Emergent Social Bias

- **Human Oversight and Feedback Loops**: Implement real-time monitoring and feedback from diverse users to correct emergent biases.
- **User Moderation and Controls**: Enable users to flag harmful content, reducing bias amplification.
- **Algorithmic Accountability**: Adapt algorithms to evolving social norms and continuously adjust based on feedback.

---

### **Popcorn Hack #2:**  

Bias in computing can lead to unfair outcomes, but there are ways to reduce it  

#### **Question:**  
In the **financial industry**, an AI system used to approve loan applications unintentionally favors **male applicants** over **female applicants** because it was trained on past loan approval data, which reflected gender biases. This is an example of **Pre-existing Social Bias.**

Give **two ways** to mitigate this bias and make the system more fair.  

<details>  
<summary>Example Responses</summary> 

A music app recommends only popular songs and ignores lesser-known artists.

- 1️⃣ **Add more variety** to the recommendations.  

- 2️⃣ **Let users choose** what types of music they want to hear.

</details>

---

<a>
</a>

| **MCQ Topic** | **Connection to Computing Bias** |
|-----------|---------------------------------|
| **2.3: Extracting Information from Data** | Bias can emerge when datasets are skewed or incomplete, leading to biased AI predictions and decisions. |
| **3.12: Calling Procedures** | If biased functions or APIs are repeatedly used, the bias spreads throughout a system, such as facial recognition errors. |
| **3.17: Algorithmic Efficiency** | Some efficient algorithms may prioritize speed over fairness, reinforcing biases in search engines or recommendation systems. |
| **5.1: Beneficial and Harmful Effects** | Biased algorithms can offer personalized recommendations (benefit) but may also create filter bubbles and reinforce stereotypes (harm). |
| **5.2: Digital Divide** | Bias in computing can worsen accessibility gaps, such as voice recognition software struggling with non-native accents. |


---

### **Homework Hack: Understanding Bias in Computing**  

<a>
</a>

#### **Question:**  
Think of a system or tool that you use every day—this could be a website, app, or device. Can you identify any bias that might exist in the way the system works? 

#### **Task:**  
1. **Describe the system** you’re thinking of.  
2. **Identify the bias** in that system and explain why it might be biased. (Is it Pre-existing Social Bias, Technical Bias, or Emergent Social Bias?)  
3. **Propose one way** to reduce or fix the bias in that system.  

#### **Example:**  
*"I use a music app that suggests songs based only on what I already listen to. The system is biased because it limits me to a narrow selection of music. This is an example of **Algorithmic Bias**. To fix this, I would add an option for the app to recommend songs from different genres that I don’t normally listen to."*  

---






<!-- Utterances comment script -->
  <script src="https://utteranc.es/client.js"
          repo="ShawnRay09/computerbias"
          issue-term="url"
          theme="github-light"
          crossorigin="anonymous"
          async>
  </script>
