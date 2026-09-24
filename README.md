# JDM Legends — Assignments 1 & 2

## Project Theme

A four-page introduction to Japanese Domestic Market cars, engineering, tuning and enthusiast culture. The visual identity uses near-black surfaces, white text and red accents. Originally built for Assignment 1 and upgraded in place for Assignment 2 using HTML5, CSS3 and local SVG assets only. No JavaScript, libraries, frameworks or build step.

## Team

```text
Team name: [TEAM NAME]
Group: [GROUP]

Student 1: [STUDENT 1 NAME]
Pages:
- index.html
- cars.html

Student 2: [STUDENT 2 NAME]
Pages:
- culture.html
- contact.html
```

## Pages

- **Home:** JDM introduction, reasons for its popularity, six manufacturers and Student 1 biography placeholders.
- **Cars:** six Flexbox cards linking to highlighted specification rows, an ordered top-five list and a five-column comparison table.
- **Culture:** named Grid areas with a topics sidebar, community, drifting, modifications, terminology, a nine-image Grid gallery and Student 2 biography placeholders.
- **Contact:** community introduction and a labeled demonstration form with text, email, select, radio, color and textarea controls.

## HTML Features Used

Headings, paragraphs, strong emphasis, ordered and unordered lists, images with meaningful alt text, relative links, table with caption and scoped headings, form with labels and fieldset, and semantic header/nav/main/section/article/aside/footer elements. Every page includes a credit comment in its head and a footer listing both students.

## CSS Features Used

- Element selectors: `body`, `h1`, `p`.
- Class selectors: `.car-card`, `.profile-image`, `.container`.
- ID selectors: `#main-header`, `#contact-form`.
- Descendant selectors: `nav a`, `.car-card img`, `footer p`.
- Box model: margins, padding, borders, width, max-width and border-box sizing.
- Consistent typography and colors, hover pseudo-class, visible keyboard focus, form styling and image styling.
- Circular profiles use `border-radius: 50%`.
- Flexbox: shared header/navigation, six car cards and their contents, hero, manufacturers, team components and form rows.
- CSS Grid: named header/sidebar/main/footer areas on Culture and a nine-image gallery.
- Responsive breakpoints at 1050px, 768px and 540px; touch-friendly captions, visible keyboard focus and reduced-motion support.

## How to Run

Open `index.html` in a web browser. The entire site works as local files.

Alternatively, from this folder run `python -m http.server 8000`, then open `http://localhost:8000`. Python is only an optional preview server, not a website dependency.

## Contact Form Behavior

The form uses `action="#"` and `method="get"`. Native browser validation checks required fields and email format. A valid submission reloads the page and puts named field values in the URL. It does not send email, store data or register anyone. The visible notice explains this; use sample details. There is no simulated success message.

## Local Images and Replacements

No source photographs were available. All ten SVG files were created for this project as clearly labeled placeholders. The six car images depict a generic coupe, **not accurate drawings of the named models**. No external image requests or missing image paths are used.

| Local asset | Intended replacement |
| --- | --- |
| `images/r34-placeholder.svg` | Licensed Nissan Skyline GT-R R34 photo (home and cars) |
| `images/supra-placeholder.svg` | Licensed Toyota Supra MK4 photo (cars and contact) |
| `images/rx7-placeholder.svg` | Licensed Mazda RX-7 FD photo |
| `images/nsx-placeholder.svg` | Licensed Honda NSX photo |
| `images/evo-placeholder.svg` | Licensed Mitsubishi Lancer Evolution VIII photo |
| `images/sti-placeholder.svg` | Licensed Subaru Impreza WRX STI GD photo |
| `images/culture-placeholder.svg` | Licensed Japanese car meet, track or landscape photo |
| `images/meet-placeholder.svg` | Licensed JDM car meet photograph |
| `images/drift-placeholder.svg` | Licensed closed-course drifting photograph |
| `images/profile-placeholder.svg` | Each student's own profile photo, if required |

Save replacement photos locally, update the matching `src`, `alt`, `width` and `height` values, and record attribution/license information here. Remove visible placeholder wording when replacing an image. Use separate filenames for the two student portraits. SVG placeholders can remain if the assignment accepts them.

## Content References

The comparison uses approximate advertised stock power in PS, not wheel horsepower. Trims and markets vary. The examples are educational rather than buying or tuning advice.

