# Background Image Composer

Creates a smooth background image using one image with any dimension, such that it fits a 1920x1080 resolution and looks good.

Each output image consists of a blurred and zoomed version of the original, to cover the whole 1920x1080 area, and then with a left-faded version of the original image overlaid on the right side, scaled to fit the height of 1080.

## Features

- Takes any `.jpg`, `.jpeg`, or `.png` images from a source directory
- Creates a faded version of each image using a left-to-right transparency mask
- Blends the faded image over a blurred, resized version of the original
- Outputs 1920x1080 background images with soft, elegant overlays

## Requirements

- [ImageMagick](https://imagemagick.org) (`magick` and `identify` must be available)

Install on Arch Linux:

```bash
sudo pacman -S imagemagick
```

## Usage

```bash
./compose-backgrounds.sh <source_dir> <output_dir>
```

- `<source_dir>`: Directory containing `.jpg`, `.jpeg`, or `.png` files
- `<output_dir>`: Directory where final images will be saved

### Example

```bash
./compose-backgrounds.sh ./ai-output ./backgrounds
```

This reads images from `./ai-output/` and saves results in `./backgrounds/`.

## Output

Each output image:

- Is resized and blurred to 1920x1080
- Has the original image faded and overlaid on the right side
- Preserves original file names

Let me know if you want a version with default fallbacks or dry-run support.
