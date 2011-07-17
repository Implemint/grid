# Grid #

Version: 0.1
Date: 16th July 2011
Github Repository: https://github.com/Implemint/Mint-Grid

## Overview

This grid is a slightly modified version of the [1140 CSS Grid](http://cssgrid.net/) by [Andy Taylor](http://andytly.com/). I liked this grid system as it's percentage based, and responsive, but there were a couple of things that I felt could have been done differently.

I utilize [headjs](http://headjs.com/) in nearly every project I work on, so for me to use this grid, I found it necessary to modify it to use headjs. This allows for html5 support in dated browsers, polyfill classes which have been applied for the responsive widths and IE fixes, so you can use them rather than @media queries to modify your responsive layouts or separate stylesheets to fix IE. As well as loading your javascript like images to reduce page loading speed.

I've also added in the ability to add padding to your grid columns. By default, the padding is set to 20 pixels, but can easily be modified in the `1104.css` file. Simply add the class `.padded` to your column element to get it to work.

## The Markup

    <div class="container">
      <div class="row">
        <div class="threecol">
          <p>Column 1</p>
        </div>
        <div class="threecol">
          <p>Column 2</p>
        </div>
        <div class="threecol">
          <p>Column 3</p>
        </div>
        <div class="threecol last">
          <p>Column 4</p>
        </div>
      </div>
    </div>

## Explanation of the classes and markup
    .container
Is a full width div that allows layouts to have a background that spans the full width of the browser. It also contains 20px padding on either side to keep content away from the edges when it becomes fluid. You can just use one big container, or use multiple to break the page horizontally.

    .row
Is a row of columns. It centres them and defines the 1140px max-width.

    .onecol, .twocol, .threecol, .fourcol, .fivecol, .sixcol, .sevencol, .eightcol, .ninecol, .tencol, .elevencol
Are the classes for each column. They can be used in any combination within a row that adds up to twelve or less.

    .last
The last column within a row also needs this class. It removes the right margin so all the columns fit within the row.
