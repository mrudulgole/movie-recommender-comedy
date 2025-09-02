# 🎬 Hollywood Comedy Movie Recommender

A progressive web application that provides personalized movie recommendations based on user preferences through an interactive choice-based system.

## Features

### 🌟 Core Functionality
- **Interactive Movie Selection**: Users choose between pairs of comedy movies (50 total choices)
- **Personalized Recommendations**: Algorithm analyzes preferences to suggest 5 perfect movies
- **Comprehensive Database**: 74+ top-rated Hollywood comedy movies from IMDB lists
- **Progressive Design**: Modern, responsive interface with glassmorphism effects
- **Mobile-Friendly**: Fully responsive design that works on all devices

### 🎯 Recommendation Algorithm
The system uses intelligent preference analysis based on:
- **Director Preferences**: Tracks favorite directors and weights recommendations accordingly
- **Era Preferences**: Analyzes preferred decades (1960s-2020s) 
- **Rating Affinity**: Considers user's preference for highly-rated vs. accessible comedies
- **Genre Matching**: Ensures all recommendations stay within the comedy genre
- **Diversity**: Prevents duplicate selections and ensures variety in recommendations

### 📊 Movie Database
Curated from multiple IMDB "Best Comedy" lists including:
- Top 100 All Time Greatest Comedy Films
- Top 100 Comedies of 21st Century  
- Top 50 Comedy Movies of All Time
- Best Rated Comedy Movies

**Featured Movies Include:**
- Classic comedies: Monty Python and the Holy Grail, Airplane!, Blazing Saddles
- Modern hits: The Hangover, Superbad, Deadpool
- Cult favorites: The Big Lebowski, Office Space, Napoleon Dynamite
- Recent successes: Knives Out, Booksmart, Palm Springs

## How It Works

### 1. Welcome Screen
- Introduction to the recommendation system
- Clear instructions for users
- Start button to begin the experience

### 2. Movie Selection Process (50 Rounds)
- Two movies displayed side-by-side with:
  - Movie title and release year
  - Director information
  - IMDB rating
  - Brief description
- Progress bar showing completion status
- Question counter (1/50, 2/50, etc.)
- Smooth animations and hover effects

### 3. Recommendation Engine
The algorithm analyzes user choices across multiple dimensions:

```javascript
// Director Analysis
- Tracks which directors users consistently choose
- Weights recommendations based on director preferences
- Considers collaborative directors (e.g., Coen Brothers)

// Temporal Analysis  
- Groups movies by decade (1960s, 1970s, 1980s, etc.)
- Identifies preferred time periods
- Balances classic vs. modern preferences

// Quality Metrics
- Analyzes rating preferences (7.0+ vs 8.0+ vs accessibility)
- Considers critical acclaim vs. popular appeal
- Balances art-house vs. mainstream comedy

// Diversity Algorithm
- Ensures recommendations span different sub-genres
- Prevents over-recommendation of similar movies
- Includes both expected and surprising choices
```

### 4. Results Display
- 5 personalized movie recommendations
- Ranked by relevance to user preferences
- Detailed information for each recommendation:
  - Title, year, director
  - IMDB rating
  - Synopsis
- Option to restart the process

## Technical Implementation

### Frontend Architecture
- **Pure HTML/CSS/JavaScript** - No external dependencies
- **Progressive Enhancement** - Works without JavaScript (graceful degradation)
- **CSS Grid & Flexbox** - Modern layout techniques
- **CSS Custom Properties** - Consistent theming
- **Responsive Design** - Mobile-first approach

### Styling Features
- **Glassmorphism Design** - Modern frosted glass effects
- **Gradient Backgrounds** - Beautiful color transitions
- **Smooth Animations** - CSS transitions and transforms
- **Hover Effects** - Interactive feedback
- **Typography** - Clear, readable font hierarchy

### Data Structure
```javascript
{
  "title": "Movie Title",
  "year": 1994,
  "director": "Director Name",
  "rating": 7.3,
  "genre": "Comedy",
  "description": "Movie synopsis..."
}
```

### Browser Compatibility
- ✅ Chrome 60+
- ✅ Firefox 55+
- ✅ Safari 12+
- ✅ Edge 79+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## Usage Instructions

### For Users
1. **Open** the `movie-recommender.html` file in any modern web browser
2. **Read** the introduction and click "Start Movie Selection"
3. **Choose** your preferred movie from each pair (50 total choices)
4. **View** your personalized recommendations
5. **Restart** to try again with different choices

### For Developers
1. **Download** both files: `movie-recommender.html` and `movies_database.json`
2. **Customize** the movie database by editing the JSON file
3. **Modify** styling by updating the CSS variables
4. **Extend** functionality by adding new preference categories
5. **Deploy** by hosting the HTML file on any web server

## Customization Options

### Adding New Movies
```javascript
{
  "title": "New Comedy Movie",
  "year": 2023,
  "director": "Director Name", 
  "rating": 7.5,
  "genre": "Comedy",
  "description": "Description of the new movie..."
}
```

### Modifying Recommendation Algorithm
- Adjust scoring weights in the `generateRecommendations()` function
- Add new preference categories (actors, sub-genres, etc.)
- Change the number of recommendations (currently 5)
- Modify the number of selection rounds (currently 50)

### Styling Customization
```css
:root {
  --primary-gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  --accent-gradient: linear-gradient(45deg, #ff6b6b, #ffd93d);
  --glass-background: rgba(255, 255, 255, 0.1);
  --glass-border: rgba(255, 255, 255, 0.18);
}
```

## File Structure
```
📁 Movie Recommender/
├── 📄 movie-recommender.html    # Main application file
├── 📄 movies_database.json      # Movie data (optional external file)
└── 📄 README.md                 # This documentation
```

## Performance Optimizations
- **Efficient Random Selection** - Prevents duplicate movie pairs
- **Lazy Loading** - Recommendations calculated only when needed
- **Minimal DOM Manipulation** - Smooth performance on mobile devices
- **CSS-only Animations** - Hardware-accelerated transitions
- **Optimized Images** - No external image dependencies

## Future Enhancements
- 🎭 **Multiple Genres** - Expand beyond comedy (drama, action, sci-fi)
- 🎬 **Movie Trailers** - Embed YouTube trailers for recommendations
- 👥 **Social Sharing** - Share recommendation lists with friends
- 📱 **PWA Features** - Offline support and app-like experience
- 🔄 **Preference Learning** - Remember user preferences across sessions
- 🎯 **Advanced Filtering** - Filter by decade, rating, or director
- 📊 **Analytics Dashboard** - Show preference breakdown and statistics

## Credits
- **Movie Data**: Sourced from IMDB Top Comedy Lists
- **Design Inspiration**: Modern glassmorphism and gradient trends
- **Icons**: Unicode emoji characters for broad compatibility

## License
This project is open source and available under the MIT License.