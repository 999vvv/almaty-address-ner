# Almaty Address NER

This project is part of a prototype system designed for use by a district-level city administration.  
Its goal is to automatically process chat messages submitted by residents, extract location-related information.

At the core of the system is a Named Entity Recognition (NER).

---

###  Named Entity Categories

The training data was manually annotated using [Label Studio](https://labelstud.io/) and includes the following entity types:

- STREET — Street names 
- PARK — Parks and public spaces
- PERESECHENIE — Intersections and avenues
- NUM — House or building numbers
The dataset includes a mix of anonymized real user messages and synthetically generated examples based on real patterns and phrasing.

The model was fine-tuned using the pre-trained spaCy model: `ru_core_news_lg`.

###  Annotation Example
<img width="1058" height="170" alt="image" src="https://github.com/user-attachments/assets/9708c180-0216-4a73-98bb-9f6d2efbc159" />


---
### 📓 Notebook

The full implementation — including data loading, model training, and prediction is available in the notebook:  
👉 [almaty_address_ner.ipynb](./almaty_address_ner.ipynb)


---

###  Example Output

Message: "По ул. Абая возле дома 28 не убирают мусор."  
  Абая → STREET  
  возле дома 28 → NUM
