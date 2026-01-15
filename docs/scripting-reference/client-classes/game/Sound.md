---
title: 'Sound'
---
# `class` Sound <font size="4">(client-side)</font>

Sound playback helper.

Provides basic control over a sound resource loaded from a file, including
playback, looping, volume, stereo balance and querying playback state.

### Constructor
```cpp
Sound.new(string file)
```

**Parameters:**

* `string` **file**: Sound file path.

## Properties
### `string` file 

Gets or sets the sound file path.

----
### `number` playingTime <font size="2">(read-only)</font>

Returns the current playback time.

----
### `number` volume 

Gets or sets the playback volume.

----
### `bool` looping 

Gets or sets whether the sound should loop.

----
### `number` balance 

Gets or sets the stereo balance (pan).

----

## Methods
### play

Starts sound playback.

```cpp
void play()
```

  

----
### stop

Stops sound playback.

```cpp
void stop()
```

  

----
### isPlaying

Returns whether the sound is currently playing.

```cpp
bool isPlaying()
```

  
**Returns `bool`:**

True if the sound is playing.

----

## Callbacks
No callbacks.

----
