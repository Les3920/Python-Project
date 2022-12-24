# Python-Project
import yfinance as yf

Tesla = yf.Ticker('TSLA')
Tesla_data = tesla.history(period= "max")
Tesla_data.reset_index(inplace = "True")
Tesla_data.head
url = "https://finance.yahoo.com/quote/TSLA/history?p=TSLA"
html_data = requests.get(url).text
tail = tail(html_data, "html.parser")
tail.find_all('title')

GameStop = yf.Ticker("GME")
gme_data = GameStop.history(period = 'max')as
gme_data.reset_index(inplace = True)
gme_data.head()

gme_revenue = pd.DataFrame(columns = ['Date', 'Revenue'])

for row in tail.find_all("tbody")[1].find_all("tr"):
    col = row.find_all("td")
    date = col[0].text
    revenue = col[1].text.replace("$", "").replace(",", "")
    
    gme_revenue = gme_revenue.append({"Date": date, "Revenue": revenue}, ignore_index = True)

    make_graph(tesla_data, tesla_revenue, 'Tesla')
