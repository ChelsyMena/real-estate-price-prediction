# 🏡 Real Estate Price Prediction in Buenos Aires  

## 📌 Overview  
This project analyzes real estate prices in **Buenos Aires, Argentina** using data from [Properati](https://www.properati.com.ar/). The goal is to explore **factors influencing property prices** and build predictive models to estimate housing costs.  

## 📊 Data & Exploratory Analysis  
The dataset includes property listings with details such as **location, size, and amenities**.  

- 🏠 **Property Types:** Houses, Apartments, and PHs  
- 📍 **Most Listings:** Concentrated in **Buenos Aires**, especially in the **Palermo** neighborhood  
- ⏳ **Time to Sell:** No clear correlation with property size or number of rooms, but **neighborhood** affects selling speed.  

### **Listings by Property Type**  
![Listings by property](/plots/plot1.png "Number of Listings by Property Type")  

### **Fastest & Slowest Selling Neighborhoods**  
| **Faster than average** | **Slower than average**  |  
|-------------------------|-------------------------|  
| Villa Santa Rita, Nuñez, Belgrano, Palermo, Colegiales, etc. | Villa Lugano, Pompeya, Puerto Madero, etc. |  

## 🔍 Machine Learning Models  
The models were trained using **80,276 listings**, selecting features based on their correlation with **price**:  

- **Features Used:** `surface_total`, `surface_covered`, `bathrooms`  
- **Error Metric:** Mean Absolute Error (MAE)  

### **Models Trained & Performance**  
| Model | Train MAE ($ USD) | Test MAE ($ USD) |  
|---|---|---|  
| **Linear Regression** | 90,192 | 92,186 |  
| **KNN (default)** | 56,969 | 66,440 |  
| **KNN (optimized)** | 39,594 | 59,580 |  
| **Decision Tree (default)** | 35,517 | 55,876 |  
| **Decision Tree (optimized)** | ✅ **35,517** | ✅ **55,876** |  

### **Predictions by Neighborhood**  
![Listings by property](/plots/plot4.png "Predicted Prices by Neighborhood")  

## 🛠 Tech Stack
- Languages: Python
- Libraries: Pandas, NumPy, scikit-learn, Matplotlib, Seaborn
- Tools: Jupyter Notebook

## 📌 Key Takeaways
✅ Neighborhood is a strong factor in price & selling time
✅ Decision Trees performed best with MAE = $55,876
✅ Data-driven insights can help optimize property valuations

## 📬 Contact

💼 [LinkedIn](https://www.linkedin.com/in/chelsy-mena-gonzalez) | 📧 chelsymg@gmail.com(mailto:chelsymg@gmail.com)
