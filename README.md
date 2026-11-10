# misKalorias

A calorie and macro counter that lives on your phone. No account, no sync, no server. Each phone keeps its own log.

## What is in this folder

Everything here is a static website. Put the whole folder on any web host that serves files over HTTPS, then open the address on each phone and add it to the home screen.

- `index.html`, `manifest.webmanifest`, `sw.js`, `*.png`: the app
- `vendor/tesseract/`: the label reader (Tesseract.js 5.1.1, Apache-2.0) with English and Spanish language data. About 13 MB, loaded only when you scan a label.

## Step 1: put it online (pick one, about 5 minutes)

**Netlify Drop (easiest).** Go to app.netlify.com/drop, drag this whole folder onto the page. You get an address like `something.netlify.app`. Make an account to keep it.

**Cloudflare Pages.** Create a project, choose "Direct upload", drag the folder in.

**GitHub Pages.** Create a repository, upload the folder's contents (`index.html` must be at the top level), then Settings > Pages > deploy from the main branch. The address is `yourname.github.io/repo-name/`.

A static host is free for something this small. The address is public unless the host adds a password, but the app has no data in it, only code. Nobody can see your log, because your log never leaves your phone.

## Step 2: install on each phone

**iPhone.** Open the address in Safari (not Chrome). Tap Share, then "Add to Home Screen". Open the app from the new icon and do the setup there.
Do the install before you enter anything. On iPhone the home screen app and Safari keep separate storage, so anything entered in a Safari tab does not carry over.

**Android.** Open the address in Chrome, tap the menu, then "Install app" or "Add to Home screen".

## Step 3: setup

1. Enter height, weight, age, activity and goal. Targets calculate as you type. Any number can be overridden.
2. More > paste a free USDA key. Get one at fdc.nal.usda.gov/api-key.html. Each of you should use your own. Do not post it anywhere public.
3. Meals: Today > Edit meals (or More > Edit meals) to add, rename, reorder or remove meals.
4. Add food: search your foods and the starter list, or tap the database button to search USDA and Open Food Facts.
5. New food > Scan a nutrition label: take a photo of the Nutrition Facts panel. The numbers fill in. Check them against the label, then save. Saved foods show up first in future searches.
6. Language: the EN | ES switch at the top right changes the whole app between English and Spanish. The first time it opens it follows the phone's language, and after that it remembers your choice on that phone. Each of you can use a different language. Food names and serving sizes always stay in English, because many foods (USDA, Open Food Facts, labels) only exist in English; you can still type a Spanish word like "pollo" and the starter list will find it. Default meal names (Breakfast, Lunch, Dinner, Snacks) show in the current language; meals you renamed stay as you typed them.
7. Progress tab: log weight and body measurements (waist, hips, chest, arm, thigh, neck) and watch the charts. Profile tab: your details and targets.

## Backups (do this)

All data (food log, saved foods, weight and measurements, meals, profile) lives in the phone's browser storage. Deleting the app, clearing website data or losing the phone erases it. More > Back up everything saves a file you can keep in Files, email to yourself or similar. More > Import a file restores it. Back up once a week or so.

You can also send each other your saved foods: More > Share saved foods. The other phone imports the file and gets those foods added. It does not touch the rest of their data.

## Updating the app later

Replace the files on the host. Phones pick up the new version the next time they open the app with a connection (close and reopen it once or twice). Stored data is kept.

## Known limits

- Label scanning reads text from a photo, and photo reading makes mistakes: a "g" read as a 9, a "3" read as an 8. The app flags numbers that do not add up, but it cannot catch everything. Always check the numbers before saving. Flat, well-lit, straight-on photos work best.
- Food database results depend on those services. Open Food Facts is crowd-sourced and some entries are wrong or incomplete. USDA branded entries come from manufacturer labels.
- Spanish wording is a translation, not a professional one. If a phrase reads oddly, tell me and it is a one-line fix. USDA results come back in English (Open Food Facts handles Spanish better). The label scanner reads both English and Spanish labels.
- Targets are estimates from the Mifflin-St Jeor formula. Adjust them from your own weigh-in trend after 2 to 3 weeks.
- This is not medical advice. If you have a medical condition, are pregnant or have a history of disordered eating, talk to your doctor or a dietitian before using calorie targets.

## Credits

Food data: USDA FoodData Central (public domain) and Open Food Facts (Open Database License). OCR: Tesseract.js. Font: Archivo (Google Fonts).
