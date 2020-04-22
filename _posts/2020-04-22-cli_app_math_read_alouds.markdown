---
layout: post
title:      "CLI App: Math Read Alouds"
date:       2020-04-22 07:50:15 +0000
permalink:  cli_app_math_read_alouds
---


I saw this project as an opportunity to create a math resource for teachers. Sometimes, it can be challenging to integrate mathematics and reading. However, a quick way to do this would be finding a read aloud that is related to mathematics. 

When starting this project, I set out to scrape a few pages from https://www.k-5mathteachingresources.com/  that highlight books for the following math topics: 
1. Counting
2. Addition
3. Subtraction
4. Multiplication
5. Division
6. Fractions
7. Geometry
8. Measurement

Looking back, I should have spent more time looking for a scrapeable site. Since I limited my app design to math-related ideas, I only knew a few sites that listed books focused on math topics. 

Although I was able to scrape the math topics using the image attributes on the first page, scraping the separate pages that focus on separate topics was challenging. When I scraped the counting page, it was easy to get the book titles, descriptions, and authors. The only challenge was the CSS selector I used to scrape a book's description included the topic name (i.e. Counting) at the end sometimes. So, if there were 5 descriptions on the page, I would get 6 results for my descriptions --5 descriptions and then the phrase "counting." I did not want to accidentally create a new instance of a book with a topic saved as a description so I added a conditional statement that only saved a description if it was longer than 30 characters. 

When I moved on to other topic pages (e.g. Addition, Subtraction, Measurement, etc.), they were not set up the same as the counting page. I assumed that they would be, but unfortunately, I was wrong! The class names were changed sometimes. The html elements were not the same. Sometimes, the information I needed to scrape on one page would appear within a paragraph element and on another page, it would be located within a span element. Therefore, I had to select different css selectors depending on the page. I thought this made my .scrape_books method look entirely too messy. This is something that I would like to fix moving forward with this app. 

Other than that, I'm very pleased with [my first project](https://github.com/keelsk/math_read_alouds). When I first saw the requirements, I doubted my abilities. However, the resources provided in the program really helped, especially the Eden Events walkthrough videos, and I built the CLI App pretty quickly. 
