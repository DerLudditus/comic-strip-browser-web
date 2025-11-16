# Comic Strip Browser To-Go

A web-based, OS-independent version of the Comic Strip Browser that runs in any web browser.

## Features

- **20 Comic Strips** from GoComics.com
- **Three-panel layout**: Comic list (left), viewer (center), calendar (right)
- **Smart navigation**: Automatically skips days without comics
- **Calendar integration**: Visual date selection (two different calendar types; arrows and Home/End also work)
- **No installation required**: Just open the HTML file in a browser (a local proxy server must run!)

## Usage

### Prerequisites

Python 3 must be installed.

### Quick Start

**Linux/Mac:**
```bash
./start.sh
```

**Windows:**
```
start.bat
```

### Manual Start
Due to CORS restrictions, you need to run a local proxy server:

1. Make sure Python 3 is installed
2. Open a terminal in the project folder
3. Run: `python3 proxy-server.py` (or `python proxy-server.py`)
4. Open your browser to: `http://localhost:8000/index.html`
5. Select a comic and enjoy!

The proxy server fetches comics from GoComics.com on your behalf, bypassing browser CORS restrictions.

## Navigation Buttons

- **First**: Go to the comic's earliest available date
- **Previous**: Go to previous available comic (searches up to 31 days back)
- **Next**: Go to next available comic (searches up to 31 days forward)
- **Today**: Go to today's comic
- **Random**: Jump to a random date

### Keyboard Shortcuts
- `←` (Left Arrow): Previous
- `→` (Right Arrow): Next
- `Home`: First
- `End`: Today

### Calendar Navigation
- Click month arrows to navigate months
- Click year buttons to jump years
- Use dropdowns to select exact date (Year, Month, Day)

## Technical Details

### Files
- `index.html` - Main HTML structure
- `styles.css` - Styling and layout
- `app.js` - Application logic
- `comics-data.js` - Comic definitions and metadata

### Layout
- Left panel: 250px max, 25% of viewport
- Center panel: Flexible width (auto)
- Right panel: 250px max, 20% of viewport

### CORS Handling
Web browsers block direct requests to GoComics.com due to CORS (Cross-Origin Resource Sharing) policies. The included `proxy-server.py` solves this by:
- Running a local web server on your machine
- Fetching comics server-side (where CORS doesn't apply)
- Serving the comic images to your browser

This is the same approach used by the desktop PyQt6 application, just adapted for web browsers.

## Limitations

- The proxy may occasionally misbehave
- Some comics may not load due to GoComics.com changes
- Not optimized for mobile devices (designed for PC/laptop/tablet)

## Supported Comic Strips

1. Calvin and Hobbes
2. Peanuts
3. Peanuts Begins
4. Garfield
5. Wizard of Id
6. Pearls before Swine
7. Shoe
8. B.C.
9. Back to B.C.
10. Pickles
11. WuMo
12. Speed Bump
13. Free Range
14. Off the Mark
15. Mother Goose and Grimm
16. The Flying McCoys
17. The Duplex
18. Reality Check
19. Adam@Home
20. Ziggy

## License

This project is licensed under the MIT License.

This is a personal project for browsing publicly available comics from GoComics.com. All comic strips are property of their respective creators and copyright holders.