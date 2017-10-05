---
title: [Load CSV files with the UI]
tags: [Data_Integ_User_Upload,Data_Integ_tsload]
keywords: "csv,data load"
last_updated: tbd
summary: "The simplest way to load data is to upload a CSV or Excel file from the ThoughtSpot Web interface. "
sidebar: mydoc_sidebar
permalink: /:collection/:path.html
---

{% include content/web_load_intro.md %}

## Formatting the CSV

Your ETL (extract, transform, load) process will typically generate CSV files. You can also create a CSV file from a Microsoft Excel spreadsheet by opening the spreadsheet in Excel, choosing **Save As** and selecting CSV.

{% include content/csv_format.md %}

If you are loading a fact table that joins to dimension tables, you must load the fact table first, and then the dimension tables. The joining key must be a single column of unique values in the dimension table. `NULL` values in the fact table cannot be joined.

## Create a CSV file

{% include content/csv_create.md %}

For general information about CSV files and the rules for creating them, see the [Comma-separated_values](http://en.wikipedia.org/wiki/Comma-separated_values) on Wikipedia.

## Load the CSV File

{% include content/csv_load.md %}


## Append to an existing table

{% include content/csv_append.md %}