# Joachim’s 70th Birthday: Historical Vietnam Week

A premium, elegant, and static website built as a 70th birthday gift. This repository contains the complete travel itinerary, historical context, and practical guidance for a one-week journey from Hanoi to Ho Chi Minh City, concluding with a family handoff in Thailand.

## Purpose
This site serves as a digital gift and comprehensive guide for Joachim’s milestone 70th birthday trip (Dates TBD, Proposed: May 2027). It traces a "historical arc" through Vietnam's dynastic, colonial, and modern heritage.

## Tech Stack
- **Framework:** [Astro](https://astro.build/) (Static Site Generation)
- **Styling:** Vanilla CSS (Modern design system with Inter & Outfit typography)
- **Deployment:** GitHub Pages via GitHub Actions
- **Data:** Structured JSON for itinerary, hotels, and dining

## New Features: Journey Map & Suggestions
The site now includes a visual **Journey Map** and a persistent **Suggestion System** to gather feedback from family and travelers.

### 🗺️ Journey Map
- **Data:** Coordinates for the travel stops (Hanoi, Hue, Hoi An, etc.) are stored in `src/data/route.json`.
- **Implementation:** Built with **Leaflet.js** and OpenStreetMap. It automatically draws a connecting route and places markers for each stop.

### 💬 Suggestions & Persistent Comments
The site uses a hybrid approach for a fully static setup:
1. **giscus (Threaded Comments):** Integrated at the bottom of each page for discussion.
2. **Structured Issues (Suggestions):** "Suggest changes" buttons open pre-filled GitHub Issue forms for Itinerary, Hotels, Dining, History, and Pricing.

#### 🛠️ Setup Instructions for Repo Owner:
To enable the suggestion system:
1. **Enable GitHub Discussions:** Go to your repository settings and check the "Discussions" box.
2. **Create a Category:** In the "Discussions" tab, create a new category named `Trip Suggestions` (select the "Announcements" or "General" type if needed).
3. **Configure giscus:**
   - The current `SectionSuggestion.astro` is set to `eliasasbrede/Jo-Ah-Kim-s-History-Trip`.
   - If you rename the repo, update the `repo` constant in `src/components/SectionSuggestion.astro`.
   - Ensure the giscus app is installed on your repository [here](https://github.com/apps/giscus).

### Content Management
- **Itinerary:** Edit `src/data/itinerary.json` to modify daily activities, descriptions, or historical notes.
- **Route:** Update `src/data/route.json` to change map marker positions or city labels.
- **Hotels & Dining:** Update `src/data/hotels.json` and `src/data/dining.json` for recommendations and official image URLs.
- **Calendar:** The `.ics` file is located at `public/files/historical-vietnam-week.ics`. Update this manually if dates change.

## Project Structure
- `/src/data/`: `itinerary.json`, `hotels.json`, `dining.json`, and `route.json`.
- `/.github/ISSUE_TEMPLATE/`: Custom YAML forms for structured feedback.
- `/src/components/`: Includes `JourneyMap.astro` and `SectionSuggestion.astro`.

## License
MIT License. See `LICENSE` for details.
