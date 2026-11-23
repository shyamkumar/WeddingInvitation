# Shyam & Neha — Interactive Wedding Invitation

A mobile-first, single-file interactive Indian wedding invitation website (`index.html`) designed in an ivory, blush, wine (`#6e1f2f`), and champagne-gold palette with Hinglish copy.

## Features
- **3D Wine-Velvet Opening Book**: Preloader, parallax blurred 3D roses, 3D cover open + camera zoom, falling rose petals, and soft fade-in looping wedding music.
- **Gold Arch Hero Page**: Fits one mobile screen cleanly with pre-blurred slowly zooming background photo, gold Ganesh ji medallion, and letter-by-letter couple names.
- **Save the Date Scroll**: Pull-or-tap tassel unroll with rose corners, petal & gold confetti burst, one-line live countdown, and `.ics` calendar export.
- **Swipeable 3D Carousels**: Infinite-looping *Wedding Festivities* cards (with pre-blurred illustrated scenes, animated icons & dress-code colour swatches) and *Our Story* photo carousel.
- **Grand Reception, Illustrated Map & Closing**: Deep wine card with blooming roses and sparkles, interactive Bengaluru map with animated route/pin (**Get directions** + **Copy address**), scroll-parallax corner roses, and swinging marigold strings.

## Quick Customization
Open `index.html` and edit the `WEDDING_CONFIG` object inside `<script>` to update:
- Groom, bride, parents' names, and family closing line
- Wedding date, pheras time, venue name, full address, and Google Maps URL
- Function schedules, venues, and dress codes
- Couple photos (`photos` array — image #1 is automatically pre-blurred for the hero arch)
- Background MP3 (`music.mp3Url`) or YouTube song link (`music.youtubeUrl`)

## Deploy to Google Cloud Run

### Option 1: From Google Cloud Shell / Terminal
```bash
gcloud run deploy wedding-invitation \
  --source . \
  --region asia-south1 \
  --allow-unauthenticated
```

### Option 2: Continuous Deployment from GitHub
1. Open **Google Cloud Console → Cloud Run → Create Service**.
2. Choose **Continuously deploy from a repository** and connect `shyamkumar/WeddingInvitation`.
3. Select **Dockerfile** as the build type and enable **Allow unauthenticated invocations**.
4. Click **Create** — Cloud Run will build the `Dockerfile` and publish your live HTTPS invite URL.
