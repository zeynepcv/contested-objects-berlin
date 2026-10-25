# Contested Objects: Provenance and Restitution in Berlin's Museums

A digital exhibition of ten objects held, or until recently held, in Berlin's museums whose presence there is disputed, from the Ishtar Gate and the Pergamon Altar to the bust of Nefertiti, the Benin Bronzes and the statue of Ngonnso. Each object is presented as a **cultural biography**: where it was made and what it meant there, how it reached Berlin, what happened to it since, and who wants it back.

**Live site:** https://zeynepcv.github.io/contested-objects-berlin/

## Pages

| Page | Content |
|---|---|
| `index.html` | The exhibition: one card per object, filterable by restitution status |
| `object.html?id=01` … `?id=10` | Object biographies: origin story, timeline of the object's life and a route map |
| `map.html` | All objects on one map, from their places of origin to Berlin |
| `about.html` | Aims, approach, data model, image rights, sustainability and limitations |

## Data

The project uses two linked tables:

- **Objects** (`data.json`): one row per object. The exhibition page loads this table live from a public Google Sheet through [opensheet](https://opensheet.elk.sh) and falls back to `data.json` if the sheet is unavailable.
- **Stations** (`stations.json`): one row per event in an object's life (date, place, coordinates, text, source), linked to an object by `ObjectID`.

To add an object, add a row to the sheet and to `data.json`, then add its stations to `stations.json`.

## Technology

Plain HTML, CSS and JavaScript; [Leaflet](https://leafletjs.com) with [OpenStreetMap](https://www.openstreetmap.org) tiles for the maps; hosted on GitHub Pages. No server, database or build step.

## Sources and rights

Facts are taken from openly accessible sources (mainly Wikipedia and its references, the Staatliche Museen zu Berlin and news reporting) and every timeline entry links to its source. All photographs come from Wikimedia Commons under public domain or Creative Commons licences and are credited on the pages. Texts and data by the author: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## Credits

Created by Zeynep Canan Vural for LV 14141 *Digital Humanities and Data Sustainability* (Dr. Christian Casey), Freie Universität Berlin, 2026. Code written with assistance from Claude (Anthropic).
