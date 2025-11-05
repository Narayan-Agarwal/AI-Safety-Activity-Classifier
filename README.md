# AI-Safety-Activity-Classifier

## 👷 Proactive Unsafe Activity Detection for Industrial Safety

This project is a software application of Machine Learning (ML) designed to enhance workplace safety by applying principles from Industrial Safety Engineering. It demonstrates a system that automatically identifies high-risk actions from worker movement data, shifting safety from a reactive to a **proactive** paradigm.

---

### 💡 Project Goal & Innovation

This project aims to solve the problem of accidents caused by human error (such as falls or improper posture) by providing automated, intelligent alerts.

* **Core Blend:** The project uniquely links **Industrial Safety Engineering** principles with **Computer Science** through Time-Series Classification.
* **Novelty:** The primary innovation is **Data Re-labeling for Safety**. We convert a standard Human Activity Recognition (HAR) problem into a **binary safety risk assessment** model, classifying movement as either "Safe" or "Unsafe."
* **Final Deliverable:** The output is a visually compelling, code-free **Jupyter Notebook report** that displays the model's classification alongside relevant visual proof (images/videos).

---

### ⚙️ Methodology and Tech Stack

#### Tech Stack Used

The project is built entirely on the Python data science stack:

* **Core Libraries:** Pandas, NumPy, and Scikit-learn (used for training and evaluation).
* **ML Algorithm:** **Random Forest Classifier** (selected for its robust performance and interpretability on time-series data).
* **Documentation:** **Jupyter Notebook** (used as the primary report and visual presentation platform).

#### Data Flow and Logic

The system follows a clear three-step process:

1.  **Input & Customization:** We load **pre-recorded Time-Series Data** (Accelerometer & Gyroscope readings) from the UCI HAR Dataset. This data is customized by converting its original labels into a simplified system: 'Walking', 'Standing', etc., become the **"Safe"** class, and 'Falling' becomes the critical **"Unsafe"** class.
2.  **Feature Engineering & Training:** The raw sensor signals are processed into measurable statistical features (like Mean, Standard Deviation, etc.). These features are used to train the Random Forest model, teaching it the unique numerical pattern associated with an "Unsafe" event (like the sudden acceleration change of a fall).
3.  **Output & Risk Mitigation:** The model generates a risk probability. If the risk is high, the system logs the classification and triggers a visual representation. This demonstrates the system's ability to **proactively identify a hazard** before an injury occurs.

---

### ▶️ How to Run the Project Locally

This project requires Python 3.x and standard data science libraries.

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/YourUsername/AI-Safety-Activity-Classifier.git](https://github.com/YourUsername/AI-Safety-Activity-Classifier.git)
    cd AI-Safety-Activity-Classifier
    ```
2.  **Install Dependencies:** Ensure all libraries are installed using the provided requirements file:
    ```bash
    pip install -r requirements.txt
    ```
3.  **Acquire Data:** Download the **UCI Human Activity Recognition Dataset**. Place the unzipped training and testing files into a dedicated `/data/` folder within this repository.
4.  **Run the Report:** Open the main Jupyter Notebook (`01_Safety_Classifier_Report.ipynb`) and run all cells to execute the data loading, model training, evaluation, and final visualization.

---

### 📊 Key Results

The model achieved high performance in classifying activities, with a primary focus on minimizing missed accidents:

* **Overall Accuracy:** The model demonstrates a high overall accuracy, ensuring reliable classification across the dataset.
* **Critical Metric Performance (for the "Unsafe" Class):** The system prioritized a high **Recall** score (e.g., typically over 97%)
