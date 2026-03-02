# Pratheeka Builders & Developers – Website

Static marketing site for **Pratheeka Builders & Developers**, inspired by the [Luzen Webflow template](https://webflow.com/templates/html/luzen-website-template). Showcases completed and upcoming residential projects with building elevations and floor plans.

## What’s included

- **Home** – Hero, About Us, Projects (previous + upcoming), Why Pratheeka, Contact
- **Project pages** – One page per building: elevation image, address, and floor plan images
- **Navigation** – Home, About Us, Projects, Floor Plans, Gallery, Contact Us
- **Contact** – Phone, email, office address; enquiry form opens a pre-filled email to your inbox

## Project structure

| File / folder | Purpose |
|---------------|--------|
| `index.html` | Homepage (hero, about, projects grid, why us, contact) |
| `project.html` | Project detail page (elevation + floor plans); content from `?building=slug` |
| `project-data.js` | Building list: names, folders, elevation/floor plan filenames, addresses, status |
| `styles.css` | All styles (header, sections, project cards, project detail, responsive) |
| `script.js` | Mobile nav toggle, footer year, contact form → mailto |
| `logo for pratheeka.png` | Logo used in header and footer |
| `ANJALI ARCADE/`, `KRISHNA RESIDENCY/`, etc. | One folder per building: elevation image(s), floor plan image(s), optional address doc |

Each building folder should contain at least an **elevation** image; optional **floor plan** images and address are configured in `project-data.js`.

## Run locally

```bash
cd pratheeka
python3 -m http.server 8000
```

Then open **http://localhost:8000** in your browser.

## Deploy with GitHub Pages

1. Create a new repository on GitHub (e.g. `pratheeka-website`).
2. Push this project to it (all files and building folders; keep the same structure).
3. In the repo: **Settings → Pages**.
4. Under **Source** choose **Deploy from a branch**.
5. Branch: **main** (or **master**), folder: **/ (root)**. Save.
6. The site will be at `https://<your-username>.github.io/<repo-name>/`.

If the repo is named `pratheeka-website`, the URL will be like:  
`https://yourusername.github.io/pratheeka-website/`

## Customize content

- **Contact details** – Edit the Contact section in `index.html` (phone, email, office address).
- **Office address** – Currently set to: 1-5-1083/146/502, Mangapuram Colony, Old Alwal, Hyderabad, Telangana 500010.
- **Enquiry email** – Form sends to the address in `script.js` (mailto); change the `to` variable to use another email.
- **Add or edit a building** – Update `project-data.js` (name, folder, elevation, floorPlans array, address, status) and add the images in the building folder.

No build step or extra dependencies; plain HTML, CSS, and JavaScript.
