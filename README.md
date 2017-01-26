# Exchange-Currency

Project - Part 1

Exchange money from one currency into another, using the ECB reference exchange rate for a particular day (within the last 90 days)

Example: convert 14.50 USD to CHF on Dec 17th

ECB reference rates as XML files https://www.ecb.europa.eu/stats/exchange/eurofxref/html/index.en.html

90 days history https://www.ecb.europa.eu/stats/eurofxref/eurofxref-hist-90d.xml

Timeline

This task should take you a couple of hours. There is no time pressure. It would be nice to have a solution within the next 2 weeks. Just send me an email when you are done.

Expectations


################

//XMLEnvelope holds the fetched data as struct of strings

type XMLEnvelope struct {
    Gesmes  string   `xml:"gesmes,attr"`
    Xmlns   string   `xml:"xmlns,attr"`
    Subject string   `xml:"subject"`
    Name    string   `xml:"Sender>name"`
    Days    []XMLDay `xml:"Cube>Cube"`
}

type XMLDay struct {
    Time          string            `xml:"time,attr"`
    CurrencyRates []XMLCurrencyRate `xml:"Cube"`
}
type XMLCurrencyRate struct {
    // Todo
}
