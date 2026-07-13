# CalAge

A single-file web app that calculates a person's exact age — down to the second — and, in reverse, helps figure out a likely birth year from an age and birthday.

No build step, no dependencies to install, no server required. Open the HTML file in a browser and it works.

## Features

### Calculate age
- Enter a date of birth (and optionally a time of birth).
- Instantly see the age broken down into **years, months, and days**.
- A live, ticking odometer-style display shows **hours : minutes : seconds** elapsed since birth, updating every second.
- Bonus stats: total number of days lived, and a countdown to the next birthday.

### Find birth year
- Enter a current age plus a birth day and month (no year needed).
- The app returns **two possible birth years**, since "age" alone is ambiguous without knowing whether this year's birthday has already passed.
- The year consistent with today's actual date is flagged **"Most likely"**; the other is shown alongside an explanation of when it would apply instead.

## How it works

- All dates and times are handled with native JavaScript `Date` objects, using calendar-aware "borrowing" arithmetic (similar to subtracting dates by hand) so that months and days are calculated correctly regardless of varying month lengths and leap years.
- The birth-year finder compares the supplied day/month to today's date to determine which of the two candidate years is consistent with the present moment, and labels that one as most likely.
- Everything runs entirely in the browser. No data is transmitted, stored, or logged anywhere.

## Privacy

This app makes no network requests with your data. Dates you enter never leave your device.

## Tech stack

- Plain HTML, CSS, and vanilla JavaScript — no frameworks, no build tools.
- Google Fonts (Fraunces, Space Mono, Inter) loaded via CDN for typography.

## License

Released under the MIT License. See [LICENSE](./LICENSE) for details.
