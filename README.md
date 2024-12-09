# Intelligent-media-player
The **Intelligent Media Player** uses hand gestures to control media playback, replacing the need for a keyboard or mouse. 

The system utilizes a **convexity defects algorithm** to count the number of fingers by identifying points farthest from the hand's convex hull. For example, detecting four convexity defects indicates four fingers, triggering the "right" arrow key.

Here's how it interprets gestures:
- **No fingers**: The program remains idle when no fingers are detected.
- **One finger**: Triggers the "space" key to play or pause media.
- **Two fingers**: Triggers the "up" arrow key to increase the volume.
- **Three fingers**: Triggers the "down" arrow key to decrease the volume.
- **Four fingers**: Triggers the "right" arrow key to skip forward in the media.


The keyboard shortcuts are customizable. For instance, to press "enter" when one finger is detected, you can modify the code like this:

```python
if count_defects == 1:
    p.press("enter")
```

You can also extend the functionality by adding gestures. For example, to rewind media, you could include:

```python
if count_defects == 5:
    p.press("left")
```

After updating the code, the player will recognize the new gestures during operation.
