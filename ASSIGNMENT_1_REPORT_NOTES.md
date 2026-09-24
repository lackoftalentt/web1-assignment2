# Assignment 1 — HTML & CSS Basics

## Team Information

Team Name: [ADD TEAM NAME]

Group: [ADD GROUP]

Members:

1. [STUDENT 1 NAME]
   Pages: Home (`index.html`) and Cars (`cars.html`).
2. [STUDENT 2 NAME]
   Pages: Culture (`culture.html`) and Contact (`contact.html`).

---

## Objective

Create a connected four-page website that demonstrates semantic HTML, lists, images, tables and forms, styled with one shared external CSS file. Practice readable typography, selectors, the box model and basic responsive adjustments without UI frameworks.

## Project Theme

JDM provides a coherent theme for descriptions, specifications, cultural explanations and a community form. Near-black surfaces and a red accent reference automotive design while keeping the pages readable. JDM strictly refers to the Japanese domestic market; the website also introduces the broader enthusiast culture.

---
## Page 1 — Home

### Purpose

Introduce JDM and the team.

### HTML Elements Used

`header`, `nav`, `main`, `section`, `article`, `h1`–`h3`, `p`, `strong`, `ul`, `img`, `figure`, `a`, `footer`.

### CSS Styling

Large hero typography, inline-block hero columns, manufacturer blocks and a circular `.profile-image`.

### Steps Performed

Created shared navigation; wrote the JDM explanation and popularity list; added six manufacturer blocks; added Student 1 placeholders.

### Screenshot

[INSERT SCREENSHOT OF HOME PAGE HERE]

---

## Page 2 — JDM Cars

### Purpose

Introduce six iconic cars and compare representative stock specifications.

### HTML Elements Used

`article`, headings, paragraphs, images, `ol`, `table`, `caption`, `thead`, `tbody`, `tr`, `th`, `td`.

### Table Implementation

Five columns: model, engine, approximate power in PS, drivetrain and production era. Six body rows use row headings. Column headings use `scope="col"`. The caption names the table; an adjacent note explains the figures. `.table-scroll` contains overflow and can receive keyboard focus.

### CSS Styling

Two-column inline-block `.car-card` blocks, consistent image ratios, borders and a horizontally scrollable table wrapper.

### Steps Performed

Added six car descriptions and engine labels; added the top-five ordered list; created and styled the comparison table; noted differences between trims.

### Screenshot

[INSERT SCREENSHOT OF CARS PAGE HERE]

---

## Page 3 — JDM Culture

### Purpose

Explain car meets, tuning, drifting and enthusiast vocabulary.

### HTML Elements Used

Sections, articles, headings, paragraphs, a modifications `ul`, images and a team biography block.

### CSS Styling

Wide landscape illustration, basic two-column articles, highlighted `.culture-item` blocks and a circular profile.

### Steps Performed

Wrote community and drifting text; added six modification categories and six terms; added Student 2 placeholders.

### Screenshot

[INSERT SCREENSHOT OF CULTURE PAGE HERE]

---

## Page 4 — Contact

### Purpose

Demonstrate an accessible community contact form.

### HTML Elements Used

`form`, `label`, `input`, `select`, `option`, `fieldset`, `legend`, `textarea`, `button`, `aside`, `img`.

### Form Implementation

Name uses `type="text"`; email uses `type="email"`. The form also includes a manufacturer select, five style radios, color picker and message textarea. Required name/email/message fields use browser validation. `action="#"` with GET reloads the page with data in the URL; there is no backend, persistence or delivery. Use sample data.

### CSS Styling

Dark input surfaces, visible focus outlines, radio/color styling and a red button with hover feedback.

### Steps Performed

Added labels and unique IDs; grouped radio buttons with a shared name; added native validation and a visible demo notice; styled the form and community panel.

### Screenshot

[INSERT SCREENSHOT OF CONTACT PAGE HERE]

---

## CSS Selectors

### Element Selector

`body` sets the shared font, foreground, background and line-height. `h1` sets the main heading scale.

### Class Selector

`.car-card` applies width, margin, border and background to each car article. `.profile-image` makes both profile placeholders circular.

### ID Selector

`#main-header` gives the header its background, border and padding. `#contact-form` gives the contact form a panel surface.

### Descendant Selector

`nav a` styles links inside navigation. `.car-card img` sizes only images within car cards. `footer p` sets smaller footer text.

## Box Model

`.container` has `width: 90%`, `max-width: 1200px` and `margin: 0 auto`. `.panel` has interior padding and a visible border. Cards use margins to separate neighboring content. The universal reset uses `box-sizing: border-box` so padding and borders are included in declared widths.

