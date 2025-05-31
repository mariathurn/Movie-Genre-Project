# 🎬 Multimodal Movie Genre Classification

This project explores the task of movie genre classification using **textual plot summaries** and **visual poster images**. A multimodal machine learning pipeline is implemented to compare the performance of text-only, image-only, and fused models.

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
