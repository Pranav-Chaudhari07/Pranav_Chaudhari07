<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:1e3a5f&height=240&section=header&text=Pranav%20Chaudhari&fontSize=42&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Computer%20Vision%20·%20Applied%20ML%20·%20AI%20Systems&descAlignY=60&descSize=16" />
</p>

<div align="center">

[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=vercel&logoColor=white)](https://github.com/Pranav-Chaudhari07)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pranavchaudhari07)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:chaudharipranav057@gmail.com)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat-square&logo=leetcode&logoColor=white)](https://leetcode.com/u/Pranav-Chaudhari07/)

</div>

---

Second-year B.Tech CSE (Data Science) student. My focus is computer vision and applied ML — I want to understand how models fail, where transfer learning breaks down, and how to deploy inference systems that hold up under real-world constraints. I build things to answer those questions. Currently exploring explainability methods (Grad-CAM, LIME) and how to make ML pipelines production-ready: fast, interpretable, and auditable.

Interned at **Vault of Code**. Applied to **Amazon ML Summer School 2026**.

---

## Projects

### [DocSecure](https://github.com/Pranav-Chaudhari07) — AI-Powered Document Fraud Detection

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)

Web application that detects forged or tampered documents using deep learning. Achieves **91% accuracy** with **sub-200ms API latency** in production.

**Architecture:**
- EfficientNetB0 (transfer learning from ImageNet) fine-tuned on a document fraud dataset — chosen over ResNet and MobileNet after benchmarking on validation accuracy vs inference speed tradeoff
- OpenCV preprocessing pipeline: adaptive thresholding, edge sharpening, and noise reduction before model input
- EasyOCR extracts text regions for cross-validation against visual tampering signals
- Grad-CAM visualization highlights exactly which document regions triggered the fraud prediction — making the model auditable, not a black box
- Flask REST API with GCP deployment; Scikit-learn post-processing layer handles edge-case classification

**Three specific decisions I had to think through:**

**Transfer learning depth** — Freezing all EfficientNetB0 layers gave 78% accuracy; fine-tuning the last 20 layers pushed it to 91%. The tradeoff was training time (3× longer) and overfitting risk, which I managed with dropout (0.4) and data augmentation on the fraud class.

**Explainability as a requirement** — Early versions returned a binary prediction. I added Grad-CAM not as a feature but as a debugging tool — it revealed the model was sometimes keying on document background texture instead of tampered regions, which I fixed by rebalancing the training set.

**Latency vs accuracy** — EfficientNetB0-B2 gave 93% accuracy but pushed API response to ~400ms. B0 at 91% stays under 200ms. For a fraud detection API used in real-time document verification, that tradeoff was worth it.

---

### Document Intelligence Pipeline — Internship Project (Vault of Code)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)

Built during internship at Vault of Code. An end-to-end pipeline for extracting structured information from unstructured document images: layout detection → OCR → NLP classification → output schema. The pipeline handled multi-format inputs (scanned PDFs, photos, digital docs) with consistent output quality across formats.

---

## Technical Focus

| Domain        | Stack                                                                      |
| ------------- | -------------------------------------------------------------------------- |
| Languages     | Python · JavaScript · C                                                    |
| ML & AI       | TensorFlow/Keras · Scikit-learn · OpenCV · EasyOCR · spaCy                |
| Computer Vision | Transfer Learning · Grad-CAM · Image Preprocessing · Object Detection   |
| Backend       | Flask · REST APIs · Node.js · Express                                      |
| Databases     | MongoDB · MySQL                                                            |
| Tools & Cloud | GCP · Docker · Git · Figma                                                 |
| Exploring     | Explainability methods (LIME, SHAP) · Model quantization · MLOps pipelines |

---

## Currently

- Extending DocSecure with LIME-based explanations and multi-document type support (Aadhaar, PAN, passports)
- Working through MLOps fundamentals — model versioning, drift detection, CI/CD for ML pipelines
- Studying for Amazon ML Summer School 2026; revisiting probability theory, optimization, and deep learning fundamentals
- Looking for ML/Computer Vision internship roles where I can work on inference systems or applied research

---

## Stats

<div align="center">

<sub>Stats reflect public repository activity.</sub><br/><br/>

<img src="https://github-readme-stats.vercel.app/api?username=Pranav-Chaudhari07&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&rank_icon=github" height="150"/>
&nbsp;&nbsp;
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Pranav-Chaudhari07&theme=tokyonight&hide_border=true&layout=compact&langs_count=5&hide=html,css" height="150"/>

</div>

---

<div align="center">

`chaudharipranav057@gmail.com` · [LinkedIn](https://www.linkedin.com/in/pranavchaudhari07) · [GitHub](https://github.com/Pranav-Chaudhari07)

</div>