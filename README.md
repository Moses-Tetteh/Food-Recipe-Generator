# Food-Recipe-Generator
# Group 34: AI-Based Recipe Generator

---

## Introduction
This project introduces an AI-based system that generates cooking recipes directly from food images. The goal is to create a more intuitive and user-friendly experience, moving beyond traditional text-based recipe searches that require prior knowledge of a dish's name or ingredients.

---

## Problem Statement
Traditional recipe search methods are often text-based, posing a challenge for users who don't know the name of a dish. Furthermore, existing AI solutions for food recognition face issues with data quality and often lack a user-friendly mobile interface. This project addresses these challenges by using deep learning to create a flexible and intuitive system.

---

## Objectives
### General Objective
To create an AI-based system that can generate accurate cooking instructions, ingredient lists, and nutritional facts from a food image.

### Specific Objectives
* Utilize **deep learning** to analyze food images and identify key components, ingredient quantities, and cooking techniques.
* Incorporate **Natural Language Processing (NLP)** to convert identified ingredients and methods into structured recipe models.
* Develop a **user-friendly mobile application** to simplify the cooking experience.

---

## Methodology
The project employs an **Agile methodology** for a flexible, iterative development process.

### Data and Algorithms
* **Data Source**: The **Recipe1M+ dataset**, containing over 1 million recipes and 13 million food images, is used. The data is preprocessed to be compatible with deep learning models.
* **Algorithms**:
    * **Convolutional Neural Networks (CNNs)** for image feature extraction.
    * **Recurrent Neural Networks (RNNs)** and **Transformers** for generating recipe text from visual features.
    * **Multimodal Embeddings** to bridge the gap between images and text.
    * **Retrieval Augmented Generation (RAG)** to ensure the generated recipes are grounded in a real-world database and prevent "hallucinations."

### Evaluation Metrics
Performance is evaluated using both objective and subjective metrics.
* **Objective**: **BLEU** and **ROUGE** scores measure similarity to ground-truth recipes, while **Recall@K** assesses retrieval performance.
* **Subjective**: Human judges evaluate the quality, relevance, and coherence of the generated recipes.

---

## Development Environment
* **Frontend**: **Flutter** is used to build a cross-platform mobile application.
* **Backend**: **Django** handles server-side logic and integrates the AI models.
* **AI/ML**: **Python** with libraries like **PyTorch** for model building and training.
* **Data Storage**: **SQLite** is used for local data storage to enable offline access and quick retrieval of user history.

---

## System Architecture
The system follows a straightforward workflow:
1.  A user captures a food image using the **Flutter UI**.
2.  The image is sent to the **Django backend**.
3.  The backend uses a **CNN** to process the image and extract features.
4.  A **Transformer** model generates the recipe text from these features.
5.  The generated recipe, in **JSON** format, is sent back to the **Flutter UI** for display.
