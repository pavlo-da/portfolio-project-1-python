# E-Commerce Sales Analysis Project

This project focuses on connecting to a Google BigQuery dataset (DA dataset), creating a structured dataset from multiple tables, and conducting comprehensive exploratory and statistical analysis of user behavior, product sales, and traffic sources.

## 📋 Project

1. **Connection to BigQuery:**
   - Used Python to connect to Google BigQuery.
   - Retrieved and joined tables from the DA dataset using appropriate join types to retain all sessions and orders, even from non-registered users.

2. **Dataset Construction:**
   The final dataset includes the following columns:
   - `order_date`
   - `ga_session_id`
   - `continent`
   - `country`
   - `device`
   - `browser`
   - `mobile_model`
   - `operating_system`
   - `language`
   - `traffic_source`
   - `traffic_channel`
   - `account_id`
   - `is_verified`
   - `is_unsubscribed`
   - `category`
   - `product_name`
   - `price`
   - `short_description`

   ### Data Join Logic:
   - All sessions and orders are preserved.
   - Left joins are used to retain non-registered users' data while integrating user-related attributes.

3. **Dataset Description:**
   - **Total columns:** 18
   - **Numeric columns (1):**
     - `price`
   - **Categorical columns (14):**
     - `ga_session_id`, `continent`, `country`, `device`, `browser`, `mobile_model`, `operating_system`, `language`, `traffic_source`, `traffic_channel`, `account_id`, `is_verified`, `is_unsubscribed`, `category`
   - **Datetime columns (1):**
     - `order_date`
   - **Text columns (2):**
     - `product_name`, `short_description`
   - **Total unique sessions:** _33538_
   - **Date range:** _from 2020-11-01 to 2021-01-27_
   - **Missing values:** Present in:
     - `account_id`, `is_verified`, `is_unsubscribed`: due to users who did not register
     - `language `

---
