# Assignment 2 — Advanced CSS: Flexbox & Grid

## Team Information

Team Name: [ADD TEAM NAME]

Group: [ADD GROUP]

Members:

1. [STUDENT 1 NAME]
   Pages:
   - Home
   - Cars
2. [STUDENT 2 NAME]
   Pages:
   - Culture
   - Contact

Deployment URL:

[ADD URL]

---

# Objective

Upgrade the existing Assignment 1 JDM website with Flexbox and CSS Grid. Improve alignment, spacing, card consistency and responsiveness while preserving the content, lists, table, form, team sections, shared stylesheet and four original pages.

# Task 1 — Flexbox Navigation

## What Was Implemented

Every page retains the same branded header and Home, Cars, Culture and Contact links. The active page has an underline and `aria-current="page"`.

## CSS Properties Used

- `display: flex` turns `.header-inner` and `.nav-menu` into flex containers.
- `justify-content: space-between` separates the brand and navigation.
- `align-items: center` vertically centers the items.
- `gap: 24px` spaces the navigation links without margin tricks.
- `flex-wrap: wrap` lets links wrap if available space becomes small.

## How It Works

`.site-header` contains `.container.header-inner`, which holds `.brand` and `.nav-menu`. At 768px and below, the header switches to `flex-direction: column`; the navigation stays a centered, wrapping row. `.nav-menu a` rules keep sidebar links separate from the global navigation. The skip link remains the first keyboard target.

## Screenshot

[INSERT SCREENSHOT — DESKTOP NAVIGATION]

[INSERT SCREENSHOT — MOBILE NAVIGATION]

---

# Task 2 — Flexbox Card Row

## What Was Implemented

`cars.html` keeps all six original car descriptions and images inside `.car-list.car-cards`. Every `.car-card` now has a `.button.card-button` linking to its actual comparison table row, such as `#spec-r34`. The targeted row is highlighted. No empty placeholder actions were added.

## CSS Properties Used

- `.car-cards` uses `display: flex`, `flex-wrap: wrap`, `align-items: stretch` and `gap: 24px`.
- `.car-card` uses `flex: 1 1 320px` and `flex-direction: column`.
- `.card-body` is another column flex container with `flex: 1`.
- `.card-button` uses `margin-top: auto` to occupy the bottom of the content area.

## Equal Height Cards

Flexbox stretches cards to the tallest card in each row. Their content bodies grow to fill the available height, and automatic top margins align buttons along the bottom of each row. Wrapped rows can have different heights; content is not clipped or forced into a fixed height.

## Hover Effect

Hover and focus within a card apply `translateY(-6px)` and a soft shadow over 0.25 seconds. Reduced-motion preferences disable the transform and transition.

## Responsive Behavior

At desktop width, three cards fit per row. Cards wrap as the container shrinks. At 540px and below, their basis becomes 100%, creating a single column.

## Screenshot

[INSERT SCREENSHOT — FLEXBOX CARDS]

[INSERT SCREENSHOT — CARD HOVER EFFECT]

---

# Task 3 — CSS Grid Page Layout

## What Was Implemented

`culture.html` has a `.page-grid` wrapper around the header, topic sidebar, main content and footer. The sidebar contains real section anchors and brief facts. Existing cultural text and Student 2's biography remain.

## Grid Areas

```css
.page-grid {
    min-height: 100vh;
    display: grid;
    grid-template-columns: minmax(220px, 1fr) minmax(0, 3fr);
    grid-template-rows: auto 1fr auto;
    grid-template-areas:
        "header header"
        "sidebar main"
        "footer footer";
}
```

The sidebar track gets one share of available space, with a 220px minimum; the main track gets three shares and may shrink below its content's automatic minimum. This avoids forcing wide content outside the page.

## Areas

- `.grid-header` has `grid-area: header` and spans both columns.
- `.grid-sidebar` has `grid-area: sidebar` and occupies the left column.
- `.grid-main` has `grid-area: main` and occupies the right column. `min-width: 0` permits shrinking.
- `.grid-footer` has `grid-area: footer` and spans both columns.

## Responsive Behavior

At 768px and below, the columns become `minmax(0, 1fr)` and the areas are `"header" "main" "sidebar" "footer"`. The sidebar becomes a section beneath the main content. The DOM keeps the sidebar before main, so keyboard/source order is still header, sidebar, main, footer; the skip link provides direct access to main content.

## Screenshot

[INSERT SCREENSHOT — DESKTOP GRID PAGE]

[INSERT SCREENSHOT — MOBILE GRID PAGE]

---

# Task 4 — CSS Grid Image Gallery

## What Was Implemented

Culture contains exactly nine `.gallery-item` figures: six car illustrations, a car meet, closed-course drifting and a Japanese mountain road. Seven existing assets are reused and two local SVG placeholders are added. Images remain explicitly identified as placeholders; car drawings are generic rather than model-accurate.

## Grid Configuration

`.jdm-gallery` uses `display: grid`, `grid-template-columns: repeat(auto-fit, minmax(260px, 1fr))` and `gap: 20px`. `minmax` sets a minimum track width and allows growth; `auto-fit` fits as many equal tracks as space allows. At 540px and below, an explicit single flexible column fits narrow screens.

## Image Styling

Every gallery image has `width: 100%`, `height: 240px` and `object-fit: cover`. The image keeps its proportions and may crop at its edges. The figure uses `position: relative` and `overflow: hidden` to contain the image scale and overlay. Overflow is clipped only inside gallery figures, never on the page to hide sizing bugs.

