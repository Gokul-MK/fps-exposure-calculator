# FPS vs Exposure Time Calculator

An interactive, browser-based calculator for understanding the relationship between camera frame rate (FPS) and exposure time. Useful for camera testing, ISP tuning, and product quality (PQ) validation.

## Live Demo

**Website:** https://gokul-mk.github.io/fps-exposure-calculator/

> If the live demo returns a 404, check the repository's **Settings → Pages** and confirm that GitHub Pages is publishing from the `main` branch and the `/(root)` folder. Allow a short time for the deployment to finish.

## Features

- Adjust frame rate from **1 to 240 FPS**.
- Adjust exposure time from **0.1 to 100 ms**.
- Automatically calculate the theoretical frame period.
- Display nominal time remaining in the frame period.
- Show the exposure duty cycle.
- Highlight when exposure time exceeds the theoretical frame period.
- Use quick presets for common example values.
- Responsive layout for desktop and mobile browsers.
- Runs locally in a modern browser; no installation or external JavaScript libraries are required.

## Formulas

Frame period in milliseconds:

```text
Frame period (ms) = 1000 / FPS
```

Nominal time remaining:

```text
Remaining time (ms) = Frame period (ms) - Exposure time (ms)
```

Exposure duty cycle:

```text
Duty cycle (%) = Exposure time / Frame period × 100
```

## How to Use

1. Open the [live calculator](https://gokul-mk.github.io/fps-exposure-calculator/).
2. Move the **Frame rate** slider to set the desired FPS.
3. Move the **Exposure time** slider to set the exposure duration.
4. Review the frame period, nominal remaining time, duty cycle, and status message.
5. Select a quick preset to load an example combination.

## Run Locally

1. Download or clone this repository.
2. Open `index.html` in a modern web browser.

No build step or package installation is required.

## Publish with GitHub Pages

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch `main` and folder `/(root)`.
4. Save and wait for the deployment to complete.
5. Open the live demo link above.

## Important Technical Note

This calculator uses the theoretical relationship between frame rate and frame period. Actual camera exposure limits can depend on sensor readout timing, blanking intervals, trigger mode, firmware, and camera implementation. Values shown here are for timing guidance and should be checked against the camera's actual reported FPS and applied exposure settings.

## Repository Structure

```text
fps-exposure-calculator/
├── index.html   # Interactive calculator (HTML, CSS, and JavaScript)
└── README.md    # Project documentation
```

## License

No license has been specified for this repository yet. Unless a license is added, the repository's contents remain subject to the applicable default copyright rules.
