# Intelligent Parking website

Open `index.html` in a browser. It is one self-contained file, so no server or install is needed.

## Rebuild after changes
Edit files in `source/`, then from inside `source/` run:

    python build.py

This writes a fresh `../index.html`.

## Use a different video
1. Run your detector so `output.mp4` exists, then from `source/` run:
       python extract_occupancy.py "../../Project Files"
2. Copy the new `img_0.jpg` and `bounding_boxes.json` into `source/data/`.
3. Adjust the `DRIVABLE` polygon at the top of `source/routing.js` to match the new lot.
4. Run `python build.py`.
