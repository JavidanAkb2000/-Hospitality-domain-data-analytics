# 🏨 AtliQ Hotels Data Analysis Project

Welcome to the AtliQ Hotels comprehensive data analysis project! 🎉 This project provides deep insights into hotel booking patterns, occupancy rates, and revenue optimization across AtliQ's luxury and business hotel chains.

## 📊 Project Overview

This analysis dives deep into AtliQ Hotels' booking data to uncover valuable insights for business decision-making. The project encompasses data exploration, cleaning, transformation, and insights generation across multiple hotel properties in major Indian cities.

### 🎯 Key Objectives
- 📈 Analyze booking patterns and trends
- 💰 Optimize revenue generation strategies  
- 🏠 Calculate and improve occupancy rates
- 🔍 Identify data quality issues and outliers
- 📋 Generate actionable business insights

## 📁 Dataset Description

Our analysis utilizes **5 comprehensive datasets**:

| Dataset | 📝 Description | 🔢 Records |
|---------|---------------|-----------|
| `fact_bookings.csv` | Individual booking transactions | 134,590 |
| `fact_aggregated_bookings.csv` | Daily aggregated booking data | 9,194 |
| `dim_hotels.csv` | Hotel property information | 25 |
| `dim_rooms.csv` | Room category details | - |
| `dim_date.csv` | Date dimension table | - |

### 🏢 Hotel Categories
- **🌟 Luxury Hotels**: 16 properties (Premium experience)
- **💼 Business Hotels**: 9 properties (Corporate-focused)

### 🛏️ Room Types
- **RT1**: Standard rooms
- **RT2**: Superior rooms  
- **RT3**: Deluxe rooms
- **RT4**: Presidential suites (Premium)

## 🛠️ Technical Implementation

### 🔧 Technologies Used
- **Python 3.8+** 🐍
- **Pandas** 📊 - Data manipulation and analysis
- **NumPy** 🔢 - Numerical computations
- **Matplotlib** 📈 - Data visualization
- **Jupyter Notebook** 📓 - Interactive analysis environment

### 📋 Project Structure
```
📦 AtliQ Hotels Analysis
├── 📂 datasets/
│   ├── 📄 fact_bookings.csv
│   ├── 📄 fact_aggregated_bookings.csv
│   ├── 📄 dim_hotels.csv
│   ├── 📄 dim_rooms.csv
│   └── 📄 dim_date.csv
├── 📓 analysis.ipynb
└── 📖 README.md
```

## 🔍 Analysis Workflow

### 1️⃣ Data Import & Exploration 🕵️‍♂️
- **Data Loading**: Imported all 5 CSV datasets
- **Initial Exploration**: 
  - 134,590 booking records analyzed
  - Identified 7 booking platforms
  - 3 booking statuses: Checked Out, Cancelled, No Show
  - Rating scale: 1-5 stars

**Key Discovery**: Found data quality issues with negative guest counts! 😱

### 2️⃣ Data Cleaning & Quality Assurance 🧹

#### ✅ Invalid Guest Records
- **Issue**: Found 12 records with negative guest counts (-17 to -1)
- **Solution**: Filtered out invalid records (guests ≤ 0)
- **Result**: Clean dataset with 134,578 valid records

#### 💰 Revenue Outlier Detection
- **Method**: Used 3-standard deviation rule
- **Revenue Generated**: 
  - Removed 5 extreme outliers (>₹294,498)
  - Highest outlier: ₹28,560,000 (data error)
- **Revenue Realized**: 
  - Identified 1,299 high-value records (all RT4 - Presidential suites)
  - Analysis confirmed these are legitimate luxury bookings

#### 📊 Missing Data Handling
- **Ratings**: 77,897 null values (57.9% missing) - Retained for analysis
- **Capacity**: 2 null values filled with median

#### 🏨 Booking Capacity Validation
- **Issue**: 6 records with bookings > capacity (overbooking scenarios)
- **Solution**: Filtered impossible booking scenarios
- **Final Dataset**: 9,194 clean aggregated records

### 3️⃣ Data Transformation 🔄

#### 📊 Occupancy Rate Calculation
```python
occupancy_percentage = (successful_bookings / capacity) × 100
```
- **Formula**: Strategic KPI for hotel performance
- **Implementation**: Applied to all room categories
- **Format**: Rounded to 2 decimal places for precision

### 4️⃣ Insights Generation 💡

#### 🏆 Key Performance Metrics

**📱 Booking Platform Analysis**:
- **Others**: 55,066 bookings (40.9%) - Dominant channel
- **MakeYourTrip**: 26,898 bookings (20.0%) - Major OTA
- **LogTrip**: 14,756 bookings (11.0%) - Growing platform
- **Direct Online**: 13,379 bookings (9.9%) - Direct engagement

**🌍 Geographic Distribution**:
Hotels strategically located across major Indian metropolitan cities

**💎 Room Category Insights**:
- **RT4 (Presidential)**: Premium revenue generator
  - Average revenue: ₹23,439 per booking
  - Higher occupancy during peak seasons
  - Target segment: Luxury travelers

## 🚀 Key Findings & Business Impact

### 📈 Revenue Optimization Opportunities
1. **🎯 Focus on Direct Bookings**: Reduce OTA dependency (currently 71% third-party)
2. **💎 Premium Suite Strategy**: RT4 rooms show highest profitability
3. **📊 Occupancy Management**: Identify low-performing periods for targeted marketing

### 🔧 Data Quality Improvements
- **✅ Implemented robust data validation**
- **🛡️ Outlier detection and handling**
- **📏 Standardized metrics calculation**

## 🏃‍♂️ Getting Started

### Prerequisites 📋
```bash
pip install pandas numpy matplotlib jupyter
```

### Running the Analysis 🚀
1. **Clone the repository**
2. **Place datasets in `/datasets` folder**
3. **Open Jupyter Notebook**
4. **Run all cells sequentially**

## 🤝 Contributing

We welcome contributions! 🎉 Please feel free to:
- 🐛 Report bugs
- 💡 Suggest new features
- 📊 Add new analysis dimensions
- 🔧 Improve code efficiency

## 📞 Contact & Support

For questions, suggestions, or collaboration opportunities:
- 📧 Email: iamjavidanakbarov@gmail.com
- 💬 LinkedIn: https://www.linkedin.com/in/javidan-akbarov-4ba8712b2/
- 🐙 GitHub: https://github.com/JavidanAkb2000

---

### 🙏 Acknowledgments

Special thanks to AtliQ Hotels for providing comprehensive booking data that enables meaningful business insights and data-driven decision making.

**📊 Happy Analyzing!** ✨

---

*Made with ❤️ for data-driven hospitality insights*
