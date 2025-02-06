---
cssclasses:
  - wide-page
---
```dataviewjs
const trackerData = {
    year: 2025, // optional, remove this line to autoswitch year
    entries: [],
    colors: {
        "intensity": [ "rgb(255, 0, 0)", // Bright Red for 8 hours
		"rgb(255, 165, 0)", // Orange for 12 hours
        "rgb(173, 255, 47)", // Yellow-Green for 16 hours
        "rgb(0, 128, 0)", // Deep Green for 20+ hours
        ]
    },
    heatmapTitle: "⏳ Fasting Tracker Heatmap ⏳",
    heatmapSubtitle: "Track fasting durations. Green means long fasting, red means short. 🌄✨",
    intensityScaleStart: 0,
    intensityScaleEnd: 1,
};

/**
 * Calculate the intensity of fasting duration.
 * Intensity is scaled based on fasting duration:
 * - 8 hours = 0 (Red)
 * - 12 hours = 0.33 (Yellow)
 * - 16 hours = 0.66 (White)
 * - 20+ hours = 1 (Green)
 *
 * @param {number} fastingHours - Fasting duration in hours.
 * @returns {number} Intensity value between 0 (worst) and 1 (best).
 */
function calculateFastingIntensity(fastingHours) {
    if (fastingHours <= 8) return 0; // Red
    if (fastingHours <= 12) return 0.33; // Yellow
    if (fastingHours <= 16) return 0.66; // White
    return 1; // Green for 20+ hours
}

for (let page of dv.pages('"02 Areas/📧 Personal Notes/📓 Daily Notes"').where(p => p.fasting)) {
    const fastingHours = Number(page.fasting); // Assuming 'fasting' field contains hours as a number
    trackerData.entries.push({
        date: page.file.name,
        intensity: calculateFastingIntensity(fastingHours),
        content: await dv.span(`[](${page.file.name})`),
    });
}

renderHeatmapTracker(this.container, trackerData);

``