# 11801674_speech-emotion-recognition

**Origin of the idea.** The project idea originally came from a friend (@Tobias Pones – 11818774) while playing DnD: 
Building a system that analyzes speech/audio during DnD sessions and recommends appropriate background music based on the detected location detected from the speech (forest, traveling, fighting, in a village, on a boat, etc.).


After research I realized there is no suitable, ready-made DnD scene dataset. That would push me into a *dataset creation* project, but my goal is to work with a model and improve it. I looked into challenges such as **DCASE** (https://dcase.community/challenge2025/). There are acoustic scene classification and localization tasks focused on public environments (airports, subways, concerts), i.e., surrounding sound; not exactly what I wanted.

Therefore I decided to do a **speech emotion categorization** project where I can use existing datasets and try to improve a baseline model. This fits the **Bring your own method** project type.

---

## Project Type

**Bring your own method.** I will build on a state-of-the-art (or SOTA-ish) public implementation for Speech Emotion Recognition (SER), fine-tune it on standard datasets (e.g., RAVDESS and/or CREMA-D), and attempt to improve performance with lightweight modeling and training strategies.

---

## Motivation and Related Competitions

There are many challenges on SER which further motivated me to look into this topic:

- Odyssey 2024 Speech Emotion Recognition Challenge  
  https://www.odyssey2024.org/emotion-recognition-challenge

- Interspeech 2025 SER Challenge (MSP-Podcast)  
  Challenge page: https://www.interspeech2025.org/challenges  
  Baseline implementation: https://github.com/msplabresearch/MSP-Podcast_Challenge_IS2025

*Note:* the MSP-Podcast challenge dataset is not freely available, but many other datasets are. A curated list: https://github.com/SuperKogito/SER-datasets

---

## Datasets

Due to accessibility and wide usage in literature and on Kaggle/HuggingFace, I will focus on:

- **RAVDESS** (Ryerson Audio-Visual Database of Emotional Speech and Song)  
  HF mirror: https://huggingface.co/datasets/narad/ravdess

- **CREMA-D** (Crowd-sourced Emotional Multimodal Actors Dataset)  
  Repo pointer: https://github.com/CheyneyComputerScience/CREMA-D

Reference dataset list for alternatives:
- Kaggle collection of SER clips: https://www.kaggle.com/datasets/dmitrybabko/speech-emotion-recognition-en/data
- SER datasets list: https://github.com/SuperKogito/SER-datasets 

---

## Baselines and Implementations to Start From


- **Lightweight SER direction:**  
  *Wav2Small: Distilling Wav2Vec 2 to 72K Parameters for Low-Resource Speech Emotion Recognition*  
  arXiv: https://arxiv.org/abs/2408.13920

I will start from a lightweight SSL-based baseline (e.g., Wav2Small or a small wav2vec2 variant).


Other Baselines:
- **Whisper-based SER (community baseline):**  
  https://huggingface.co/firdhokk/speech-emotion-recognition-with-openai-whisper-large-v3

---

## Approach

1. **Preprocessing.**
2. **Model baselines.**: **Lightweight SSL model**: Wav2Small or small wav2vec2
3. **Training strategy.** -> to be decided
4. **Planned improvements** -> to be decided
5. **(Optional) Application sketch.**
   - Minimal demo that takes live mic audio, predicts emotion per window (see on huggingfaces.io), and prints/logs the predicted state (could later drive DnD music selection).

---

## Work-Breakdown Structure

- **Dataset preparation:** 6–8 hours  
- **Design of network:** 10–12 hours  
- **Build training pipeline:** 10–12 hours  
- **Baseline training & fine-tuning:** 10–14 hours  
- **Improvement experiments:** 14–18 hours  
- **Build a minimal demo application:** 4–6 hours  
- **Final report writing:** 6-9 hours  
- **Presentation preparation:** 3–6 hours

*Total estimate:* ~75 hours 

---


## References

1. **Dionyssos Kounadis-Bastian et al. (2024).**  
   *Wav2Small: Distilling Wav2Vec 2 to 72K Parameters for Low-Resource Speech Emotion Recognition.*  
   https://arxiv.org/abs/2408.13920

2. **Alef Iury S. Ferreira et al. (2025).**  
   *Enhancing Speech Emotion Recognition with Graph-Based Multimodal Fusion and Prosodic Features for the Interspeech 2025 SER Challenge.*  
   https://arxiv.org/abs/2506.02088

3. **Odyssey 2024 SER Challenge:**  
   Goncalves, L. et al. (2024). *Odyssey 2024 – Speech Emotion Recognition Challenge: Dataset, Baseline Framework, and Results.*  
   DOI: 10.21437/odyssey.2024-35

4. **Huang-Cheng Chou & Chi-Chun Lee (2025).**  
   *Revisiting Modeling and Evaluation Approaches in Speech Emotion Recognition: Considering Subjectivity of Annotators and Ambiguity of Emotions.*  
   https://arxiv.org/abs/2510.05934  

5. **Shahana Yasmin Chowdhury, Bithi Banik, Md Tamjidul Hoque & Shreya Banerjee (2025).**  
   *A Novel Hybrid Deep Learning Technique for Speech Emotion Detection using Feature Engineering.*  
   https://arxiv.org/abs/2507.07046 

---

## Appendix: Quick Links

- DCASE Challenge 2025: https://dcase.community/challenge2025/  
- SER datasets list: https://github.com/SuperKogito/SER-datasets  
- RAVDESS (HF): https://huggingface.co/datasets/narad/ravdess  
- CREMA-D (repo pointer): https://github.com/CheyneyComputerScience/CREMA-D  
- Whisper SER baseline (HF): https://huggingface.co/firdhokk/speech-emotion-recognition-with-openai-whisper-large-v3
