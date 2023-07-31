## App Store and Google Play Store Data Analysis

This Python script performs data analysis on datasets from both the App Store and the Google Play Store. The code is designed to explore and extract insights from these datasets to understand various aspects of mobile applications.

### Dataset Overview

The script uses two datasets, each corresponding to a different app store:

1. ## Google Play Store Dataset Description

The Google Play Store dataset contains information about various mobile applications available on the Google Play Store. Each row represents a unique app, and the dataset includes the following columns:

- `App`: The name of the app.

- `Category`: The category to which the app belongs.

- `Rating`: The average user rating of the app.

- `Reviews`: The number of user reviews for the app.

- `Size`: The size of the app.

- `Installs`: The number of times the app has been installed.

- `Type`: The type of the app (e.g., Free or Paid).

- `Price`: The price of the app (if applicable).

- `Content Rating`: The content rating of the app (e.g., Everyone, Teen, Mature 17+, etc.).

- `Genres`: The genre(s) of the app.

- `Last Updated`: The date when the app was last updated.

- `Current Ver`: The current version of the app.

- `Android Ver`: The minimum required Android version to run the app.

### Sample App Data

Here is a sample row of data from the dataset:

| App                                              | Category       | Rating | Reviews | Size  | Installs    | Type  | Price | Content Rating | Genres          | Last Updated      | Current Ver | Android Ver    |
|-------------------------------------------------|----------------|--------|---------|-------|--------------|-------|-------|----------------|-----------------|-------------------|--------------|--------------------|
| Photo Editor & Candy Camera & Grid & ScrapBook | ART_AND_DESIGN | 4.1     | 159        | 19M  | "10,000+" | Free  | 0       | Everyone          | Art & Design   | January 7, 2018  | 1.0.0        | 4.0.3 and up    |

This row represents the app "Photo Editor & Candy Camera & Grid & ScrapBook" in the category "Art & Design," with an average user rating of 4.1 and 159 user reviews. The app is free, has a size of 19M, and belongs to the "Everyone" content rating.

The dataset contains valuable information about the characteristics and attributes of numerous mobile applications on the Google Play Store, making it suitable for various data analyses and insights for app developers and researchers.


2. **App Store Dataset:**

The App Store dataset contains information about various mobile applications available on the App Store. Each row represents a unique app, and the dataset includes the following columns:

- `id`: A unique identifier for the app.

- `track_name`: The name of the app.

- `size_bytes`: The size of the app in bytes.

- `currency`: The currency used for pricing the app.

- `price`: The price of the app.

- `rating_count_tot`: The total number of user ratings for the app.

- `rating_count_ver`: The number of user ratings for the current version of the app.

- `user_rating`: The average user rating for the app.

- `user_rating_ver`: The average user rating for the current version of the app.

- `ver`: The version of the app.

- `cont_rating`: The content rating of the app (e.g., 4+, 9+, 12+, etc.).

- `prime_genre`: The primary genre/category of the app.

- `sup_devices.num`: The number of supported devices for the app.

- `ipadSc_urls.num`: The number of screenshots displayed for the app on iPad.

- `lang.num`: The number of supported languages for the app.

- `vpp_lic`: Vpp Device Based Licensing Enabled (1 if enabled, 0 if not).

### Sample App Data

Here is a sample row of data from the dataset:

| id        | track_name | size_bytes | currency | price | rating_count_tot | rating_count_ver | user_rating | user_rating_ver | ver | cont_rating | prime_genre    | sup_devices.num | ipadSc_urls.num | lang.num | vpp_lic |
|-----------|--------------|----------------|---------|---------|--------------------|---------------------|--------------|------------------|-------|--------------|----------------|------------------|------------------|------------|------------|
| 284882215 | Facebook   | 389879808    | USD     | 0.0     | 2974676             | 212                        | 3.5             | 3.5                      | 95.0 | 4+                | Social Networking | 37                 | 1                   | 29            | 1            |

This row represents the "Facebook" app with various details such as its size, pricing, ratings, and genre.

The dataset contains valuable information about the characteristics and attributes of numerous mobile applications on the App Store, making it suitable for various data analyses and insights for app developers and researchers.


### Data Exploration and Cleaning

1. The function `explore_data()` is defined to display a slice of the dataset, and it is used to print the first three rows of both datasets.
2. The script identifies and deletes a row from the Google Play Store dataset with an incorrect entry (row 10472).
3. Duplicate apps are identified in both datasets, and duplicate entries are removed from the Google Play Store dataset to ensure accuracy in the analysis.

### Language Filter

1. The script filters out non-English apps by checking if their names contain more than three non-ASCII characters.
2. The filtered datasets, 'android_english' and 'ios_english', contain only English apps.

### Analysis on Free Apps

1. The analysis focuses on free apps only.
2. The final datasets, 'android_final' and 'ios_final', contain free English apps.

### App Genre Analysis

1. The function `freq_table()` computes the frequency of genres in both datasets.
2. The function `display_table()` prints the frequency table for different genres.
3. The script calculates the average number of user ratings for each app genre in the App Store dataset.

### Conclusion

The Python script performs a comprehensive analysis of app datasets from both the App Store and Google Play Store. It ensures data accuracy by eliminating duplicates and non-English apps. The genre analysis helps identify app categories with high user engagement. This analysis can provide valuable insights for developers to make data-driven decisions in building successful mobile applications.

Please note that the code provided here is a summary of the analysis steps. For detailed implementation and further exploration, refer to the Python script or Jupyter Notebook in this repository.
