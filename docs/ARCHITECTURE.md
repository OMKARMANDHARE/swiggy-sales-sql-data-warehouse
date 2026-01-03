# Database Architecture

## Star Schema Design (Visual)

See `diagrams/ER.png` for complete ER diagram showing:
- **5 Dimension Tables**
- **1 Central Fact Table**
- **All proper relationships**

## Table Structure

| Dimension Table | Purpose | Key Fields |
|-----------------|---------|------------|
| dim_date | Time analysis | date_id, Full_Date, Year, Month, Quarter |
| dim_location | Geographic analysis | location_id, State, city, Location |
| dim_restaurant | Restaurant performance | restaurant_id, Restaurant_Name |
| dim_category | Category analysis | category_id, Category |
| dim_dish | Menu analysis | dish_id, Dish_Name |
| **fact_swiggy_orders** | **Central Fact** | **order_id, Price_INR, Rating, Rating_Count** |

## Schema Benefits
✅ **Star Schema** - Optimized for analytics  
✅ **No redundancy** - Normalized design  
✅ **Fast queries** - Direct dimension-fact relationships  
✅ **Scalable** - Easy to extend  
✅ **BI Ready** - Works with Excel, Power BI, Tableau
