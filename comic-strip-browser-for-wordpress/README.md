# Comic Strip Browser for WordPress

A web-based comic strip browser designed to run on WordPress sites or any PHP-enabled web server.

## Features

- **20 Comic Strips** from GoComics.com
- **Three-panel layout**: Comic list (left), viewer (center), calendar (right)
- **Smart navigation**: Automatically skips days without comics
- **Calendar integration**: Visual date selection (two different calendar types; arrows and Home/End also work)
- **PHP-based proxy**: Works on any PHP server (WordPress, Apache, Nginx, etc.)

## Installation on WordPress


### Option 2: Upload to WordPress Root (Recommended)
1. Create a folder in your WordPress root, say `/public_html/comic-browser/`
2. Upload all files to this folder
3. Set file permissions (if needed): files: 644, folder: 755
4. Access directly via: `https://yoursite.com/comic-browser/`

### Option 3:  WordPress Plugin Folder
1. Upload to something like `/wp-content/plugins/comic-browser/`
2. Access directly via URL (no need to activate as plugin)

## Files

- `index.html` - Main HTML page
- `styles.css` - Styling and layout
- `app.js` - Application logic
- `comics-data.js` - Comic definitions
- `fetch-comic.php` - PHP proxy script (handles CORS)
- `.htaccess` - Optional, for Apache, if the defaults are restrictive

## Requirements

- PHP 5.4 or higher
- cURL extension enabled (usually enabled by default)
- Web server (Apache, Nginx, etc.)

## How It Works

The PHP proxy (`fetch-comic.php`) fetches comics from GoComics.com server-side, bypassing browser CORS restrictions. This is necessary because browsers block direct requests to external sites.

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
21. Foxtrot
22. Foxtrot Classics

## Troubleshooting

### Comics not loading
- Check that PHP cURL extension is enabled: Create a file `test.php` with `<?php phpinfo(); ?>` and look for "cURL support: enabled" in the output
- Verify `fetch-comic.php` has proper permissions (644 or 755)
- Check server error logs for PHP errors

### 403 or 404 errors
- Ensure all files are uploaded correctly
- Check file permissions (should be 644)
- Verify the path to `fetch-comic.php` is correct

### Styling issues
- Clear browser cache
- Check that `styles.css` is loading correctly
- Verify Google Fonts can load (check Content Security Policy)

## Security Notes
- The PHP proxy only accepts URLs from gocomics.com
- CORS headers are set to allow cross-origin requests
- No user data is stored or transmitted


## License

This project is licensed under the MIT License.

This is a personal project for browsing publicly available comics from GoComics.com. All comic strips are property of their respective creators and copyright holders.
