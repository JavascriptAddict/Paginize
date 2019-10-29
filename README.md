# Paginize.js
Paginize.js is a simple Javascript wrapper function which aims to simplify the creation of pagination. View below for more information.

### Sample Webpage
Visit this [sample Paginize.js implementation](https://javascriptaddict.github.io/Singapore-Traffic-Camera-Webpage "Singapore Traffic Camera Webpage").

## Usage
### Initialization
```javascript
Paginize.initialize(No_Of_Results_Per_Page, Data_Array, Box_Set);
```
* No_Of_Results_Per_Page refers to how many results is to be displayed per page. 
```
E.g. 5
```
* Data_Array refers to the data array obtained from a response or elsewhere. 
```
E.g. [{data: "This is PageJS"}, {data: "It helps with pagination"}]
```
* Box_Set refers to how many page number boxes per segment. 
```
E.g. 5
```
### Pagination & Segmentation Calculations
```javascript
Paginize.calculatePages();
```
* There is no need to run this function as the initialization function will automatically run it.
### Change Box Segment
```javascript
Paginize.changeBoxSegment(Direction)
```
* Direction refers to decrease or increase to the next box segment.
```
E.g. -1 or 1
```
#### Data Returned
```
E.g. [[6, 7 , 8, 9, 10]]
```
* **IMPORTANT: Please use the data returned to set the page number and ID of the pagination boxes**
### Change Page
```javascript
Paginize.changePage(BoxID);
```
* BoxID refers to the ID of the pagination box that was clicked. Refer to the important note under Change Box Segment for more information.

#### Data Returned
* This function will run the data splitting function automatically and return the sliced data array.
```
E.g. [{data: "This is page 56"}, {data: "This is page 56"}]
```
