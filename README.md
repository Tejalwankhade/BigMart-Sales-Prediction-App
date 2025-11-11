## BigMart Sales Forecasting Pipeline

##  Project Overview 
This project showcases a complete Data Engineering + Machine Learning pipeline using BigMart retail sales data. It includes automated data ingestion, MySQL database setup, model training, and deployment via a Streamlit app.

Live demo:- https://data-engineering-project-ubs3vc8izb4hgvaidg9shz.streamlit.app/

## 🏗 Architecture & Workflow  
1. **Data ingestion**  
   - Raw input files: `df_item.xml`, `df_outlet.xml`, `df_sales.xml`  
   - Python script `create_database_sql.py` for setting up MySQL tables & ingesting data.  
2. **Model training**  
   - Using `train_model_pickle.py` to perform feature engineering, model training and save a pickle file (`bigmart_best_model.pkl`).  
3. **Deployment / App**  
   - `app.py` serves a lightweight interface (via Streamlit) that loads the model and allows user interaction (enter item/outlet features → get forecasted sales).  
4. **Requirements**  
   - See `requirements.txt` for all Python dependencies.  
   
## 🧰 Technologies Used  
- Python (pandas, sklearn, etc)  
- MySQL (RDBMS for structured data)  
- Pickle (for model serialization)  
- Streamlit (for quick web app deployment)  
- XML parsing (for dataset ingestion)  

## 📊 Dataset Description  
The dataset includes:  
- `df_item.xml`: Item-level metadata (item identifier, item type, price etc)  
- `df_outlet.xml`: Outlet metadata (outlet ID, location type, size etc)  
- `df_sales.xml`: Historical sales data (Item_Outlet_Sales per item per outlet)  
The goal: predict `Item_Outlet_Sales` given item/outlet features and historical patterns.

