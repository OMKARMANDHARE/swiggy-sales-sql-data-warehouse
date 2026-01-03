# Data Dictionary - Complete

## All 5 Dimension Tables

### dim_date
| Column | Type | Description |
|--------|------|-------------|
| date_id | INT | Unique date ID |
| Full_Date | DATE | Calendar date |
| Year | INT | Calendar year |
| Month | INT | Month number |
| Month_Name | VARCHAR | Month name |
| Quarter | INT | Quarter number |
| Day | INT | Day of month |
| Week | INT | Week of year |

### dim_location
| Column | Type | Description |
|--------|------|-------------|
| location_id | INT | Unique location ID |
| State | VARCHAR | State name |
| city | VARCHAR | City name |
| Location | VARCHAR | Specific location |

### dim_restaurant
| Column | Type | Description |
|--------|------|-------------|
| restaurant_id | INT | Unique restaurant ID |
| Restaurant_Name | VARCHAR | Restaurant name |

### dim_category
| Column | Type | Description |
|--------|------|-------------|
| category_id | INT | Unique category ID |
| Category | VARCHAR | Food category (Indian, Chinese, etc.) |

### dim_dish
| Column | Type | Description |
|--------|------|-------------|
| dish_id | INT | Unique dish ID |
|Dish_Name | VARCHAR | Dish names 



### fact_swiggy_orders (Central Fact Table)

| Column | Type | Description |
|--------|------|-------------|
| order_id | INT | Unique order ID |
| date_id | INT | FK to dim_date |
| Price_INR | DECIMAL | Order value |
| Rating | DECIMAL | Customer rating |
| Rating_Count | INT | Number of ratings |
| location_id | INT | FK to dim_location |
| restaurant_id | INT | FK to dim_restaurant |
| category_id | INT | FK to dim_category |
| dish_id | INT | FK to dim_dish |
