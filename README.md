# Web Scraping with Python using Selenium and BeautifulSoup (condomenium listings in Bangkok, Thailand)

This is the second episode of web scraping project and we are still working on condomenium listings in Bangkok, Thailand. You can find my first project [here.](https://github.com/ekapope/Baania-webscraping)

The page we are going to pull data from is called [Hipflat](https://www.hipflat.co.th/). This project will be using Selenium library to run the first get (request) to obtain all condo links, and then extract info elements using BeautifulSoup package.

We were able to specify the input data format, but I wanted to keep the code simple. Therefore, we still need to do some data cleaning before further analysis process. 


[01_Scrape_All_Links_gh.ipynb](https://github.com/ekapope/web-scraping-using-selenium-and-bs4/blob/master/01_Scrape_All_Links_gh.ipynb) is Selenium to retrive all listing links. The output of this code is [condo_links_all.txt](https://github.com/ekapope/web-scraping-using-selenium-and-bs4/blob/master/condo_links_all.txt), contains total of 2540 links retrived.

[02_Scrape_info_for_each_condo.ipynb](https://github.com/ekapope/web-scraping-using-selenium-and-bs4/blob/master/02_Scrape_info_for_each_condo.ipynb) is using BeautifulSoup to extract the data from each listing. The final output is [df_completed.pkl](https://github.com/ekapope/web-scraping-using-selenium-and-bs4/blob/master/df_completed.pkl) data frame which contains significant infos we scraped of all condos. Noted that some listings were rejected and not written in this file as the pricing data were missing from the page.

I have done some preliminary cleaning for 'df_completed.pkl' and got the output as ['df_hipflat_cleaned_01_gh.csv'](https://github.com/ekapope/web-scraping-using-selenium-and-bs4/blob/master/df_hipflat_cleaned_01_gh.csv). This file will be used in another repository for example data cleaning and EDA.

Please note:

As always, scraping the website is only allowed for personal use. Given the "sleep" intervals embedded in the code, it gently scrapes the pages so it will take a while to complete the whole operation.

Selenium can be run in headless mode. Check out this handy [guide](https://medium.com/@pyzzled/running-headless-chrome-with-selenium-in-python-3f42d1f5ff1d).

Again, thanks https://www.hipflat.co.th/ for the listing data.
