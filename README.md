# NaN (Nocturnal Access Network)

## Introduction
Welcome to the documentation for NaN (Nocturnal Access Network). This API provides endpoints to access data from Spotify, Tidal, and Apple Music, without rate limits and unlimited requests.

## Base URL
All endpoints are relative to the base URL: `https://api.nansess.com/search/`

## Authentication
"No authentication is needed for now. If any larger projects plan to use my API, please just credit me. Authentication might occur in the future."

## Rate Limits
The only rate limits you may face are imposed by Cloudflare. This could occur if your project is large-scale. If you are encountering rate limiting by Cloudflare and would like to avoid it, please join our Discord server at [discord.gg/nanbot](https://discord.gg/nanbot) and open a ticket. We'll work it out together. Thank you.

### Future Endpoints
Endpoints for YouTube and Pandora are planned for future implementation.

## Endpoints

### Spotify Endpoints

#### 1. Recommendations Endpoint
- **URL:** `/spotify/recommendations`
- **Method:** `GET`
- **Parameters:**
  - `q`: Track ID
  - `limit`: Number of recommendations to return (default: 20)
- **Example Usage:** `https://api.nansess.com/search/spotify/recommendations?q=track_id&limit=20`

#### 2. Track Endpoint
- **URL:** `/spotify/track`
- **Method:** `GET`
- **Parameters:**
  - `q`: Track ID
- **Example Usage:** `https://api.nansess.com/search/spotify/track?q=track_id`

#### 3. Playlist Endpoint
- **URL:** `/spotify/playlist`
- **Method:** `GET`
- **Parameters:**
  - `q`: Playlist ID
  - `page`: Page number (default: 1)
  - `limit`: Number of playlists per page (default: 100)
- **Example Usage:** `https://api.nansess.com/search/spotify/playlist?q=playlist_id&page=2&limit=100`

#### 4. Search Endpoint
- **URL:** `/spotify/search`
- **Method:** `GET`
- **Parameters:**
  - `q`: Song title
  - `limit` (optional): Limit the number of search results (default: 5)
- **Example Usage:** 
  - [`https://api.nansess.com/search/spotify/search?q=song_title`](https://api.nansess.com/search/spotify/search?q=song_title)
  - Please note that you can also look up songs by ISRC (International Standard Recording Code) using the format `q=isrc:YOUR_ISRC_CODE`.
    - [`https://api.nansess.com/search/spotify/search?q=isrc:USA2P2413259`](https://api.nansess.com/search/spotify/search?q=isrc:USA2P2413259)

#### 5. User Playlist Endpoint
- **URL:** `/spotify/user`
- **Method:** `GET`
- **Parameters:**
  - `q`: User ID
- **Example Usage:** `https://api.nansess.com/search/spotify/user?q=user_id`

### Tidal Endpoints

#### 1. Playlist Endpoint
- **URL:** `/tidal/playlist`
- **Method:** `GET`
- **Parameters:**
  - `q`: Playlist ID
  - `page`: Page number
- **Example Usage:** `https://api.nansess.com/search/tidal/playlist?q=playlist_id&page=number`

#### 2. Track Endpoint
- **URL:** `/tidal/track`
- **Method:** `GET`
- **Parameters:**
  - `q`: Track ID
- **Example Usage:** `https://api.nansess.com/search/tidal/track?q=track_id`

#### 3. Album Endpoint
- **URL:** `/tidal/album`
- **Method:** `GET`
- **Parameters:**
  - `q`: Album ID
  - `limit`: Number of albums to return (default: 50)
- **Example Usage:** `https://api.nansess.com/search/tidal/album?q=album_id&limit=number`

#### 4. Search Endpoint
- **URL:** `/tidal/search`
- **Method:** `GET`
- **Parameters:**
  - `q`: Song title
- **Example Usage:** `https://api.nansess.com/search/tidal/search?q=song_title`

### Apple Music Endpoints

#### 1. Track Endpoint
- **URL:** `/apple/track`
- **Method:** `GET`
- **Parameters:**
  - `q`: Track ID
- **Example Usage:** `https://api.nansess.com/search/apple/track?q=track_id`

#### 2. Search Endpoint
- **URL:** `/apple/search`
- **Method:** `GET`
- **Parameters:**
  - `q`: Query
  - `limit` (optional): Limit the number of search results (default: 5)
- **Example Usage:** `https://api.nansess.com/search/apple/search?q=query`

## Finished Support for playlists and albums coming soon for Apple Music
