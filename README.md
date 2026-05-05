FOYLESIDE SHOPPING CENTRE
Store Directory — Kiosk System
README & Operations Guide
Version 8.0 | May 2026
════════════════════════════════════════════════════════════════


CONTENTS
────────
1. Overview
2. Files
3. How to Update the Directory
4. Uploading to GitHub
5. Loading on the Xiaohui Screen
6. Xiaohui System Settings
7. Troubleshooting
8. Store Data Reference
9. Contact


════════════════════════════════════════════════════════════════
1. OVERVIEW
════════════════════════════════════════════════════════════════

The Foyleside Store Directory is a touch-screen kiosk application
built as a single self-contained HTML file (index.html). It runs
inside the xiaohui digital signage player via the HTML layer.

The directory covers all four shopping levels:

  Level 1 — Foyle Street Entrance · Car Parking · Supermarket
  Level 2 — Orchard Street Entrance · Main Shopping Level
  Level 3 — Fashion · Dining · Shopping
  Level 4 — Ferryquay Street Entrance · Top Shopping Level

Features:
  - Touch-friendly store cards with brand colour tiles
  - Category filter pills per floor
  - Live search across all floors and levels
  - Tap any store for full details, opening hours and location
  - Tap any facility button for full information
  - Toilet facility information per level
  - Customer Service Desk information (Level 3)
  - Centre Facilities panel (Toilets, Accessibility, Car Parking,
    ATM, Gift Cards, Shopmobility, Sensory Room, Info Desk)
  - Live clock and date in the header
  - Footer shows YOU ARE ON LEVEL 3 and centre phone number
  - Idle reset — returns to Level 2 after 3 minutes of no activity
  - Fully offline — fonts are embedded, no internet required
    once the file is loaded


════════════════════════════════════════════════════════════════
2. FILES
════════════════════════════════════════════════════════════════

  index.html          The kiosk application — this is the only
                      file needed. Everything is self-contained.

  foyleside_editor.html
                      The editor tool — open this in Chrome on
                      a laptop to make changes to store data,
                      then export a new index.html.

  README.txt          This file.


════════════════════════════════════════════════════════════════
3. HOW TO UPDATE THE DIRECTORY
════════════════════════════════════════════════════════════════

To add, edit or remove stores:

STEP 1
  Download foyleside_editor.html to your laptop or PC.
  Open it in Google Chrome (not Edge, not Safari).

STEP 2
  The editor shows the kiosk on the right and edit controls
  on the left. Use the L1 / L2 / L3 / L4 tabs to switch floors.

STEP 3 — Editing a store
  - Click the store name or unit field and type your changes.
  - Click "+ More" to expand description, hours and badge options.
  - Click the coloured tile to change the icon/initials.
  - Badges available: Dining / Drinks / Coming 2026

STEP 4 — Adding a store
  - Click the "+ Add Store" button under the relevant category.
  - A new blank store appears at the bottom — fill in the details.

STEP 5 — Removing a store
  - Click the red ✕ button on the store row.

STEP 6 — Changing floor info or hours
  - At the top of each floor tab is a "Floor Info" section.
  - Edit the description and opening hours there.

STEP 7 — Export
  - Click the "⬇ Export index.html" button in the top right.
  - This downloads a new index.html with all your changes.
  - Upload this file to GitHub (see Section 4).


════════════════════════════════════════════════════════════════
4. UPLOADING TO GITHUB
════════════════════════════════════════════════════════════════

The kiosk is hosted on GitHub Pages at:

  https://paulanthonydoherty34-ops.github.io/foylesidekiosk/

To upload a new version:

STEP 1
  Go to: github.com/paulanthonydoherty34-ops/foylesidekiosk

STEP 2
  Click on index.html in the file list.

STEP 3
  Click the pencil ✏️ edit icon (top right of the file view).

STEP 4
  Press Ctrl+A to select all the existing code, then Delete.

STEP 5
  Open your newly exported index.html in a text editor
  (Notepad, TextEdit etc.), press Ctrl+A to copy all.

STEP 6
  Paste into the GitHub editor.

STEP 7
  Scroll down and click "Commit changes", then
  "Commit changes" again to confirm.

STEP 8
  Wait approximately 60 seconds. The live URL will update
  automatically. The xiaohui screen will refresh on its
  next scheduled refresh cycle (default: 15 minutes).

  To force an immediate refresh on the xiaohui screen,
  use the "Play now" option in the xiaohui system menu.


════════════════════════════════════════════════════════════════
5. LOADING ON THE XIAOHUI SCREEN
════════════════════════════════════════════════════════════════

The kiosk loads via the HTML layer in the xiaohui editor.

Settings for the HTML layer:

  Route (URL):    https://paulanthonydoherty34-ops.github.io/foylesidekiosk/
  X position:     0
  Y position:     0
  Width (W):      2160
  Height (H):     3840
  Web style:      Computer
  Scaling factor: 100%
  Refresh time:   15 minutes (recommended)

IMPORTANT — Screen resolution must be set to 2160 x 3840 (portrait).
If the content appears too small, the resolution may be set
incorrectly on the device. Check System Control > Display.


════════════════════════════════════════════════════════════════
6. XIAOHUI SYSTEM SETTINGS
════════════════════════════════════════════════════════════════

To access the xiaohui system menu:
  Hold down on the screen edge / use the back panel button
  (method varies by device model).

