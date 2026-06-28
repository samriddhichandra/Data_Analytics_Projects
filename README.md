# Data Analytics Portfolio
### E-Commerce | Customer Churn | Streaming Analytics

A comprehensive collection of production-grade data analytics projects demonstrating end-to-end data science workflows including SQL analysis, machine learning, exploratory data analysis (EDA), and interactive visualizations.

---

## Projects Overview

This repository contains three complete analytics projects:

| Project | Description | Technologies |
|---------|-------------|--------------|
| **E-Commerce Analytics Dashboard** | Sales analytics with SQL queries, KPI tracking, and revenue analysis | Python, SQL, Pandas, Matplotlib, Seaborn |
| **Customer Churn Analysis** | ML-powered churn prediction with classification models and business insights | Python, Scikit-learn, Random Forest, Logistic Regression |
| **Streaming Data Analysis** | Netflix/Spotify-style analytics with user engagement metrics and content insights | Python, SQL, Pandas, Matplotlib, Seaborn |

---

## Repository Structure

```
ecommerce_analyytics_dashboard/
│
├── E-Commerce Analytics
│   ├── ecommerce_analytics_dashboard.py    # Main analysis script
│   ├── ecommerce_data.db                   # SQLite database (50K records)
│   ├── ecommerce_dashboard.png             # Dashboard visualization
│   └── 01_monthly_revenue.csv              # Exported reports
│   ├── 02_category_performance.csv
│   ├── 03_regional_analysis.csv
│   └── 04_retention_metrics.csv
│
├── Customer Churn Analysis
│   ├── customer_churn_analysis.py          # ML pipeline script
│   └── churn_analysis_dashboard.png        # Model performance dashboard
│
├── Streaming Analytics
│   ├── streaming_data_analysis.py          # Analytics script
│   └── streaming_data.db                   # SQLite database (500K watch records)
│
├── README.md                               # This file
└── .gitignore                              # Git ignore rules
```

---

## Quick Start

### Prerequisites

