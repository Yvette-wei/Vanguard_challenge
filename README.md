# Vanguard_challenge

Below is the link to the database db file I created from my notebook. The file size was too big for Github upload so I uploaded to a Google drive folder.

https://drive.google.com/drive/folders/1jrHXp1jxHn-QiaWgNYddqTPqZ52JEaNx?usp=sharing

I created the database "vanguardcons.db" with the constituents tickers and corresponding sectors for each month in the constituents_history.pkl, with the yfinance stock information for each day. So the header of the table "stocks" looks like: Date, ticker, Sector, Open, High, Low, Close, Adj Close, Volume. The primary key would be (Date, ticker). And some ticker whose information cannot be retrieved from yfinance are stored in a list called "delisted", and they are not added in the stock table. Another note is that for notebook readability, I hid the download output for the transform&load cell. 

For the first analyze question, I added another table "indextbl" in the same database "vanguardcons.db" to store the index for every day I have data in 2018, 2019, and 2020. The header for "indextbl" should look like: Date, DailyIndex.

For the second analyze question, I used the "stocks" table and looked at the end of year ("12-31") for 2018, 2019, 2020, and used "Close" similarly to the first question, but this time to calculate a relative weight for each sector. I created a dictionary to store data from "stocks", and then a list of lists to calculate the weight, and displayed as a dataframe in the end. The header for the dataframe should look like: Year, Ticker, Sector, RelWeight.
