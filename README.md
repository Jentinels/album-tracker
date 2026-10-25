# Album Tracker

Album Tracker is a React web app for searching music albums, previewing their tracks, and keeping a personal listening log with statuses, star ratings, and notes. It can also play full albums through Deezer's embeddable player and suggest new albums with LLM-powered recommendations based on your saved collection.

**Live link:** _add your Vercel link here_

![Album Tracker screenshot](./screenshot.png)
_(add a screenshot named `screenshot.png` to the repository)_

## Features

- Search albums and artists with the iTunes Search API
- Album page with cover, year, genre, track list, and 30-second previews
- Links to listen on Spotify, YouTube, and Apple Music
- Mini player with play/pause, previous/next, and a seek bar that keeps playing while you browse
- Personal collection with status (Want to listen, Listening, Listened), 1-5 star rating, and notes
- Filter and sort the collection; it persists between visits
- Optional full-album playback through the Deezer player
- LLM-powered recommendations based on the user's saved albums and ratings

## Tech stack

React, Vite, Context API, iTunes Search API, Deezer, Google Gemini, Vercel (serverless functions)

## Run it locally

```bash
git clone https://github.com/YOUR-USERNAME/album-tracker.git
cd album-tracker
npm install
```

Create a file named `.env.local` in the project root:

```
GEMINI_API_KEY=paste-your-key-here
```

Then start the app:

```bash
npm run dev
```

## Limitations

- Previews are 30 seconds long because that is all the iTunes API provides
- The collection is saved only in your browser (localStorage)
- Deezer needs you to be logged in, and a plan that includes full tracks in your country, to play full albums

## Privacy note

The recommendations feature sends your saved albums' titles, artists, ratings, and statuses to Google's Gemini API. Your notes are not sent.

## Disclaimer

This is a learning project. It is not affiliated with Apple, Spotify, Deezer, or Google. Music data, artwork, and audio belong to their owners.
