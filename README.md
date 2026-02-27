# AI + Robotics Portfolio (Static Website)

This is a minimal, academic-style personal portfolio for an **AI + Robotics** student, built with **HTML, CSS, and vanilla JavaScript**. It is designed to work out-of-the-box with **GitHub Pages** and to be easy to customize.

## Structure

- `index.html` – main landing page with sections:
  - Hero
  - About
  - Projects
  - Research
  - Skills
  - Contact
- `projects/` – individual project detail pages:
  - `grape-counting.html`
  - `motion-blur-depth.html`
  - `soft-actuator-simulation.html`
  - `raspberry-pi-fruit.html`
  - `terrain-aware-planning.html`
- `assets/` – place all media here (images, videos, PDFs, etc.)
  - `assets/resume.pdf` (resume used by the button in the hero)
  - `assets/papers/...` (PDFs linked in the Research section)
- `style.css` – global styles, responsive layout, dark/light theme
- `script.js` – smooth scrolling, section animations, dark/light toggle

## Customization

All text content is written directly in HTML so that you can edit it quickly:

- Open `index.html`:
  - Replace **Your Name** with your actual name.
  - Update the hero tagline and short description.
  - Update links for GitHub, LinkedIn, and email in the **Contact** section.
  - Edit the **Research** entries and project descriptions as needed.
- Open each file in `projects/`:
  - Adjust the **Problem**, **Approach**, **Results**, **Tech stack**, and **Media** descriptions for your real projects.
  - Replace media placeholders with your images/videos from `assets/`.
- Open `style.css` and tweak colors if you want a different palette. The theme uses CSS variables at the top of the file.

### Adding media

1. Create an `assets/` folder (already referenced by the HTML).
2. Drop images and videos there, e.g.:

   - `assets/grapes-demo.mp4`
   - `assets/robot-setup.jpg`

3. In the relevant project page, update the media panel:

   ```html
   <div class="media-body">
     <video controls muted loop>
       <source src="../assets/grapes-demo.mp4" type="video/mp4" />
     </video>
   </div>
   ```

4. Ensure paths are **relative** and start with `../assets/` in project pages (since they live in `projects/`).

### Dark / light mode

- The site uses a small JS snippet (`script.js`) to toggle between dark and light themes.
- The current mode is stored in `localStorage` and applied on the next visit.

## Running locally

You do not need any build tools – this is a static site.

1. Clone or copy the repository.
2. Open `index.html` in your browser, or start a simple static server:

   ```bash
   # Python 3
   python -m http.server 8000
   ```

3. Visit `http://localhost:8000` in your browser.

## Deploying to GitHub Pages

1. **Create a new GitHub repository** (e.g., `ai-robotics-portfolio`).
2. In your local project folder:

   ```bash
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/ai-robotics-portfolio.git
   git push -u origin main
   ```

3. In GitHub:
   - Go to **Settings → Pages**.
   - Under **Source**, select:
     - **Branch**: `main`
     - **Folder**: `/ (root)`
   - Click **Save**.

4. After a minute or two, GitHub Pages will publish your site at:

   - `https://<your-username>.github.io/ai-robotics-portfolio/`

If you instead use a **user site** (`<your-username>.github.io`), ensure the code lives in a repository with that exact name and configure Pages the same way.

## Notes

- The design intentionally leaves room for figures and videos in each project page, suitable for hardware experiments and demos.
- All code is framework-free (no React/Vue/etc.), so it is easy to move or extend.

