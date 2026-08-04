## Joshua Isbister — Engineering Portfolio

Personal portfolio site showcasing mechanical and mechatronic engineering projects. Built as static HTML/CSS — no build step, no dependencies beyond a couple of Google Fonts and a CDN QR code library.

Live site: https://joshuaisbister.github.io

Branches
main — development branch. New pages, edits, and work-in-progress content go here first.
publish — deployed branch. GitHub Pages serves the live site from this branch. Only merge into publish when content is ready to go live.

Workflow:

bash
# work on main
git checkout main
# ...make changes, commit...
git push origin main

# when ready to deploy
git checkout publish
git merge main
git push origin publish
Structure
index.html         Home page — about section, project grid, capabilities, contact
project-1.html      Embedded Step Tracker Watch
project-2.html      Warman Challenge Robot
project-3.html      6-DOF Industrial Robot Simulation
project-4.html      ROS2 Racing Simulation
project-5.html      UTS Motorsports Seat — FSAE
project-6.html      Suspension Kinematics & Linkages — FSAE
project-7.html      FDM Printed Pliers Challenge

All pages are self-contained single HTML files with inline CSS — no build tools, no bundler. Links between pages are relative, so every file must stay in the same root folder for navigation to work.

Adding a new project
Duplicate any project-N.html file and rename it (e.g. project-8.html)
Edit the title, eyebrow, tags, specs, and body copy
Update the "next project" link at the bottom to point somewhere sensible
Add a matching card to the project grid in index.html, linking to the new file
Adding your photo

In index.html, find the about-photo-ph placeholder block inside <section id="about"> and replace it with:

html
<img src="your-photo.jpg" alt="Your Name">

Add the image file to the repo root alongside the HTML files.

Access via QR / NFC

The contact section auto-generates a QR code pointing at whatever URL the page is hosted on — no setup needed. For a tap-to-open NFC card, write the live site URL to an NFC tag using an app like NFC Tools.

Local preview

No server required — just open index.html directly in a browser. All pages are plain static HTML.
