# qasi

This Python package provides a function to query a language model (like Deepseek) with candidate context and questions, and returns short, clean answers.

Try: 
pip install qasi==0.1.5
python -m spacy download en_core_web_sm

How to use -> 

from qas import nlp
import os
cwd = os.getcwd()

questions = [
  "How many years of work experience do you have using React?",
  "How many years of experience do you have in IT?",
  "Do you have experience with Go?",
  "What is your level of proficiency in React?",
  "Do you have the following license or certification: AWS Certification?"
]

temp = {
    "industry": "Software Industry",
    "preferred_location": "Pune",
    "current_work_location": "Chennai"
}

answers = t.answer("{cwd}/sample2.pdf", temp, questions)

for q, a in zip(questions, answers):
    print(f"Q: {q}\nA: {a}\n")