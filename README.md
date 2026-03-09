# Forkify - Recipe Search Application

A modern, interactive recipe search application built with vanilla JavaScript, Parcel, and the Forkify API. Search for recipes, view detailed instructions, and save your favorite recipes to a personalized bookmarks collection.

> **Note**: This project is deployed on Netlify with continuous integration/continuous deployment (CI/CD) enabled for automatic updates.

🚀 **Live App**: https://forkify-jiit.netlify.app/

## Features

- 🔍 **Recipe Search**: Search from a vast database of recipes via the Forkify API
- 📖 **Recipe Details**: View complete recipe information including:
  - Ingredients with adjustable servings
  - Cooking instructions
  - Cooking time
  - Servings information
- 🔖 **Bookmarks**: Save and manage your favorite recipes locally
- 📄 **Pagination**: Browse search results with intuitive pagination
- ➕ **Upload Recipes**: Add your own custom recipes to the application
- 📱 **Responsive Design**: Optimized for desktop and mobile viewing
- 🎨 **Modern UI**: Clean and intuitive user interface with SASS styling

## Project Structure

```
forkify-app/
├── src/
│   ├── js/
│   │   ├── config.js           # API configuration and constants
│   │   ├── controller.js       # Application logic and event handling
│   │   ├── model.js            # Data management and API calls
│   │   ├── helpers.js          # Utility functions
│   │   └── views/              # View components
│   │       ├── view.js         # Base view class
│   │       ├── searchView.js   # Search input handling
│   │       ├── resultsView.js  # Recipe results display
│   │       ├── recipeView.js   # Detailed recipe display
│   │       ├── bookmarksView.js # Bookmarks management
│   │       ├── addRecipeView.js # Recipe upload form
│   │       ├── paginationView.js # Pagination controls
│   │       └── previewView.js  # Recipe preview cards
│   ├── sass/                   # SCSS stylesheets
│   │   ├── main.scss           # Main stylesheet
│   │   ├── _base.scss          # Base styles
│   │   ├── _components.scss    # Component styles
│   │   ├── _header.scss        # Header styles
│   │   ├── _preview.scss       # Preview card styles
│   │   ├── _recipe.scss        # Recipe detail styles
│   │   ├── _searchResults.scss # Search results styles
│   │   └── _upload.scss        # Upload form styles
│   └── img/                    # Image assets
├── index.html                  # Main HTML file
├── package.json                # Project dependencies and scripts
└── README.md                   # This file
```

## Installation

### Prerequisites
- Node.js (version 14 or higher)
- npm (comes with Node.js)

### Setup

1. **Clone or download the project**
   ```bash
   cd forkify-app
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm start
   ```
   The application will open in your default browser at `http://localhost:1234`

## Usage

### Searching for Recipes
1. Enter a recipe name or ingredient in the search bar
2. Press Enter or click the search button
3. Browse through the results with pagination controls
4. Click on a recipe to view full details

### Viewing Recipe Details
- Click any recipe from the search results to view:
  - Full ingredient list with quantities
  - Cooking instructions
  - Cooking time and servings
  - Adjust servings using the + and - buttons (ingredients will scale accordingly)

### Bookmarking Recipes
- Click the bookmark icon on any recipe to add it to your bookmarks
- View all bookmarked recipes from the bookmarks section
- Your bookmarks are saved to browser localStorage and persist between sessions

### Adding Custom Recipes
1. Click the "Add Recipe" button
2. Fill in the recipe form with:
   - Recipe title
   - Image URL
   - Publisher name
   - Cooking time
   - Servings
   - Ingredients (with quantities)
3. Submit the form to add your recipe

## Building for Production

To create an optimized production build:

```bash
npm run build
```

The built files will be generated in the `dist/` directory.

## Technologies Used

- **Frontend**: Vanilla JavaScript (ES6+)
- **Build Tool**: Parcel 2
- **Styling**: SASS/SCSS
- **API**: Forkify RecipeAPI
- **Storage**: Browser localStorage
- **Utilities**: core-js, fractional, regenerator-runtime

## API

The application uses the [Forkify API](https://www.notion.so/forkify-API-fd7b7269187341139ea5ee8942dcc820) for recipe data. The API endpoint is configured in `src/js/config.js`.

### Configuration

- `API_URL`: API endpoint for recipe requests
- `TIMEOUT_SEC`: Request timeout duration (10 seconds)
- `RES_PER_PAGE`: Recipes displayed per page (10)
- `MODAL_CLOSE_SEC`: Modal close animation duration (2.5 seconds)
- `KEY`: API key for recipe uploads

## Browser Compatibility

Works on all modern browsers including:
- Chrome 60+
- Firefox 60+
- Safari 12+
- Edge 79+

## Author

**Jitendra**

## License

ISC

## Notes

- Bookmarks are stored locally in your browser. Clearing browser data will clear saved bookmarks.
- Custom recipes are temporary and stored locally until the browser cache is cleared.
- The application requires an active internet connection to fetch recipes from the API.