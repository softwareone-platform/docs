---
description: Adjust the data grid layout to suit your needs.
---

# Customize the data grid

The Marketplace Platform uses data grids to display data.&#x20;

A data grid is a table with rows and columns, and it contains several operations that allow you to customize the display of information.

You can sort and filter data, show or hide columns, adjust the column width, change the default rows per page, and more. This topic describes each of these tasks.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/DataGrid (2).png" alt=""><figcaption><p>Use the data grid to view data in a structured way.</p></figcaption></figure></div>

### Sorting data

Sorting enables you to reorganize your data in ascending or descending order so you can understand and visualize it better. There are two ways to use the sort function in the grid.

**Sort a single column**

You can sort the data for a column by selecting the column header. When you select the header, the preconfigured sort options are displayed. You can choose any option from the list.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/data_grid_sort_filter.png" alt=""><figcaption><p>Use the available options to sort a single column.</p></figcaption></figure></div>

**Sort multiple columns**

If you want to apply multiple sorts, select<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGAAAABgCAYAAADimHc4AAAAAXNSR0IArs4c6QAAA/BJREFUeF7tnVGPEjEQgKc/Uu9JQFjDciaaaPTFM2pOXzSaaOKxxF0EfNL7kTXLhUA42Gm3nc62O/dCLls67fftTI8eBQXyw0pAsUaX4CACmG8CESACmAkwh5cMEAHMBJjDSwaIgD2BwTh/X/+2WRbbxz78dCYDavhKwbsautbwoS8SOiHgEP7uru+LBHYBp+D3SQKrgCb4fZHAJsAEfh8ksAiwgZ+6hOAC2sBPWUJQAS7wU5UQTIAP+ClKCCLAJ/zUJJALoICfkgRSAZTwU5FAJiAE/BQkkAgICT92Cd4F2MHXtwDqQfO2s0mbux5i3MDzKsAW/rpaPBxOct0kYF0VajiZ/sNFxSnBm4A28GtkJgLu2qUpwYuAtvBtBKQqwVmAC3xbASlKcBYwzPI3oOEj/v9bfVvX/ON2piXo8HnG5UjB1bosPuFj42vhLKAe+mA8e6GU/np+Gqfht8mAXQxMgtbq5WY5/8aH1iyyFwF1qNFkeqlB/bwf9jx8FwFN5UiBfrqqFjdmCHhbeROwzYTJLFOgf+2n1AzfVcApCRrUk001L3mxmkf3KuAuE/JHGmADgMP3IeBQggIYrKrij/n0+Vt6F7DNhGx6sSkXf02m12YRPtWvTUyTcYVqQyLAZvC+BNjE7FJbEcBsQwSIAHwzjpkRaXjJAFK8eOciAGdE2kIEkOLFOxcBOCPSFiKAFC/euQjAGZG2SF5A119pi4CqYGXAGtzXbmhTjZAMQCooNSDq/l0XCMkAKUG0e0GSAVKCGglICep7CXJdxLDnSwnCCBFfFwHEgLHuRQBGiPi6CCAGjHUvAjBCxNdFADFgrHsRgBEivi4CiAFj3YsAjBDxdRFAAHiQXV5sypvAb/41j2kzZfa9IJvB1m1H43ykFfxmefu7hserZbGyHXNT+6gEjMbTXCs1308IP4PgWoKOj0IprWer5aLwJSEaAcMsfwYavt+fePgjUKDg+bosfviQEIWAUTZ7pbX+fH7C4Q8BKqVer8r5F1cJnRcwnMyuAPQ1PlGGY7Cg3q6rucER3fOj77yA1A+Cd15Afe+4SLBZhLGzx4f3sa9PZolCgIsEUwEc8Ot5RSOgrQQTAVzwoxPQRgL+OUO8HwgVVQbsarDdmoD//WTSwlfNP44VpQD7TDBB3PAqg/ALJaIVEEoC1Z2/0x21AGoJ1PCjXIRPFQqKNSEE/GQE+M6EUPCTEuBLQkj4yQlwlRAafpIC2krggJ+sAFsJXPCTFmAqgRN+8gIwCdzweyHgnIQuwO+NgGMJXYHfKwE7CfVjl76pNfq9ILd9Tv5niwBmByJABDATYA4vGSACmAkwh5cMEAHMBJjD/wfY3bt/biV2ewAAAABJRU5ErkJggg==" alt="<svg xmlns=&#x22;http://www.w3.org/2000/svg&#x22; height=&#x22;24px&#x22; viewBox=&#x22;0 -960 960 960&#x22; width=&#x22;24px&#x22; fill=&#x22;#5f6368&#x22;><path d=&#x22;M320-440v-287L217-624l-57-56 200-200 200 200-57 56-103-103v287h-80ZM600-80 400-280l57-56 103 103v-287h80v287l103-103 57 56L600-80Z&#x22;/></svg>" data-size="line">**Sort** in the grid and then follow these steps:&#x20;

