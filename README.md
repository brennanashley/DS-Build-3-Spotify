# Data-science

- [Spotify Song Suggester API](#spotify-song-suggester-api)
  - [Usage](#usage)
    - [Suggestion of 30 songs based on one track_id given](#retrieve-30-songs-suggested-based-on-one-track_id-given)
    - [Radar chart image based on one track_id given](#radar-chart-image-based-on-one-track_id-given)

## Spotify Song Suggester API

A simple back-end Flask API to suggest spotify songs in the Spotify Song Suggester app
based on a track_id chosen by the user or a list of favorite songs

The spotify song suggester API uses the Spotify Audio Features dataset, uploaded to Kaggle joined with webscraped genre.

A KNN model was integrated into the Flask app. 
The app handles the requests, returning the appropriate JSON data.

---

## Usage

#### Retrieve 15 songs suggested based on one track_id given

### `[GET] /song/<track_id>`


**Parameters:** None

- request:track_id

**Returns:** JSON array containing the full details of the top 30 suggestions for a track_id given.

Example:

` https://spotify-ash.herokuapp.com/song/6VjBxj5OhlHqL4h5qwo6gL`

Returns:

    `[{"index":37134,"artist_name":"Moby","track_id":"3UigcTkkcvBLnq6GVCjE3i",
    "track_name":"Like a Motherless Child - Broken Places Remix","acousticness":0.00176,
    "danceability":0.573,"duration_ms":349747,"energy":0.858,"instrumentalness":0.301,
    "key":2,"liveness":0.208,"loudness":-6.335,"mode":1,"speechiness":0.0497,
    "tempo":101.984,"time_signature":4,"valence":0.241,"popularity":27,"genre":"electronic"}...`

---


#### Radar chart image based on one track_id given

### `[GET] /image/<track_id>`

**Parameters:** None

- request:track_id

**Returns:** Renders a radar chart image based on one track_id given.

Example:

`https://spotify-ash.herokuapp.com/image/6VjBxj5OhlHqL4h5qwo6gL`

Returns:

    `<img src='data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAoAAAAH
    gCAYAAAA10dzkAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAAPYQAAD
    2EBqD+naQAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9u
    My4xLjIsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy8li6FKAAAgAElEQVR
    4nOzdd1SUV/4G8GdmGIcyoKAGwYJKEcUOAoJGUowNsG3EbiyJRtPjJ
    tnklxizm03ZTdFolsTE2BNj1BUsaFBRULEQsaCUiFhRERmkw5TfHwi
    rhihl4M4783zO8WwOyMwjyxmeud/...`

---
