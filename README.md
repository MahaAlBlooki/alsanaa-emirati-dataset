# alsanaa-emirati-dataset

This repository contains a curated and preprocessed dataset for traditional Emirati Arabic Automatic Speech Recognition (ASR) research. The dataset includes audio file references and cleaned transcriptions based on recordings from the _Aloula_ radio station and the *Alsanaa* book by Abdullah bin Dalmook.


## 📁 Contents

- `audio/` — Emirati Arabic speech recordings in `.mp3` format
- `transcriptions.txt` — Plain text transcription for each utterance
- `metadata.csv` — Metadata file including file IDs and durations in seconds

## ✍️ Ground Truth Format

Each row in transcriptions.txt corresponds to a complete utterance. The format is:

<utterance_id> <transcription>

**Example:**
1 العلم فخر والعلم شي معنوي اكثر من انه شي مادي ...

- `1`: Utterance ID or audio file number
- Text: Original, preprocessed transcription


## 🔧 Preprocessing Pipeline

Preprocessing is a critical step in preparing speech data for ASR training and evaluation. The following steps were applied to ensure high-quality linguistic input:

### 1. Diacritics Removal
Diacritics were removed to normalize Arabic script and match ASR output expectations. For example:
- `إن` → `ان`
- `أ`, `إ`, `آ` → `ا`
- All tashkeel marks were removed.
  `ءَ`, `ءِ`, `ءُ`, `ءٌ`, `ءً`, `ءٍ`

### 2. Punctuation Removal
Punctuation marks such as periods, commas, question marks, and exclamation points were stripped to improve consistency and reduce model confusion.

### 3. Audio Processing
- **Cropping**: Removed leading/trailing silence and background music
- **Resampling**: All audio files resampled to 16kHz, mono-channel WAV format
- **Normalization**: Volume normalized across all samples


## 🧑‍💻 Use Cases

This dataset is intended for:
- Traditional Emirati Arabic ASR model training and evaluation
- Dialect identification and classification tasks
- Phonological and lexical analysis of traditional Emirati/Gulf Arabic
- Speech variation and sociolinguistic studies


## 🚀 Getting Started

To use this dataset:
1. Clone the repository
2. Load transcriptions and audio files
3. Use any ASR training toolkit (e.g., Whisper, Wav2Vec 2.0) with the preprocessed data


## 📜 Citation

If you use this dataset in your research, please cite:

```bibtex
@misc{alsanaa-emirati-dataset-2025,
  author       = {Maha AlBlooki},
  title        = {Traditional Emirati Arabic Speech Dataset: Curated from Aloula Radio and the Alsanaa Book},
  year         = {2025},
  howpublished = {\url{https://github.com/yourusername/emirati-speech-dataset}},
  note         = {Accessed: March 27, 2025}
}
```

## 📬 Contact
For questions, contributions, or collaboration, please contact:
📧 mahablooki@hotmail.com



