# Music Recommender System 🎵

## Overview

This application is a **Music Recommender System** built using **Streamlit** and **Spotipy**. It provides song recommendations based on the cosine similarity of song lyrics. Recommended songs are displayed along with their album covers fetched from Spotify.

## Libraries and Tools Used

### Frontend
- **Streamlit**: A Python library used for building the web interface.
- **Spotipy**: A Python library for accessing the Spotify Web API to fetch album covers.

### Backend
- **pandas**: For data handling and preprocessing.
- **nltk**: For natural language processing and text tokenization.
- **scikit-learn**: For text vectorization and calculating cosine similarity.
- **pickle**: For saving and loading preprocessed data and similarity matrices.

## Setup and Running the Application

### Environment Setup

1. **Clone the Repository**

    ```bash
    git clone https://github.com/Bhagwan-D-GoD/Music_Recommendation.git
    ```

2. **Create a Virtual Environment**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. **Install Dependencies**

    ```bash
    pip install -r requirements.txt
    ```

    ```

4. **Prepare the Data**

    Ensure you have the preprocessed data files:
    - `df`: A DataFrame of songs with lyrics and other information.
    - `similarity`: A cosine similarity matrix between the songs.

    If these files are not available, generate them using the script provided in `data_preprocessing.py`.

5. **Run the Application**

    ```bash
    streamlit run app.py
    ```

    The application will be available at `http://localhost:8501` by default.

## Approach and Thought Process

1. **Text Preprocessing**:
   - **Text Cleaning**: Cleaned and processed song lyrics using `nltk` for tokenization and stemming.
   - **Vectorization**: Converted lyrics into numerical vectors using `TfidfVectorizer`.

2. **Recommendation System**:
   - **Cosine Similarity**: Calculated similarities between songs based on their lyrics to recommend similar songs.
   - **Spotify Integration**: Used `Spotipy` to fetch album covers for recommended songs.

3. **Streamlit Application**:
   - **User Interface**: Built a simple and interactive interface using Streamlit to select songs and view recommendations.
   - **Display Recommendations**: Showed recommended songs along with their album covers in a responsive layout.

4. **Error Handling**:
   - **Fallback Images**: Provided a fallback image if album cover retrieval fails.
   - **Empty Recommendations**: Handled cases where no recommendations are available gracefully.

## Future Enhancements

- **Enhanced Recommendations**: Improve the recommendation algorithm with additional features or models.
- **User Authentication**: Add user authentication to save and manage user-specific preferences.
- **UI Improvements**: Enhance the user interface for a better user experience.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Streamlit](https://streamlit.io/)
- [Spotipy](https://spotipy.readthedocs.io/en/2.22.1/)
- [pandas](https://pandas.pydata.org/)
- [nltk](https://www.nltk.org/)
- [scikit-learn](https://scikit-learn.org/)
- [Spotify API](https://developer.spotify.com/)

