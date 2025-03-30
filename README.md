# Email Spam Classification

This project is an email spam classification system that processes and analyzes email data to distinguish between spam and ham (non-spam) emails using various machine learning techniques, including custom feature extraction, traditional classifiers, and a BERT-based deep learning model.

## Prerequisites

- Python 3.11.7

## Installation

### 1. Clone the Repository
```bash
git clone <repository_url>
cd <repository_folder>
```

### 2. Create a Virtual Environment (Optional but Recommended)
```bash
python -m venv venv
source venv/bin/activate  # On macOS/Linux
# venv\Scripts\activate    # On Windows
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

## How to Run the Code

### 1. Prepare the Dataset
Ensure that you have the email datasets available in the following directory structure:
```
project_folder/
│-- ham_zipped/
│   ├── main_ham/
│       ├── email1
│       ├── email2
│       └── ...
│-- spam_zipped/
│   ├── main_spam/
│       ├── email1
│       ├── email2
│       └── ...
```

### 2. Run the Email Processing and Classification Script
```bash
python main.py
```

The script will:
1. Load and parse emails from `ham_zipped` and `spam_zipped` directories.
2. Extract email structures and transform them into feature vectors.
3. Train and evaluate a BERT-based deep learning classifier.

### 3. Visualize Data and Model Performance
The script will generate:
- Word clouds for spam and ham email structures.
- Histograms for email length distribution.
- Confusion matrices and classification reports for various classifiers.

## Troubleshooting

- If dependencies fail to install, ensure your Python version is correct and update `pip`:
  ```bash
  python -m pip install --upgrade pip
  ```
- If `torch` fails due to CUDA issues, install the appropriate version for your system:
  ```bash
  pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
  ```

## License
This project is open-source and provided under the MIT License.