## Typography and Color Palette

Arial/Helvetica/system sans-serif requires no downloaded fonts. Large, tightly spaced headings establish hierarchy; body text uses line-height 1.7. The palette is near-black `#101112`, dark surface `#191b1d`, white `#f4f4f4`, muted gray `#b3b5b8` and red `#ff5863`. Focus outlines and underlined source links make interaction visible.

## Assets

All images are local original SVG placeholders. Car illustrations are generic, not model-accurate. Follow README replacement instructions for licensed photographs and personal portraits. No identity details have been invented.

## Deployment

GitHub Pages URL:

[ADD URL]

Publish the contents of `jdm-assignment-1/` as the site root. This project is prepared for hosting but has not been deployed.

## Final Reflection

Draft for the students to personalize: This project demonstrates how semantic HTML gives content structure and shared CSS creates a consistent appearance. Lists, tables and labeled controls serve different purposes. Relative paths connect the pages and assets, while simple media queries help the same content fit smaller screens.

[ADD YOUR OWN LEARNING EXPERIENCE AND CHALLENGES]

---

# Defense Cheat Sheet

- **What is HTML?** The markup language used to structure our four pages.
- **What is CSS?** The language used in css/style.css to control appearance and layout.
- **What is &lt;!DOCTYPE html&gt;?** It tells the browser to use modern HTML standards mode.
- **What is &lt;head&gt;?** The metadata area containing our title, character encoding, viewport, credit comment and stylesheet link.
- **What is &lt;body&gt;?** The page content, including navigation, main sections and footer.
- **Difference between &lt;h1&gt; and &lt;p&gt;.** h1 is the main page heading; p contains paragraph text.
- **Difference between &lt;ol&gt; and &lt;ul&gt;.** ol numbers the Cars top-five list; ul gives bullet points to popularity and modifications.
- **What is an HTML attribute?** Extra information on an element, such as href, src, id or required.
- **What does alt do on an image?** It supplies a text alternative; ours clearly describes each placeholder.
- **What is an &lt;a&gt; tag?** A hyperlink, such as the Cars navigation link.
- **What is a relative path?** A location resolved from the current document, such as images/r34-placeholder.svg.
- **How are the 4 pages connected?** Every header links to index.html, cars.html, culture.html and contact.html.
- **What is a table?** A structure for related data in rows and columns; ours compares car specifications.
- **What are &lt;tr&gt;, &lt;th&gt;, and &lt;td&gt;?** A table row, a heading cell and a data cell.
- **What is an HTML form?** A group of controls for entering data; our form is a classroom demo without a backend.
- **Difference between type=&quot;text&quot; and type=&quot;email&quot;.** Text accepts general text; email lets the browser check email syntax.
- **What is &lt;select&gt;?** The dropdown for choosing a favorite manufacturer.
- **What is &lt;textarea&gt;?** The multiline message control.
- **What is external CSS?** Styles stored in a separate file shared by the pages.
- **How is style.css connected to HTML?** Each head has &lt;link rel=&quot;stylesheet&quot; href=&quot;css/style.css&quot;&gt;.
- **What is an element selector?** It matches a tag name, such as body or h1.
- **What is a class selector?** It matches a class attribute, such as .car-card.
- **What is an ID selector?** It matches a specific id, such as #contact-form.
- **Difference between class and ID.** Classes can repeat on a page; an ID must be unique within that page.
- **What is a descendant selector?** It matches elements inside another element; nav a targets navigation anchors.
- **What is the CSS box model?** Content, padding, border and margin together describe an element’s box.
- **What is margin?** Space outside a border; card margins separate articles.
- **What is padding?** Space inside a border; panels use padding around their content.
- **What is border?** The visible edge around a box, such as the form’s 1px border.
- **What is box-sizing: border-box?** Declared width includes padding and border, simplifying our percentage columns.
- **What is :hover?** A pseudo-class active while the pointer is over an element; our links and buttons change appearance.
- **What is :focus?** A pseudo-class active when a control receives focus; our inputs gain an outline.
- **What does border-radius: 50% do?** It rounds the square profile images into circles.
- **What is max-width?** It caps width; our container stops growing at 1200px.
- **What does margin: 0 auto usually do?** It centers a block of limited width horizontally.
- **What is semantic HTML?** Elements describe purpose, such as nav for navigation and footer for page credits.
- **Why is the same stylesheet used on all pages?** It keeps styling consistent and lets one edit update all four pages.
- **Why are relative paths important for GitHub Pages?** They keep internal links and assets working when the site is hosted under a repository subdirectory.