1. In the **Sort** box, select **Add another sort**.&#x20;
2. Choose the required property and select the display order (**Ascending** or **Descending**). To add another sorting rule, select **Add another sort**. You can add multiple rules.
3. Select **Close**. All columns that have sort conditions applied are highlighted in the table.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/data_grid_sort.png" alt=""><figcaption><p>Sort multiple columns.</p></figcaption></figure></div>

### Filtering data

Filters help you narrow down data based on specific attributes. Depending on the type of data you are searching for, you can use a single filter or create multiple filters using different conditions and **AND/OR** operators.

For example, when ordering new items, you can create a filter to show only the items with a specific name. Similarly, if you have multiple subscriptions, you could use the **AND/OR** operators to view subscriptions that are active AND have auto-renewal enabled.&#x20;

You can also use the **Search Query** filter to enter a search term to find matching records within other filter conditions, such as orders, agreements, and more. Additionally, you can use the second-level filter condition called **Add a conditional group** to build advanced filters by combining multiple rules and conditions.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/filter-options.png" alt=""><figcaption><p>Apply filter to easily find the data.</p></figcaption></figure></div>

To start filtering data:

1. Select the <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGAAAABgCAYAAADimHc4AAAAAXNSR0IArs4c6QAAActJREFUeF7t2TFOQ0EQBFF8UgISjkRCwElBpASg0Y5VtnmOZ6e9Vb+Db1+efFIClzRd+BMB8UNAAAExgTheAwiICcTxGkBATCCO1wACYgJxvAYQEBOI4zWAgJhAHK8BBMQE4ngNICAmEMdrAAExgTheAwiICcTxGnBvAp5fXj/j73zT8R/vb6OHejT8fXMCfvdPQNwPAgiICcTxGkBATCCO14BHFxDf7+Hix+8BD0cgvhABBMQE4ngNICAmEMdrAAExgTheAwiICcTxGkBATCCOv3oD7v0vzOmvm1OfBPxBjIDpI7U8T8Ay0Ok6AqbElucJWAY6XUfAlNjyPAHLQKfr7l7A9ML/bf7q7wH/Dej0vgRMiS3PE7AMdLqOgCmx5XkCloFO1xEwJbY8T8Ay0Ok6AqbElucJWAY6XUfAlNjyPAHLQKfrbl7A6X/K1/4xbQr85zwBpwQPzxNwCPD0OAGnBA/PE3AI8PQ4AacED88TcAjw9DgBpwQPz9+8gMP73fxxAmJFBBAQE4jjNYCAmEAcrwEExATieA0gICYQx2sAATGBOF4DCIgJxPEaQEBMII7XAAJiAnG8BhAQE4jjNYCAmEAcrwEExATi+C97b2BhPsA2DAAAAABJRU5ErkJggg==" alt="<svg xmlns=&#x22;http://www.w3.org/2000/svg&#x22; height=&#x22;24px&#x22; viewBox=&#x22;0 -960 960 960&#x22; width=&#x22;24px&#x22; fill=&#x22;#5f6368&#x22;><path d=&#x22;M400-240v-80h160v80H400ZM240-440v-80h480v80H240ZM120-640v-80h720v80H120Z&#x22;/></svg>" data-size="line">**Filter** option.
2. In the **Filters** box, do the following as necessary:
   * Enter the **search query** to find records matching a specific keyword or select a predefined property from the list (for example, Buyer name).
   * To add another condition and combine those conditions using the **And** or **Or** operators, select **Add another condition**. Then, define conditions as follows:
     1. Select the desired **And** or **OR** operator.
        * **And** - If you select this operator, the results are displayed only if both conditions are met.
        * **Or** - If you select this operator, only one of the conditions needs to be met for the results to be displayed.
     2. Choose the required property.
     3. Select the condition, such as equal, contains, starts with, and so on.
     4. Choose a value from the list of preconfigured values or type the keyword.
   * To add another condition, select **Add another condition** and define conditions as needed.
   * To add a conditional action, select **Add a conditional group** and use the dropdowns to select the criteria. If you want to add another condition within the same group, select **Add another condition**.

As you define filters, the data in the grid refreshes automatically. If the platform is unable to find any data matching the filters, it displays a message.&#x20;

### Managing columns

**Show or hide columns**

