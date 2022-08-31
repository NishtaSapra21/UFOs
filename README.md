# UFOs

## Overview

This analysis of UFO sighting allows user to filter for multiple criteria like date, city, state, country and shape on dynamic table displaying on webpage using HTML and JavaScript. 

## Results

### HTML and JavaScript 

Let’s have a look how HTML and JavaScript work together for this multiple filter criteria. 

  1.	The __index.html__ file contains all CSS and JavaScript files locations within __<link rel=”stylesheet” />__ and __<script src=”path to js file”></script>__           tags. There are also a link to __Bootstrap's content delivery network (CDN)__ and  a link to a __D3.js CDN__.
  
  2.	The __data.js__ file contains all the data about UFOs. 
  
  3.	The __app.js__ file is the file where we write functions to create a dynamic table with filter search
  
        •	__buildTable()__ 

           This function loops through each objects in data and data row and append table rows and cell values to HTML table.
           
        •	__searchFilter()__

          This function get the filtered element value using __d3.select(this)__  and get the id of that filter to save __{id : value}__ in dictionary. The dictionary           can hold more than one search criteria until there’s no criteria to match. 

        •	__filterTable()__

          This function loops through all the filters(dictionary)  and keeps the data that matches the filtered values. 
        
### Filter Criteria and Results with Images

Let’s have a look how we can use multiple criteria to filter table data. 
This is the table with all data.

![table_data](https://user-images.githubusercontent.com/107717882/187778523-7ad5422b-3315-4e61-85fc-83377e01ac0f.png)

Now, let’s have data for the date __”1/5/2010”__. 

![filter_date](https://user-images.githubusercontent.com/107717882/187778565-a980b145-b426-4c31-9c4f-e279e229b4bb.png)

Now, we want state “nj” data for above date. You can see how result has been filtered in below figure. 

![filter_date_state](https://user-images.githubusercontent.com/107717882/187778598-b7772c03-fba0-4480-8b60-9ce63a50983f.png)

Now, we want one more filter __"cigar shape"__ with state __“nj”__ and date __“1/5/2020”__. Below image shows all three filters together on the table. 

![filter_date_state_shape](https://user-images.githubusercontent.com/107717882/187778637-badaff7c-33c2-4e22-b9ed-fe685ddd88ff.png)


## Summary

•	Drawback 

  This design enables user to search on multiple criteria but when user wants go back , there’s no proper way how to get original table back. You have to delete your     search criteria to get back original table.  This is confusing for end user. 

•	Additional Recommendation

  1.	Adding a calendar to choose date with start and end date helps user to visualize date range easily.
  
  
![calendar](https://user-images.githubusercontent.com/107717882/187779779-453eb25f-e48e-4e87-9f9a-7151cca7865d.png)

  
  2.	User has to erase filter each time to get back original data; there should be a __“CLEAR”__ button to clear all filters. We can achieve same with __reset               button__ and using  __addEventListener()__ in Javascript using function to get back original table. 

  3.	It would be easy for user if city, state , country and shapes provide dropdown list to select. For larger data its diffcult , so choosing                               among dropdown items wil be helpful. 
  
  4.	Some message should be displayed if there's no data related to entered search criteria. 





