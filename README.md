# Multimedia Signal Processing Toolkit

A collection of **CM3065 Intelligent Signal Processing** projects covering computer vision, object tracking, lossless audio coding, multimedia format compliance and emerging intelligent multimedia applications.

## Projects

### 1. Traffic Vehicle Detection, Tracking & Counting
`exercise-1-traffic-vehicle-tracking/`

Two OpenCV notebooks implement motion-based vehicle detection and tracking on traffic video.

The pipeline combines:
- polygon/rectangular road regions of interest
- MOG2 background subtraction
- frame differencing
- morphological mask cleaning
- contour filtering by size, aspect ratio, extent and solidity
- fragmented-box merging
- object tracking using overlap and centroid distance
- direction estimation
- counting vehicles travelling toward downtown

Compressed demonstration videos are included under `demos/`.

### 2. Lossless Audio Compression with Rice Coding
`exercise-2-rice-audio-compression/`

A Python notebook implementing a complete lossless audio coding pipeline:
- first-order prediction
- residual generation
- reversible signed-to-unsigned mapping
- Rice coding with `k = 2` and `k = 4`
- binary bitstream generation
- decoding and waveform reconstruction
- sample-by-sample lossless verification
- compression-size comparison

The original generated `.ex2` bitstreams are intentionally excluded because some recovered outputs were hundreds of megabytes to more than 1 GB. Small decoded WAV results are retained as evidence of reconstruction.

> The original course-provided `Sound1.wav` and `Sound2.wav` input files were not present in the recovered submission ZIP. The notebook expects them in an `Exercise2_Files` folder one level above the notebook output directory.

### 3. Video Format Compliance & Transcoding
`exercise-3-video-format-compliance/`

A notebook-based media validation tool that uses FFprobe/FFmpeg to inspect videos against a required delivery specification and convert non-compliant files.

It checks properties such as:
- container/codec compatibility
- HEVC video and AAC audio
- frame rate
- resolution and aspect ratio
- video/audio bitrate constraints

The generated converted MP4 files are omitted from version control to keep the repository lightweight; the compliance report is retained.

### 4. Emerging Intelligent Applications in Retail & E-Commerce
`exercise-4-emerging-applications-report/`

A written technical discussion of computer-vision and audio-processing applications in retail and e-commerce, including visual product search, shelf monitoring, automated checkout, accessibility and modern detection/segmentation approaches.

## Technologies

- Python
- Jupyter Notebook
- OpenCV
- NumPy
- SciPy
- FFmpeg / FFprobe
- computer vision
- object tracking
- predictive coding
- Rice entropy coding
- multimedia transcoding

## Setup

Install the Python dependencies:

```bash
pip install -r requirements.txt
```

Exercise 3 additionally requires `ffmpeg` and `ffprobe` to be available on the system PATH.

## Repository Size & Generated Artefacts

The original recovered submission contained very large generated binary outputs, including Rice-coded `.ex2` files larger than GitHub's normal file limit and multiple generated videos. These are build/results artefacts rather than source code, so they have been excluded or replaced with compressed demos. The notebooks and small evaluation outputs remain intact.

## Coursework Context

This is a cleaned portfolio version of the original CM3065 coursework. macOS metadata, Jupyter checkpoints and oversized generated results are intentionally excluded.

## Author

**Abdullah Humayun**  
BSc Computer Science – University of London / Goldsmiths