- [Nissan Skyline GT-R V-Spec II specifications](https://www.nissan.co.jp/HERITAGE/DETAIL/280.html)
- [Toyota 1993 Supra launch](https://global.toyota/en/detail/7868203)
- [Mazda RX-7 power variants](https://newsroom.mazda.com/en/publicity/release/1998/9812/981215be.html)
- [Honda C30A engine](https://global.honda/en/tech/engine/car/C30A_NSX_vtec_DOHC/)
- [Mitsubishi vehicle history](https://www.mitsubishi-motors.com/en/company/history/car/)
- [Subaru 2004 Japanese STI spec C catalog](https://ucar.subaru.jp/php/catalog/grade.php?cat_id=10020623)

## Deployment

GitHub Pages URL: [ADD URL AFTER DEPLOYMENT]

Use the **contents of `jdm-assignment-1/` as the publishing root** so `index.html` is at the root of the published site. For example, copy this folder's contents into a dedicated repository, then publish that branch's root in GitHub Pages settings. If the whole parent workspace is published instead, the website will be under `/jdm-assignment-1/`. All internal page, CSS and image paths are relative and case-consistent. External reading links are intentionally HTTPS URLs.

## Before Submission

Replace [TEAM NAME], [STUDENT 1 NAME], [STUDENT 2 NAME], [GROUP], biography/interest/hobby placeholders, and corresponding report placeholders. Add personal photos if required, capture report screenshots and enter the actual deployment URL after publishing. `ASSIGNMENT_1_REPORT_NOTES.md` is retained unchanged as historical preparation material. `ASSIGNMENT_2_REPORT_NOTES.md` describes the current implementation, includes all ten screenshot placeholders and a defense cheat sheet. Neither is a final DOCX report. Do not submit its reflection as your own until reviewed.

## Assignment 2 Implementation Map

| Task | Location | Main classes |
| --- | --- | --- |
| Flexbox navigation | All four headers | `.header-inner`, `.nav-menu` |
| Six equal-height cards | Cars | `.car-cards`, `.car-card`, `.card-body`, `.card-button` |
| Named Grid areas | Culture | `.page-grid`, `.grid-header`, `.grid-sidebar`, `.grid-main`, `.grid-footer` |
| Nine-image Grid gallery | Culture | `.jdm-gallery`, `.gallery-item`, `.gallery-caption` |

Open `culture.html#gallery` to inspect the gallery. Car buttons navigate to existing table rows. Gallery figures support hover and keyboard focus; touch devices always show captions. Card heights are equal within each flex row. The original folder name is retained so existing links continue to work.

## Assignment 1 Preservation Checklist

The original content, table, form controls, biographies and credits are retained. Assignment 1's restriction on advanced layouts applied to that version; Assignment 2 intentionally upgrades the layout while preserving its HTML features. Real identities, photos if required, report screenshots and actual deployment remain manual steps.

- [x] Exactly 4 main HTML pages exist.
- [x] index.html exists.
- [x] cars.html exists.
- [x] culture.html exists.
- [x] contact.html exists.
- [x] Every page has valid HTML boilerplate.
- [x] Every page has a descriptive title.
- [x] Head credit comment exists on every page.
- [x] All pages are connected through navigation.
- [x] Every page contains at least one image.
- [x] Every image has valid alt text.
- [x] Ordered list exists.
- [x] Unordered list exists.
- [x] Table exists.
- [x] Table contains at least 3 columns.
- [x] Contact/registration form exists.
- [x] Form contains Name input.
- [x] Form contains Email input.
- [x] Form contains dropdown/radio/color selection.
- [x] Form contains textarea.
- [x] Form contains submit button.
- [x] About Team Member section exists for Student 1.
- [x] About Team Member section exists for Student 2.
- [x] Every page contains footer.
- [x] Footer lists both students.
- [x] css/style.css exists.
- [x] Every page links to css/style.css.
- [x] Element selector demonstrated.
- [x] Class selector demonstrated.
- [x] ID selector demonstrated.
- [x] Descendant selector demonstrated.
- [x] Typography is customized.
- [x] JDM color palette is consistent.
- [x] Links have hover effects.
- [x] Navigation is styled.
- [x] Margin demonstrated.
- [x] Padding demonstrated.
- [x] Border demonstrated.
- [x] Appropriate CSS sizing units used.
- [x] At least one circular image exists.
- [x] Form is styled.
- [x] Table is styled.
- [x] No Bootstrap/Tailwind/UI frameworks used.
- [x] No broken page links.
- [x] No broken CSS paths.
- [x] No broken image paths.
- [x] README.md exists.
- [x] ASSIGNMENT_1_REPORT_NOTES.md exists.
- [x] Project is ready for GitHub Pages.

## Assignment 2 Validation Results

All four pages passed browser checks at 1440, 1024, 768 and 390 CSS pixels (16 combinations). Navigation, images, equal card heights and aligned buttons, named Grid areas, header/footer spans, gallery columns and stacked form fields were verified. There was no document horizontal overflow. The table remains scrollable within its wrapper.

| Width | Cars per row | Gallery columns | Culture layout |
| --- | --- | --- | --- |
| 1440px | 3 | 3 | Sidebar + main |
| 1024px | 2 | 2 | Sidebar + main |
| 768px | 2 | 2 | Single column |
| 390px | 1 | 1 | Single column |

Interaction checks passed for card hover and specification links, all sidebar anchors, gallery hover/keyboard focus/touch captions/reduced motion, page navigation and native form validation/submission. Original main content, table values, form controls, team sections, local links, metadata, credits and HTML nesting passed static preservation checks. HTML/CSS formatting passed. The Assignment 1 report is unchanged byte-for-byte (SHA-256 `c89d42da42e1c12d52afe8ff52c0fdf60d78df62f7dd8d63e04d72f061ba0c96`).

Layout refinements during verification: adjusted the flex card basis to 320px for three desktop cards, widened gallery tracks to 260px for a balanced three-column desktop gallery, and kept global navigation selectors scoped so sidebar links have independent styling. No page-wide overflow hiding is used.

All implementation checklist items below are satisfied. Report screenshots remain placeholders as requested; real browser captures used for development checks were kept outside the project. Real identities, optional photos and actual deployment still need to be supplied.

## Assignment 2 Checklist

## Task 1 — Navigation

- [x] Header exists.
- [x] Logo/project name on left.
- [x] Links on right.
- [x] Header uses Flexbox.
- [x] Navigation links use Flexbox.
- [x] Links have consistent gap.
- [x] Logo and links are vertically centered.
- [x] Navigation works on mobile.

## Task 2 — Cards

- [x] At least 3 cards exist.
- [x] Every card contains image.
- [x] Every card contains title.
- [x] Every card contains text.
- [x] Every card contains button/link.
- [x] Cards container uses Flexbox.
- [x] Cards appear in a row on desktop.
- [x] Cards have equal height.
- [x] Cards have consistent gap.
- [x] Cards have hover effect.
- [x] Cards wrap/stack responsively.

## Task 3 — Grid Layout

- [x] Parent uses display: grid.
- [x] grid-template-columns is used.
- [x] grid-template-rows is used.
- [x] grid-template-areas is used.
- [x] Header spans top.
- [x] Sidebar is on left.
- [x] Main content is on right.
- [x] Footer spans bottom.
- [x] grid-area is assigned explicitly.
- [x] Mobile layout becomes single column.

## Task 4 — Gallery

- [x] At least 9 images exist.
- [x] Gallery uses CSS Grid.
- [x] Multiple equal-width columns exist.
- [x] Consistent gap exists.
- [x] Images do not distort.
- [x] Hover caption overlay exists.
- [x] Gallery is responsive.

## Final Result

- [x] Flexbox and Grid are both clearly demonstrated.
- [x] All 4 pages retain JDM styling.
- [x] Existing Assignment 1 functionality remains.
- [x] Site works at 1440px.
- [x] Site works at 1024px.
- [x] Site works at 768px.
- [x] Site works around 390px.
- [x] No unwanted horizontal scrolling.
- [x] Footer remains on all pages.
- [x] Form remains functional as HTML form.
- [x] Table remains present.
- [x] Ordered and unordered lists remain present.
- [x] Team blocks remain present.
- [x] ASSIGNMENT_1_REPORT_NOTES.md remains untouched.
- [x] ASSIGNMENT_2_REPORT_NOTES.md exists.

## Assignment 1 Regression Checklist

- [x] Exactly 4 main pages remain.
- [x] Every page has full HTML boilerplate.
- [x] Every page has descriptive title.
- [x] Credit comments remain.
- [x] Every page has navigation.
- [x] Every page contains image(s).
- [x] alt attributes remain.
- [x] Table remains.
- [x] Form remains.
- [x] Ordered list remains.
- [x] Unordered list remains.
- [x] Circular profile image remains.
- [x] Shared `css/style.css` remains.
- [x] Element selector remains.
- [x] Class selector remains.
- [x] ID selector remains.
- [x] Descendant selector remains.
- [x] Footer contains both students.
