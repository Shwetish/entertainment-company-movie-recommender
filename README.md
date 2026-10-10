# entertainment-company-movie-recommender
An automated recommendation algorithm for an online movie-watching platform to optimize its media catalog and suggest highly rated titles based on user viewing footprints and a -9 to +9 rating scale.

# Online Movie Recommendation Engine

## 1. Business Problem
### 1.1. What is the business objective?
An online movie-watching platform (The Entertainment Company) wants to curate and improve its movie collection by showcasing highly rated titles and automating personalized movie recommendations based on user viewing footprints and sentiment scores (measured on a scale from -9 to +9).

### 1.2. Are there any constraints?
* **Rating Scale Handling:** The custom rating scale ranging from -9 to +9 requires specific data normalization and handling of negative vs. positive sentiment feedback.
* **Real-time Performance:** Recommendations must be computed and served quickly to maintain a seamless streaming platform UX.
* **Catalog Quality:** Ensuring niche or newly added movies receive fair exposure alongside blockbuster titles.

---

## 2. Data Dictionary
| Feature Name | Data Type | Description |
| :--- | :--- | :--- |
| `UserID` | Integer / Categorical | Unique identifier for each platform user. |
| `MovieID` | Integer / Categorical | Unique identifier for each movie in the collection. |
| `Rating` | Numeric (-9 to +9) | User feedback score indicating negative to positive sentiment towards a movie. |
| `Watch_Footprint` | Timestamp / Categorical | User viewing history, watch duration, or interaction logs. |

---

## 3. Exploratory Data Analysis (EDA)
* **3.1. Summary:** Comprehensive statistical overview of user ratings, active user counts, and movie catalog coverage.
* **3.2. Univariate Analysis:** Distribution of the -9 to +9 ratings, most/least viewed movies, and user activity frequency.
* **3.3. Bivariate Analysis:** Correlation between viewing duration and ratings, genre preferences across user segments, and rating distribution patterns.

---

## 4. Data Pre-processing & Data Mining
* **Data Cleaning:** Filtering out noise, resolving invalid user entries, and managing missing footprints.
* **Scale Transformation:** Rescaling or normalizing the unique -9 to +9 rating scale into standard bounds (e.g., 0 to 1 or -1 to +1) for algorithmic compatibility.
* **Matrix Factorization Preparation:** Constructing user-movie utility matrices for downstream machine learning models.

---

## 5. Model Building
* **Recommendation Algorithm:** Built a robust collaborative filtering and content-aware hybrid recommendation engine.
* **Model Training:** Utilized similarity measures and matrix factorization techniques tailored to the platform's rating distribution.
* **Evaluation:** Tested recommendation accuracy using metrics like RMSE, MAE, Precision@K, and Recall@K.

---

## 6. Business Benefits & Impact
* **Curated Catalog Management:** Highlights high-performing content and uncovers gaps in the platform's movie collection.
* **Personalized User Experience:** Increases watch-time and platform retention by surfacing movies aligned with individual viewing footprints.
* **Operational Efficiency:** Fully automates the recommendation pipeline, reducing manual content curation overhead.
