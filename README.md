README

# airbnb_impact

### Table of Contents

1. [Installation](#installation)
2. [Project Description](#description)
3. [Project Motivation](#motivation)
4. [File Descriptions](#files)
5. [Results](#results)
6. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

There should be no necessary libraries to run the code here beyond the Anaconda distribution of Python. The code should run with no issues using Python versions 3.*.

## Project Description <a name="description"></a>

### Business Understanding

Airbnb, founded as part of the sharing economy, enables everyone to rent out accommodations for short term. After it’s expansion in the last decade, the company faces criticism as rising Airbnb rentals extract living spaces and leads to higher rents for locals.

The analysis should show if Airbnb is a serious competitor to the hospitality industry, who offers accommodations and how cities are impacted from this development.

### Data Understanding

This analysis project uses data from insidedairbnb. Key objects are Airbnb listings and their reviews, which are provided in separated files. Airbnb states that about 50% of guests leave a review, which makes them a good proxy for the platform usage in a city. The listing file consists of one row per listing and contains an ID, listings and hosts name as several aggregated values. The review file contains the listings ID and a date for every review.

### Data Preparation and Modeling

To analyze listings and reviews the single files have to be merged (via listing id). As there is no identification between commercial and private hosts a self defined rule is applied to the dataset, explained in the associated blogpost. The review files come without missing values. The listing files have some missing values in the name and host columns, which are not relevant for the analysis. But the last_review and reviews_per_month columns have a lot of empty values. For counting active listings (criteria: at least one review in 2019) these listings would be ignored. Other analysis regarding reviews make use of the single entry data from the review file instead of the aggregated values in the listings file.

### Result Evaluation

The visualizations show intresting differences between cities. In every considered city airbnb is still growing, but there are differences in growth rate and in proportion of private and commercial hosts.

## Project Motivation<a name="motivation"></a>

As a frequent traveller and Airbnb customer I was looking for a critical view on the impacts the platform has for cities and their residents. Also this analysis and the blogpost on Medium are part of my Udacity Data Science Nanodegree program.

## File Descriptions <a name="files"></a>

The python code can be found in a Jupyter Notebook. The analysis process is documented with Markdown cells, comments and docstrings.

## Results<a name="results"></a>

The main findings of the code can be found at the post available [here](https://medium.com/@ewarest/the-municipalities-fight-against-airbnb-9a0fe89d39dd).

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Thanks to insidedairbnb.com for providing latest data on Airbnb listings. The analysis was done with data released in September 2019.
