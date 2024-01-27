# Music Artwork Search API

## Overview

The Music Artwork Search API allows users to retrieve artwork related to songs by providing the song title as a query. It simplifies the process of obtaining visually appealing representations associated with various music tracks.

## Endpoint

```
GET https://api.nansess.com/search/artwork
```

## Usage

### Parameters

- **q** (required): The title of the song to search for artwork.

### Example

```bash
curl -X GET "https://api.nansess.com/search/artwork?q=example_song_title"
```

### Response

```json
{
  "status": "success",
  "data": [
    {
      "name": "Let Me Have You",
      "artist": "Costa Azul Quartet, Jazz Harmony Guitar Connection",
      "image": "https://api.nansess.com/kcZDVsoYY",
      "album": "We Fight To Live"
    },
    {
      "name": "Slidin' (feat. Kodak Black)",
      "artist": "Jason Derulo, Kodak Black",
      "image": "https://api.nansess.com/7nrU89aXVp",
      "album": "Slidin' (feat. Kodak Black)"
    },
    {
      "name": "Let Me Live My Life",
      "artist": "Saint Asonia",
      "image": "https://api.nansess.com/H3444xeGt_",
      "album": "Saint Asonia"
    },
    {
      "name": "Have You Met Miss Jones? - Live",
      "artist": "Chet Baker",
      "image": "https://api.nansess.com/p7eLlnNOKT",
      "album": "Live in London"
    }
  ]
}
```

## Status Codes

- **200 OK**: Successful request.
- **400 Bad Request**: Missing or invalid parameters.
- **404 Not Found**: No artwork found for the given song title.
- **500 Internal Server Error**: Server error.


# Spotify Track Search API

## Overview

The Spotify Track Search API enables users to search for tracks on Spotify by providing the song title as a query. It allows for seamless integration with Spotify to retrieve information about specific songs.

## Endpoint

```
GET https://api.nansess.com/search/spotify/track
```

## Usage

### Parameters

- **q** (required): The title of the song to search on Spotify.

### Example

```bash
curl -X GET "https://api.nansess.com/search/spotify/track/example_title"
```

### Response

```json
{
  "status": "success",
  "data": [
    {
      "name": "Example Song Title",
      "artist": "Example Artist",
      "album": "Example Album",
      "preview_url": "https://api.nansess.com/example_preview",
      "spotify_url": "https://open.spotify.com/track/example_track_id"
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
curl -X GET "https://api.nansess.com/search/deezer/track?q=sad"
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

