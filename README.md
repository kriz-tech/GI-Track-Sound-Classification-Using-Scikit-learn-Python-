# GI-Track-Sound-Classification-Using-Scikit-learn-Python-

##  Objective
This project aims to classify gastrointestinal (GI) tract sounds into three clinically significant categories:
- **Normal**
- **Hyperactive**
- **Hypoactive**

This classification supports early diagnosis of GI issues using non-invasive sound recordings.

---

##  Background
GI sounds provide insight into digestive health and motility. Traditional auscultation lacks standardization and is subjective. This machine learning-based approach brings automation and accuracy to GI sound interpretation.

---

##  Dataset Description
- **Source**: `dataset.txt` //ex:record1
- **Fields**:
  - `start`: Start time of sound segment (seconds)
  - `end`: End time
  - `label`: GI sound label (`SB`, `CRS`, `MB`, `HS`, `unsure_MB`)

**Derived Features**:
- `duration` = `end - start`
- `midpoint` = (`start + end`) / 2

---

## Methodology

### 1. Preprocessing
- Label encoding (`SB`: 0, `CRS`: 1, etc.)
- Handling missing/unknown labels

### 2. Model
- **Random Forest Classifier**
- **Train-test split**: 80-20
- **Features used**: `duration`, `midpoint`

### 3. Mapping to Clinical Classes
| Label       | Mapped Class  |
|-------------|----------------|
| SB, unsure_MB | Normal        |
| CRS, MB       | Hyperactive   |
| HS            | Hypoactive    |

---

## 📈 Results

### Detailed Label Classification
| Label | Precision | Recall | F1-score |
|-------|-----------|--------|----------|
| SB    | 1.00      | 1.00   | 1.00     |
| CRS   | 0.80      | 0.92   | 0.86     |
| MB    | 0.91      | 0.77   | 0.83     |
| **Accuracy** | **0.92** |

### Clinical Activity Classification
| Class       | Precision | Recall | F1-score |
|-------------|-----------|--------|----------|
| Normal      | 1.00      | 1.00   | 1.00     |
| Hyperactive | 1.00      | 1.00   | 1.00     |
| Hypoactive  | -         | -      | -        |
| **Clinical Accuracy** | **1.00** |

---

##  Visualization
- **Box plot** showing distribution of `duration` per GI sound type.
- Built using `matplotlib` and `seaborn`.

---

##  Tools & Libraries
- Python 3.12
- pandas
- scikit-learn
- matplotlib
- seaborn

---

## 🧑‍💻 Author
- GitHub: [@kriz-tech](https://github.com/kriz-tech)
- Project by a biomedical engineering student focusing on signal processing.

---

