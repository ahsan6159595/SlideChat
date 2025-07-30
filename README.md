# SlideChat 🧬 A LARGE VISION-LANGUAGE ASSISTANT FOR WHOLE-SLIDE PATHOLOGY IMAGE UNDERSTANDING

## **INTRODUCTION** 
Computational pathology aims to improve the analysis of digitized tissue samples, such as whole
slide images (WSIs), by applying artificial intelligence to aid in the diagnosis, identification, and
understanding of disease. Recently, the development of this field has gained rapid momentum, mainly driven by breakthroughs in the visual foundation model. These models learn generalized representations by pretraining on large-scale data and perform well in various downstream tasks, including rare cancer
detection and biomarker prediction.

---
## 📌 Features

- 🖼 **Patch Extraction**: Segment meaningful regions from WSIs using OpenSlide.
- 🔬 **Tissue Analysis**: Perform simulated or CNN-based classification (normal, hypercellular, necrotic).
- 📊 **Quantitative Metrics**: Analyze nuclei count, circularity, tissue area %, color stats, texture, and more.
- 🧪 **Synthetic Tissue Generator**: Create and visualize simulated H&E-like tissue with anomalies.
- 🤖 **Medical QA**: Ask medical questions to a Bio_ClinicalBERT model or GPT-2 for fast interaction.
- 📈 **Model Training & Evaluation**: Simulate model training using CNNs and generate confusion matrices, F1 scores.
- 🎯 **Interactive Commands**: Use a conversational interface to describe, analyze, or query slides.

---
## Dataset
Dataset not included in this repository due to size. Download from: https://huggingface.co/datasets/General-Medical-AI/SlideChat

---
## 🔧 Installation

### 📦 Dependencies

Install Python requirements via pip:

```bash
pip install -r requirements.txt

pip install opencv-python matplotlib numpy pandas scikit-learn \
            torch torchvision transformers seaborn \
            openslide-python pyvips large-image Pillow scikit-image

sudo apt-get install openslide-tools

---
🚀 Getting Started

1. Clone the Repository
bash

git clone https://github.com/your-username/SlideChat.git
cd SlideChat
2. Download Sample WSI
bash

wget https://openslide.cs.cmu.edu/download/openslide-testdata/Aperio/CMU-1.svs -O sample_slide.svs
3. Run the Project
bash

python slidechat_project.py

💬 Interactive Commands
Start the chat interface (inside the script):

describe
This is a Whole Slide Image (WSI) of tissue, typically used in pathology.

analyze
Found 125 patches with meaningful tissue. No immediate anomalies detected.

📊 Quantitative Metrics Output
Nuclei Count
Nuclei Density
Avg. Area and Circularity
Tissue Area %
Texture (GLCM contrast/homogeneity)
Color Intensity (RGB mean/std)
All metrics are visualized using matplotlib.

🧪 Run Demo
Generate and analyze synthetic pathology tissue:

python
from slidechat_project import run_demo
run_demo()

🧠 Medical Question Answering
Ask diagnostic questions using a transformer model:
python
from slidechat_project import ask_medical_question
ask_medical_question("Is this abnormal tissue?")
Supports models like emilyalsentzer/Bio_ClinicalBERT.

📁 Folder Structure
cpp
SlideChat/
├── slidechat_project.py
├── slidechat_project.ipynb
├── requirements.txt
├── README.md
└── results/
    ├── classification report.png
    ├── patches.png
    ├── slidechat digital pathology analysis.png
    ├── slidechat model evaluation metrics.png
    ├── slidechat pathology analysis.png
    ├── slidechat quantitative pathology analysis.png
    └── whole slide image.png


📜 License
This project is licensed under the MIT License.

🙌 Acknowledgments
TCGA and CMU for sample WSI data.
OpenSlide for WSI processing tools.
HuggingFace Transformers for QA models.
scikit-image, PyTorch, OpenCV for analysis and visualization.

Contact
GitHub: ahsan6159595
