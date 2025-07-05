# DSA-PROJECT-1---EXCEL
Amazon Product Review Analysis - My detailed analysis on this project will assist the management on product improvement, marketing strategies and customer engagement. They will know the areas of the business to focus on. It will be a guide for them to know the businesses that are working and the ones that are not working.

CASE STUDY 1: Amazon Product Review Analysis.

No product should have more than a record since its all about reviews and ratings. This is *Ultimate Underlying Assumption:*
To get that done with the dataset, duplicated - Product_Id were removed, to confirm if there are duplicated products- I simply Clicked on any cell within the dataset and apply *Ctrl + A* to highlight all the data.

So while still highlighted, *Data* Tab was clicked. locate *Remove Duplicate* tool that is under "Data Tool" group. There is a dialogue box, once it;s clicked on, *Unselect All* first, then only select *product_id*. 114 Duplicate values found and removed; 1351 unique values remain
I now have my Unique/Distinct Products. *NEXT* is CATEGORY.
*Category* is key in all just as the *product_id*.  *Text to Columns* was adopted.
 *Copy and Paste the Category Column* to a "playing ground" environment. By adding new *worksheet* It’s there on Excel sheet, titled – Category split. *Category* for set up for "interrogation" . This is because, its "multi-level category" wise.
Copy to the clipboard, the common delimited in the overall categories details, which is |
Then, highlight *column A* where the category details is, and click *Text to Columns*. This dialogue box would come up once. proceed with this step... Paste the copied delimiter into this *Other* space, Then click on *Finish*
My single-cateory had now spread across *5* columns already. Now that I have 5 Columns, I have to name each Column giving them unique headers. The Mother Category's interrogation has therefore ended this moment since she gave us the names of her children already who are responsible for grouping our data
Going back to the original dataset, columns *D to G* was highlighted since we need space to accommodate *4* more category headers. Then right-click on the highlight columns and click *Insert*.
Meanwhile, there were 7 category splits, but we'll only address 5 of them - No need for long listing. Because of that we'll retain the mother-category, so you have the option to pick which other category level you want to take along. The choice is personal.
Personally, I chose the first *4* along side with the Mother-Category as I don't want to have more than 4 of them on my dashboard.
Back to the category-splits sheet, then *highlight* and *copy* only the relevant from top to bottom of the 4 columns as shown here. Then go to the Dataset and Paste value on cell *D1*

NEXT is Clean Up
Confirm that columns *H* to *L* values are reliable. Use the filter tool to validate each columns's values.
From Data Tab, click on filter. Since we are done with column *A-G*, so you do this for column *H* and the rest of the columns. Most irregulars are often at the TOP or BOTTOM of the values listings.
If you proceed to column *I*, meant for *actual_price*, you will notice that the data type is incorrect. The correct value should be have been *139,900*, but it was written – 1,39,900
So select it and get it fixed with the correct value.
As for column *J*, checked. Column *K* has this symbol | on it, Select it and click OK. In Data Analysis,  you can either use N/A meaning not available for characters or 0 for numbers where we are unsure.. So we replace the delimiter | with  "0"
In column *L*, you'll notice *Blanks*. So click it to see the products affected. Since in Data Analysis, we can use "0" for price or number column where we are unsure. We replace the Blank rating count with "0".
Nothing to be fixed on columns *M to T* respectively. Checked 

NEXT is *Calculated Columns*
Lets start with *Total Potential Revenue*
Click on column *M* to insert a new column beside column *L*. Then label it like - Total Potential Revenue
How to derive those values - multiply *actual_price* by *rating_count*
So go ahead and compute that for each product_id. Please note, *Rating_Count* is the same as *Total Number of Reviewers* per Product

Next is *Price Range Bucket*. You can Insert the column beside *discounted_Price*
Before doing this, apply your currency to conform with what is on the Case Study. By applying this India currency on all price related columns. You can get it this way. Highlight all your price related columns at once and apply this format on them to change the currency.
I highlighted - discounted price, Price Range Bucket, Actual Price and Total Potential Revenue.
Then from Home page,  goto - Accounting Number Format beside %, click on - More Options to Accounting to English(India), then ok. Once that is done, go back to the new column
I copied this currency *₹* it will be needed as a text for the formula.
Then you go *=IF(H2<200,"<₹200",IF(OR(H2=200,H2<=500),"₹200 - ₹500",">₹500"))*⁸
Now that your dataset is cleaned now, click on any cell within your dataset and turn it to a table by applying *Ctrl + T*

SOME FORMULARS USED:
- 	To get Top 5 products by rating + number of reviews combined. I created CALCULATED COLUMNS:
Create calculated column:
=Average Rating + (Rating Count / Scaling Factor)
(Choose a factor like 1000 to balance weight)
Sort descending and pick top 5.

- 	Formula used to get – *Discount Range Bucket* on Dataset:
 =IF([@[discount_percentage]]>=50%,"Yes","No") 

- 	*Discounts Range* formula:
 =IF([@[discount_percentage]]<=10%,"0-10%",IF([@[discount_percentage]]<=20%,"11-20%",IF([@[discount_percentage]]<=30%,"21-30%",IF([@[discount_percentage]]<=40%,"31-40%",IF([@[discount_percentage]]<=50%,"41-50%",IF([@[discount_percentage]]<=60%,"51-60%",IF([@[discount_percentage]]<=70%,"61-70%",IF([@[discount_percentage]]<=80%,"71-80%",IF([@[discount_percentage]]<=90%,"81-90%","91-100%"))))))))
### Tools Used
- Microsoft Excel for Data cleaning [Download here](https://www.microsoft.com)
 - For data collection
 - Data manipulation
   
![Ex1](https://github.com/user-attachments/assets/80c6c986-a702-4868-a36e-5851b3d6064c)
![Ex2](https://github.com/user-attachments/assets/bca1143c-5960-4e88-a6d8-9a849d153c0d)
![Ex3](https://github.com/user-attachments/assets/b5b943b9-98c2-4940-ad3d-a45703e8c71a)
![Ex4](https://github.com/user-attachments/assets/5b4f4cc6-d24e-4a34-abfd-a466ac389f01)
![Ex5](https://github.com/user-attachments/assets/dbdff96e-3c8a-4540-bb34-05eafb10944b)


[EXCEL PROJECT - Amazon Case Study.xlsx](https://github.com/user-attachments/files/21052903/EXCEL.PROJECT.-.Amazon.Case.Study.xlsx)




