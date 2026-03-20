Screenwatch
Quick-lookup web app for movie and TV series ratings, powered by the Trakt and TMDB APIs. Search by title or browse trending and popular content. Single HTML file — no build tools required.
�
Load image
Features
Instant search — debounced as-you-type search across movies and TV shows, with filter toggles
Browse trending & popular — poster grid homepage with tabs for Trending Movies, Trending Shows, Popular Movies, and Popular Shows, including live watcher counts
Detail modal — click any title to see full metadata: Trakt rating and vote count, runtime, certification, genres, network, status, overview, and backdrop artwork
Poster art — fetched from TMDB and cached in memory for fast browsing
Direct links — jump straight to IMDb, TMDB, or Trakt for any title
Zero dependencies — single index.html file, no frameworks, no build step
Responsive — works on desktop and mobile
Screenshots
Browse Trending
Search Results
Detail Modal
�
Load image
�
Load image
�
Load image
Replace the placeholder images above with your own screenshots.
Setup
1. Get your API keys (free)
You'll need two free API keys:
Trakt Client ID
Sign in at trakt.tv
Go to trakt.tv/oauth/applications
Create a new application (use urn:ietf:wg:oauth:2.0:oob as the redirect URI)
Copy the Client ID from the app detail page
TMDB API Key
Sign up at themoviedb.org
Go to Settings → API
Request an API key (select "Developer" and fill in the form)
Copy the API Key (v3 auth)
2. Run locally
Just open index.html in your browser. On first load, click the gear icon and paste both keys. They're saved in your browser's localStorage so you only need to do this once.
3. Deploy to GitHub Pages
git init
git add index.html README.md
git commit -m "Initial commit"
git remote add origin git@github.com:YOUR_USERNAME/screenwatch.git
git push -u origin main
Then go to Settings → Pages in your repo and set the source to main / root. Your app will be live at:
https://YOUR_USERNAME.github.io/screenwatch/
How it works
Screenwatch is a client-side only app. All API calls are made directly from the browser:
Trakt API — provides search, trending/popular lists, ratings, metadata (genres, runtime, certification, network, status, overview)
TMDB API — provides poster images, backdrop artwork, and taglines
No data is sent to any server other than the Trakt and TMDB APIs. Your API keys are stored only in your browser's localStorage.
API Rate Limits
Both APIs are free and generous for personal use:
Trakt — 1,000 GET requests per 5 minutes
TMDB — ~50 requests per second
Screenwatch caches browse data and poster URLs in memory to minimise API calls during a session.
Roadmap
[ ] Watch tracking (requires Trakt OAuth)
[ ] Rotten Tomatoes / Metacritic scores via OMDB
[ ] Season and episode breakdown for TV shows
[ ] Watchlist management
[ ] PWA support with offline caching
License
MIT
Credits
Trakt API for ratings and metadata
TMDB API for poster and backdrop artwork
Built with vanilla HTML, CSS, and JavaScript
