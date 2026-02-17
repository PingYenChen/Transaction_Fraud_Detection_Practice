# 🛡️ Smart Fraud Detector – Catch Suspicious Money Moves

Hello! 👋  

Welcome to the project that tries to spot **fraudulent transactions** in mobile money and online payment systems.

**Project Goals:**  
Build a computer program that learns to recognise “this payment looks really strange” so people lose less money to scammers.

---

## Why does this matter to normal people?

Every year fraudsters trick people and companies out of **billions of dollars**.  
Common tricks include:

- taking over someone’s account  
- using stolen cards  
- sending money to fake “friends” or merchants  
- quickly emptying an account right after it receives money

A good fraud detector quietly watches millions of payments every second and can say:  
“Hey — this one doesn’t feel right. Let’s ask for extra proof or stop it.”

That small warning can save someone’s rent money, holiday savings, or business cash flow.

---

## What data are we using?

We are practising with a public dataset that contains **~6.3 million fake transactions** (you can download it free from Kaggle:https://www.kaggle.com/datasets/amanalisiddiqui/fraud-detection-dataset).

Important fact: only about **1 out of every 775 transactions** (~0.13%) is real fraud.  
→ That makes fraud **very rare and very hard to find** without accidentally blocking innocent people.

---

## What have we done so far? (Exploration phase)

In the file `analysis.ipynb` we:

- Loaded the huge dataset  
- Checked how much money usually moves  
- Saw which actions are most dangerous (almost all fraud happens in **TRANSFER** and **CASH_OUT**)  
- Made simple charts showing how normal vs fraud transactions look different  
- Confirmed there are almost **no fraud cases in PAYMENT** type  
- Noticed useful clues like:  
  → sender suddenly sends almost everything they have  
  → receiver account receives money and immediately becomes empty again

This “looking and understanding” step is super important — it’s like reading the crime scene before you start building the alarm system.

---

## The Machine Learning part – how the computer actually learns to catch fraud

We then use LogisticRegression to playaround and deployed by Streamlit~~~

Here’s what happens when we add machine learning:

1. We give the computer **millions of past examples** — most are “safe”, a few are labelled “fraud”.
2. The computer looks for hundreds of tiny patterns, for example:
   - “This person never sent money before and now sends a huge amount”
   - “The amount is normal, but the account balance goes from full → zero in one move.”
   - “Money goes to an account that was created yesterday.”

Popular algorithms people use for this job (you can try them later):

- Random Forest  
- XGBoost / LightGBM (very popular in fraud right now)  
- Simple neural networks  
- Sometimes even CatBoost or simple logistic regression as a strong baseline

The project is credicted to "Data Science with Onur", where I learned how to use data science and machine learning techniques for fraud detection.

Thanks for stopping by! 

