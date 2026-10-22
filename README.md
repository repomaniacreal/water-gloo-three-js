# Water Gloo --- A Fresh Perspective

A responsive, single-page promotional landing page concept for **Water
Gloo**, built around a playful everyday-water brand identity and an
interactive 3D can that moves as visitors scroll.

## Overview

The page introduces the Water Gloo concept through editorial typography,
soft color palettes, short brand stories, and a scroll-driven 3D product
presentation. It is a front-end demo only; it does not connect to a
backend or collect visitor information.

## Features

-   **Responsive layout** for desktop and mobile screens.
-   **Scroll-driven 3D can** rendered with Three.js, with the can's
    position, scale, and rotation changing between page sections.
-   **Interactive label color concepts**:
    -   Cloud White
    -   Daylight Green
    -   Golden Hour
-   **Scroll progress indicator** at the top of the page.
-   **Reveal-on-scroll content** for selected sections.
-   **Launch waitlist modal** with email input validation for
    demonstration purposes.
-   **Reduced-motion support** for visitors who prefer less animation.
-   **Keyboard focus styles** for links, buttons, and inputs.

## Sections

1.  **Home** --- Brand introduction and primary call to action.
2.  **The Perspective** --- The brand's everyday-water concept.
3.  **The Little Details** --- Three short brand/product principles.
4.  **The Collection** --- Interactive color and label concepts.
5.  **Join / Launch Waitlist** --- A modal that previews the planned
    signup experience.

## Tech Stack

-   HTML5
-   CSS3, including responsive media queries and CSS custom properties
-   Vanilla JavaScript
-   [Three.js](https://threejs.org/) `0.170.0` loaded from jsDelivr
-   Google Fonts: Space Grotesk and DM Sans

No build tool or package installation is required. The page is
implemented in a single file named `index.html`.

## Getting Started

### Requirements

-   A modern browser with JavaScript modules and WebGL support.
-   An internet connection to load Three.js from jsDelivr and the fonts
    from Google Fonts.

### Run locally

Because the page imports Three.js as an ES module, serving it over a
local HTTP server is more reliable than opening the HTML file directly.

1.  Put `index.html` in a project folder.

2.  Open a terminal in that folder.

3.  Start a local server:

    **Python 3**

    ``` bash
    python -m http.server 8000
    ```

4.  Open <http://localhost:8000/> in your browser.

## Customization

### Brand colors

The main site colors are defined near the top of the stylesheet:

``` css
:root {
  --ink: #193a30;
  --paper: #e9ede3;
  --lime: #d4f06b;
}
```

The orange accent used by the scroll progress indicator and the Golden
Hour option is `#ee6b3e`. The collection section also uses a warm peach
background.

### Fonts

The stylesheet imports **Space Grotesk** for display typography and **DM
Sans** for body text from Google Fonts.

### 3D can label and colors

The can is created programmatically with Three.js geometry. Its label
artwork is drawn onto a canvas in the `drawLabel(color)` function. The
collection buttons update the label color and the displayed color name.

### Page content

The brand copy, section headings, navigation links, and calls to action
are written directly in the HTML. Update the text and matching section
IDs together if you change the navigation structure.

## Waitlist Form: Demo Limitation

The email form currently **does not send or store email addresses**.
Submitting it only displays a demo status message. To make the waitlist
functional, connect the form to a backend endpoint or an email marketing
service, add appropriate validation and consent/privacy messaging, and
handle submission errors.

## Troubleshooting

-   **The 3D can does not appear:** Check that WebGL is enabled and that
    the browser supports it.
-   **The page shows a 3D preview fallback:** Check your internet
    connection, access to jsDelivr, and browser console errors.
-   **Fonts look different:** Google Fonts may not have loaded; the page
    will use fallback fonts.
-   **The page looks unstyled or incomplete:** Serve the HTML from a
    local HTTP server and check the browser console for errors.

## Deployment

This is a static front-end page. You can deploy `index.html` to a static
hosting service such as GitHub Pages, Netlify, or Vercel. Make sure the
file is included in the published directory and that external CDN
requests are allowed.

## Project Status

**Concept / front-end demo.** The branding, 3D product visualization,
and waitlist interaction are present as a prototype. No production
signup service or backend integration is included.

## License

No license is specified in the source file. Add a license before
redistributing the project if needed.