- Python 3.8+
- pip package manager
- Git (for version control)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/samriddhichandra/Data_Analytics_Projects.git
   cd Data_Analytics_Projects
   ```

2. **Run setup script** (recommended)
   ```bash
   # Windows
   run_analytics.bat setup
   
   # Linux/Mac
   chmod +x run_analytics.sh
   ./run_analytics.sh setup
   ```

   Or manually create virtual environment:
   ```bash
   # Windows
   python -m venv .venv
   .venv\Scripts\activate
   
   # Mac/Linux
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn sqlite3
   ```

---

## Project 1: E-Commerce Analytics Dashboard

### Overview
Comprehensive sales analytics system analyzing 50,000 e-commerce transactions with SQL-powered insights, KPI tracking, and interactive visualizations.

### Key Features
- **SQL Database**: SQLite database with 50K transaction records
- **Revenue Analysis**: Monthly trends, YoY comparisons, growth metrics
- **Category Performance**: Product category breakdown with profit margins
- **Regional Insights**: Geographic sales distribution and market share
- **Customer Segmentation**: VIP, Premium, and Standard customer tiers
- **Retention Metrics**: New vs returning customer analysis
- **Automated Reports**: CSV exports for all analysis modules

### Data Schema
```
sales table:
- order_id, customer_id, order_date
- product_category, quantity, unit_price
- discount_pct, region, payment_method
- customer_age, is_returning_customer
- revenue, profit_margin
```

### Usage

```bash
python ecommerce_analytics_dashboard.py
```

### Output
- **Console Output**: KPI report with revenue, orders, customers, and profit metrics
- **Visualization**: `ecommerce_dashboard.png` (6-panel dashboard)
- **CSV Reports**: 4 exported analysis files

### Dashboard Preview

![E-Commerce Dashboard](https://raw.githubusercontent.com/samriddhichandra/Data_Analytics_Projects/main/ecommerce_dashboard.png)

**Dashboard Includes:**
1. Monthly Revenue Trend (line chart with fill)
2. Revenue by Category (horizontal bar chart)
3. Regional Distribution (pie chart)
4. Order Value Distribution (histogram with mean line)
5. Quantity vs Revenue Relationship (scatter plot)
6. New vs Returning Customers (comparison bar chart)

### Key Metrics Generated
- Total Revenue & Profit
- Average Order Value (AOV)
- Customer Retention Rate
- Top 3 Categories by Revenue
- Regional Market Share

---

## Project 2: Customer Churn Analysis & Prediction

### Overview
Machine learning pipeline for predicting customer churn using classification algorithms. Includes comprehensive EDA, feature engineering, model training, and actionable business insights.

### Key Features
- **Synthetic Data Generation**: 10,000 realistic customer records
- **Exploratory Data Analysis**: Statistical summaries and churn patterns
- **Feature Engineering**: 15+ engineered features including customer value metrics
- **ML Models**: Logistic Regression & Random Forest classifiers
- **Model Evaluation**: Accuracy, Precision, Recall, ROC AUC, F1 Score
- **Visual Analytics**: ROC curves, confusion matrices, feature importance
- **Business Insights**: High-risk segments, retention critical periods, churn drivers

### Data Schema
```
customer_data:
- customer_id, tenure_months, monthly_spending
- contract_length_months, num_support_tickets
- satisfaction_score, payment_delay_days
- num_services_used, discount_percentage
- age_group, customer_segment
- churned (target variable)
```

### Usage

```bash
python customer_churn_analysis.py
```

### Output
- **Console Output**: EDA report, model metrics, business insights
- **Visualization**: `churn_analysis_dashboard.png` (6-panel dashboard)
- **Best Model**: Automatically selected based on ROC AUC score

### Dashboard Preview

![Churn Analysis Dashboard](https://raw.githubusercontent.com/samriddhichandra/Data_Analytics_Projects/main/churn_analysis_dashboard.png)

**Dashboard Includes:**
1. Customer Churn Distribution (bar chart with percentages)
2. Tenure Distribution by Churn Status (overlapping histograms)
3. Churn Rate by Satisfaction Score (line chart)
4. ROC Curve - Model Performance (AUC visualization)
5. Confusion Matrix (heatmap)
6. Top 10 Important Features (feature importance from Random Forest)

### Model Performance
- **Algorithms**: Logistic Regression, Random Forest
- **Metrics Tracked**: Accuracy, Precision, Recall, ROC AUC, F1 Score
- **Best Model**: Selected automatically based on ROC AUC
- **Cross-Validation**: Stratified train/test split (80/20)

### Business Insights Generated
- High-risk customer segments (churn rate > 20%)
- Critical retention periods (tenure-based churn patterns)
- Key churn drivers (satisfaction, tenure, spending patterns)

---

## Project 3: Streaming Data Analysis

### Overview
Comprehensive analytics platform for streaming content performance, user engagement, and content quality metrics. Analyzes 500K watch events across 1,000 shows/movies.

### Key Features
- **Dual Database**: Shows metadata + 500K watch history records
- **SQL Analytics**: Complex JOIN queries for content performance
- **Genre Analysis**: Performance metrics by content genre
- **Country Insights**: Content production and viewership by country
- **Device Analytics**: User device preferences and engagement
- **User Segmentation**: Power Users, Heavy Users, Regular Users, Casual Users
- **Quality Metrics**: Content rating tiers and completion rates
- **CSV Exports**: 6 comprehensive report files

### Data Schema
```
shows table:
- show_id, title, type (Movie/TV Show)
- release_year, genre, country, rating
- duration_minutes, imdb_score, views

