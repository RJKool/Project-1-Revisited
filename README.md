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

![rf_reg_SHAP_summary_barplot](https://github.com/RJKool/Project-1-Revisited/blob/main/Images/rf_reg_SHAP_summary_barplot.png)


* Four of the Top 5 Most Important Features (Item_MRP, Outlet_Type_Grocery Store, Item_Visibility, and Outlet_Type_Supermarket Type3) are shared with the top five items in our Shap summary plot of features that contributed to the most to the model decision process.

---

![rf_reg_SHAP_summary_dotplot](https://github.com/RJKool/Project-1-Revisited/blob/main/Images/rf_reg_SHAP_summary_dotplot.png)


Explanation of the top 3 items in the Dot-plot:
1. Item_MRP:  The higher the item manufacture retail price of the individual item, the higher the positivly predicted price of the item for the retail outlet.
2. Outlet_Type_Grocery Store:  Outlet types of classification "Grocery Store" will be predicted more negatively towards total item retail price.
3. Outlet_Type_Supermarket Type3:  Outlet types of classification "Supermarket Type3" will predicted with more positively (higher) items prices for the retail outlet.

---

## Example A
1. High Item MRP
2. Outlet Type: Grocery Store
3. High Item Visibility

**Selection Explanation:**  The SHAP Summary Plot shows there is a opposing outcome in total item sales for both Outlet Type class Grocery Store and Outlet Type class Supermarket Type 3.  I would like to find filtered examples of these two opposing affects on total sales.

In this example, I choose feature "Outlet_Type_Grocery Store" as my point of focus.

![GroupA_LIME](https://github.com/RJKool/Project-1-Revisited/blob/main/Images/GroceryStore_GroupA_LIME.png)

**LIME Explanation:**  In our LIME explanation, we see that Outlet_Type_Grocery_Store greatly influenced price prediction the most with a value of -2221.10.  Item_MRP is the second highest influence on predicted price by with a positive influence of value 1637.71. 

**Total Predicted Sales:**  663.59

![GroupA_Individual_ForcePlot](https://github.com/RJKool/Project-1-Revisited/blob/main/Images/GroceryStore_GroupA_I_Force.png)

The above Individual Force Plot shows the two most heavily influenced features are "Outlet_Type_Grocery Store" (which pushes the price prediction lower) and "Item_MRP" (which pushes the price prediction higher).

---

## Example B
1. High Item MRP
2. Outlet Type: Supermarket Type3
3. High Item Visibility

**Selection Explanation:**  The SHAP Summary Plot shows there is a opposing outcome in total item sales for both Outlet Type class Grocery Store and Outlet Type class Supermarket Type 3.  I would like to find filtered examples of these two opposing affects on total sales.

In this example, I choose feature "Outlet_Type_Supermarket Type3" as my point of focus.

![GROUPB_LIME](https://github.com/RJKool/Project-1-Revisited/blob/main/Images/Supermarket%20Type3_GroupB_LIME.png)

**LIME Explanation:** In our LIME explanation, we see that Outlet_Type_Supermarket 3 greatly influenced price prediction the most with a value of 2224.35. Item_MRP is the second highest influence on predicted price by with a positive influence of value 1679.02.

**Total Predicted Sales:** 4073.34

![GROUPB_Individual_ForcePlot](https://github.com/RJKool/Project-1-Revisited/blob/main/Images/Supermarket%20Type3_GroupB_I_Force.png)

The above Individual Force Plot shows the two most heavily influenced features are "Outlet_Type_Supermarket Type3" (which pushes the price prediction higher) and "Item_MRP" (which pushes the price prediction higher).
