# Bruin Olympiad Society - Development Log
**Last Updated:** 2026-01-20

## Project Overview
- **Live Site:** https://bruin-olympiad-society-7988c.web.app/
- **GitHub Repo:** https://github.com/Badrivinayakmishra/BruinOlympiadSociety
- **Firebase Project:** bruin-olympiad-society-7988c
- **Localhost:** http://localhost:8080

## Recent Changes (2026-01-20)

### Major Updates
1. **Cursor Removed**
   - Removed custom black dot cursor from all pages (team.html, events.html, tutoring.html)
   - Restored default browser cursor for better user experience
   - Removed `cursor: none;` CSS and `.cursor-dot` elements

2. **Team Photos Updated**
   - **Dr. Deifel:** Recentered photo with `object-position: 50% 30%`
   - **Dr. Lazazzera:** Replaced with new professional photo (`dr_lazazzera.png`)
   - **Bernice Nkemnji:** Recentered to `50% 20%` to show medals without cutoff

3. **Tutoring Page Redesign**
   - Consolidated course layout into single row
   - Three main categories: Chemistry, Life Sciences, Physics
   - Chemistry: All Chem 14 series + 20/30 series in one card
   - Life Sciences: LS 7A/B/C/107 + LS 30A/B/40 + Stats 13 in one card
   - Physics: Physics 5A/B/C in one card
   - Courses listed on single lines for cleaner presentation

4. **Weekly Meetings Added**
   - **Events Page (Upcoming):** Added weekly general meetings card
     - Location: Kaplan A32
     - Time: 7-8pm
     - Description and icons included
   - **Tutoring Page:** Added weekly meetings info box
     - Displayed prominently in info section with location and time

## Previous Changes (2026-01-15)

### Major Updates
1. **Instagram Update**
   - Changed from `@uclaolympiad` to `@bruinolympiadsociety`
   - Updated across ALL pages

2. **Mailing List**
   - Now redirects to: `bruin.olympiad@gmail.com`
   - Opens email client with pre-filled message

3. **Team Photos**
   - **Bill Wang:** New high-quality photo (`bill_new_updated.png`)
   - **Badri Vinayak Mishra:** Recentered photo (30% center positioning)

4. **Past Winners Updates**
   - **Spring 2025 O-Chem Olympiad** (changed from Spring 2024):
     - Daniel Rosado (1st) - Added photo & bio
     - Toon (2nd) - Added photo
     - Landon (3rd) - Placeholder

   - **Fall 2025 Biology Olympiad**:
     - Bernice Nkemnji (3rd) - Added photo & full bio

5. **Cleaned Up Repository**
   - Removed 15 HAND website remnant pages
   - Kept only BOS-specific pages

6. **Auto-Deployment Setup**
   - GitHub Actions workflow for Firebase deployment
   - Deploys automatically on push to `main` branch
   - Fixed firebase.json gitignore issue

### Files Structure

#### Core Pages (public/)
```
index.html          - Homepage
team.html           - Team/Founders page
events.html         - Events & Winners
past-winners.html   - Full winners gallery
tutoring.html       - Tutoring services
join.html           - Join/Apply page
contact.html        - Contact info
404.html            - Error page
```

#### Key Images
```
images/bill_new_updated.png  - Bill's team photo
images/daniel.png            - Daniel Rosado winner photo
images/toon.png              - Toon winner photo
images/bernice.png           - Bernice winner photo
images/badri.png             - Badri's team photo
images/dhruv.png             - Dhruv's team photo
images/jay.png               - Jay's team photo
images/dr_pham.png           - Dr. Pham advisor photo
images/dr_ko.png             - Dr. Ko advisor photo
images/dr_lazazzera.png      - Dr. Lazazzera advisor photo
images/dr_deifel.png         - Dr. Deifel advisor photo
images/bos_logo.png          - BOS logo
```

### Links to Preserve (NEVER REMOVE)
- **Slack:** https://join.slack.com/t/bruinstemolym-sdv4736/shared_invite/zt-3eahr02a9-HUB2ADJe6w1_AycRYfjBEw
- **Instagram:** https://www.instagram.com/bruinolympiadsociety
- **Linktree:** https://linktr.ee/uclaolympiad
- **Email:** bruin.olympiad@gmail.com

### Git Commits Today
```
f0f47f6 - Update events page with winner photos and recenter Badri's photo
dc609e0 - Add automatic Firebase deployment via GitHub Actions
82fa1ee - Major site updates: Instagram, mailing list, winners, and cleanup
4bab9f4 - Add Firebase config files to repo for auto-deployment
```

### Technical Setup

#### Firebase Deployment
- Manual: `npx firebase deploy --only hosting`
- Auto: Pushes to `main` branch trigger GitHub Actions
- Secret: `FIREBASE_SERVICE_ACCOUNT_BRUIN_OLYMPIAD_SOCIETY_7988C`

#### Local Development
```bash
cd /Users/badri/Desktop/Desktop/BruinOlympiadSociety/public
python3 -m http.server 8080
```

### Winner Information

#### Spring 2025 O-Chem Olympiad
1. **Daniel Rosado** - 1st Place
   - Major: Chemical Engineering
   - Bio: "Hi, I'm Daniel Rosado, a chemical engineering major and 2024 USNCO camper. I love playing tennis, solving integrals, and all things ochem!"

2. **Toon** - 2nd Place

3. **Landon** - 3rd Place

#### Fall 2025 O-Chem Olympiad
1. Helen - 1st Place
2. Ashley - 2nd Place
3. Jasmine - 3rd Place

#### Fall 2025 Biology Olympiad
1. Zachary - 1st Place
2. Jasmine - 2nd Place
3. **Bernice Nkemnji** - 3rd Place
   - Major: Biology (Freshman)
   - Bio: "Bernice Nkemnji is a freshman at UCLA and is majoring in biology. Currently, Bernice aspires to pursue a medical career in the future, with a particular interest in dermatology. In her free time, she likes to read, go for runs, and listen to music. Recently, she has started learning how to knit, and she also wants to learn how to crochet."

### Team/Founders

#### Co-Founders
- **Bill Wang** - 3rd Year Biochemistry
- **Dhruv Suresh** - 3rd Year MCDB
- **Badri Vinayak Mishra** - 3rd Year MCDB
- **Jay Bhatnagar** - 3rd Year Neuroscience

#### Faculty & Advisors
- **Dr. Pham** - Organic Chemistry Professor
- **Dr. Ko** - Life Sciences Lecturer

---

## Commands Reference

### Git Operations
```bash
git status
git add -A
git commit -m "message"
git push origin main
```

### Firebase
```bash
npx firebase deploy --only hosting
firebase login
```

### GitHub CLI
```bash
gh run list
gh run view <run-id> --log
gh secret set <SECRET_NAME> < file.json
```

---

## Notes
- All changes tracked in git with detailed commit messages
- Auto-deployment active via GitHub Actions
- Firebase credentials stored in GitHub Secrets
- Localhost server runs on port 8080
