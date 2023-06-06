# project-1
Project 1: Group #2




Readme Start:
Project Readme

    This project involves analyzing building data using the Socrata API. The data contains information about various properties in San Francisco, including their floor area, property type, property subcategory, year built, and energy consumption metrics. The goal is to perform data analysis and generate insights from the dataset.

Dependencies

    The following dependencies are required for this project:

        pandas
        sodapy
        matplotlib
        scipy
        numpy

    Make sure to install these dependencies before running the code.

Roadmap

    - Figures: This directory contains graphical representations that summarize the results of our analyses. Each file is appropriately labeled to correspond with the specific question and answer derived from the code.nergy 
    - Consumption Analysis for Buildings in San Francisco: This PowerPoint presentation serves as a comprehensive overview of our findings and will be utilized during our project presentation.
    - Project_1.ipynb: This Jupyter Notebook file contains the code we developed to address the various data-related inquiries we encountered throughout the project.
    
Data Retrieval

    To retrieve the data, we used the Socrata API provided by data.sfgov.org. The API allows us to access the dataset and retrieve the first 60,000 results in JSON format. We then convert the data into a pandas DataFrame for further analysis.

Data Cleaning

    The initial dataset may contain missing values represented as NaN, "Not Available," or 0. We cleaned the data by dropping rows with any of these values. Additionally, we combined all commercial buildings into a single property type for simplicity.

Renaming Columns

    To improve readability, we renamed the columns in the DataFrame. This step makes it easier to understand the data and perform analysis.

Data Type Conversion

    We converted numerical columns to float data type for further analysis. This conversion allows us to perform mathematical operations and calculations on the data.

Property Type Analysis

    We analyzed the distribution of properties based on their property type. The count of each property type is calculated and displayed, showing the number of commercial and mixed residential properties in the dataset.

Property Subcategory Analysis

    We also analyzed the distribution of properties based on their property subcategory. The count of each subcategory is calculated and displayed, showing the different types of properties within the commercial and mixed residential categories.

    1. Visualizing GHG Emissions and Energy Use Intensity by Property Subcategory:
    - The code groups the data by the "Property Subcategory" column and calculates the median values for "2022 Total GHG Emissions Intensity (kGCO2e/ft2)" and "2022 Source EUI (kBtu/ft2)".
    - Two bar plots are created, one for GHG emissions intensity and the other for energy use intensity, with the property subcategories on the x-axis and the corresponding values on the y-axis.

    2. Analyzing the Relationship between Source EUI and GHG Emissions:
    - The code extracts the "2022 Source EUI (kBtu/ft2)" and "2022 Total GHG Emissions Intensity (kGCO2e/ft2)" columns from the dataset.
    - A linear regression analysis is performed using these two variables, and the results are stored in variables like pe_slope, pe_int, pe_r, pe_p, and pe_std_err.
    - A scatter plot of the data points is created, and a regression line is plotted based on the regression equation obtained from the analysis.
    - The r-value (coefficient of determination) is printed to indicate the strength of the linear relationship between the two variables.

    3. Analyzing the Relationship between Year Built and GHG Emission Intensity for Commercial and Residential Buildings:
    - The code categorizes the "Year Built" column into bins using the pd.cut() function.
    - Two separate analyses are performed for commercial and residential buildings:

        For commercial buildings:
        - The code filters the data to include only commercial buildings.
        - The count of buildings in each bin is calculated.
        - The median value of "2022 Total GHG Emissions Intensity (kGCO2e/ft2)" is calculated for each bin.
        - A line plot is created to visualize the trend of GHG emissions intensity for commercial buildings over time.

        For residential buildings:
        - The code filters the data to include only mixed residential buildings.
        - The median value of "2022 Total GHG Emissions Intensity (kGCO2e/ft2)" is calculated for each bin.
        - A line plot is created to visualize the trend of GHG emissions intensity for residential buildings over time.

    Overall, the code provides visualizations and analyses of the GHG emissions and energy use intensity by property subcategory and explores the relationship between source EUI and GHG emissions. It also examines the relationship between year built and GHG emission intensity for commercial and residential buildings.
