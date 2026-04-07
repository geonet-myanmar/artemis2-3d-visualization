# Contributing to Artemis II Trajectory Visualization

Thank you for your interest in improving this project. Contributions that enhance accuracy, add features, or fix issues are welcome.

## How to Contribute

### Reporting Issues

If you find a bug, data inaccuracy, or have a feature request, please [open an issue](https://github.com/geonet-myanmar/artemis2-trajectory/issues) with the following details:

- A clear, descriptive title
- Steps to reproduce the issue (for bugs)
- Browser and OS information
- Screenshots, if applicable
- For data corrections, please include the official source link

### Submitting Changes

1. **Fork** the repository and create a new branch from `main`:
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes** in the new branch. Since the visualization is a single HTML file, most edits will be to `index.html`.

3. **Test locally** by opening `index.html` in a browser. Verify that:
   - The 3D scene renders correctly
   - All ten mission phases display properly on the timeline
   - The lunar flyby swings behind the Moon before the distance-record phase
   - Telemetry values update as the simulation progresses
   - Camera controls (drag, scroll, touch) still work
   - No console errors appear

4. **Update related assets** if your change affects visuals, mission copy, or telemetry. In particular, keep `artemis2-trajectory.gif` and the README metadata in sync with `index.html`.

5. **Commit** with a clear message:
   ```bash
   git commit -m "Add: description of your change"
   ```

6. **Push** and open a Pull Request against `main`.

## Contribution Areas

Here are areas where contributions would be especially valuable:

### Data Accuracy
- Updating trajectory parameters with post-mission finalized data once NASA publishes it
- Correcting any telemetry values (velocity profile, distance calculations) against official sources
- Adding additional mission milestones as they become available

### Visualization Enhancements
- Improving the Earth and Moon shaders (higher-fidelity textures, cloud layers)
- Adding the Deep Space Network communication cone visualization
- Implementing a more physically accurate n-body trajectory simulation
- Adding the Orion spacecraft's solar eclipse view during flyby

### User Interface
- Responsive design improvements for tablet and mobile
- Accessibility enhancements (screen reader support, keyboard navigation)
- Localization and internationalization (Myanmar, Thai, and other languages)

### Performance
- WebGL optimization for lower-end devices
- Level-of-detail rendering for the starfield and celestial bodies
- Frame rate monitoring and adaptive quality

## Code Style

- Use clear, descriptive variable names
- Comment complex shader code and physics calculations
- Keep the single-file architecture — all HTML, CSS, and JS should remain in `index.html`
- External dependencies should be loaded from CDNs (currently only Three.js and Google Fonts)
- Use `const` and `let` (no `var`)

## Data Source Requirements

Any new data added to the project must be traceable to an official source. Acceptable sources include:

- NASA.gov (mission pages, blogs, press releases)
- Canadian Space Agency (asc-csa.gc.ca)
- European Space Agency (esa.int)
- Peer-reviewed publications
- Official NASA social media accounts (for real-time updates during mission)

When adding or modifying data values, include the source URL in a code comment.

## Code of Conduct

This project follows standard open-source community practices. Please be respectful, constructive, and inclusive in all interactions. Focus discussions on the technical content of contributions.

## Questions?

If you have questions about the codebase or want to discuss a larger change before implementing it, feel free to open a Discussion or reach out via an Issue.

---

*Thank you for helping make space exploration data more accessible and visual.*
