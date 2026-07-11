# Weather Field

The weather condition(s) currently active. Usually contains one entry, but can contain more than one when multiple conditions apply at once.

|field|type|description|
|---|---|---|
|weather|list of objects|The weather condition(s) currently active. Usually contains one entry, but can contain more than one when multiple conditions apply at once (e.g., `light drizzle with partial sun).|
|weather[].id|integer|A numeric code identifying the specific weather condition, grouped by category (e.g., 200–232 = `Thunderstorm`, 300–321 = `Drizzle`, 500–531 = `Rain`, 600–622 = `Snow`, 800 = `Clear`, 801–804 = `Clouds`). Useful for programmatically grouping related conditions — e.g., checking whether a code falls in the `200–299` range to detect any thunderstorm variant, rather than matching against the main text field.|
|weather[].main|string|A short weather category (e.g., `Rain`, `Clear`, `Snow`), useful for building conditional logic in an application.|
|weather[].description|string|A more detailed, human-readable phrase describing the condition (e.g., `light intensity drizzle`), suited for direct display to end users.|

```json
"weather": [{"id": 300, "main": "Drizzle", "description": "light intensity drizzle", "icon": "09d"}]
```
