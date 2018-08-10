
It is about OHLC chart and get the live data from url: https://www.alphavantage.co
and it will differentiate the color of the bearish and bullish period (like green
and red).

Open read_json.html from internet browser and it will
retrieve live data (daily) from web site.

The script is accomplished in javascript with CanvasJS.

You can add in additional stock option by editing read_json.html with below operation :

Currently apikey is registered under the developer name which you may need to register yourself by accessing
below url :

https://www.alphavantage.co/support/#api-key

Once you get the api key, you can make the changes in $.getjson statement apikey value.


1. Copy one of the stock function (like amazon) and change its name to the stock option you want to add

Example :

Add in citibank stock by changing the function name and symbol value.

function citibank() {
   dps = [];

   create_chart("Citibank");
   $.getJSON("https://www.alphavantage.co/query?function=TIME_SERIES_DAILY&symbol=C&apikey=KOOP0G6C9B8MOM3R", callback);
}

2. You can test out the url is working or not by pasting in internet browser, it shoulds display citibank share price in 
   json format.  

3. Add a button option and change its onclick function to citibank().

   <button onclick="citibank()">Citibank</button>

4. Save the read_json.html file and refresh in internet browser, the citibank button will appear.

