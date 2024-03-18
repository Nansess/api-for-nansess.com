# Music Artwork Search API

## Overview

The Music Artwork Search API allows users to retrieve artwork related to songs by providing the song title as a query. It simplifies the process of obtaining visually appealing representations associated with various music tracks.
### Search Artwork

- **Example Usage:**
  ```
  https://api.nansess.com/search/artwork?q=artwork_title
  ```

### Recommendations Endpoint

- **Example Usage:**
  ```
  https://api.nansess.com/search/spotify/recommendations?q=track_id&limit=20
  ```

### Track Endpoint

- **Example Usage:**
  ```
  https://api.nansess.com/search/spotify/track?q=trackID
  ```

### Playlist Endpoint

- **Example Usage:**
  ```
  https://api.nansess.com/search/spotify/playlist?q=playlistID&page=1
  ```

### Search Endpoint

- **Example Usage:**
  ```
  https://api.nansess.com/search/spotify/search?q=song_title
  ```

## Status Codes

- **200 OK**: Successful request.
- **400 Bad Request**: Missing or invalid parameters.
- **404 Not Found**: No tracks found for the given song title.
- **500 Internal Server Error**: Server error.


# Deezer Track Search API

## Overview

The Deezer Track Search API allows users to search for tracks on Deezer by providing the song title as a query. It provides an interface to integrate with Deezer's vast music catalog.

## Endpoint

```
GET https://api.nansess.com/search/deezer/track
```

## Usage

### Parameters

- **q** (required): The title of the song to search for on Deezer.

### Example

```bash
curl -X GET "https://api.nansess.com/search/deezer/track/sad"
```

### Response

```json
{
  "status": "success",
  "data": [
    {
      "name": "Sad Song",
      "artist": "Example Deezer Artist",
      "album": "Example Deezer Album",
      "preview_url": "https://api.nansess.com/deezer/example_preview",
      "deezer_url": "https://www.deezer.com/track/example_track_id"
    },
    // Additional tracks...
  ]
}
```

## Status Codes

- **200 OK**: Successful request.
- **400 Bad Request**: Missing or invalid parameters.
- **404 Not Found**: No tracks found for the given song title.
- **500 Internal Server Error**: Server error.

# Spotify Track Search by ID API

## Overview

The Spotify Track Search by ID API allows users to retrieve information about a specific track on Spotify using its unique track ID. This endpoint facilitates direct access to details such as the song name, artist, album, and additional metadata.

## Endpoint

```
GET https://api.nansess.com/search/uri/trackid/{spotify_track_id}
```

## Usage

### Path Parameters

- **spotify_track_id** (required): The unique identifier for the Spotify track.

### Example

```bash
curl -X GET "https://api.nansess.com/search/uri/trackid/spotify:track:5R8dQOPq8haW94K7mgERlO"
```

### Response

```json
{
  "status": "success",
  "data": {
    "name": "Example Song Title",
    "artist": "Example Artist",
    "album": "Example Album",
    "preview_url": "https://api.nansess.com/example_preview",
    "spotify_url": "https://open.spotify.com/track/5R8dQOPq8haW94K7mgERlO"
  }
}
```

## Status Codes

- **200 OK**: Successful request.
- **400 Bad Request**: Invalid or missing track ID.
- **404 Not Found**: No track found for the given Spotify track ID.
- **500 Internal Server Error**: Server error.

