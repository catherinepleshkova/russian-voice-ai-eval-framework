# 🎙️ Russian Voice AI Evaluation Framework

<p align="center">
  <img src="https://img.shields.io/badge/Language-Russian%20(ru--RU)-blue" alt="Language">
  <img src="https://img.shields.io/badge/Domain-TTS%20%7C%20Voice%20AI%20%7C%20RLHF-green" alt="Domain">
  <img src="https://img.shields.io/badge/Standard-Russian%20ToBI%20%7C%20IPA-orange" alt="Standard">
  <img src="https://img.shields.io/badge/Status-Active%20Prototype-success" alt="Status">
</p>

A structured methodology and benchmarking framework for auditing, scoring, and providing linguistic quality assurance (LQA) for Russian generative speech (TTS/Voice AI models).

---

## ⚡ Quick Overview

Generative AI models often struggle with Russian prosody, vowel reduction, lexical stress, and intonation contours. This framework establishes a rigorous, production-ready evaluation pipeline designed for **RLHF, data annotation, and LLM/TTS quality control**.

### 🌟 Key Components
* **5-Point Likert Scoring Rubrics:** Clear grading criteria spanning Pronunciation & Stress, Prosody & Naturalness, and Acoustic Authenticity.
* **ToBI-Based Error Taxonomy:** Standardized classification codes for pitch accents, boundary tones, and phonetic deviations.
* **Edge Case Calibration:** Guidelines handling conversational reductions versus true errors, and standard literary norms.
* **Golden Rationales:** Examples of precise, actionable English feedback designed for engineering teams and model trainers.

---

## 📚 Full Documentation

The complete evaluation guidelines, detailed taxonomy, and stress-test benchmarks have been compiled into the project repository:

👉 **[Russian Voice AI Evaluation Framework & Documentation](https://github.com/catherinepleshkova/russian-voice-ai-eval-framework)**

---

## 🛠️ Example Evaluation Format

```json
{
  "sample_id": "ru_tts_eval_001",
  "model": "Multilingual-TTS-v2",
  "scores": {
    "pronunciation_and_stress": 2,
    "prosody_and_naturalness": 4,
    "acoustic_authenticity": 5
  },
  "error_code": "PHON-STR-HOM",
  "timestamp": "00:04",
  "rationale": "Model failed to resolve homograph stress in 'замок' (castle vs. padlock), applying incorrect root pitch excursion."
}
