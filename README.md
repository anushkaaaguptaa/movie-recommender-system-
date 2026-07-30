# 🎬 Movie Recommender System

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-1.47.1-FF4B4B.svg)
![Pandas](https://img.shields.io/badge/Pandas-2.3.1-150458.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

**An intelligent content-based movie recommendation system powered by machine learning**

</div>

---

## 📖 About The Project

The Movie Recommender System is an intelligent application that suggests movies similar to your favorites using advanced content-based filtering techniques. Built with Streamlit, it provides an intuitive interface where users can explore and discover new movies based on their preferences.

The system analyzes various movie attributes including genres, keywords, cast, crew, and overview to calculate similarity scores using cosine similarity, ensuring highly relevant recommendations.


## ✨ Features

- 🎯 **Smart Recommendations**: Get 5 personalized movie suggestions based on content similarity
- 🖼️ **Visual Interface**: Beautiful movie posters fetched in real-time from TMDb API
- 🔍 **Easy Search**: Type or select from a comprehensive dropdown of movies
- ⚡ **Fast Performance**: Optimized with pre-computed similarity matrices using pickle
- 🎨 **User-Friendly UI**: Clean and responsive Streamlit interface
- 🌐 **Real-Time Data**: Live poster fetching from The Movie Database


The application provides an interactive interface where you can:
1. Select a movie from the dropdown menu
2. Click "Show Recommendation" button
3. View 5 similar movies with their posters displayed in a grid layout

## 🛠️ Tech Stack

- **Frontend Framework**: [Streamlit](https://streamlit.io/) - For creating the interactive web interface
- **Data Processing**: [Pandas](https://pandas.pydata.org/) - For data manipulation and analysis
- **Machine Learning**: [Scikit-learn](https://scikit-learn.org/) - For computing cosine similarity
- **API Integration**: [TMDb API](https://www.themoviedb.org/documentation/api) - For fetching movie posters
- **Data Serialization**: Pickle - For storing pre-computed models
- **HTTP Requests**: [Requests](https://requests.readthedocs.io/) - For API calls

## 📋 Prerequisites

Before running this project, make sure you have:

- Python 3.8 or higher installed
- pip (Python package manager)
- An active internet connection (for fetching movie posters)

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/DevanshiGoyal/movie-recommender-system.git
   cd movie-recommender-system
   ```

2. **Install required dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Ensure required files are present**
   
   Make sure you have the following pickle files in the root directory:
   - `movies_dict.pkl` - Contains the processed movie dataset
   - `similarity.pkl` - Contains the pre-computed similarity matrix

## 💻 Usage

1. **Start the Streamlit application**
   ```bash
   streamlit run app.py
   ```

2. **Access the application**
   
   The app will automatically open in your default browser at `http://localhost:8501`

3. **Get recommendations**
   - Select or type a movie name in the dropdown
   - Click the "Show Recommendation" button
   - Browse through 5 recommended movies with their posters

## 📁 Project Structure

```
movie-recommender-system/
│
├── app.py                              # Main Streamlit application
├── movie-recommender-system.ipynb      # Jupyter notebook for model training
├── requirements.txt                    # Python dependencies
├── movies_dict.pkl                     # Serialized movie dataset
├── similarity.pkl                      # Pre-computed similarity matrix
└── README.md                           # Project documentation
```

## 🔍 How It Works

### 1. **Data Processing**
   - Movie dataset from TMDb 5000 Movies Dataset
   - Features extracted: genres, keywords, cast, crew, and overview
   - Text preprocessing and vectorization

### 2. **Similarity Computation**
   - Uses **Cosine Similarity** to measure movie similarity
   - Computes similarity based on content features
   - Matrix stored as pickle file for efficient loading

### 3. **Recommendation Engine**
   - Finds the selected movie's index in the dataset
   - Retrieves similarity scores for all movies
   - Sorts and returns top 5 most similar movies
   - Fetches posters from TMDb API for visual display

### 4. **Algorithm**
   ```python
   Cosine Similarity = (A · B) / (||A|| × ||B||)
   ```
   Where A and B are feature vectors of two movies

## 🔑 API Configuration

This project uses The Movie Database (TMDb) API for fetching movie posters. 
> **Note**: For production use, it's recommended to use environment variables to store API keys securely.

## 🎓 Dataset

The model is trained on the **TMDb 5000 Movies Dataset**, which includes:
- 4,800+ movies
- Movie metadata (genres, keywords, budget, revenue)
- Cast and crew information
- User ratings and popularity metrics


## 📝 Future Enhancements

- [ ] Add collaborative filtering for hybrid recommendations
- [ ] Implement user ratings and feedback system
- [ ] Add movie trailers and detailed information
- [ ] Include multiple recommendation algorithms
- [ ] Deploy on cloud platform (Streamlit Cloud, Heroku, AWS)
- [ ] Add user authentication and personalized profiles
- [ ] Implement advanced filtering (by genre, year, rating)
- [ ] Add movie search functionality
- [ ] Include trending and popular movies section

<div align="center">
</div>
