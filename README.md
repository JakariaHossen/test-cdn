# Test Color Picker for CDN Learning

## 🎨 Project Description

This is a simple, self-contained JavaScript color picker library created as a test project to learn the process of hosting a library on a CDN (like cdnjs or Cloudflare).

It demonstrates:
- Basic project structure (`src`, `dist`)
- Version control with Git
- Licensing
- Releasing new versions on GitHub

## 🚀 Installation / Usage (How you'd expect a user to use it)

*(Note: The actual CDN URL will be provided by cdnjs/Cloudflare once published. For now, this shows the format.)*

**Via CDN (Future State):**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Using Test Color Picker</title>
</head>
<body>
    <h1>My Webpage with Test Color Picker</h1>
    <div id="my-picker-container"></div>

    <script src="[https://example.com/cdn/path/to/test-cdn.min.js](https://example.com/cdn/path/to/test-cdn.min.js)"></script>

    <script>
        // Example usage of your color picker
        // (Adjust this based on how your actual color picker works)
        document.addEventListener('DOMContentLoaded', () => {
            const pickerElement = document.getElementById('my-picker-container');
            if (typeof initTestColorPicker === 'function') { // Assuming your picker exposes a global function
                const myPicker = initTestColorPicker(pickerElement, {
                    initialColor: '#FF0000'
                });

                myPicker.onColorChange((color) => {
                    console.log('Selected color:', color);
                    pickerElement.style.backgroundColor = color;
                });
            } else {
                console.error("Test Color Picker not loaded or API changed.");
            }
        });
    </script>
</body>
</html>
