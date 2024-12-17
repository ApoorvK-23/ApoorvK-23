flowchart TD
    %% Fact Table
    Sales_Fact["Sales Fact Table"]

    %% Dimension Tables
    Date_Dim["Date Dimension Table"]
    Product_Dim["Product Dimension Table"]
    Store_Dim["Store Dimension Table"]

    %% Aggregated Tables
    Summary_Table["Summary Table"]
    Rollup_Table["Rollup Table"]
    Multidimensional_Cube["Multidimensional Cube"]

    %% Connections to Fact Table
    Sales_Fact --> Date_Dim
    Sales_Fact --> Product_Dim
    Sales_Fact --> Store_Dim

    %% Connections to Aggregated Tables
    Summary_Table --> Sales_Fact
    Rollup_Table --> Sales_Fact

    %% Multidimensional Cube Connections
    Multidimensional_Cube --> Sales_Fact
    Multidimensional_Cube --> Date_Dim
    Multidimensional_Cube --> Product_Dim
    Multidimensional_Cube --> Store_Dim

