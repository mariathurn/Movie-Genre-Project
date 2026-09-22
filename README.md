# 🎬 Multimodal Movie Genre Classification

This project explores the task of movie genre classification using **textual plot summaries** and **visual poster images**. A multimodal machine learning pipeline is implemented to compare the performance of text-only, image-only, and fused models.

- Report:
[CCS2-Project-Thurn.pdf](https://github.com/user-attachments/files/32522960/CCS2-Project-Thurn.pdf)

### Abstract 
Automatic movie genre classification is a challenging task with applications in content recommendation, organization, and retrieval. While prior approaches have focused on either textual metadata or visual content, this study explores a multimodal method that combines plot summaries and poster images to predict a movie’s primary genre. I constructed a dataset of approximately 1,000 movies; each paired with a synopsis and a poster sourced from The Movie Database and assigned a single genre label per film. To represent the two modalities, I extracted TF-IDF features from the plot summaries and ResNet50-based CNN features from the posters. I trained separate classifiers—a logistic regression model for text and a support vector machine for images—and then applied late fusion by averaging their predicted probabilities. Evaluation was conducted using accuracy and macro-averaged F1-score across multiple genre classes. The fused model significantly outperformed both unimodal baselines, achieving 34.3% accuracy and a macro F1-score of 0.316. However, statistical testing showed that the two models did not make significantly different errors, suggesting limited complementary behaviour. Overall, the results demonstrate the value of combining modalities and highlight opportunities for future work in more advanced fusion strategies and multi-label classification.


## 📂 Project Structure

- `GenreClassification.ipynb` – Main notebook for preprocessing, feature extraction, modeling, and evaluation.
- `DownloadPosters.ipynb` – Script to download movie poster images using the TMDb API.
- `posters/` – Directory where downloaded poster images are saved.
- `balanced_movies_downsampled.csv` – Processed dataset with movie IDs, summaries, and genres.

## 🔧 Requirements

Install dependencies using:

```bash
pip install -r requirements.txt
```

How to Download Posters

To retrieve poster images:
	1.	Get a TMDb API key:
	•	Sign up at https://www.themoviedb.org/
	•	Go to API Settings
	•	Generate a v3 API key
	2.	Set up your environment:
	•	Replace YOUR_API_KEY in DownloadPosters.ipynb with your own API key.
	•	Make sure you have the requests library installed.
	3.	Run the notebook:
	•	Open DownloadPosters.ipynb in Jupyter Notebook.
	•	It will download and save posters in the posters/ directory.
