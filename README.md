# Movie App

I made this project to learn React. It's a small movie browser that shows popular movies, lets you search for any movie, and lets you save favorites. It gets its movie data from [The Movie Database (TMDB)](https://www.themoviedb.org/) API.

## Features

- Browse currently popular movies on the home page
- Search for movies by title
- Add movies to your favorites and remove them
- Favorites are saved in the browser (`localStorage`), so they're still there after a reload
- Separate Home and Favorites pages using React Router

## What I learned

- Building a UI out of reusable components (`MovieCard`, `NavBar`)
- Managing state with `useState` and side effects with `useEffect`
- Fetching data from a REST API with `async`/`await`, including loading and error states
- Sharing state across the app with the Context API (`MovieContext`)
- Client-side routing with `react-router-dom`
- Persisting data with `localStorage`
- Keeping API keys out of source code with environment variables

## Tech stack

- [React 19](https://react.dev/)
- [Vite](https://vite.dev/)
- [React Router](https://reactrouter.com/)
- [TMDB API](https://developer.themoviedb.org/)

## Running it locally

1. Clone the repo and install dependencies:

   ```bash
   git clone <this-repo-url>
   cd <repo-folder>/frontend
   npm install
   ```

2. Get a free API key from [TMDB](https://www.themoviedb.org/settings/api).

3. Copy `.env.example` to `.env.local` and put your key in it:

   ```
   VITE_TMDB_API_KEY=your_tmdb_api_key_here
   ```

4. Start the dev server:

   ```bash
   npm run dev
   ```

## Project structure

```
frontend/src/
├── components/   # MovieCard, NavBar
├── contexts/     # MovieContext (favorites state)
├── css/          # Stylesheets
├── pages/        # Home, Favorites
├── services/     # api.js (TMDB requests)
├── App.jsx
└── main.jsx
```

---

This product uses the TMDB API but is not endorsed or certified by TMDB.
