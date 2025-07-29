

🎬 Movie Recommender System using Cosine Similarity

A "Content-Based Movie Recommendation System" that uses **TF-IDF Vectorization** and **Cosine Similarity** to suggest similar movies based on genres, cast, keywords, and crew.


🚀 Features

* Reads and merges movie metadata, credits, and keywords datasets
* Cleans and transforms features like cast, genres, keywords, and crew
* Uses **TF-IDF Vectorization** to convert text features into numeric vectors
* Computes **cosine similarity** between movies
* Recommends top 5 similar movies based on the selected input movie

---

## 📁 Project Structure

```
Movie-Recommender-System/
├── Movie recommender system finalized.ipynb  # Jupyter notebook containing the full implementation
⚙️ How It Works

1. **Load Datasets**: Load `credits.csv`, `keywords.csv`, and `movies_metadata.csv`.
2. **Data Preprocessing**:

   * Merge datasets
   * Select important features like title, genres, keywords, cast, crew, and overview
   * Transform JSON-like columns using `ast.literal_eval`
   * Extract top 3 cast members and the director
   * Combine relevant text features into a `tags` column
3. **Vectorization**:

   * Use `TfidfVectorizer` with unigrams and bigrams
   * Stop words removed
   * Max features = 200
4. **Similarity Calculation**:

   * Calculate cosine similarity between movie vectors
5. **Recommendation**:

   * Input a movie title
   * Return 5 most similar movies based on cosine similarity scores
 
 📤 Input

```python
recommend('Titanic')
📈 Output

```
Similar movie recommendations:
1. The Notebook
2. Pearl Harbor
3. Romeo + Juliet
4. Atonement
5. The Great Gatsby
```
 🧠 Techniques Used

* Pandas & NumPy for data wrangling
* `ast.literal_eval` for parsing stringified JSON
* `TF-IDF Vectorizer` from scikit-learn
* `Cosine Similarity` for finding closeness between movies
* Content-based filtering logic

---

## 💡 Suggested Improvements

* Add GUI using Streamlit or Flask
* Use genres/cast/overview weighting
* Extend with collaborative filtering for hybrid recommendations
