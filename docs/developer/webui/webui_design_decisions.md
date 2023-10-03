---
id: webui_design_decisions
title: WebUI Design Decisions
---

The aim of this section is create an overview of the individual design decisions
that drove the development of the WebUI project. Note that above all other
choices, it was an aim to keep the design functional and easy to implement. At
the end of the day, Rucio and the WebUI are tools used by specialists. In
addition, we are no graphic designers. It followed that the WebUI is styled in
its entirety by simple Tailwind classes, using the default colour palette, and
minimising fancy additions such as animations, fonts, gradients, etc.

As a reminder, the requirements were:

- Common design language
- Dark mode
- Responsive
- Accessible

## General Guiding Concepts

### Font

We make use of one single font throughout the entire project, this is the system
monospace font. The Tailwind-classes `sans`, `mono` and `serif` have all been
overridden in order to use the standard monospace font-family. Only by using
`forcesans` and `forceserif` can the developer force the application of system
sans and serif fonts, respectively. This design decision drastically simplified
the design process, since we use the same font for all usecases. Monospace fonts
are practical for displaying our data (which often calls for fixed-width fonts,
such as when showing and comparing numerical data). In addition, they give a
retro vibe.

While we use the same font, this font can be varied in weight and colour, it may
also be underlined and italicised.

### Icons

We make use of icons from the [Heroicons
2](https://react-icons.github.io/react-icons/icons?name=hi2) set, which is
developed and endorsed by the same team that stands behind Tailwind.  We
sometimes fall back to
[Heroicons](https://react-icons.github.io/react-icons/icons?name=hi).

There is no clear guidance on whether to use the outlined icons or the filled
ones.

### Colour

We use the [standard palette](https://tailwindcss.com/docs/customizing-colors)
provided by Tailwind. Note that the syntax for classnames associated with any
colour is of the form `<usage>-<colour name>-<colour intensity>`, such as
`bg-gray-100` for a very light grey background and `text-red-800` for a very
deep red font colour.

:::note

There are many modifiers to colour available within Tailwind, but we usually do
not use those.

:::

In general, we attempt to use colour to indicate a vertical layering in the
website. Fully saturated colours and their components are the closest to the
viewer and are "highest", whereas muted colours are the furthest away and
"lowest". In doing so, we contribute to the [visual
hierarchy](https://www.interaction-design.org/literature/topics/visual-hierarchy)
of the page.

For interactive elements such as buttons and links, we change the colour when
the mousepointer hovers over it in order to reflect the interactivity of the
element. An example would be `bg-blue-500 hover:bg-blue-600` for the standard
blue button.

Elements can be grouped (e.g. button groups, metadata listings, etc.) and these
groupings can be signified by having a darker shade than the surrounding
component. 

An example of these colour choices in action can be seen in the following image,
which shows the ListDID component. The full page as provided by NextJS would
frame this component in the Layout component, which would add a header and
footer. The screenshot was taken in light mode and using a wide screen width.

![Colour Example ListDID](/img/webui/ListDID.png)

Note the use of colour:
- The main colour is white
- Enabled buttons are in blue
- Disabled buttons in grey
- Radio buttons are grouped on a light grey background
- Metadata is underlaid with light stone background (stone is the name of the colour)
- Alternating white and stone rows
- Pastel colours of green/blue underlying the pills below the table
- Text within coloured boxes is the same shade as the box (note that "No Errors" is dark green, "Query for DID Types" is dark grey, etc.)
- Light grey outlines for the main two boxes.



### Separation of Views and Interactors

### Async

### Page Layout

## Special Components

### Interactive Elements

### Widgets




## Dark Mode

## Responsive Design