watch_history table:
- watch_id, user_id, show_id
- watch_date, minutes_watched
- completion_rate, device_type
```

### Usage

```bash
python streaming_data_analysis.py
```

### Output
- **Console Output**: KPI report with user, content, and viewing metrics
- **Visualization**: `streaming_analytics_dashboard.png` (6-panel dashboard)
- **CSV Reports**: 6 exported analysis files

### Dashboard Preview

![Streaming Analytics Dashboard](https://raw.githubusercontent.com/samriddhichandra/Data_Analytics_Projects/main/streaming_analytics_dashboard.png)

**Dashboard Includes:**
1. Watches by Genre (Top 8 genres, horizontal bar chart)
2. Content Distribution: Movies vs TV Shows (pie chart)
3. Watches by Device Type (horizontal bar chart)
4. Avg Completion Rate by Content Quality (grouped bar chart)
5. Watch Duration Distribution (histogram with mean line)
6. User Engagement Segments (user tier distribution)

### Key Metrics Generated
- Total Users & Watch Events
- Total Hours Watched
- Average Completion Rate
- Content Quality Distribution
- Device Usage Patterns
- User Engagement Segments

---

## Technologies Used

### Core Libraries
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Matplotlib**: Data visualization
- **Seaborn**: Statistical graphics
- **Scikit-learn**: Machine learning (Project 2 only)
- **SQLite**: Database management

### Development Tools
- **Python 3.8+**: Primary programming language
- **Git**: Version control
- **VS Code**: Development environment

---

## Dependencies

```txt
pandas>=1.5.0
numpy>=1.21.0
matplotlib>=3.5.0
seaborn>=0.11.0
scikit-learn>=1.0.0
sqlite3 (built-in)
```

Install all dependencies:
```bash
pip install -r requirements.txt
```

---

## Data Generation

All projects use **synthetic data generation** with realistic patterns:

- **E-Commerce**: 50,000 transactions over 2 years
- **Churn Analysis**: 10,000 customer records with realistic churn patterns
- **Streaming**: 1,000 shows + 500,000 watch events

Data generation ensures:
- Reproducible results (fixed random seeds)
- Realistic distributions and correlations
- Production-like data structures

---

## Visualization Standards

All dashboards follow consistent design principles:

- **Resolution**: 300 DPI for high-quality exports
- **Color Palette**: Professional blue theme (#2980B9 primary)
- **Layout**: 2×3 grid (6 visualizations per dashboard)
- **Typography**: Clear labels, bold titles, readable fonts
- **Accessibility**: High contrast, clear legends, grid lines

---

## Best Practices

### Code Quality
- Object-oriented design with class-based architecture
- Comprehensive docstrings for all methods
- Type hints where applicable
- Modular function design
- Error handling and validation

### Data Handling
- SQLite for efficient data storage
- Pandas for data manipulation
- Proper data type conversions
- Memory-efficient processing

### Documentation
- Detailed README for each project
- Inline code comments
- Usage examples
- Output specifications

---

## Analysis Workflows

### E-Commerce Analytics Workflow
```
1. Generate Sample Data (50K records)
   ↓
2. Create SQLite Database
   ↓
3. Execute SQL Queries (Revenue, Category, Regional, Retention)
   ↓
4. Generate KPI Report
   ↓
5. Create 6-Panel Dashboard
   ↓
6. Export CSV Reports
```

### Churn Analysis Workflow
```
1. Generate Synthetic Customer Data (10K records)
   ↓
2. Exploratory Data Analysis
   ↓
3. Feature Engineering (15+ features)
   ↓
4. Train/Test Split (80/20, stratified)
   ↓
5. Model Training (Logistic Regression, Random Forest)
   ↓
6. Model Evaluation & Selection
   ↓
7. Generate Visualizations & Business Insights
```

### Streaming Analytics Workflow
```
1. Generate Shows Data (1,000 titles)
   ↓
2. Generate Watch History (500K events)
   ↓
3. Create Dual-Table SQLite Database
   ↓
4. Execute SQL Analytics Queries
   ↓
5. Generate KPI Report
   ↓
6. Create 6-Panel Dashboard
   ↓
7. Export 6 CSV Reports
```

---

## Use Cases

### E-Commerce Analytics
- Sales performance tracking
- Product category analysis
- Regional market expansion
- Customer retention strategies
- Revenue forecasting

### Customer Churn Analysis
- Proactive customer retention
- Risk segment identification
- Feature importance analysis
- Model deployment for predictions
- Business strategy optimization

### Streaming Analytics
- Content performance optimization
- User engagement tracking
- Device usage patterns
- Content acquisition strategy
- Quality metrics monitoring

---

## Performance Metrics

### E-Commerce Dashboard
- **Data Volume**: 50,000 transactions
- **Query Performance**: <1 second per SQL query
- **Visualization Time**: ~3 seconds
- **Report Generation**: Instant CSV export

### Churn Analysis
- **Data Volume**: 10,000 customers
- **Training Time**: ~5 seconds
- **Model Accuracy**: 75-85% (typical range)
- **ROC AUC**: 0.80-0.90 (typical range)

### Streaming Analytics
- **Data Volume**: 1,000 shows + 500K watch events
- **Query Performance**: <2 seconds per complex JOIN
- **Visualization Time**: ~4 seconds
- **Report Generation**: 6 CSV files instant

---

## Testing

### Using Run Scripts (Recommended)

```bash
# Windows
run_analytics.bat all              # Run all projects
run_analytics.bat ecommerce        # Run e-commerce only
run_analytics.bat churn            # Run churn analysis only
run_analytics.bat streaming        # Run streaming only

