# belly-button-challenge
Belly Button Biodiversity Dashboard

 Purpose of this Project is to build a interactive dashboard to explore the Belly Button Biodiversity  which catalogs the microbes that colonize human navels.

Dataset: The dataset reveals that a small handful of microbial species (called  OTUs, in the study) were present in more than 70% of people, while the rest were relatively rare.

I created a repository with belly-button-challenge name on github

## Dashboard Creation Process

The backend of the dashboard, handled by JavaScript (`app.js`), is responsible for extracting, transforming, and loading the data subsets into the corresponding HTML tags and visuals.

#### How it works:
- **Data Retrieval**: Calling the Belly Button API to GET the data response and dividing it into three main subsets using `D3.json(URL)`:
  - `metadata`
  - `names`
  - `samples`
- **Mapping Subsets**: Mapping the subsets to extract relevant fields for the dashboard's visuals and assigning the filtered subsets to global scope variables (`sampleData` and `metaField`).
- **Dropdown Menu Population**: Using `document.getElementById` to refer to the corresponding HTML dropdown tag and assigning it to a variable. Then, utilizing `forEach` to loop over the items and create new options using `document.createElement`.
- **Error Handling**: Chaining the `catch` function to `D3.json(URL)` to catch errors while working with the dataset.

### 2. Data Visuals
To create an interactive dashboard, a function is made to plot visuals based on one condition: if the selected value exists within the subset, filter the results and use the return value to plot the visuals.

## Libraries Used
- Plotly
- D3

## Languages Used
- **Frontend**: HTML
- **Backend**: JavaScript


## Create a horizontal bar chart with a dropdown menu to display the top 10 OTUs found in that individual.
- Use sample_values as the values for the bar chart.
- Use otu_ids as the labels for the bar chart
- Use otu_labels as the hovertext for the chart.

## Create a bubble chart that displays each sample.
- Use otu_ids for the x values.
- Use sample_values for the y values.
- Use sample_values for the marker size.
- Use otu_ids for the marker colors.
- Use otu_labels for the text values.

## Display the sample's metadata, 
i.e., an individual's demographic information.

## Dashboard Images:
![Demographic info](images/demograph.png.png)
![Top 10 Bacteria Culture Found](images/top_10_bacteria.png.png)
![Bacteria Culture Per Sample](images/bacteria_culture_per_sample.png.png)


## Github Pages
https://seyhr.github.io/belly-button-challenge/