## Hover Caption

`.gallery-caption` is positioned at the bottom with a dark translucent background. Its opacity changes from 0 to 1 on hover or figure focus. Figures have `tabindex="0"` and a visible focus outline. Touch devices show captions continuously using `@media (hover: none)`. Image scaling is subtle and disabled for reduced motion.

## Screenshot

[INSERT SCREENSHOT — FULL IMAGE GALLERY]

[INSERT SCREENSHOT — GALLERY CAPTION HOVER]

---

# Combining Flexbox and Grid

Flexbox manages navigation, car cards, the home hero, manufacturer blocks, team alignment, cultural blocks and contact form rows. `.form-row` groups the name and email fields; `.radio-options` wraps native radio controls.

Grid manages the overall Culture page, sidebar/main placement and the gallery. Flexbox handles linear component alignment; Grid handles explicit rows and columns.

# Responsiveness

- Desktop: horizontal brand/navigation, three car cards per row, a sidebar/main Grid layout and multiple gallery columns.
- At 1050px and below: smaller hero text, reduced Culture padding, stacked cultural articles and form fields.
- At 768px and below: stacked header, hero and contact sections; single-column named Grid areas; centered wrapping navigation.
- At 540px and below: single-column cards and gallery, stacked team members and smaller headings/padding.
- `.table-scroll` retains horizontal scrolling inside the table region. Images use responsive sizing, and flex/grid children have sensible minimum widths.

Target validation widths: 1440px, 1024px, 768px and 390px.

## Screenshot

[INSERT SCREENSHOT — 390PX MOBILE VIEW]

---

# Final Website

The original four pages remain connected with the same visual identity. Modern layout rules replace manual percentage and inline-block columns. Buttons align consistently, the Culture sidebar provides section navigation, and the nine-image gallery adds a clear Grid demonstration. The form remains an HTML-only classroom demo and does not deliver messages.

## Screenshot

[INSERT SCREENSHOT — FINAL HOME PAGE]

# Deployment

GitHub Pages / Netlify URL:

[ADD URL]

Publish the contents of `jdm-assignment-1/` as the site root, keeping `index.html` beside the other three HTML files. All internal paths are relative. No build or JavaScript dependency exists. Actual publication has not been performed.

# Final Reflection

Draft to review and personalize: This upgrade helped us understand the difference between arranging a row of components with Flexbox and defining a page in two dimensions with Grid. We practiced equal-height cards, spacing with gap, named areas and responsive breakpoints. We also learned to keep labels and keyboard focus useful while improving the visual layout.

[ADD YOUR OWN EXPERIENCE AND CHALLENGES]

# Defense Cheat Sheet

- **What is Flexbox?** A CSS layout system for arranging items along a row or column.
- **What is CSS Grid?** A CSS layout system that controls rows and columns together.
- **Main difference between Flexbox and Grid.** Flexbox handles one main direction; Grid defines a two-dimensional layout.
- **Why is Flexbox good for navigation?** It centers our links and spaces the logo and menu easily.
- **Why is Flexbox good for cards?** It wraps cards and stretches cards in each row to equal height.
- **What does display: flex do?** It makes direct children flex items.
- **What does flex-direction do?** It chooses row or column; our cards use column.
- **What does justify-content do?** It aligns items along the main axis; the header uses space-between.
- **What does align-items do?** It aligns items on the cross axis; our header uses center.
- **What does gap do?** It adds space between items without adding outer margins.
- **What does flex-wrap do?** It lets our car cards and navigation move onto another line.
- **What does flex: 1 1 320px mean?** Grow factor 1, shrink factor 1, starting basis 320px.
- **How were equal-height cards achieved?** The row stretches cards, and each card and body is a growing column flex container.
- **Why was margin-top: auto used?** It pushes the card button to the bottom of the available space.
- **What does display: grid do?** It makes direct children grid items, used by page-grid and jdm-gallery.
- **What does grid-template-columns do?** It defines the number and size of column tracks.
- **What does 1fr mean?** One share of the available flexible space.
- **What does grid-template-areas do?** It names regions and describes where they appear in the grid.
- **What does grid-area do?** It assigns an element to a named region, such as main.
- **Why are header and footer repeated twice?** Each spans both desktop columns.
- **How was the sidebar placed on the left?** The middle area row is "sidebar main".
- **How does the Grid layout change on mobile?** At 768px it becomes one column: header, main, sidebar, footer.
- **What does repeat() do?** It repeats a track definition in the gallery columns.
- **What does minmax() do?** It sets a minimum and maximum track size.
- **What does auto-fit do?** It fits as many gallery tracks as possible and collapses empty tracks.
- **What does object-fit: cover do?** It fills the image box without stretching, cropping when needed.
- **How does the gallery hover caption work?** An absolutely positioned bottom caption changes opacity on hover or focus.
- **What is a media query?** A conditional CSS rule, such as our max-width: 768px layout changes.
- **Why do cards wrap on smaller screens?** flex-wrap allows a new row when the card bases and gaps no longer fit.
- **When should you use Flexbox instead of Grid?** For a row or column of components, such as our navigation or card contents.
- **When should you use Grid instead of Flexbox?** For coordinated rows and columns, such as the Culture layout or gallery.
- **How did Assignment 2 improve Assignment 1?** It added responsive modern layouts, consistent card alignment, a topic sidebar and an accessible gallery while retaining the original features.
