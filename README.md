# Speaker Segmentation Evaluation Dataset

## 📌 Overview
This dataset is prepared for evaluating speaker segmentation (diarization) systems.

- Total files: 20  
- Data type: Multi-speaker audio recordings  
- Labels: RTTM format (speaker-level segmentation)  
- Languages: German, Japanese, Spanish, Chinese, English  
- Use case: Segmentation / diarization model evaluation  

---

## 📂 Dataset Structure

speaker-segmentation-dataset/

├── dataset/  
│   ├── audio/        # Audio files (.wav)  
│   ├── labels/       # RTTM files (.rttm)  

├── samples/          # Sample pair for quick testing  
│   ├── sample.wav  
│   ├── sample.rttm  

└── README.md  

👉 Each `.wav` file has a corresponding `.rttm` file with the same name.

---

## 📁 File Naming

### CALLHOME dataset samples
- callhome_deu_01  
- callhome_deu_02  
- callhome_jpn_01  
- callhome_jpn_02  
- callhome_jpn_03  
- callhome_spa_01  
- callhome_spa_02  
- callhome_spa_03  
- callhome_zho_01  
- callhome_zho_02  

### English samples
- abjxc  
- afjiv  
- ahnss  
- aisvi  
- akthc  
- ampme  
- asxwr  
- atgpi  
- aufkn  
- azisu  

---

## 🌍 Languages Covered

- German (deu)  
- Japanese (jpn)  
- Spanish (spa)  
- Chinese (zho)  
- English  

---

## 🏷️ Label Format (RTTM)

Example:

SPEAKER callhome_deu_01 1 0.00 2.50 <NA> <NA> speaker1 <NA> <NA>

### Field Explanation:
- callhome_deu_01 → recording ID  
- 1 → channel ID  
- 0.00 → start time (seconds)  
- 2.50 → duration (seconds)  
- speaker1 → speaker label  

---

## 🔍 Segmentation Details

- Speaker segments are defined using timestamps  
- Each RTTM file represents speaker turns  
- Time resolution is in seconds  
- Compatible with diarization evaluation frameworks  

---

## ✅ Validation

The dataset has been validated for:

- Audio and RTTM alignment  
- Correct timestamp ranges  
- Consistent formatting across all files  
- No missing or corrupted labels  

---

## 🚀 How to Use

Example:

python evaluate.py \
  --audio dataset/audio/callhome_deu_01.wav \
  --rttm dataset/labels/callhome_deu_01.rttm  

Steps:
1. Load audio file  
2. Load corresponding RTTM file  
3. Run segmentation evaluation  

---

## 📦 Full Dataset Access

👉 Google Drive Link: [https://drive.google.com/drive/folders/1wAPMETkc5HlYxdrENFCiL-51iujfGg4o?usp=drive_link]

---

## ⚠️ Notes

- Dataset contains 20 files  
- Multi-language dataset  
- Suitable for testing and benchmarking  

---

## 📌 Future Improvements

- Add more files  
- Add more languages  
- Include overlapping speech  

---

## 📬 Contact

For any questions, please contact the dataset owner.
