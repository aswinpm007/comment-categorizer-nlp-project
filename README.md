🎉 Comment Categorizer & Reply Assistant

A simple project to classify comments using AI

🌟 1. What Is This Project?

People write many types of comments on videos, posts, and pictures.
Some comments are good, some are bad, some are questions, and some are just spam.

This project is a small AI tool that can:

✔ Read a comment
✔ Understand what type it is
✔ Put it in the correct group (category)
✔ Give a simple reply message

This helps creators reply to comments easily.



🎯 2. What The Project Can Do

Our AI can find these 8 types of comments:

Praise – Good comments

Support – Encouraging comments

Constructive Criticism – Helpful negative comments

Hate/Abuse – Bad/fight comments

Threat – Comments with danger

Emotional – Feelings or memories

Spam – Ads, promotions

Question/Suggestion – Asking something or giving ideas


📁 3. What You Need

You only need:

✔ Google Colab (free tool)
✔ A CSV file with comments and labels
✔ Internet connection

🧠 4. How To Open Google Colab (Step-by-Step)

Go to: https://colab.research.google.com

Click New Notebook

A page will open with cells

We write code in these cells

Press Shift + Enter to run each cell


📘 5. How To Upload the Dataset (CSV)

Look at the left side menu

Click the Folder icon

Click the Upload button (⬆️)

Choose your file:
comments_dataset.csv

It will appear in the list

That's it.

📚 6. Code Explanation (Very Simple)

Below is what each cell in your Colab does.
This explains why we write that code.

🟦 Cell 1 — Load CSV File

import pandas as pd
df = pd.read_csv("comments_dataset.csv")
print("Rows:", len(df))
display(df.head(10))
df['label'].value_counts()


✔ Reads the CSV file
✔ Shows first 10 comments
✔ Counts each category


🟦 Cell 2 — Download NLTK Tools
import re
import nltk
# Required downloads for latest NLTK
nltk.download('punkt')
nltk.download('punkt_tab')
nltk.download('stopwords')
nltk.download('wordnet')
nltk.download('averaged_perceptron_tagger')
nltk.download('averaged_perceptron_tagger_eng') 
nltk.download('omw-1.4')

✔ Downloads English tools
✔ Needed for cleaning text


🟦 Cell 3 — Text Cleaning Functions

✔ Removes symbols
✔ Makes words simple
✔ Changes words to root form ("running" → "run")

🟦 Cell 4 — Make Labels Into Numbers

✔ Converts categories to numbers
✔ Easy for machine learning

🟦 Cell 5 — Train The Model

✔ Uses Logistic Regression (simple, good model)
✔ Learns from comments
✔ Understands patterns

🟦 Cell 6 — Test Model + Show Charts

✔ Shows accuracy
✔ Shows confusion matrix
✔ Shows label distribution

Teacher will love this part.

🟦 Cell 7 — Save Model

✔ Model saved as:

tfidf_lr_model.pkl

label2id.pkl

id2label.pkl

🟦 Cell 8 — Categorize Whole Dataset

✔ AI predicts each comment
✔ Adds suggested reply
✔ Saves new CSV file:

👉 categorized_comments_with_replies.csv

🟦 Cell 9 — Gradio App (UI)

✔ Makes a small website
✔ You can type a comment
✔ It predicts category and reply

🎨 7. What the Gradio App Does

You get:

A text box

A button

Two outputs

Category

Suggested reply


💾 8. How To Download Files From Colab

Go to the left folder menu

Right-click any file

Click Download

Files to download:

✔ tfidf_lr_model.pkl
✔ label2id.pkl
✔ id2label.pkl
✔ comments_dataset.csv



📥 Sample Input and Output Examples

Below are simple examples to show how the Comment Categorizer works.

Example 1

Input Comment:
Amazing job! I loved this video.

Predicted Category:
Praise

Suggested Reply:
Thanks so much! 😊 We’re thrilled you enjoyed it.

Example 2

Input Comment:
The idea is good but the sound quality needs improvement.

Predicted Category:
Constructive Criticism

Suggested Reply:
Thanks for the feedback — could you tell us which part you mean so we can improve?

Example 3

Input Comment:
This is trash. Stop making videos.

Predicted Category:
Hate/Abuse

Suggested Reply:
We’re sorry you feel that way. Please keep feedback respectful.

Example 4

Input Comment:
Can you make a video on space next time?

Predicted Category:
Question/Suggestion

Suggested Reply:
Great question/suggestion — we’ll consider it!

Example 5

Input Comment:
Follow me for free gifts!!!

Predicted Category:
Spam

Suggested Reply:
This comment appears promotional and may be removed according to our policy.

Example 6

Input Comment:
This reminded me of my childhood. Thank you.

Predicted Category:
Emotional

Suggested Reply:
Thank you for sharing — we’re glad it resonated with you.

Example 7

Input Comment:
You are doing great! Keep going!

Predicted Category:
Support

Suggested Reply:
Thanks for the encouragement — it keeps us going!




🌟 11. Why This Project Is Useful (Simple Words)

This tool helps:

✔ Save time
✔ Reply to comments faster
✔ Understand how people feel
✔ Find spam
✔ Learn Machine Learning basics






