# Project 1 Revisited
 Week 17 - (Core) Project 1 Revisited: Importances and Coefficients


![top3_largest_coefficients](https://github.com/RJKool/Project-1-Revisited/assets/123280849/e54409fb-db7d-4d68-9c5e-a63da3049c66)


The 3 largest coefficients are:
1.  "Outlet_Type_Supermarket Type3" - If the Outlet Type is of category "Supermarket Type3", the predicted item sales for an outlet with this type increases by 2248.745.
2.  "Item_MRP" - Individual item sale price increased outlet sales by 954.767
3.  "Outlet_Type_Grocery Store" - If the Outlet Type is of category "Grocery Store", the predicted item sales for an outlet with this type decreased by 1644.829.

---

![top5_feature_importance](https://github.com/RJKool/Project-1-Revisited/assets/123280849/59a1e584-8dad-4e33-b704-5361eee4bf17)


The top five most important features are:
1.  Item_MRP
2.  Outlet_Type_Grocery Store - where Grocery Store is second most important categorical feature used by the model during the training process.
3.  Item_Visibility
4.  Outlet_Type_Supermarket Type3 - where Supermarket Type3 Store is fourth most important categorical feature used by the model during the training process.
5.  Item_Weight

What is an "important" feature?


* An "important" feature is one that was used extensively/repeatedly by the model during the training process.  Feature Importance does not indicate directionality.

---

![rf_reg_SHAP_summary_barplot](/Users/Rashad/Documents/GitHub/Project-1-Revisited/Images/rf_reg_SHAP_summary_barplot.png)


* Four of the Top 5 Most Important Features (Item_MRP, Outlet_Type_Grocery Store, Item_Visibility, and Outlet_Type_Supermarket Type3) are shared with the top five items in our Shap summary plot of features that contributed to the most to the model decision process.

---

![rf_reg_SHAP_summary_dotplot](/Users/Rashad/Documents/GitHub/Project-1-Revisited/Images/rf_reg_SHAP_summary_dotplot.png)


Explanation of the top 3 items in the Dot-plot:
1. Item_MRP:  The higher the item manufacture retail price of the individual item, the higher the positivly predicted price of the item for the retail outlet.
2. Outlet_Type_Grocery Store:  Outlet types of classification "Grocery Store" will be predicted more negatively towards total item retail price.
3. Outlet_Type_Supermarket Type3:  Outlet types of classification "Supermarket Type3" will predicted with more positively (higher) items prices for the retail outlet.