# Homework1

Homework 1 Code Refactor

First, I went through both the html and css files and labeled the sections. There is a header section, a main image section, a main content section, a side section, and a footer section. I then checked the indentation of the html elements and I did not see any issues with them. 

In the header section, I checked that the links were correctly linked to the section. I did see an issue with the Search Engine Optimization link as it did not link to the search engine optimization section. To fix this, I added the id “search-engine-optimization” to the div for that section. So when the href: #search-engine-optimization anchor tag gets clicked the page goes to that specific section. In the style sheet, I saw multiple selectors were used at the same time. To make the style sheet cleaner and easier to read, I created classes so only one selector is used. For example, the header class, h1, and the seo class was used at the same time to target the span element:

.header h1 .seo {
        color: #d9dcd6;
}

Since the span had the class name “seo”, I just used the class name as the selector for simplicity. Below, the .header and the h1 is used, but since there is only one h1 in the entire page, only h1 is needed as the selector for the h1 to be styled.

.header h1 {
    display: inline-block;
    font-size: 48px;
}

For the code below, I assigned a class name “Nav-bar” to the div and just used the class as the selector.
.header div {
    padding-top: 15px;
    margin-right: 20px;
    float: right;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    font-size: 20px;
}

I did notice that these following codes were repeated many times throughout the style sheet. To avoid repetition, I placed these styles with the body selector. However, the color of the text in the footer section is black, so I added the color black to the footer class to override the white colored text.

font-size: 16px
color: #ffffff


In the main section and the benefits section, I did see multiple class selectors that had the same property and values. For example, the code below has the same property and value for the h3 element. To avoid repetition, I assigned a class and named it “benefits-heading-texts” to all the h3’s in order to target all three of the h3 elements.

.benefit-lead h3 {
    margin-bottom: 10px;
    text-align: center;
}

.benefit-brand h3 {
    margin-bottom: 10px;
    text-align: center;
}

.benefit-cost h3 {
    margin-bottom: 10px;
    text-align: center;
}

Another example is the code below. All three have the same property and value for the h2 elements. I assigned the class “main-content-header” to each h2 element in the main content section in order to target all the h2’s at the same time.

#search-engine-optimization h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

#online-reputation-management h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

#social-media-marketing h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

Overall, I was able to decrease the CSS style sheet from 200 lines of code down to about 120 lines of code.

