# Micro Frontend App

This project demonstrates the use of micro frontends in a music app built using Vite, React, and TypeScript, with the help of Module Federation. It consists of independent applications that come together to provide functionality such as displaying a list of artists, showing artist details, and reusable UI components.

## Project Structure

- **artist-list**: Displays a list of top artists using the Last.fm API.
- **artist-details**: Displays detailed information about a selected artist.
- **ui**: Contains reusable UI components (e.g., title, loading indicator) shared across the applications.
- **types**: Shared TypeScript types used across all applications.

## Features

- Micro Frontend architecture with Module Federation
- State and TypeScript type sharing between micro frontends
- Integration with Last.fm API for artist data
- TailwindCSS and NextUI for UI components
- SWR for data fetching

## Setup

0. Set up the Last.fm API key:
   - Create an account on [Last.fm](https://www.last.fm/api/account/create).
   - Get your API key from [Last.fm API](https://www.last.fm/api/account/create).
   - Create a `.env` file in the root directory and add your API key:
     ```bash
     VITE_LAST_FM_API_KEY=your_api_key_here
     ```

1. Clone the repository:

   ```bash
   git clone https://github.com/bogachenkov/vite-micro-frontends.git
   ```

2. Install dependencies, build and run the individual apps:
  - ArtistList (host application)
    ```bash
    cd artist-list
    yarn build
    yarn preview
    ```
  - ArtistDetails (remote application)
    ```bash
    cd artist-details
    yarn build
    yarn preview
    ```
  - UI (remote application)
     ```bash
     cd ui
     yarn build
     yarn preview
     ```
3. Visit http://localhost:3000 to see the host application in action.
