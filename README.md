# Drug-Recommendation-System


## Introduction
This Report summarizes the development and implementation of a drug recommendation system based on user symptoms and medical conditions. The system integrates multiple recommendation techniques—collaborative filtering, content-based filtering, and a hybrid approach—to provide personalized drug recommendations. The goal is to assist users in finding suitable treatments based on their described symptoms and conditions.

## Approach
The drug recommendation system utilizes NLP, ML, and collaborative filtering techniques to generate recommendations. The primary steps in the development of this system include:

### Data Collection: The dataset used for training consists of drug names, their associated conditions, user ratings, and drug descriptions. Source : https://www.kaggle.com/datasets/jessicali9530/kuc-hackathon-winter-2018/data


### Model Selection: The system utilizes Sentence-BERT (a variant of BERT optimized for sentence embeddings) to generate embeddings for drug names and condition descriptions. These embeddings allow the system to compute semantic similarities between user input and drug descriptions, forming the basis for content-based recommendations.

### Recommendation Techniques:
- Content-Based Filtering: This method generates recommendations based on the similarity between user input (symptoms or conditions or reviews) and pre-encoded drug descriptions using cosine similarity.
- Collaborative Filtering: Using a matrix factorization approach, drugs are recommended based on patterns of ratings or interactions between users and drugs. This allows the system to recommend drugs that are     
   popular for specific conditions.
- Hybrid Approach: The system combines content-based and collaborative filtering techniques, giving a weighted score to each, allowing for more comprehensive recommendations.

### Methods Used 

- Sentence-BERT: Used for creating embeddings of user input (symptoms) and drug descriptions, enabling semantic similarity comparisons.
- Cosine Similarity: Used to compute similarity between input symptoms and drug embeddings for content-based recommendations.
- Collaborative Filtering: Based on condition-drug interactions, using cosine similarity to find similar conditions and their most highly-rated drugs.

### Challenges Faced

During the development of this recommendation system, several challenges were encountered:

- Data Sparsity: Some conditions had very few drugs with available ratings, leading to sparse matrices that made collaborative filtering challenging. This was addressed by using hybrid methods that blend content-based recommendations with collaborative filtering.



### Insights Derived

- Hybrid Methods: Combining content-based and collaborative filtering methods yields more robust recommendations. Content-based methods work well when there is sufficient drug description data, while collaborative filtering performs better in situations where user ratings provide rich interaction data.
- Personalization: The system provides highly personalized recommendations based on user-provided symptoms. However, user experience could be improved by incorporating feedback loops, where users can refine their symptom descriptions or select conditions manually.
- Data Quality: The quality of the recommendations depends heavily on the quality and quantity of the dataset. For example, rare conditions(like pulmonary edema) may not have enough data to generate meaningful collaborative recommendations.


### Strengths
- Hybrid Approach: The hybrid model increases the recommendation accuracy by combining the strengths of both content-based and collaborative filtering methods.
- Scalability: The model is scalable and can be easily adapted to different drug datasets or expanded with additional features, such as user demographics.
- Personalization: The system tailors its recommendations based on the user’s input, providing personalized drug suggestions.


### Limitations
- Condition Detection: The system currently uses a placeholder for condition detection, which limits its effectiveness. More sophisticated symptom-to-condition mapping methods are needed for better results.
- Data Sparsity in Collaborative Filtering: Some conditions and drugs may have very few ratings or interactions, making collaborative filtering less effective. The hybrid approach mitigates this to some extent, but challenges remain.
- Dependency on Data Quality: The quality of the recommendations is heavily dependent on the quality and completeness of the drug and condition data.



### Future Work

- Improved Condition Detection: Implement more advanced NLP techniques to automatically detect conditions from user input, possibly through symptom classification or mapping to medical ontologies.
- User Feedback Integration: Incorporate user feedback to improve recommendation accuracy over time.
- We can enhance the recommendation system by implementing user login functionality, tracking their drug usage and preferences, and incorporating user feedback to refine recommendations based on their history and   interactions with the system.
- Model Optimization: Experiment with other models, such as transformers trained specifically for medical data, or fine-tune pre-trained models like BioBERT for better accuracy in the medical domain.


### Conclusion
The drug recommendation system developed offers a promising approach to personalized healthcare, leveraging hybrid recommendation techniques to suggest drugs based on user-described symptoms. While there are still challenges to address, particularly around condition detection and data sparsity, the system provides a solid foundation for further development and deployment.

### Screenshots and Demo
![Screenshot 2024-12-03 194924](https://github.com/user-attachments/assets/5238f748-874f-4edf-b47d-3aac43ab243d)

![Screenshot 2024-12-03 194952](https://github.com/user-attachments/assets/e1150c2a-7fb4-4a0a-8d9a-19988098af1c)


![Screenshot 2024-12-03 195137](https://github.com/user-attachments/assets/6a421c78-52b6-4572-ae02-018a378549ab)

![Screenshot 2024-12-03 195153](https://github.com/user-attachments/assets/9fd492c0-78cc-45d7-91e3-1a7b81c67ea0)

