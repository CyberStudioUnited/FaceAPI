# FaceAPI
This brand new machine works on any camera up to 2015 or newer.

# Screenshots
![ss1fapi](https://user-images.githubusercontent.com/72953518/111711211-9b8dec80-8821-11eb-8fa6-d68a88e33ff3.PNG)
![ss2](https://user-images.githubusercontent.com/72953518/111711216-9c268300-8821-11eb-8ff6-a7fcd11b7f5e.PNG)

# IMPORTANT: Bug Fixes

## `navigator.getUserMedia`

`navigator.getUserMedia` is now deprecated and is replaced by `navigator.mediaDevices.getUserMedia`. To fix this bug replace all versions of `navigator.getUserMedia` with `navigator.mediaDevices.getUserMedia`

## Low-end Devices Bug

The video eventListener for `play` fires up too early on low-end machines, before the video is fully loaded, which causes errors to pop up from the Face API and terminates the script (tested on Debian [Firefox] and Windows [Chrome, Firefox]). Replaced by `playing` event, which fires up when the media has enough data to start playing.

## `videoCamera.Play();`

`videoCamera.Play();` is a very rare bug that happens if your camera is broken.
