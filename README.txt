PROPRO9 POLISHED SITE

Files:
- index.html          Main website
- favicon.svg         Included favicon
- screenshots.json    Controls which screenshots appear
- .nojekyll           Keeps GitHub Pages simple
- .github/workflows/pages.yml
                       Optional GitHub Pages workflow

NO PC BUSINESS STUFF IS INCLUDED.

ADDING SCREENSHOTS
------------------
Put your image files in the same folder as index.html.

Then edit screenshots.json.

Example:
[
  "img_1.png",
  "img_2.png",
  "img_3.png"
]

You can use any names:
[
  "backrooms_hall.png",
  "chair_scene.png",
  "computer_room.png"
]

If a listed image does not exist, the site quietly skips it instead of
making your Python localhost terminal experience 50 consecutive 404s.

LOCAL TESTING
-------------
Open Command Prompt in this folder and run:

python -m http.server 8000

Then visit:

http://localhost:8000

If you change the favicon and Chrome refuses to acknowledge reality,
change ?v=1 in index.html to ?v=2.

GITHUB PAGES
------------
Upload the contents of this folder to the root of your repository.

If you use the included workflow, GitHub Pages should be configured to
deploy using GitHub Actions.

The workflow uses:
concurrency:
  group: "pages"
  cancel-in-progress: false
