# XIRR_PIPELINE
1.DESCRIPTION:

   The notebook is used to calculate XIRR value of a input Tradebook for stocks listed in Indian Markets NSE and BSE.
   The input is Tradebook which is a csv file of the portfolio having following columns Symbol which is TICKER Symbol of the company,
   ISIN code which is used for listing the company in the market, Exchange i.e. market NSE/BSE,
   Segment: This indicates the market segment where the trade occurs. For example, common segments include the Cash Market (CM) for normal equity trading, or Future & Options (FO) for derivatives trading,
   Series:  For example, "BE" series on NSE stands for "Book Entry" and is used for Trade-to-Trade segment shares. Other series codes include "EQ" for normal equity shares and "BT" for block trades,
   Auctions are special processes initiated by exchanges to resolve settlement or delivery issues such as shortages or bad deliveries,
   Trade Type: sell / bought,
   Quantity: Quantity of  stocks bought/sold,
   Price : Price at stock bought at.
2. Challenges:
   1.Date formats:
     After downloading tradebook and importing in csv, all values in date column should be
     in yyyy-mm-dd or dd-mm-yyyy format. Then convert it into datetime.
   2.External Data Ambiguity:
     1. Companies might be delisted or renamed therefore stock split data wont be accessible
        using yahoo finance,fmp, polygon.io.Therefore this data must be provided externally
     2. Stock name amibiguity: For our company's tradebook TIPSINDLTD and TIPSMUSIC are the            same as well as HBLPOWER and HBLENGINE. For fetching price data and stock split data
        these edge cases need  to be handled.
     3. Stock split data fetching :
        For TIMETECHNO when stock split data is fetched using yahoo finance consecutive stock
        split for 2 days could be seen where as the stock split occurred only on one day.
        Therefore verifying using multiple ways is safer.

    
    
        
  
   
     
     
   
   



