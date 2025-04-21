Bias Detection and Mitigation in Text and Images
This project focuses on identifying and reducing bias in textual and visual content using machine learning (ML) and deep learning (DL) models. Bias in AI systems—especially gender and racial bias—can lead to unfair outcomes, and our system aims to make content analysis more fair, inclusive, and responsible.

🔍 Problem Statement
In many real-world applications—such as news articles, job recommendations, and search engines—AI models unintentionally learn and repeat biased patterns from historical or skewed data. For example:

Text: Sentences like “Women are too emotional to be leaders” reflect gender stereotypes.

Images: Google Images shows mostly men for the term “CEO” and mostly women for “nurse”.

These examples show the need for a system that can detect and mitigate such bias.

💡 Solution Overview
This project is divided into three key components:

A. Text Bias Detection
We used two techniques to classify news text as biased or unbiased:

TF-IDF + Logistic Regression:

TF-IDF (Term Frequency - Inverse Document Frequency) identifies important words in a sentence.

Logistic Regression is a supervised ML algorithm used to classify a sentence as biased or not.

BERT (Bidirectional Encoder Representations from Transformers):

A transformer-based deep learning model that understands sentence context bidirectionally to improve bias classification.

📌 Example: Input: “Women are too emotional to be leaders.”
Output: Biased (with confidence score)

B. Text Bias Mitigation
To rewrite biased sentences in a more neutral tone, we used:

T5 (Text-to-Text Transfer Transformer):

A transformer model that reformulates a biased input sentence into a fair and inclusive version.

📌 Example: Input: “Women are too emotional to be leaders.”
Output: “People of all genders are equally capable of being leaders.”

C. Image Bias Analysis
We analyzed image search results for job-related terms (e.g., “CEO”, “teacher”, “doctor”) using Google Images. The gender and racial distribution of the images was recorded and visualized to highlight stereotypes.

📌 Example:

“CEO” results → majority male images

“Nurse” results → majority female images

We used Python libraries like matplotlib and seaborn to generate visual bias graphs.

🛠️ Technologies Used
Python – Main programming language

scikit-learn – Logistic Regression, TF-IDF

Hugging Face Transformers – BERT and T5 models

Gradio – Web interface for interactive demo

Google Images – Source for image data

matplotlib, seaborn – For image bias visualization

📈 Results
Text bias detection accuracy: ~85%

T5 model generated effective and neutral rewrites

Image analysis revealed clear gender/professional stereotypes

📌 Example: Biased: “Men are better leaders.”
Rewritten: “Leadership is not based on gender.”

⚠️ Challenges
Difficulty in sourcing clean, labeled datasets for bias classification

Ambiguity in defining what counts as “biased”

Ensuring that T5 rewrites preserved original meaning while removing bias
