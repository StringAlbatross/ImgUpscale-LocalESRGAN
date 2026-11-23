<p align="center">
  <img src="https://i.postimg.cc/6p8QV1My/banner.png" alt="ImgUpscale Local AI Upscaler — Offline 2x & 4x Photo, Anime & Texture Enhancer" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-0078D6?style=flat-square&logo=windows" alt="Platform: Windows 10/11 x64">
  <img src="https://img.shields.io/badge/Mode-AI%20Image%20Upscaler-2EA44F?style=flat-square" alt="Mode">
  <img src="https://img.shields.io/badge/Release-imgupscale--v1.3-5391FE?style=flat-square" alt="Release Tag">
  <img src="https://img.shields.io/badge/License-MIT-8B5CF6?style=flat-square" alt="License: MIT">
</p>

# ImgUpscale Local AI Upscaler — Offline 2x & 4x Photo, Anime & Texture Enhancer

**Online AI image upscalers charging credits per photo or stamping watermarks on 4K exports? Enhance blurry screenshots, old family photos, anime wallpapers, and game textures 2x or 4x locally on your GPU—100% offline and unlimited.**

ImgUpscale Local AI Upscaler wraps Vulkan/DirectML Real-ESRGAN inference into a simple drag-and-drop Windows desktop utility: **sharpening edges, reconstructing fine textures, and batch-exporting crisp PNG/JPG files without Python setup or cloud uploads**.

This project is aimed at **Windows 10 and Windows 11 (64-bit) creators, photographers, and modders** who need fast, unlimited 2x/4x image upscaling on local hardware.

## Quick Use-Case & Troubleshooting Reference

| Scenario / Issue | Cause | Solution |
| --- | --- | --- |
| Web AI upscalers limit free users to 2 images or add watermarks | Cloud GPU services paywall batch runs and 4K exports | Upscale unlimited images locally at 2x or 4x with zero watermarks |
| Standard bicubic resizing makes small images blurry and pixelated | Traditional interpolation stretches pixels without reconstructing edges | Use neural Real-ESRGAN Photo & Anime models for crisp detail |
| Installing Python, PyTorch, and CUDA takes 10+ GB and breaks easily | Command-line ML repos require complex virtual environments | Run a standalone portable Windows `.exe` with bundled Vulkan backend |
| Upscaling large 4K images crashes out-of-VRAM on 6 GB–8 GB GPUs | Full-frame inference exceeds GPU memory buffers | Automatic tile-based processing handles huge outputs cleanly |

## Download for Windows

[**Download ImgUpscale.zip — Latest GitHub Release (Windows x64)**](../../releases/latest/download/ImgUpscale.zip)  
[View All Releases & Changelog](../../releases) · [Report an Issue](../../issues)

### Why use `ImgUpscale.exe`? (Key features)

- Upscales `.jpg`, `.png`, `.webp`, and `.bmp` images by `2x` or `4x` using local Real-ESRGAN models.
- Includes dedicated presets for **General Photography** and **Anime / Illustration / Game UI**.
- Uses tiled Vulkan/DirectML GPU inference so even 6 GB–8 GB GPUs upscale large images without OOM crashes.
- Supports drag-and-drop batch folder processing with zero watermarks or internet connection.

### Sample Output

```text
[ImgUpscale] Loaded: Screenshot_720p.png (1280x720 -> Target 4x: 5120x2880)
[INFO] Compute Backend  : Vulkan GPU (Tile Size: 256px | Model: RealESRGAN-x4plus)
[OK]   Exported Image   : Screenshot_720p_4x.png (5120x2880 | Done in 2.4s)
```

The release ZIP is named `ImgUpscale.zip`; the Windows executable inside is named `ImgUpscale.exe`.

1. Close ImgUpscale before updating or replacing executable files.
2. Click **Download ImgUpscale.zip** above.
3. Right-click the downloaded archive and choose **Extract All**.
4. Open the extracted folder and run `ImgUpscale.exe`.
5. Review the options and output paths before processing files.

**Requirements:** Windows 10 or 11 (64-bit), 8 GB+ RAM (Vulkan / DirectX 12 GPU acceleration supported).

### Verification & Windows SmartScreen Note

- **Offline & standard user permissions:** `ImgUpscale.exe` runs locally without uploading your files and does not require disabling Windows Defender.
- **Windows SmartScreen:** Because this is an independent open-source utility without a commercial EV code-signing certificate, Windows SmartScreen may show *"Windows protected your PC"* on first launch. Click **More info → Run anyway** after verifying the release checksum on the [Releases](../../releases) page.

## Problems this project solves

### Zero subscription fees or per-image credit limits

Enhance entire folders of wallpapers, product photos, or textures locally.

### Dedicated Photo vs. Anime/Illustration models

Prevents over-smoothing on real photos while keeping line art razor-sharp.

### Tiled processing prevents GPU out-of-memory errors

Processes large outputs safely on mid-range graphics cards.

### 100% private local processing

Personal photos and unreleased artwork never leave your drive.

## Default folders and configuration paths

ImgUpscale saves enhanced images into an `Upscaled` subfolder next to your source files:

```text
%USERPROFILE%\Pictures\Upscaled\
```

Typical directory layout:

```text
Pictures\Raw\
├── wallpaper_1080p.png
└── Upscaled\
    └── wallpaper_1080p_4x.png   (Crisp 4x super-resolution output)
```

Original images are never overwritten.

## Quick start guide

Follow these steps to get started:

1. **Extract `ImgUpscale.zip` to a local folder.** Avoid running directly from inside Explorer's temporary ZIP preview.
2. **Launch `ImgUpscale.exe` and drop images or folders onto the window.** Supports JPG, PNG, WebP, and BMP.
3. **Select scale factor (`2x` or `4x`) and model (`Photo` or `Anime/Art`).** Click **Upscale All**.
4. **Open the `Upscaled` folder to inspect the enhanced images.** Compare 100% zoom detail against your source files.

### Data safety note

Source files remain untouched in their original directory.

## What the status summary shows

ImgUpscale displays **input/output pixel dimensions, active Vulkan GPU device, tile count, and elapsed time**.

## FAQ

**Does ImgUpscale work on AMD and Intel GPUs as well as NVIDIA?**

Yes—it uses standard Vulkan compute, supporting NVIDIA, AMD Radeon, and Intel Arc graphics cards.

**Does it add watermarks or require an account?**

No. It runs 100% offline with zero watermarks or logins.

**What scale factors are supported?**

2x and 4x super-resolution.

## Useful reading

- [Real-ESRGAN Open-Source Reference](https://github.com/xinntao/Real-ESRGAN)

## More Windows Desktop Utilities

- [CleanCut-OfflineBgRemover](../CleanCut-OfflineBgRemover) — Offline batch image background remover & PNG cutout tool
- [SnapFormat-BatchMediaConverter](../SnapFormat-BatchMediaConverter) — Offline batch HEIC/WebP/MKV to JPG/PNG/MP4 converter
- [GIFMaker-ClipToWebP](../GIFMaker-ClipToWebP) — Convert gameplay videos into high-FPS GIF & animated WebP
- [ExifScrub-PhotoMetadataCleaner](../ExifScrub-PhotoMetadataCleaner) — Strip GPS, EXIF & camera metadata from photos offline

*Independent open-source desktop utility for Windows.*