The <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGAAAABgCAYAAADimHc4AAAAAXNSR0IArs4c6QAAAzlJREFUeF7tnDFuE0EUQP+44ARAjUQHB6ChIC03iCC2YoOzEgVHiHMFCrJCtsVacASUkjRUVJRIXABxBrLIIUaJxNr/79/1l+2XemZ+5r3582fX9iThL5RACo1OcEFA8CJAAAKCCQSHJwMQEEwgODwZgIBgAsHhyQAEBBMIDk8GICCYQHB4MgABwQSCw5MBCAgmEByeDEBAMIHg8GTApgs4OBw+Sp1ON4k8EJGHInIneE5th/8pkr6V6eK7XHTOZtPTM09AVwb0+tkzSfLB8w9sfN8kH4tx/rzuPGoL6A6yT0nkad3A29avmOS1WNbqdNDPXnaSvNs2iK75JHldjPM31jHMAvaHw9u3fne+isg9a7AdaP+4mORfLPM0C+i9ODqUMk0tQXalbSnydjbJX1nmaxfQPzqVlDJLkB1qe15M8j3LfO0CBtkPEblvCbJDbX8Vk/yuZb51BJTLAtQ5DfQG2WcReVI1bkqy936cn1sm1u1nxynJqKpPWcpoNs1PLGPO2/YGWaPzR4DRAAKUwMgAJairtGYL0vJqOgURoCV/1Q4BFGHVkqEGqDD9bcQx1Aar0XMwAgzw23gQQQACTASaPoTwJGzCz6sINS5OQWpUnIIMqJpPQYqwCT8CKMLKBUMNUIJiCzKA4kGs+S14m58DRinJcdX64iPJa2Raehm3SsDJbJpXfmZcJY4irNwyu/0MAUpWbb2ORgACVhPY5SJMDVisD4rw6kz516LpU0CLD2LUAK1XMkBLqoXvRpIBBvgb9iqCLUjrli1IS4otiK+na9cKryK0pNr7Zhw1QOuAGqAlRQ2gBmjXCjVAS4oaYCDFFsQWpF0u27wF8UPt6lWwhh9qc1XBsiRcw1UFXNZRKWAtl3VwXc3SKtT+dTXz8FzY9B8J67qwaRGaK8tuSqhzScl8BPO3Iq6H5dK+S4Ixl/YtRHBtZeC1ldqHItpVE3BtQYD1E0CAn6FrBAS48Pk7I8DP0DUCAlz4/J0R4GfoGgEBLnz+zgjwM3SNgAAXPn9nBPgZukZAgAufvzMC/AxdIyDAhc/fGQF+hq4REODC5++MAD9D1wgIcOHzd0aAn6FrBAS48Pk7/wFgPoCO+qZK/AAAAABJRU5ErkJggg==" alt="<svg xmlns=&#x22;http://www.w3.org/2000/svg&#x22; height=&#x22;24px&#x22; viewBox=&#x22;0 -960 960 960&#x22; width=&#x22;24px&#x22; fill=&#x22;#5f6368&#x22;><path d=&#x22;M121-280v-400q0-33 23.5-56.5T201-760h559q33 0 56.5 23.5T840-680v400q0 33-23.5 56.5T760-200H201q-33 0-56.5-23.5T121-280Zm79 0h133v-400H200v400Zm213 0h133v-400H413v400Zm213 0h133v-400H626v400Z&#x22;/></svg>" data-size="line">**Columns** selector in the data grid lets you show or hide a column. Using this option, you can view only the information you need and hide other columns from the page.&#x20;

You can use the checkbox next to each column name to hide or display a column. If you have hidden a column, you can make it visible again by selecting the same checkbox. Note that some columns are shown by default, and you cannot hide them.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/data_grid_columns.png" alt=""><figcaption><p>Use the Columns selector to show oe hide columns.</p></figcaption></figure></div>

**Adjust column widths**

The **Columns** selector also contains options to adjust the column width. These options include:

* **Default size** - This option resets each column in the table to its default size. You can use this option if you've made adjustments and want to return all columns to their original state.
* **Fit to content** - This option resizes each column in the table to fit its specific content. It means that the width is adjusted to the content within the column.
* **Fit to screen** - This option resizes each column to make the entire table fit your screen.

### Refreshing data

If the data in the grid has changed, you can refresh the data to make sure you are working with the latest data at all times. Use the <img src="../../../.gitbook/assets/refresh_24dp_5F6368_FILL0_wght400_GRAD0_opsz24.png" alt="<svg xmlns=&#x22;http://www.w3.org/2000/svg&#x22; height=&#x22;24px&#x22; viewBox=&#x22;0 -960 960 960&#x22; width=&#x22;24px&#x22; fill=&#x22;#5f6368&#x22;><path d=&#x22;M121-280v-400q0-33 23.5-56.5T201-760h559q33 0 56.5 23.5T840-680v400q0 33-23.5 56.5T760-200H201q-33 0-56.5-23.5T121-280Zm79 0h133v-400H200v400Zm213 0h133v-400H413v400Zm213 0h133v-400H626v400Z&#x22;/></svg>" data-size="line">**Refresh** option to fetch the latest data from the system.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Refresh.png" alt=""><figcaption><p>Use the Refresh option to manually refresh the table.</p></figcaption></figure></div>

### Changing default rows per page

By default, the Marketplace Platform displays 10 rows of data on a page.&#x20;

You can change the default value by selecting another value from the **Rows per page** option on the lower-right side of the grid. You can choose to show 5, 10, 25, 50, or 100 rows per page.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Rows.png" alt=""><figcaption><p>Change the number of rows displayed on the page.</p></figcaption></figure></div>

### Navigating between pages

If the grid contains several rows, the rows are split into pages, and page numbers are displayed on the lower-left side of the table.

You can view the page number you are currently on and navigate between pages using the **Next** and **Previous** options. You can also go to a page directly by entering the number in the **Page** field and pressing **Enter**.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/interface_navigation.png" alt=""><figcaption><p>Navigate to different pages within the table.</p></figcaption></figure></div>
