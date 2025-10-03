
# 🤖 CYBER ROBOTS AI - Predictive Maintenance System

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-1.29.0-red.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3.2-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

**An advanced AI-powered predictive maintenance system for industrial equipment monitoring**

[Features](#-key-features) • [Installation](#-installation) • [Usage](#-usage) • [Models](#-machine-learning-models) • [Demo](#-demo)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Technology Stack](#-technology-stack)
- [Machine Learning Models](#-machine-learning-models)
- [Installation](#-installation)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [Data Format](#-data-format)
- [Screenshots](#-screenshots)
- [Contributing](#-contributing)
- [Troubleshooting](#-troubleshooting)
- [License](#-license)

---

## 🎯 Overview

CYBER ROBOTS AI is an intelligent predictive maintenance system that leverages state-of-the-art machine learning algorithms to predict equipment failures before they occur. The system provides real-time analytics, interactive 3D visualizations, and comprehensive health monitoring dashboards, enabling proactive maintenance decisions and reducing unexpected downtime.

### Why Predictive Maintenance?

- **Reduce Costs**: Prevent costly unexpected equipment failures
- **Increase Uptime**: Maintain optimal operational efficiency
- **Data-Driven Decisions**: Make informed maintenance scheduling decisions
- **Safety**: Identify potential hazards before they become critical

---

## ✨ Key Features

### 🔮 Real-Time Predictive Analytics
- Instant equipment health assessment using ML models
- Remaining Useful Life (RUL) prediction in operational hours
- Maintenance requirement classification (Normal/Needs Maintenance)
- Anomaly detection through unsupervised learning

### 📊 Interactive Dashboard
- **3D Sensor Visualization**: Explore multi-dimensional sensor relationships
- **Health Gauge**: Real-time system health scoring (0-100)
- **Distribution Charts**: Visualize maintenance status and RUL distribution
- **Time Series Analysis**: Track sensor trends over operational hours

### 📁 Batch Processing
- Upload CSV files for bulk equipment analysis
- Process multiple equipment records simultaneously
- Export prediction results with detailed metrics
- Support for custom sensor configurations

### 🎨 Advanced Visualizations
- **3D Scatter Plots**: Interactive sensor space exploration
- **Heatmaps**: Correlation analysis between sensors
- **Box Plots**: Statistical distribution of sensor values
- **Line Charts**: Temporal trend analysis

---

## 🛠 Technology Stack

| Category | Technology | Version | Purpose |
|----------|-----------|---------|---------|
| **Backend** | Python | 3.10+ | Core programming language |
| **Web Framework** | Streamlit | 1.29.0 | Interactive web application |
| **Data Processing** | Pandas | 2.1.3 | Data manipulation |
| | NumPy | 1.26.2 | Numerical computing |
| **Visualization** | Matplotlib | 3.8.2 | Static plots |
| | Seaborn | 0.13.0 | Statistical graphics |
| | Plotly | 5.18.0 | Interactive 3D charts |
| **Machine Learning** | scikit-learn | 1.3.2 | ML models & preprocessing |
| **UI Components** | streamlit-option-menu | 0.3.6 | Enhanced navigation |

---

## 🧠 Machine Learning Models

### 1. Random Forest Regressor (RUL Prediction)

```python
Model: RandomForestRegressor(n_estimators=100, random_state=42)
Features: [sensor_1, sensor_2, sensor_3, operational_hours]
Target: RUL (Remaining Useful Life)
Output: Continuous value (hours)
Preprocessing: StandardScaler normalization
```

**Purpose**: Predicts the remaining operational hours before maintenance is required.

### 2. Random Forest Classifier (Maintenance Status)

```python
Model: RandomForestClassifier(n_estimators=100, random_state=42)
Features: [sensor_1, sensor_2, sensor_3, operational_hours]
Target: maintenance (0=Normal, 1=Needs Maintenance)
Output: Binary classification
```

**Purpose**: Determines whether equipment requires immediate maintenance attention.

### 3. K-Means Clustering (Anomaly Detection)

```python
Model: KMeans(n_clusters=2, random_state=42)
Features: [sensor_1, sensor_2, sensor_3, operational_hours]
Output: Cluster assignment (0=Normal, 1=Anomaly)
```

**Purpose**: Identifies unusual sensor patterns that may indicate emerging issues.

---

## 📥 Installation

### Prerequisites

Before installation, ensure you have:
- Python 3.10 or higher
- pip (Python package manager)
- Git
- 4GB+ RAM recommended
- Modern web browser (Chrome, Firefox, Safari, Edge)

### Step-by-Step Installation

1. **Clone the Repository**
```bash
git clone https://github.com/Mohammad-Khaliafah/Predictive-Maintenance-System.git
cd Predictive-Maintenance-System
```

2. **Create Virtual Environment** (Recommended)
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

3. **Install Dependencies**
```bash
pip install -r requirements.txt
```

4. **Verify Installation**
```bash
python -c "import streamlit; print(streamlit.__version__)"
```

---

## 🚀 Usage

### Starting the Application

1. **Navigate to Project Directory**
```bash
cd Predictive-Maintenance-System
```

2. **Launch Streamlit App**
```bash
streamlit run app.py
```

3. **Access the Application**
- The app will automatically open in your default browser
- Default URL: `http://localhost:8501`
- Network URL will be displayed in terminal for external access

### Using the Dashboard

#### 🏠 Home Page
- View overall system statistics
- Monitor real-time health metrics
- Explore interactive 3D visualizations
- Review system capabilities

#### 📊 Historical Data
- Browse the complete dataset
- View data statistics
- Download sample format for uploads
- Understand data structure

#### 📤 Input Data

**Option 1: Upload CSV**
1. Navigate to "Input Data" → "Upload CSV" tab
2. Click "Drop your CSV file here"
3. Select file with required columns:
   - sensor_1
   - sensor_2
   - sensor_3
   - operational_hours
4. Click "Process Data"
5. View results and download predictions

**Option 2: Generate Random Data**
1. Navigate to "Input Data" → "Generate Random" tab
2. Click "Generate Random Values"
3. Review generated sensor values
4. Click "Use These Values"
5. Check Results page for predictions

**Option 3: Manual Input**
1. Navigate to "Input Data" → "Manual Input" tab
2. Adjust sliders for each sensor value
3. Set operational hours
4. Click "Submit"
5. View predictions on Results page

#### 📈 Results
- View prediction summaries
- Analyze maintenance requirements
- Review anomaly detection results
- Download detailed reports

#### 📉 Visualizations
- Explore histograms of sensor readings
- View scatter plots vs operational hours
- Analyze RUL trends over time
- Study correlation heatmaps
- Review box plots for distribution analysis

---

## 📁 Project Structure

```
Predictive-Maintenance-System/
│
├── app.py                          # Main Streamlit application
├── requirements.txt                # Python dependencies
├── README.md                       # Project documentation
│
├── Predictive Maintenance.ipynb    # Jupyter notebook with model training
├── machinery_data.csv              # Sample dataset
│
└── .gitignore                      # Git ignore file
```

### File Descriptions

- **app.py**: Main application file containing the Streamlit interface and ML model integration
- **Predictive Maintenance.ipynb**: Development notebook with data generation, model training, and evaluation
- **machinery_data.csv**: Sample industrial equipment sensor data (1000 records)
- **requirements.txt**: All Python package dependencies with versions

---

## 📊 Data Format

### Required CSV Columns

| Column | Type | Description | Range |
|--------|------|-------------|-------|
| `sensor_1` | Float | Primary sensor reading | Normalized: -3 to 3 |
| `sensor_2` | Float | Secondary sensor reading | Normalized: -3 to 3 |
| `sensor_3` | Float | Tertiary sensor reading | Normalized: -3 to 3 |
| `operational_hours` | Integer | Equipment running hours | 100 - 5000 |

### Example Data

```csv
sensor_1,sensor_2,sensor_3,operational_hours
0.496714,-0.138264,0.647689,2256
-0.234153,1.523030,-0.234137,3993
-0.469474,0.542560,-0.463418,1811
0.241962,-1.913280,-1.724918,4859
```

### Optional Output Columns (After Prediction)

| Column | Type | Description |
|--------|------|-------------|
| `Predicted_RUL` | Float | Predicted remaining useful life (hours) |
| `Maintenance_Status` | String | "Normal" or "Needs Maintenance" |
| `Anomaly_Status` | String | "Normal" or "Anomaly" |

---


## 🤝 Contributing

Contributions are welcome! Please follow these guidelines:

### How to Contribute

1. **Fork the Repository**
```bash
git fork https://github.com/Mohammad-Khaliafah/Predictive-Maintenance-System.git
```

2. **Create Feature Branch**
```bash
git checkout -b feature/AmazingFeature
```

3. **Commit Changes**
```bash
git commit -m 'Add some AmazingFeature'
```

4. **Push to Branch**
```bash
git push origin feature/AmazingFeature
```

5. **Open Pull Request**

### Development Guidelines

- Follow PEP 8 style guide for Python code
- Add comments for complex logic
- Update documentation for new features
- Test thoroughly before submitting PR
- Include screenshots for UI changes

### Areas for Contribution

- 🐛 Bug fixes
- ✨ New features
- 📝 Documentation improvements
- 🎨 UI/UX enhancements
- ⚡ Performance optimizations
- 🧪 Additional test coverage

---

## 🔧 Troubleshooting

### Common Issues

**Issue: Port already in use**
```bash
# Solution: Specify different port
streamlit run app.py --server.port 8502
```

**Issue: Module not found error**
```bash
# Solution: Reinstall requirements
pip install -r requirements.txt --force-reinstall
```

**Issue: CSV upload fails**
```
Solution: Ensure CSV has exact column names:
- sensor_1 (not Sensor_1 or sensor1)
- sensor_2
- sensor_3
- operational_hours
```

**Issue: Predictions seem incorrect**
```
Solution: Check that:
1. Sensor values are within reasonable ranges
2. Operational hours are positive integers
3. Data is not corrupted or contains NaN values
```

### Performance Issues

If the app runs slowly:
1. Reduce dataset size for testing
2. Close other applications
3. Check available RAM
4. Use virtual environment

### Getting Help

- 🐛 Issues: [GitHub Issues](https://github.com/Mohammad-Khaliafah/Predictive-Maintenance-System/issues)
- 💬 Discussions: [GitHub Discussions](https://github.com/Mohammad-Khaliafah/Predictive-Maintenance-System/discussions)

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 Mohammad Khaliafah

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🙏 Acknowledgments

- Streamlit team for the amazing framework
- scikit-learn contributors for ML tools
- Plotly team for interactive visualizations
- Open-source community

---

## 📞 Contact

**Mohammad Khaliafah**

- GitHub: [@Mohammad-Khaliafah](https://github.com/Mohammad-Khaliafah)

---

<div align="center">

**⭐ Star this repository if you find it helpful!**

Made with ❤️ by Mohammad Khaliafah

</div>
