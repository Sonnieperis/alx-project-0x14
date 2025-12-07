# alx-project-0x14 — MoviesDatabase API Overview (TMDb)

## API Overview
The Movie Database (TMDb) is a community-driven movie and TV database that provides rich metadata, images, cast/crew details, search, discovery and trending endpoints. Developers use TMDb to build movie apps, search UIs, watchlists, and recommendation engines. TMDb exposes both v3 and v4 APIs with broad coverage for movies, TV shows, people, images and configuration data.

## Version
TMDb offers multiple API versions. The v3 REST API is the most feature-complete for content retrieval; v4 supports modern token-based authentication and some additional user-level operations. (See TMDb docs for which endpoints live on v3 vs v4.)

## Available Endpoints (main examples)
> The list below highlights the most commonly used endpoints for content retrieval. Each endpoint supports query params for paging, filtering and language.

- `GET /3/search/movie` — Search movies by title/keywords (query parameter `query`).  
- `GET /3/movie/{movie_id}` — Fetch movie details by TMDb movie ID (supports `append_to_response` to include extras).  
- `GET /3/discover/movie` — Discover movies using filters (genre, release date, sort options).  
- `GET /3/configuration` — Return base image URL and supported poster sizes (used to construct image URLs).  
- `GET /3/genre/movie/list` — List available movie genres.  
- `GET /3/person/{person_id}` — Get details on an actor/crew member.  
- `GET /3/trending/{media_type}/{time_window}` — Get trending movies/TV (e.g., `media_type=movie`, `time_window=week`).

## Request and Response Format
- TMDb APIs are RESTful and return **JSON** responses.
- Typical request (search movie example):
