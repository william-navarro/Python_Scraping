# Python_Scraping
A bot to get the products you want and compile into an excel file.




The purpose of this program is to send a list of product's code, referred in this description as "SKU", and return an excel with all possible information about the product on Fast Shop's website.

I will describe how it works in a few steps:
1- Opens a Chrome's tab in headless mode(won't show to the user)
2- Pops up a window asking you to choose and submit an excel file
3- Looks for a column in excel named "SKU_FASTSHOP" and get all lines into a list
4- Sends the entire list into site's search box and submit
5- In search results, scrolls to the bottom of the page to completely load all SKUs in website
6- Opens the first product on a new tab and tries to insert CEP number and apply. Then, if the CEP worked, it will begin to extract information for each product. If doesn't work, it will try again on the next product of the list.
7- For each product it will: Open it in a new tab and get: Title, SKU number, Normal, PIX price(if available), Special price(if available), Description, First and Second image, Category and Tension(if available).
8- Then compile it into an excel file 
9- And finish by bringing two informations on the screen: From X products on the sheet, it found Y products on the website and the name of generated file with finished time, day and month.
