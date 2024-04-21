# NaN (Nocturnal Access Network)

## Introduction
Welcome to the documentation for NaN (Nocturnal Access Network) This API provides endpoints to access data from Spotify and Tidal, Apple Music, without rate limits and unlimited requests

## Base URL
All endpoints are relative to the base URL: `https://api.nansess.com/search/`

## Authentication
[No Authentication is needed for Now, if any Larger Projects Plan to use my API, please just credit me Authentication might occur in the future]

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
- **Example Usage:** `https://api.nansess.com/search/spotify/search?q=song_title`

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
