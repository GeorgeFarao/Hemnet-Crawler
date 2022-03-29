# Hemnet Crawler
A crawler for Hemnet, Sweden's largest housing platform, using Scrapy.

I have created a crawler that collects data from the website. First I start with the url of a page containing various house listings. From this page I extract the url for each listing's page, since that's where the useful data are located. As the starting page can have many listings, that can't fit in a single page, the program follows the `next_page` class in order to get each one of them.

Afterwards inside the `parseInnerPage` function the data are collected. First the streetName, then the price and then I create a dictionary for each listing containing all it's adsitional data and their labels. In this function I also "clean" the data from whitespaces and unnecessary characters.

All the data for each listing are stored in a dictionary and after the spider finishes collecting the data, the results are stored inside `results.json`.
