# Analysis and Recommendation system for Netflix Data
This repository contains a comprehensive analysis of Netflix content data and the development of a recommendation system using machine learning. The project incorporates interactive dashboards built in Power BI and Tableau, along with a recommendation model that leverages text-based analysis for suggesting relevant content.

## Table of Contents
- [Overview](#overview)
- [Key Objectives](#key-objectives)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Repository Contents](#repository-contents)
- [Results and Insights](#results-and-insights)
- [Usage](#usage)
- [Contributing](#contributing)

## Overview
The project aims to explore and analyze Netflix's content catalogue using data visualization and machine learning techniques. It involves three main components:

1. **Interactive Dashboards:**
   - A Power BI dashboard providing insights into Netflix's content distribution, rating trends, and popular genres.
   - A Tableau dashboard that offers similar visualizations with additional customization and interactivity.
2. **Recommendation System:**
   - Built using natural language processing (NLP) techniques such as Bag of Words (BoW) and TF-IDF Vectorizer to recommend content based on text input.

## Key Objectives

1. **Data Analysis:**
   - Perform exploratory data analysis (EDA) to uncover patterns in Netflix's content data.
   - Provide insights into user preferences, popular genres, and content trends.
2. **Interactive Dashboards:**
   - Build user-friendly dashboards in Power BI and Tableau to visualize Netflix content distribution, trends, and performance metrics.
   - Enable interactive exploration of data for improved decision-making.
3. **Recommendation System:**
   - Develop a content-based recommendation system to suggest relevant movies and TV shows based on user input.
   - Compare the effectiveness of different techniques, such as Bag of Words (BoW) and TF-IDF, for generating accurate recommendations.
4. **Insights Delivery:**
   - Present actionable insights for enhancing Netflix's content strategy and improving user engagement.
  
## Dataset
The dataset used in this project comes from publicly available information about Netflix's catalog in Kaggle. It contains several columns, including:
- **Title**: The name of the movie or TV show.
- **Genre**: The genre(s) associated with the content.
- **Release Year**: The year the movie or TV show was released.
- **Rating**: The content rating (e.g., PG, R, etc.).
- **Duration**: The length of the content (for movies) or the number of seasons (for TV shows).
- **Language**: The primary language(s) of the content.

You can find the **Netflix Content Data** dataset in the `data` folder of this repository. If you prefer to download it yourself, ensure you get the dataset from Kaggle and place it in the `data` directory.

### Preprocessing Steps
- Removal of duplicate entries
- Filtering of sparse user-product interactions
- Normalization and preparation for models

## Technologies Used
The project is implemented using:
- **Programming Language:** Python
- **Libraries and Frameworks:**
   - Data Analysis: `pandas`, `numpy`
   - Data Visualization: `matplotlib`, `seaborn`
   - Machine Learning: `scikit-learn`
   - NLP Techniques: `TF-IDF`, `Bag of Words`
   - Similarity Metrics: `cosine_similarity`, `jaccard`
- **Dashboard Tools:**
   - **Power BI:** Interactive visualizations and insights for Netflix content.
   - **Tableau:** Advanced dashboards for exploring content trends and performance.
- **Other Tools:**
   - **Jupyter Notebook:** For conducting analysis and building the recommendation system.

## Repository Contents
### Dashboards
1. **Power BI Dashboard:**
   - Interactive visualizations of Netflix content distribution by genre, rating, and release year.
   - Files:
     - `Netflix Data Analysis Dashboard - Power BI.png`: Preview of the dashboard.
     - `Netflix_Content_Dashboard.pbix`: Power BI file with interactive visualizations.
2. . **Tableau Dashboard:**
   - Visual analysis of Netflix's catalog, including top content and trends.
   - Files:
     - `Netflix Data Analysis Dashboard.png`: Preview of the dashboard.
     - `Netflix Data Analysis Dashboard.twbx`: Tableau workbook with interactive visualizations.
### Recommendation System
- **Overview:** This section includes a recommendation system based on text analysis of Netflix titles. It uses TF-IDF and Bag of Words (BoW) models to recommend similar movies or TV shows based on textual descriptions.
- **Workflow:**
  1. Import Libraries and Data.
  2. Perform Exploratory Data Analysis (EDA) using data visualization.
  3. Build a **Content Recommendation System**.
  4. Use **BoW Model** and **TF-IDF Vectorizer** to recommend content.
- **Methods:**
  - The **BoW Model** is used for basic similarity calculations, but the **TF-IDF Vectorizer** produces more accurate results for content recommendations.
  - The **TF-IDF approach** outperforms BoW by generating relevant recommendations based on word frequency, reducing dimensionality issues.
  - The **Jaccard Similarity** metric was tested but proved slower and less accurate compared to **Cosine Similarity**.
- **Recommendation Systems:**
  - **Test System:** Recommends content based on the name of the movie or TV series.
  - **Recommendation System:** Recommends content based on a user-inputted text or sentence. This system offers a more flexible and accurate approach by analyzing the text and providing better results.

## Results and Insights
### Dashboards:
- **Power BI Dashboard**

The Power BI Dashboard offers a comprehensive and interactive analysis of Netflix's content. It provides valuable insights into various aspects, such as genres, ratings, and content release trends. This dashboard allows users to explore and understand the distribution of different genres, the popularity of content based on ratings, and the historical trends in content release.

- **Tableau Dashboard**

The Tableau Dashboard delivers a detailed and customizable analysis similar to the Power BI Dashboard. It offers users more options to explore and visualize Netflix's catalog. With its flexible interface, users can dive deep into the data, customize their views, and uncover unique insights into Netflix's content distribution and trends.

### Recommendation System
The recommendation system developed in this project demonstrates a significant enhancement in providing accurate and relevant content recommendations. There is no time difference between the different methods used because the most similar movies for each movie have been precalculated. However, each method produces different outcomes:

- **TF-IDF vs. BoW:** The "tf-idf" method produces more comparable and accurate results than the "BoW" method. While the boolean method can generate some relevant content based on the input words, the suggestions are not as accurate. The tf-idf technique, on the other hand, recommends numerous accurate films and television episodes and appears to function well. Furthermore, calculating jaccard similarity takes a long time compared to cosine similarity, which is much faster. Considering that it is more accurate and takes less time, tf-idf is unquestionably the best method to utilize.
- **Cosine Similarity:** The superiority of tf-idf is evident. Even with limited data, the tf-idf method yields numerous relevant outcomes. The "BoW" method fails to keep up because it takes significantly longer to calculate jaccard similarity than cosine similarity and produces poorer results. Due to the curse of dimensionality, short descriptions make data sparse, which is less useful in BoW.

We designed two recommendation systems for the project:
1. **Test System:** Recommendations were made according to the name of the movie/TV series provided.
2. **Recommendation System:** Recommendations were generated by analyzing the text or sentence provided. This system makes the search easier and provides better results than the first-designed system.

Overall, the TF-IDF Vectorizer, combined with cosine similarity, proves to be the most effective method for generating accurate and relevant recommendations quickly and efficiently. This approach enhances the user experience by delivering personalized content suggestions.


## Usage
To run this project on your local machine, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/HarshaEadara/Analysis-and-Recomendation-system-for-Netflix-Data.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Analysis-and-Recommendation-system-for-Netflix-Data
   ```
3. Install Dependencies:
Make sure you have Python installed. Then install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
4. Run the Notebook:
Open the Jupyter Notebook and execute the cells
   ```bash
   jupyter notebook Analysis_and_Recomendation_system_for_Netflix_Data.ipynb
   ```
5. Ensure the dataset `netflix_content_data.csv` is available in the `data` folder in the project directory.
6. Run the cells sequentially to execute the analysis.
7. Explore the Power BI and Tableau dashboards by opening the respective `.pbix` and `.twbx` files in Power BI and Tableau.

## Contributing
Contributions are welcome! If you have suggestions or improvements, feel free to fork this repository, make changes, and submit a pull request. Please ensure your code adheres to the project structure and is well-documented.


