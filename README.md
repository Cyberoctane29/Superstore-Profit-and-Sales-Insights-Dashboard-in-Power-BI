# Superstore Profit and Sales Insights Dashboard in Power BI - A Holistic Analysis of Business Performance through Interactive Reporting
This project is an interactive Power BI dashboard built to analyze Superstore sales and profitability. By combining KPI tracking, time-series trends, and comparative analysis across categories, regions, and segments, the report provides a holistic view of business performance. Advanced features such as drill-through navigation, dynamic titles, Top/Bottom N state analysis, bookmarks, and one-click slicer reset enhance interactivity and usability. Designed with a clean and minimalistic, pastel-blue layout and whitespace-oriented visuals, the dashboard delivers clear, actionable insights through modern data storytelling.
<br>
</br>
<img width="1862" height="350" alt="Image" src="https://github.com/user-attachments/assets/4757a984-2d31-4fce-8d3d-2d1cc54ed143" />
<br>
</br>
### Access the Dashboards

If you’d like to directly explore the interactive dashboards and project files, you can access them here:

[Google Drive link](https://drive.google.com/drive/folders/11AKkFq23TPwhmNALWlp_FA7vUWmqxRuS) : https://drive.google.com/drive/folders/11AKkFq23TPwhmNALWlp_FA7vUWmqxRuS

[Interactive dashboard video walkthrough](https://drive.google.com/file/d/1W56o1b3vuZuJJCv3ShkRUR73nW17-icQ/view?usp=sharing): https://drive.google.com/file/d/1W56o1b3vuZuJJCv3ShkRUR73nW17-icQ/view?usp=sharing

For the complete project details, including dataset context, analysis workflow, and documented insights, continue with this repository.

## **Project Overview**

The **Superstore Sales & Profit Insights Dashboard** project aims to:

* **Provide a Holistic Business View**: Track key KPIs such as Sales, Profit, and Quantity, and uncover long-term trends with interactive time-series analysis  
* **Compare Sales vs. Profitability**: Reveal critical mismatches by comparing high-revenue sub-categories against their actual profit performance, with losses instantly flagged through conditional formatting  
* **Enable Deep-Dive Exploration**: Use cascading slicers for Region and State to filter the entire report, drill through from summary to detailed sub-category pages, and explore interactive geographical maps  
* **Highlight Key Drivers & Outliers**: Identify top- and bottom-performing sub-categories and states with dynamic ranking analysis, helping decision-makers focus on profit improvement opportunities  
* **Support Strategic Decisions**: Deliver clear, actionable insights through clean visual design, advanced interactivity, and modern data storytelling in Power BI  
## **Dataset Structure**

The project is built on the **Superstore Sales Dataset**, a transactional dataset widely used for retail analytics. It captures order-level details, customer information, shipping modes, product hierarchies, and financial metrics, enabling both high-level performance tracking and granular profitability analysis.

**Order & Customer Information:**  
Provides the transactional backbone and customer profile for each purchase.  
* `Order_ID`, `Order_Date`, `Ship_Date`: Unique order reference and temporal details  
* `Ship_Mode`: Delivery type such as Standard, Second Class, or First Class  
* `Customer_ID`, `Customer_Name`, `Segment`: Identifies customers and their business segment (Consumer, Corporate, Home Office)  

**Geographical Information:**  
Supports regional and state-level profitability analysis.  
* `Country/Region`, `City`, `State`, `Postal_Code`, `Region`: Hierarchical location details for drill-down and mapping  

**Product Information:**  
Captures product hierarchy for category-level and sub-category-level analysis.  
* `Product_ID`, `Category`, `Sub-Category`, `Product_Name`: Structured identifiers for analyzing sales trends by product line  

**Financial Metrics:**  
Quantifies performance and profitability of each transaction.  
* `Sales`: Transaction revenue  
* `Quantity`: Units sold  
* `Discount`: Discount applied on sale  
* `Profit`: Net profit from transaction  

This rich dataset provides the foundation for the **Superstore Sales & Profit Insights Dashboard**, enabling dynamic KPI tracking, profitability analysis, regional comparisons, and sub-category deep dives through advanced Power BI interactivity.  

## **Dashboard Development & Analytical Workflow**

- **Formulated Analytical Objectives**  
  Defined key strategic questions to guide the dashboard design, including:  
  - Which sub-categories drive high sales but low or negative profits?  
  - What seasonal patterns exist in sales and profitability?  
  - How do performance and profitability vary across regions and states?  

- **Data Preparation & Modeling**  
  - Cleaned and transformed the Superstore dataset using Power Query to ensure consistency and accuracy.  
  - Structured a star-schema style model across Orders, Customers, Products, and Geography to optimize analysis.  
  - Built explicit DAX measures for Sales, Profit, and Quantity, alongside advanced measures like dynamic titles for contextual drill-through pages.
  
- **Dashboard Design & Interactivity**  
  - Designed a two-page Power BI report: a summary dashboard with KPIs, trends, and comparative charts, and a drill-through page for deep-dive sub-category insights.  
  - Configured cascading slicers (Region → State) with a one-click reset option using bookmarks.  
  - Adopted a minimalist, whitespace-oriented layout with a consistent pastel-blue palette to ensure clarity and accessibility.
  - Developed Top N / Bottom N state analysis powered by DAX variables, bookmarks, and toggles.  
  - Implemented conditional formatting in visuals to automatically highlight loss-making sub-categories and states.

- **Insight Generation & Storytelling**  
  - Identified high-revenue but unprofitable sub-categories (e.g., Tables) for strategic review.  
  - Revealed quarterly profit seasonality, enabling better inventory planning and forecasting.  
  - Exposed regional disparities where overall profitable regions mask unprofitable state-level performance.  
  - Delivered a structured narrative flow, guiding users from high-level KPIs to detailed geographical and sub-category insights.  

## **Dashboard Previews**  

### Superstore Profit and Sales Dashboard
<img width="3434" height="1976" alt="Image" src="https://github.com/user-attachments/assets/a55e976b-8dc9-476b-b62d-13c8f25183cb" />

### Drill-Through: Sub-Category Details (View 1 - Top 10 States) 
<img width="3434" height="1976" alt="Image" src="https://github.com/user-attachments/assets/44d24e49-ac52-4e31-8fb0-bf2a0d2042f0" />

### Drill-Through: Sub-Category Details (View 2 - Bottom 10 States) 
<img width="3434" height="1976" alt="Image" src="https://github.com/user-attachments/assets/b8d8f0f7-738f-4c3c-ac21-e6fd9d34e332" />

## **Key Insights**

### **Profitability & Product Performance**
* **Overall Profit Margin**: The business operates on an approximate 12.5% profit margin, with `$2.3M` in sales generating `$286.35K` in profit, indicating a need to focus on high-margin products.
* **Sales vs. Profit Discrepancy**: Several sub-categories, notably **Tables** (`$0.21M` sales), **Bookcases** (`$0.11M` sales), and **Supplies** (`$0.05M` sales), were identified as unprofitable despite generating significant revenue. This highlights a critical disconnect between sales volume and bottom-line contribution.
* **Category-Level Weakness**: The entire **Furniture** category is a major area of concern, contributing only 6.44% of total profit, largely due to the heavy losses from Tables and Bookcases.
* **Key Profit Drivers**: **Copiers** and **Phones** were identified as the most profitable sub-categories, with Copiers being particularly efficient, generating `$56K` in profit from relatively moderate sales.

### **Geographical & Seasonal Trends**
* **Regional Disparities**: Performance is not uniform across the country. The **West** is the most profitable region, contributing 37.87% of the total profit, while the **Central** region is the weakest performer at only 13.83%.
* **State-Level Granularity**: The drill-through feature reveals critical state-level insights. For the highly profitable "Phones" sub-category, success is heavily concentrated in states like **New York** (`$13.4K` profit), while significant losses are incurred in others like **Pennsylvania** (`-$3.6K`) and **Ohio** (`-$2.8K`).
* **Seasonal Profit Peaks**: The time-series analysis shows a clear and consistent seasonal trend, with profits peaking in the fourth quarter (Q4) of each year. This pattern is crucial for inventory planning, marketing campaigns, and sales forecasting.

## **Project Highlights**

* Developed a **two-page interactive Power BI report** (Summary Dashboard & Drill-Through) to provide both high-level executive overviews and granular sub-category insights.  
* Conducted a **comparative analysis of Sales vs. Profitability**, using side-by-side visuals and conditional formatting to highlight high-revenue but unprofitable product lines (e.g., Tables).  
* Engineered **advanced interactive features**, including dynamic DAX-driven titles, cascading slicers, drill-through navigation, and a bookmark-based toggle for "Top 10 vs. Bottom 10" state comparisons.  
* Uncovered **critical business insights**, such as quarterly profit seasonality, unprofitable sub-categories masked by strong sales, and hidden state-level disparities within profitable regions.  
* Implemented a **clean, user-centric design** with whitespace emphasis, a pastel-blue palette, and contextual tooltips to ensure clarity, accessibility, and a professional user experience.  
* Delivered a **scalable, end-to-end analytical solution** from Power Query data modeling to a polished report that empowers stakeholders to explore data, diagnose performance gaps, and make data-driven decisions.  

This project showcases how Power BI can transform a standard Superstore dataset into a **dynamic, story-driven business intelligence solution**, bridging strategic and operational decision-making with actionable insights.
