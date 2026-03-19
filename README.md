# Image-Standardization-Pipeline-Python-PIL-
This project implements an automated image preprocessing pipeline designed for jewelry imaging workflows. It standardizes image resolution, corrects orientation using EXIF metadata, and prepares images for consistent use in catalogs, reporting, or machine learning applications.

---

## Project Overview

Jewelry imaging requires high-quality, consistent visuals for applications such as:

- E-commerce product catalogs  
- Digital asset management  
- Computer vision / ML datasets  
- Marketing and reporting  

Raw images often vary in orientation, resolution, and format. This pipeline automates the preprocessing step to ensure uniformity and quality across all images.

---

## Key Features

- Automatic EXIF-based orientation correction  
- High-quality image resizing using Lanczos resampling  
- Batch processing of multiple image formats  
- Standardized resolution output  
- Option to overwrite or save processed images separately  

---

## Workflow


Raw Jewelry Images
│
├── EXIF Orientation Detection
│ → Auto-rotation (no manual correction needed)
│
├── Resolution Standardization
│ → Resize to fixed dimensions (3000 × 4000)
│
└── Output
→ Clean, consistent images ready for use


---

## Implementation Details

### Image Processing

- Uses **Pillow (PIL)** for image manipulation  
- Extracts EXIF metadata to detect orientation  
- Applies rotation:
  - 180° (orientation = 3)  
  - 270° (orientation = 6)  
  - 90° (orientation = 8)  

---

### Resolution Standardization

- Target resolution: **3000 × 4000 pixels**  
- Uses **LANCZOS resampling** for high-quality resizing  
- Ensures minimal loss of detail for high-resolution product images  

---

### Batch Processing

- Processes all images in a directory  
- Supports formats:
  - `.jpg`, `.jpeg`, `.png`, `.gif`, `.bmp`  

---

### Output Handling

Two modes supported:

1. **Overwrite mode**
   - Replaces original images  

2. **Separate output mode**
   - Saves processed images to:
     ```
     Processed_Images/
     ```

---

## Technologies Used

- Python  
- Pillow (PIL)  
- OS file handling  

---

## Example Use Case

- Standardizing jewelry product images before uploading to an e-commerce platform  
- Preparing image datasets for computer vision models (e.g., classification, detection)  
- Ensuring consistent resolution across marketing materials  

---

## Key Skills Demonstrated

- Image preprocessing and computer vision fundamentals  
- Handling EXIF metadata  
- Batch data processing  
- Automation of domain-specific workflows  
- Preparing high-quality datasets for downstream applications  

---

## Notes

- Handles missing EXIF data gracefully  
- Designed for scalability across large image datasets  
- Can be extended with:
  - Background removal  
  - Image enhancement  
  - Metadata tagging  

---

## Author

Lakshita Arunkumar