# Linux/Mac
./run_analytics.sh all             # Run all projects
./run_analytics.sh ecommerce       # Run e-commerce only
./run_analytics.sh churn           # Run churn analysis only
./run_analytics.sh streaming       # Run streaming only
```

### Manual Execution

Each project includes built-in validation:

```bash
# Test E-Commerce Analytics
python ecommerce_analytics_dashboard.py
# Expected: Database created, KPI report, dashboard saved

# Test Churn Analysis
python customer_churn_analysis.py
# Expected: Model trained, metrics printed, dashboard saved

# Test Streaming Analytics
python streaming_data_analysis.py
# Expected: Database created, KPI report, dashboard saved
```

---

## Learning Outcomes

### Technical Skills Demonstrated
- **SQL**: Complex queries, JOINs, aggregations, window functions
- **Python**: OOP, data manipulation, statistical analysis
- **Machine Learning**: Classification, feature engineering, model evaluation
- **Visualization**: Matplotlib, Seaborn, dashboard design
- **Data Engineering**: Database design, ETL pipelines, data generation

### Business Skills Demonstrated
- **KPI Definition**: Revenue, retention, engagement metrics
- **Insight Generation**: Actionable business recommendations
- **Report Generation**: Automated CSV exports
- **Performance Tracking**: Model metrics, A/B testing readiness

---

## Contributing

This is a portfolio project. Feel free to:
- Fork and experiment with the code
- Suggest improvements via issues
- Use as reference for your own projects

---

## License

This project is licensed under the MIT License - feel free to use for learning and portfolio purposes.

---

## Author

**Samriddhi Chandra**

- GitHub: [@samriddhichandra](https://github.com/samriddhichandra)
- LinkedIn: [Samriddhi Chandra](https://linkedin.com/in/samriddhichandra)
- Email: samriddhi.chandra@example.com

---

## Acknowledgments

- Dataset inspiration from real-world e-commerce, telecom, and streaming platforms
- Visualization best practices from data science community
- Machine learning techniques from scikit-learn documentation

---

## Support

For questions or issues:
1. Check the documentation above
2. Review code comments in each script
3. Open an issue on GitHub

---

## Run Scripts

The repository includes cross-platform run scripts for easy execution:

### Windows (run_analytics.bat)
```batch
run_analytics.bat setup      # First-time setup
run_analytics.bat all        # Run all projects
run_analytics.bat ecommerce  # Run e-commerce analytics
run_analytics.bat churn      # Run churn analysis
run_analytics.bat streaming  # Run streaming analytics
run_analytics.bat clean      # Clean generated files
run_analytics.bat help       # Show help
```

### Linux/Mac (run_analytics.sh)
```bash
chmod +x run_analytics.sh
./run_analytics.sh setup      # First-time setup
./run_analytics.sh all        # Run all projects
./run_analytics.sh ecommerce  # Run e-commerce analytics
./run_analytics.sh churn      # Run churn analysis
./run_analytics.sh streaming  # Run streaming analytics
./run_analytics.sh clean      # Clean generated files
./run_analytics.sh help       # Show help
```

### Script Features
- Automatic Python detection
- Virtual environment activation
- Dependency installation
- Project execution with status feedback
- Clean generated files functionality
- Cross-platform compatibility

## Roadmap

Future enhancements (optional):
- [ ] Add interactive Plotly/Dash visualizations
- [ ] Implement Flask/FastAPI web interface
- [ ] Add real-time data streaming capabilities
- [ ] Create Jupyter notebook versions
- [ ] Add unit tests and CI/CD pipeline
- [ ] Deploy to cloud (AWS/GCP/Azure)
- [ ] Add Docker containerization

---

## Project Statistics

- **Total Lines of Code**: ~1,500+
- **Total Visualizations**: 18 (6 per project)
- **SQL Queries**: 20+
- **ML Models**: 2 classification algorithms
- **Data Records**: 560K+ (50K + 10K + 500K)
- **CSV Reports**: 10 exported files

---

## Star History

If you found this portfolio helpful, please consider giving it a star!

---

**Last Updated**: 2026  
**Version**: 1.0.0  
**Status**: Production Ready

## Documentation Update

## E-Commerce Section

## Churn Section

## Streaming Section

## Tech Stack

## Schema

## Usage

## Performance

## Testing

## Scripts

## GitHub URL

## Demo Images

## Statistics

## Author

# Production Ready

# Comprehensive docs

# Code review

# Version 1.0.0

# Initial release
