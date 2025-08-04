# Flickr8k Dataset

The **Flickr8k dataset** is a benchmark dataset widely used for research in image captioning and multimodal deep learning. This repository provides both the image and text annotation components of the dataset, ready for use in computer vision and natural language processing projects.

---

## Contents

### 1. Flickr8k_Dataset.zip

- **Images**: 8,092 JPEG photos in a single folder (`Flicker8k_Dataset/`)
- **Size**: ~1GB
- **Source**: Selected from six different Flickr groups, designed to capture a broad variety of everyday scenes and situations
- **Content**:
  - No famous people or locations
  - Diverse, realistic scenarios
- **Structure**: All images (train, val, test) are kept together—not pre-split into sets

### 2. Flickr8k_text.zip

- **Size**: ~2.2MB
- **Components**:
  - `Flickr8k.token.txt`: Image IDs paired with 5 human-written captions per image
  - `Flickr_8k.trainImages.txt`: Filenames for training images
  - `Flickr_8k.testImages.txt`: Filenames for test images
  - `Flickr_8k.devImages.txt`: Filenames for validation (dev) images
  - `ExpertAnnotations.txt`: Identifies captions written by expert annotators vs. crowdsourced workers
  - Additional files: Various metadata and annotation resources

---

## How to Use

Download and extract the dataset with the commands below:

```bash
# Download archives from the repository releases
print("Downloading Flickr8K dataset...")
!wget -q https://github.com/Avaneesh40585/Image-Captioning/releases/download/dataset/Flickr8k_Dataset.zip  # Images
!wget -q https://github.com/Avaneesh40585/Image-Captioning/releases/download/dataset/Flickr8k_text.zip     # Text annotations

# Extract to current directory
print("Extracting dataset...")
!unzip -qq Flickr8k_Dataset.zip
!unzip -qq Flickr8k_text.zip

# Clean up to save disk space
print("Cleaning up zip files...")
!rm Flickr8k_Dataset.zip Flickr8k_text.zip

print("Dataset setup complete!")
```


After extraction, you'll find the images in the `Flicker8k_Dataset/` folder and all text files in your working directory. Use the split files to separate images for training, validation, and testing.

---

## Attribution

- Original dataset and descriptions: University of Illinois at Urbana-Champaign, created for image captioning research.
- Please ensure to cite the original Flickr8k paper when publishing work using this dataset.

---

## License

Check the original dataset documentation for terms of use and licensing conditions. Typically, usage is permitted for academic and non-commercial research.

---

## Dataset Structure Example

```
├── Flicker8k_Dataset/         # JPEG images (8,092 total)
│   ├── 1000268201_693b08cb0e.jpg
│   ├── ...
├── Flickr8k.token.txt         # Main caption file
├── Flickr_8k.trainImages.txt  # Training split
├── Flickr_8k.testImages.txt   # Test split
├── Flickr_8k.devImages.txt    # Validation split
├── ExpertAnnotations.txt      # Expert/crowd annotation info
```

---

Happy researching!
