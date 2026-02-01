# Valentines Day 26 💘

A tiny, single-page Valentine’s site built with plain HTML/CSS/JS and hosted on GitHub Pages.

It shows a cute landing card with Yes / No buttons:
- “No” dodges the cursor (and scrolling/tapping it makes “Yes” grow).
- Clicking “Yes” swaps the UI into a “success” state and shows a GIF from /gifs/.
- You can optionally control the displayed name (and which gif appears) via URL parameters.

# URL parameters
```name```

Change the name shown in the headline:
- Default: ```lucia```
- Example:
    - ```/?name=david```
    - Shows: ```david will you be my valentine?```

Notes:

URL encoding applies (spaces should be ```%20``` or ```+```).

If ```name``` is missing or empty, it falls back to ```lucia```.

```gif```

Deterministically pick which success GIF appears (instead of random):

Mapping:
- ```gif=1``` → ```penguinarrow.gif```
- ```gif=2``` → ```penguins.gif```
- ```gif=3``` → ```snoopyslaplonger.gif```
- ```gif=4``` → ```snoopyvalentinesday.gif```

Example:
- ```/?name=david&gif=1```
- Clicking ```Yes``` will show ```penguinarrow.gif```

If ```gif``` is missing or invalid, the page falls back to random selection from the available GIF list.

# Run locally
Because the page loads assets (PNG/GIF) using relative paths, you should run it from a local web server (not by double-clicking index.html).

```python3 -m http.server 8000```

Then open:
- http://localhost:8000/