KEY SETTINGS:

  Date & Time
  ───────────
  Location:   System Control > Date & Time
              OR Advanced Options > Date & Time
  Timezone:   Set to GMT+0 London/Dublin
              (automatically adjusts for BST in summer)
  Sync:       Enable automatic NTP time sync if WiFi connected
  The kiosk clock reads from the device system clock.
  Correct timezone = correct clock display.

  WiFi / Network
  ──────────────
  Location:   Network Settings
  The kiosk file is hosted online (GitHub Pages).
  WiFi is required to:
    - Load the kiosk on first run
    - Receive updates when index.html is changed on GitHub
  Once loaded, the page runs offline until next refresh.

  Display / Resolution
  ────────────────────
  Location:   System Control > Display
  Set to:     2160 x 3840 portrait (9:16)

  Restart / Refresh
  ─────────────────
  Play now:   Forces immediate content refresh from GitHub
  Restart:    Full system reboot (use if screen freezes)


════════════════════════════════════════════════════════════════
7. TROUBLESHOOTING
════════════════════════════════════════════════════════════════

ISSUE: Content not filling the full screen / gap at bottom
FIX:   Check the HTML layer dimensions are W:2160 H:3840.
       Check Y position is 0. Check Scaling factor is 100%.

ISSUE: Clock showing wrong time
FIX:   Check device timezone in System Control.
       Set to GMT+0 London/Dublin and enable NTP sync.

ISSUE: Directory not updating after GitHub upload
FIX:   Wait 60 seconds after committing to GitHub.
       Use "Play now" in the xiaohui menu to force refresh.
       Check WiFi is connected.

ISSUE: Screen appears slow or sluggish
FIX:   The fonts are now embedded in the file — no internet
       request needed. If still slow, restart the device.
       Check no other apps are running in the background.

ISSUE: Store detail panel not opening when tapped
FIX:   The tap target may be too small at full resolution.
       The store cards and buttons are touch-optimised for
       2160 x 3840. Ensure the correct resolution is set.

ISSUE: Search not working
FIX:   Tap the search bar at the top of the screen.
       Type the store name, category or keyword.
       Results appear from all four floors.

ISSUE: Screen reverted to Level 2 on its own
FIX:   This is normal — the idle reset returns the directory
       to Level 2 after 3 minutes of no interaction.


════════════════════════════════════════════════════════════════
8. STORE DATA REFERENCE
════════════════════════════════════════════════════════════════

LEVEL 1 — Foyle Street Entrance
  Supermarket & Food:  Iceland, UMI
  Car Parking:         West Car Park (WCP), East Car Park (ECP)
  Services:            Valet Centre

LEVEL 2 — Orchard Street Entrance
  Fashion:             Marks & Spencer, Dunnes Stores,
                       Edinburgh Woollen Mill
  Health & Beauty:     Boots, SC Beauty, The Body Shop,
                       BPerfect Cosmetics, Rituals,
                       The Perfume Shop, Holland & Barrett,
                       Superdrug (Coming 2026)
  Shoes:               Clarks Shoes, Schuh, Pavers
  Jewellery:           H. Samuel
  Food & Drink:        Costa Coffee, Greggs
  Gifts & Cards:       Yankee Candle, Clintons,
                       Card Factory, Real Image
  Services:            Vision Express, EE,
                       Bureau de Change, Lottery Kiosk

LEVEL 3 — Fashion · Dining · Shopping
  Fashion:             H&M, NEXT, MANGO, River Island, DV8,
                       Regatta, Smiggle, Office Shoes,
                       Waterstones
  Dining:              Starbucks Coffee, Caffè Nero,
                       Dunnes Café
  Entertainment:       Angry Cherry
  Phones & Tech:       Three Mobile, O2, Uberfone
  Services:            Hays Travel, Nova Nails, The Barber

LEVEL 4 — Ferryquay Street Entrance
  Fashion & Accessories: River Island, Pandora, Timpson
  Food & Drink:          McDonald's, All Sweet Hi, Toasted
  Drinks:                Hey Boba.

CENTRE FACILITIES (available on all levels)
  Toilets      Level 1 — Ladies, Gents, Accessible, Baby Change
               Level 4 — Ladies, Gents, Accessible, Parent Room,
                          Sensory Room, Hoist Facility
               Level 2 — Inside Marks & Spencer
               Level 3 — Inside Starbucks, Caffè Nero, Dunnes

  ATM          Level 4 — x1 Ferryquay Street Entrance
               Level 2 — x1 outside Dunnes Stores
               Level 2 — x1 outside The Body Shop

  Gift Cards   Available from Customer Service Desk, Level 3
               Valid for 12 months from date of purchase

  Sensory Room Level 4 — please ask a member of the team

  Car Parking  West Car Park: Mon–Tue 07:00–19:00
                              Wed–Fri 07:00–22:00
                              Sat 08:00–19:00
                              Sun 10:00–19:00
               East Car Park: Same hours as West Car Park


════════════════════════════════════════════════════════════════
9. CONTACT
════════════════════════════════════════════════════════════════

Foyleside Shopping Centre
19 Orchard Street
Derry BT48 6XY

Tel:    028 7137 7575
Email:  info@foyleside.co.uk
Web:    www.foyleside.co.uk

Kiosk live URL:
  https://paulanthonydoherty34-ops.github.io/foylesidekiosk/

GitHub repository:
  github.com/paulanthonydoherty34-ops/foylesidekiosk

════════════════════════════════════════════════════════════════
END OF DOCUMENT
════════════════════════════════════════════════════════════════
