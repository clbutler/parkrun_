
# **ParkRun Lifetime Statistics Power BI Dashboard:**

This Power BI dashboard provides a comprehensive analysis of your personal ParkRun journey, offering insights into your performance over time and across different locations.

The dashboard is organized into two main pages, each designed to give you a detailed view of your ParkRun statistics:

## **A. Time Dashboard**

This page focuses on your running performance, allowing you to track your times and see how you've progressed.

  **Lifetime ParkRun Count:** _See the total number of ParkRuns you've completed._

  **Fastest Run Time:** _Discover your personal best time._

  **Average Run Time:** _Get an understanding of your typical performance._
  
  **Run Time Distribution:** _A box and whisker plot visualizes the spread and central tendency of your run times._

  **ParkRun Times by Date/Year:** _Track your run times over time with detailed views by date and year._

  **Event and Year Slicers:** _Easily filter your data to focus on specific events or years._

**Example Output:** ![image](https://github.com/user-attachments/assets/bbc1db3b-a770-4b8d-ab10-9f52f0211110)

### **B. Location Dashboard**

Explore your ParkRun adventures geographically and analyze your performance at different courses.

  **Interactive Map of All ParkRun Locations Attended:** _Visualize all the different ParkRun events you've participated in on an interactive map._

  **Unique Location Count:** _See how many different ParkRun events you've run at._

  **Fastest Location:** _Identify the location where you achieved your fastest time._

  **Favorite (Most Popular) Location:** _Discover which ParkRun event you've attended the most._

  **Example Output:** ![image](https://github.com/user-attachments/assets/ebe6eab3-1912-402e-b1bb-9bcd95ff1665)

---

## **Instructions for Use**

Getting started with your ParkRun Power BI Dashboard is straightforward! Just follow these steps to set up and visualize your data:

### **1. Download the Files**

First, download the following three files from this GitHub page:

* `parkrun.csv`
* `parkrun.pbix`
* `parkrun_locations.json`

Place all three files into **the same folder** on your computer.

### **2. Load the Power BI Dashboard**

The `parkrun.pbix` file is your Power BI dashboard. Simply open this file, and it'll load all the visualizations and data models.

### **3. ParkRun Locations (No Action Needed)**

The `parkrun_locations.json` file contains the geographical coordinates for all ParkRun locations, accurate as of June 16, 2025. This file is automatically parsed within Power BI (using Power Query), so you **don't need to do anything** with it. I'll periodically update this file to keep the location data current.

### **4. Update Your ParkRun Data**

The `parkrun.csv` file is where your personal ParkRun results live. Since ParkRun doesn't offer API connectivity or allow web scraping, you'll need to **manually update this file** with your own data:

1.  **Log in** to your ParkRun account.
2.  Navigate to the **"Results"** tab.
3.  Click on **"View stats for all parkruns by this parkrunner"**.
4.  **Copy and paste** the entire table (currently titled "All Results") directly into your `parkrun.csv` file.

Once you've updated the `parkrun.csv` file, simply **refresh the data** within your Power BI dashboard to see your latest statistics!

---
---

## **Troubleshooting**

Ideally, with all your files in the same folder, you should be able to simply refresh the dashboard (using the **Refresh button** on the Power BI **Home tab**) to see your own data. If that's not working, here are a few things to double-check:

### **1. Verify `parkrun_locations` Data Structure**

Ensure the `parkrun_locations` data table within Power BI's table layer matches the expected format, especially regarding its headers.

 ![image](https://github.com/user-attachments/assets/b0f49509-2ead-4968-b049-a6ce76fca46d)


### **2. Verify `parkrun` Data Structure and Freshness**

Confirm that your `parkrun` data table in Power BI has the correct headers and is up-to-date with your latest copied data from the ParkRun website.

 ![image](https://github.com/user-attachments/assets/c4150d2b-3d56-4c8c-ba3e-4b97d47b73f3)

### **3. Check Data Model Relationships**

For the dashboard to function correctly, these two data tables (entities) need to communicate. Verify that the following relationship is set up in the **Model View**:

* The **'Event' columns** in both `parkrun` and `parkrun_locations` act as **keys** and should be linked.
* There should be a **many-to-one relationship** from the `parkrun` entity to the `parkrun_locations` entity. This makes sense because each ParkRun location can have multiple runs associated with it.

You can manage these relationships using the **Manage Relationships button** on Power BI's **Home ribbon**.

 ![image](https://github.com/user-attachments/assets/4116ffe5-53e7-4889-a75e-3efc5ce3a649)

 Finally I have GitHub Issues open if you find any bugs you can escalate them to me, and GitHub Discussions are also open if you want to suggest new features

---





