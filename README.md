# Web Tools

A small collection of browser-based scientific tools.

## Available tool

### Online Fresnel Calculator

The Fresnel calculator can:

- Compute the Mueller matrix for arbitrary internal and external refractive indices.
- Visualize Mueller-matrix elements as a function of reflection angle.
- Explore circular polarization through the M34 element.
- Study the effect of absorption in the medium.

The calculator is implemented in JavaScript and runs entirely in a web browser.

[Open the Fresnel calculator](tools/my.jqplot.fresnel.html)

## History

The original Fresnel calculator was developed in 2012 and was previously hosted
at Texas A&M University. The source code was recovered and moved to GitHub in
2020.

This repository now provides a single landing page for the Fresnel calculator
and additional browser-based scientific tools.

## Repository structure

```text
fresnel_calculator/
├── index.html
├── README.md
├── assets/
│   └── style.css
├── tools/
│   ├── my.jqplot.fresnel.html
│   └── future_tool.html
└── .github/
    └── workflows/
        └── pages.yml
```

`index.html` is the single landing page. Individual web applications are stored
under `tools/`.

## GitHub Pages

The GitHub Actions workflow publishes the repository as a static GitHub Pages
site whenever a commit is pushed to `main`.

After committing the files:

1. Open the repository on GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, select **GitHub Actions** as the source.
4. Push the files to `main`.

The landing page will be available at:

`https://kiwiriver.github.io/fresnel_calculator/`

The Fresnel calculator will be available at:

`https://kiwiriver.github.io/fresnel_calculator/tools/my.jqplot.fresnel.html`

## Adding another web tool

Place the new HTML file under `tools/`, for example:

```text
tools/my_new_tool.html
```

Then add a corresponding tool card/link to `index.html`. The GitHub Pages
workflow does not need to be changed.
