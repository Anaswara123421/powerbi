Power BI Order Analysis

Overview

This project is a Power BI Desktop data model created for analyzing order details, customer/order information, sales targets, and profit.

The Power BI file contains a model with multiple tables and relationships that allow data from order-level and detail-level tables to be used together for analysis.

File

powerbi.pbix — Power BI Desktop report and data model

Tables

1. List of Orders

Contains order-level information such as:

Customername

Location

Order Date

Order ID

2. Order Details

Contains detailed information for each order, including:

Amount

Category

Order ID

Profit

Profit Status

Quantity

Sub-Category

Total Margin

3. Sales Target

Contains target information by category and month:

Category

Month of Order Date

Target

4. Orders Data

Contains additional order/customer information, including fields such as:

City region

Customername

Order Date

Order detail information

5. Order Details summary

A summary table containing:

Order ID Count

Order ID

6. Average Profit

Contains the average profit calculation by category.

Data Model Relationships

The main relationships established in the model are:

List of Orders → Order Details

The relationship is created using:

List of Orders[Order ID] → Order Details[Order ID]

This connects each order in the order-level table with its corresponding detailed order records.

Order Details → Sales Target

The relationship is created using:

Order Details[Category] → Sales Target[Category]

This allows order details to be associated with the corresponding sales target category.

The relationship is configured as active in Power BI.

Model View

The Power BI Model view is used to visually manage the tables and their relationships. The model includes the Order ID relationship between the order tables and the Category relationship between Order Details and Sales Target.

Key Calculations

The model includes calculations such as:

Average Profit

Order ID Count

Sales Target

Profit

Total Margin

Quantity

Amount

These calculations can be used to build Power BI reports and visualizations.

How to Use

Open powerbi.pbix using Power BI Desktop.

Go to Model view to inspect the tables and relationships.

Open Manage relationships to verify that the relationships are active.

Go to Report view to create or modify visualizations.

Use fields such as Category, Order Date, Amount, Profit, Quantity, and Target to perform analysis.

Relationship Verification

Before using the model, verify:

List of Orders[Order ID] is related to Order Details[Order ID].

Order Details[Category] is related to Sales Target[Category].

The Sales Target relationship is active.

The column data types used in each relationship are compatible.

Purpose

The project demonstrates how to:

Build a relational data model in Power BI

Connect tables using common keys

Establish active relationships

Work with order and sales-target data

Create measures and calculations

Prepare a model for interactive business analysis

Tools Used

Power BI Desktop

Power Query / Power BI Data Model

DAX calculations

Author

Power BI Data Analysis Project
