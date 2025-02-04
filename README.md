# Grubhub Email Label Scraper
Logs grubhub email prices, items, locations, and dates where I spent money, because I'm a broke ass college student who needs to watch their wallet like a hawk.
But you could also use it for any easy scraping abilities if you play around with some things. The labels itself are pretty easy to change in the code.

## How it works
The scraper checks for a label like "Dining Dollar expenses (Grubhub)" in your email inbox. 

[![email-label-ex.png](https://i.postimg.cc/yN5ZQKNR/email-label-ex.png)](https://postimg.cc/JyN009Z7)

When it finds it, it grabs the plain text version of every email with that label. Once it has it, it separates the whole email's lines into an array.  Since Grubhub's email is pretty bare-bones, I didn't need to have the full HTML version of it to parse it. Once in that array, it checks what each of those lines starts with.

In this code, if a line starts with "1 x ", "Total: " or "Shop: ", it will save it to its corresponding arrays (items, prices, shops, etc). The reason it checks for those was because the eamail and plain Body text looked like this:

[![email-2-plain-body-ex.png](https://i.postimg.cc/9M1TV9m6/email-2-plain-body-ex.png)](https://postimg.cc/r00zNKtj)

So once it finishes parsing & removing extra parts like the ": $3.95" from Hot Chocolate, it directs those arrays to the function that puts the data onto the spreadsheet. Although that function doesn't *split* the data, it is still called splitGrubData(), because I made that one first and didn't feel like changing the name. That function grabs the spreadsheet the app is connected to, selects all the rows in a column (starting from the second) then puts the data into each row. So the final table winds up looking like:

[![Formatted-table.png](https://i.postimg.cc/Qd5TCwNk/Formatted-table.png)](https://postimg.cc/68W31Hvy)

*Note: The S'More's cake was bought with the Quessdilla combo above it, so it doesn't need the data repeated.*

## How to change this code to your needs (without much coding)
Putting this here, because when I started this, I'd hoped to find something like it pretty easily, and well... I either didn't look hard enough or didn't feel like understanding how to change someone else's code to fit my needs better. I've done it before, but I guess I just didn't feel like it this time around. So you're in luck!

1. **Check the **
hold on I'm late for my class

