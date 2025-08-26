# Cyber Hacking Breaches Prediction Using Machine Learning

A comprehensive web application that predicts cyber hacking breaches using various machine learning algorithms including Random Forest, Support Vector Machine, Artificial Neural Network, and Convolutional Neural Network.

## 🚀 Features

- **User Authentication**: Registration and login system
- **Data Management**: Upload and process CSV datasets
- **Machine Learning Models**:
  - Random Forest Classifier (Accuracy: 90.53%)
  - Support Vector Machine (Accuracy: 69.32%)
  - Artificial Neural Network (Accuracy: 79.23%)
  - Convolutional Neural Network (Accuracy: 75.97%)
- **Real-time Predictions**: Predict attack types based on input features
- **Web Interface**: Modern, responsive UI built with Flask and Bootstrap

## 🛠️ Technologies Used

- **Backend**: Python, Flask
- **Machine Learning**: Scikit-learn, TensorFlow, Keras
- **Database**: MySQL
- **Frontend**: HTML, CSS, JavaScript, Bootstrap
- **Data Processing**: Pandas, NumPy

## 📋 Prerequisites

- Python 3.9 or higher
- MySQL Server
- Git

## 🚀 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/cyber-hacking-prediction.git
cd cyber-hacking-prediction
```

### 2. Install Python Dependencies
```bash
pip install -r requirements.txt
```

### 3. Set Up MySQL Database
```bash
# Connect to MySQL as root
mysql -u root -p

# Run the database setup script
source db.sql;
```

### 4. Configure Database Connection
Update the database credentials in `app.py`:
```python
mydb = mysql.connector.connect(
    host='localhost',
    port=3306,          
    user='root',        
    passwd='your_password',  # Replace with your MySQL password
    database='cyber1'  
)
```

## 🏃‍♂️ Running the Application

### Method 1: Direct Python Execution
```bash
python app.py
```

### Method 2: Using Docker (Optional)
```bash
# Build and run with Docker Compose
docker-compose up --build

# Or build and run manually
docker build -t cyber-hacking-app .
docker run -p 5000:5000 cyber-hacking-app
```

## 🌐 Access the Application

Open your web browser and navigate to:
- **Local**: http://localhost:5000
- **Network**: http://your-ip-address:5000

## 📊 Dataset

The application uses the `DataBreaches(2004-2021).csv` dataset containing:
- Entity information
- Year of breach
- Number of records affected
- Organization type
- Attack method

## 🔧 Usage

1. **Register/Login**: Create an account or sign in
2. **Upload Data**: Load your CSV dataset
3. **Preprocess**: Split and prepare data for training
4. **Train Models**: Choose and train ML algorithms
5. **Make Predictions**: Input features to predict attack types

## 📁 Project Structure

```
cyber-hacking-prediction/
├── app.py                 # Main Flask application
├── requirements.txt       # Python dependencies
├── db.sql                # Database setup script
├── Dockerfile            # Docker configuration
├── docker-compose.yml    # Docker orchestration
├── static/               # CSS, JS, and image files
├── templates/            # HTML templates
└── README.md            # This file
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Your Name**
- GitHub: [@yourusername](https://github.com/yourusername)

## 🙏 Acknowledgments

- Flask framework for web development
- Scikit-learn for machine learning algorithms
- TensorFlow/Keras for neural networks
- Bootstrap for responsive UI design

## 📞 Support

If you encounter any issues or have questions:
1. Check the [Issues](https://github.com/yourusername/cyber-hacking-prediction/issues) page
2. Create a new issue with detailed description
3. Contact: your.email@example.com

---

⭐ **Star this repository if you find it helpful!**
