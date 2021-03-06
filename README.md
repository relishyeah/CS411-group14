# [Fractalist](https://quence-dev.github.io/fractalist) (Group 14)

# Project Description

The project creates a fractal Spotify playlist cover based on attributes of the music in a playlist, specifically valence, mode, and energy. Users would also be able to customize the cover by modifying various elements such as font and color. The fractal image can then be downloaded to the user’s device or automatically publish to Spotify.

Frontend design by Spencer Vilicic & Nick Mohler. Visit the [frontend GitHub repository.](https://github.com/quence-dev/fractalist)

# Usage
1. User logs into their Spotify account
2. User selects a playlist in their library to create a fractal
3. User downloads fractal and/or publishes their Spotify playlist cover


# APIs
* Spotify
* Fractal (https://github.com/rafgraph/fractal)

# Databases
* Postgres

# Implementation




## Song Attributes
The attributes displayed in the fractal

**Mode:** modality (major or minor) of a song, (0 or 1)

**Valence:** positivitiness of a song, (value between 0.0 and 1.0)

**Energy:** intensity and activity of a song, (value between 0.0 and 1.0)


## Coloring Algorithm
The coloring of the fractal is implemented based rgb values and average values for features of the songs in a playlist:

### Mode:
**Major:** if the average modality of the playlist is 1, converts all black to white ([0,0,0] to [255,255,255])
  
**Minor:** if the average modality of the playlist is 0, converts all white to black ([255,255,255] to [0,0,0])
  
### Valence:  
**High valence:** if the average valence is >= 0.5, warmer colors will be used (higher red values and lower blue values)

**Low valence:** if the average valence is < 0.5, cooler colors will be used (higher blue values and lower red values)

### Energy:
**High energy:** if the average energy is >= 0.5, colors will be brighter (rbg values > 127)

**Low energy:** if the average energy is < 0.5, colors will be darker (rgb values <= 127)
  

## Project start date: April 10, 2021


