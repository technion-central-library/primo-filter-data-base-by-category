# primo-filter-data-base-by-category

# A-Z listing for Databases search by category on Primo VE 
On November 2018 ExLibris release the option of assigning categories to the database records. This feature allows the institute to add a list of subjects in order to improve databases accessibility. 
We have created an A-Z listing plug-in for this list to ease navigation due to a very long list of subjects in our various databases.
To implement this plug-in in Primo VE please follow these stages:
1.	Assigning Categories to the Database Records (From Ex Libris documentation):
Choose a local bibliographic field (for example, select any 6XX or 9XX field for MARC21) in which to store the database categories in your local bibliographic records, and then enter that field in the db_categories_field parameter on the Alma Customer Parameters page 

# The Primo New UI Customization Workflow Development Environment


## Package documentation

The development package allows you to configure :

- css

- images

- html

- JavaScript

- The root directory of the package should be named either by the `viewCode` or `CENTRAL_PACKAGE` in case of a consortia level package
- Whether you develop a consortia level package or a view level package the process remains the same
- Once deployed the hierarchy is as follows:
    1. For css - use the cascading ability of css and load the consortia level (CENTRAL_PACKAGE) css first and the view level css afterwards
    2. For images and html - the system checks for every file if it exists in each level - and prefers the view level file if exists
    3. For JavaScript - the two package types define 2 different Angular modules:
        - ```var app = angular.module('viewCustom', ['angularLoad']);```
        - ```var app = angular.module('centralCustom', ['angularLoad']);```

  and loads both of the modules,

- For each configuration type there is a specified folder in the custom package folder (that can be downloaded form your Primo Back Office)
- In each folder you will find a specific README.md file with recipes/examples.

  [CSS](./VIEW_CODE/css/README.md "css documentation")

  [HTML](./VIEW_CODE/html/README.md "html documentation")

  [Images](./VIEW_CODE/img/README.md "images documentation")

  [JavaScript](./VIEW_CODE/js/README.md "javascript documentation")

-  For `colors.json.txt` instructions - please see [CSS](./VIEW_CODE/css/README.md "css documentation") documentation
