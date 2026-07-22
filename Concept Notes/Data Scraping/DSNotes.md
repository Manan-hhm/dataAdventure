<h3>Data Scraping</h3>
-> Process of getting useful, semi-structured data from the Internet <br>
-> Not used much in large companies but used a lot in smaller companies and SaaS based startups. <br>

<h4>Types of Web Scraping</h4>
<ol>
  <li>Reqeuest/API Scraping</li>
  <p>
    -> Directly load data from Internet via an API. <br>
    -> Considered to be the easiest type of Scraping.
  </p>
  <li>Static HTML Scraping</li>
  <p>
    -> We load a sample static website. <br>
    -> We extract HTML data from the website. <br>
    -> Considered to be easy scraping. But it is difficult than API scraping
  </p>
  <li>Dynamic JS Scraping</li>
  <p>
    -> We load a complex dynamic website. <br>
    -> We interact with it like an end user. <br>
    -> Considerably more complex type of scraping. <br>
  </p>
</ol>

<h3>API Scraping</h3>
-> API (Application Programming Interface) is a way to get an external program to do something. <br>
-> For Scraping, we send a request to the API program to get data for us. <br>

<h4>JSON</h4>
-> A way to store data in text, similar to CSV. <br>
-> It is very similar to python dictionaries (objects) and lists (arrays). <br>
-> A common format used in Scraping. It is supported by many languages like C, Java, JavaScript, Python, etc.<br>

<h3>HTML Scraping</h3>
-> Using tools like Scrapy & BeautifulSoup for scraping using python.
-> Scrapy: A python framework allow us a simple way to scrape and crawl a website. It can also gather images and save our data as a CSV file. <br>
-> BeautifulSoup: A library test our scrape code and initialize a scrape code. <br>

<h4>Spider</h4>
-> A function that allows you to find all the pages that you want to scrape. <br>

-> For example, at books.toscrape.com, we need a spider that can crawl through/find all the book pages. <br>

<h4>Creating Spider for our website</h4>

1. Initialize a project. <br>
>scrapy startproject books_scraper <br>
'books_scraper' is the name of our project. (We can use any name) <br>

Then change the directory (cd) to be in "books_scraper" <br>

2. Initialize a spider with a start URL (where our spider will start crawling). <br>
> scrapy genspider books books.toscrape.com <br>
'books' is the name of our spider (We can use any name) <br>


