# PERSONAL PROJECT NO. 1
## INJECTIVE-STAGE-OF-PERSONAL-PROFIT
Stage of profit or loss of cryptocurrency Injective at a given moment in relation to your personal crypto wallet or the coins you own

### Task:
You need to create a program code that will read the required information from the website and save the relevant data in an Excel file. The information read below should be used for the calculation, the result of which will also be saved in an Excel file table. The code only needs to perform the action once after it is run. A website that generates real-time value of "Injective" cryptocurrency is chosen. This value should be read from the opened homepage and saved in an Excel file table by recording the date and time. When this is done, the fixed price is considered the current "Injective" unit price. Next, a calculation must be made that will reflect my profit or loss. Accordingly, the program requires you to enter the number of "Injective" currency units you own, where, using the previously fixed value, your current profit/loss is calculated. Note that when you run the code for the first time, the previous value will not be fixed, but only the current one, so this should also be specified in the code lines themselves, so as not to generate redundant error messages. The next time you run the code, the previous value will already be available in the Excel file.

### The aim:
The purpose of the program is to save human time for small analysis, as these small steps are usually performed multiple times to track real-time currency fluctuations. In the daily process, you usually open the website, look at the price, then use the calculator to calculate the value you own (the price of one unit multiplied by the number of units you own). Next, you need to record this price somewhere in order to make your own profit/loss calculation with mathematical subtraction operations. This software will make this process much faster and will also organize the data instantly in an Excel file in a transparent way. Not only is time saved, but there are potential opportunities to perform new analysis or perform other important calculations from the data stored in our Excel file. In this exercise, this process will be carried out directly for the joy of "Injective" cryptocurrency, because it is mine.

### Calculation:
Current price and previous price per unit of "Injective" will be obtained. To calculate the profit per unit, you need to subtract the previous price from the current price. This will not be possible the first time you run the code, as only one existing price defined as current will be fixed, but with the next run, this calculation will be possible. I also fixed this nuance in the code lines. Next, when the subtraction is done, it is necessary to multiply by the number of units owned by the user.

Formula:(pašreizējā_cena - iepriekšējā_cena) * piederīgie_vienu_skaits


### Website:
In this case, choosing the home page is a critical factor in code generation to avoid error messages. Since we work with active currencies, price fluctuations happen every millisecond, so many websites that display real-time currency values are in HTML. Such factors prevent the program from reading the price, because it constantly changes during the change of the reading process. Therefore, it is recommended to choose API homepages that still reflect the real-time price, but the price refreshes after a certain frequency. I'm using diadata.org in a section on the home page that reflects the value of "Injective" directly. This homepage refreshes at a frequency equal to 120 seconds, which is enough time for my code to read the information.

Link: https://www.diadata.org/app/price/asset/Ethereum/0xe28b3B32B6c345A34Ff64674606124Dd5Aceca30/ 


## Python libraries I used:
1. Selenium library. This library is used to perform automated test cases for browsers or web applications. In our case, the homepage was opened with the help of this library. Pressed "accept" button for notification signal about cookies. Next, a value for the price of "Injective" was found and read. Then the website was closed.
2. Openpyxl library. This library is used to read/write Excel 2010 xlsx/xlsm/xltx/xltm files. In our case, the data read by the program was saved/written to an xlsx file with the help of this library. This library was then used to read the information previously stored in the same xlsx file so that calculations could be performed. After the calculations were made, the data calculated with the help of this library were recorded and recorded in an Excel file.
3. Python datetime library. We captured the date and time with the help of this library.
4. Python time library. Provides a variety of functions for working with time-related activities. In our case, it was used to give the program the necessary time to perform an action before the software moves on to the next step.

> [!IMPORTANT]
> The code creation took place on the VS code platform, as the selenium library was used, which could not access the chromedriver paths through the github site.

## Program development description:
1. Required libraries are imported.
2. The Chrome driver is set up.
3. Open the browser and go to the specific link from the diadata.org homepage.
4. It takes a while for the website to load (I used 5 seconds because the homepage was slow to load).
5. The cookie notification is automatically closed.
6. The current price is read and the browser is closed.
7. The existing Excel file named 'crypto_dati.xlsx' is loaded using load_workbook.
8. The existing worksheet (worksheet) opens.
9. The current date and time are set.
10. A new line is added to the worksheet with data, where the date and time are from the current moment, the price (data['price']), the number of "Injective" units (data['number_of']), and the calculation (data[' calculation']).
11. Save the changes in the Excel file.
12. The previous price and the current price are converted from text format (with currency symbols and commas) to a decimal number.
13. Profit or loss is calculated using formulas.
14. The result is returned, which is rounded to two decimal places. If any of the conversion steps fail or if there are other problems, then 'N/A' is returned.
15. Lines are written down, with the help of which we get the current price, as well as the previous price from the Excel file.
16. Getting the number of "Injectives" owned by the user manually (Since I currently own 30 units, I could just use the number 30 automatically every time, but the crypto market is volatile, so in order not to have to change this value in the code and Excel file every time, when units are sold or replenished, I chose to manually enter this step for the user).
17. Profit or loss is calculated.
18. The data is saved in an Excel file.
19. A message is displayed that the program has ended its operation and the results are visible in an Excel file.

## Methods of using this software
Use of the program is very simple. As a user, you must start the program by pressing the "run" button. You have to wait a little (~10 seconds) while the program performs operations with the selenium library. Then the program itself will ask you to enter the number of Injective units you own. Next, the results will be visible by opening the excel file. I see myself using this program very often, as I check the fluctuations of "Injective" several times throughout the day, with interest in how profitable or losing I am at a given moment. This program makes this process much faster. In addition, the advantage of this program is that the data is transparently saved in an Excel document. Hence the ability to quickly compare dates and times. This advantage also plays a big role in successful subsequent analysis. The completed Excel file of this program can be useful for cryptocurrency forecast analysis and calculations. This analysis can also be automated later using the final result table and code template of this program.


