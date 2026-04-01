# Joachim’s 70th Birthday: Historical Vietnam Week

A premium, elegant, and static website built as a 70th birthday gift. This repository contains the complete travel itinerary, historical context, and practical guidance for a one-week journey from Hanoi to Ho Chi Minh City, concluding with a family handoff in Thailand.

## Purpose
This site serves as a digital gift and comprehensive guide for Joachim’s milestone 70th birthday trip (Dates TBD, Proposed: May 2027). It traces a "historical arc" through Vietnam's dynastic, colonial, and modern heritage.

## Tech Stack
- **Framework:** [Astro](https://astro.build/) (Static Site Generation)
- **Styling:** Vanilla CSS (Modern design system with Inter & Outfit typography)
- **Deployment:** GitHub Pages via GitHub Actions
- **Data:** Structured JSON for itinerary, hotels, and dining

## Project Structure
- `/src/data/`: Contains `itinerary.json`, `hotels.json`, and `dining.json`. This is the core of the site content.
- `/src/components/`: Reusable Astro components (Cards, Nav, Footer).
- `/src/pages/`: Individual site pages.
- `/public/files/`: Contains the downloadable `.ics` calendar file.
- `/public/images/`: (Planned) Directory for optimized local images.

## Local Development
1. **Install Dependencies:**
   ```bash
   npm install
   ```
2. **Start Development Server:**
   ```bash
   npm run dev
   ```
3. **Build Static Site:**
   ```bash
   npm run build
   ```

## Content Management
- **Itinerary:** Edit `src/data/itinerary.json` to modify daily activities, descriptions, or historical notes.
- **Hotels & Dining:** Update `src/data/hotels.json` and `src/data/dining.json` for recommendations and Michelin details.
- **Calendar:** The `.ics` file is located at `public/files/historical-vietnam-week.ics`. Update this manually if dates or event details change.

## Image Replacement
Current images are high-quality placeholders from Unsplash to ensure a premium aesthetic for the gift preview. For the final version:
1. Place your own high-resolution photos in `public/images/`.
2. Update the image paths in `src/data/hotels.json` or within the individual `.astro` pages.
3. The site is optimized to handle high-resolution assets with lazy loading.

## Deployment
The site is configured for **GitHub Pages**. Every push to the `main` branch triggers a GitHub Action (`.github/workflows/deploy.yml`) that builds and publishes the site automatically.

## License
MIT License. See `LICENSE` for details.
