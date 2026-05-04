# Test Automation UI - Assignment 1, Option 2

This project is a small Playwright test written in Python. It opens the [PixelsSuite](https://www.pixelssuite.com/) PNG conversion page, uploads a sample image, and checks whether a preview appears after the upload.

## What you need

- Python 3.11 or 3.12
- Google Chrome is recommended, although Playwright can install Chromium if you do not already have it

## Getting set up

If you extracted the ZIP file to your D: drive, the project should already be sitting here:

```text
D:\test_automation_ui
```

Once you are in that folder, install the Python packages and browser binaries:

```bash
pip install -U pip
pip install playwright openpyxl
playwright install
```

## Running the test

From the project folder, run:

```bash
python image_preview_test.py --url "https://www.pixelssuite.com/convert-to-png" --slow-mo-ms 2000
```

The `--slow-mo-ms` flag is there mostly to make the browser actions easier to watch while the test runs.

## What to expect

When the script finishes, it writes a row to `execution_results.csv` and saves a screenshot in the `results` folder. If everything works, you should see `results\preview_pass.png`. If something goes wrong, the script saves a failure or error screenshot instead.

## Test at a glance

| Field | Value |
|-------|-------|
| Feature tested | Image Format Conversion (Convert to PNG) |
| Test type | Positive preview check |
| Input | `sample.png` |
| Expected result | A preview is visible after upload |
| Tooling | Playwright (Python) |
