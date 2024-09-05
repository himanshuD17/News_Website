# News_Website

This is a simple news website that fetches and displays news articles using the [News API](https://newsapi.org). The website is built using HTML, CSS, JavaScript, and the API to provide users with the latest news based on their search queries and navigation options.

## Features

- Fetches and displays news articles from News API.
- Allows users to search for news by keyword.
- Predefined categories such as Finance, Cricket, and Politics.
- Responsive layout with a clean and modern design.
- Dynamic content loading and rendering of articles.
- User can click on articles to view the full news on an external website.

## Tech Stack

- **HTML**: Structure of the website.
- **CSS**: Styling using custom styles and responsive design.
- **JavaScript**: Fetching news from API and dynamically displaying articles.
- **API**: [News API](https://newsapi.org) used to fetch the latest news.

## How It Works

1. **News Fetching**: 
   - On page load, news about "India" is fetched from the News API.
   - Users can click on navigation items (Finance, Cricket, Politics) to fetch news relevant to those categories.
   - Users can also search for any topic using the search bar.

2. **Dynamic Rendering**: 
   - The fetched news articles are displayed as cards, showing the title, source, publication date, and description.
   - If the article has an image, it is displayed; otherwise, the article is skipped.
   - Clicking on a news card will open the full article in a new tab.

## Project Structure

- `index.html`: The main structure of the website including navigation, search bar, and the container for displaying news cards.
- `style.css`: Styling for the website, including responsive design, card styles, and hover effects.
- `script.js`: JavaScript file to fetch news from the API, handle navigation clicks, and search functionality.

## API Usage

The website uses the News API to fetch the latest news articles. Below is an example of how the API is called in the code:

```js
const API_KEY = "your_api_key";
const url = "https://newsapi.org/v2/everything?q=";

async function fetchNews(query) {
    const res = await fetch(`${url}${query}&apiKey=${API_KEY}`);
    const data = await res.json();
    bindData(data.articles);
}
```

## Setup Instructions

1. Clone the repository or download the code.
2. Replace the `API_KEY` in the `script.js` file with your own key from [News API](https://newsapi.org).
3. Open the `index.html` file in your browser to view the website.

## License

This project is licensed under the MIT License.
