# Turtle Example
<p dir="auto"><a href="https://opensource.org/licenses/MIT" rel="nofollow"><img src="https://camo.githubusercontent.com/78f47a09877ba9d28da1887a93e5c3bc2efb309c1e910eb21135becd2998238a/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4c6963656e73652d4d49542d79656c6c6f772e737667" alt="License: MIT" data-canonical-src="https://img.shields.io/badge/License-MIT-yellow.svg" style="max-width: 100%;"></a>
</p>

This repository contains the codebase for a <strong>Turtle Graphics</strong> example, implemented using the TurtleGraphics package in R Studio. This package can be used to create sophisticated graphics by drawing lines by describing the location and orientation of the <strong>"turtle"</strong> in code. The graphic can be further coustomized by changing the line type and colors.

<ul dir="auto">
<li><a href="#contributors">Contributors</a></li>
<li><a href="#abstract">Abstract</a></li>
<li><a href="#codeoverview">Code Overview</a></li>
<li><a href="#development">Development</a></li>
<li><a href="#citation">Citation</a></li>
<li><a href="#contact">Contact</a></li>
</ul>

## Contributors
<p dir="auto">See <a href="https://github.com/harmansingh1412/test/blob/main/CONTRIBUTORS.md">CONTRIBUTORS.md</a></p>

## Abstract

## Code Overview

<h3 tabindex="-1" dir="auto"><a id="user-content-install-dependency" class="anchor" aria-hidden="true" href="#install-dependency"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a>Install Packages</h3>

Follow the commands below to prepare the environment:
<div class="snippet-clipboard-content notranslate position-relative overflow-auto">
 <pre class="notranslate">
 <code> 
#
install.packages('TurtleGraphics') #comment out this line once the package has been installed
library(TurtleGraphics)
#
</code>
</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="# The repos argument is just to skip the repo selection.
# You can simply omit the argument if you want.
#
install.packages(c('abind', 'foreach', 'progress'), repos = 'http://cran.us.r-project.org')

devtools::install_github('Weiming-Hu/RAnEnExtra')" tabindex="0" role="button" style="display: inherit;">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
  
 <p dir="auto">Learn more about the package: <a href="https://cran.rstudio.com/web/packages/TurtleGraphics/index.html">TurtleGraphics</a></p>

<h3 tabindex="-1" dir="auto"><a id="user-content-install-dependency" class="anchor" aria-hidden="true" href="#install-dependency"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a>What is a Turtle?</h3>

<p align="center" dir="auto">
    <a target="_blank" rel="noopener noreferrer" href="https://github.com/harmansingh1412/Paper-Publishing-Template/blob/main/Images/turtle.jpg"><img src="https://github.com/harmansingh1412/Paper-Publishing-Template/blob/main/Images/turtle.jpg" width="90px" style="max-width: 100%;"></a>
</p>

Children are frequently introduced to programming through turtle graphics. It was a component of the first version of the **Logo programming language**, which was created in **1967** by Wally Feurzeig, Seymour Papert, and Cynthia Solomon. The TurtleGraphics package in R includes functions for turning the turtle by a certain angle and moving it forward or backward by a specified distance.
For example, the the **turtle_init()** function makes a plot area and positions the turtle facing north in the center of the terrarium. By default, turtle_init()'s size is 100 by 100 units. These size of the terrarium can be adjusted. One can also set the mode option to specify what occurs if the turtle moves outside the plot region.For example:

-**Clip:** This is the default setting indicates that the turtle may freely exit the board without being seen.

-**Error:** Prevents the turtle from leaving the terrarium and gives an error the turtle tried to leave.

-**Cycle:** If the turtle leaves the board it emerges on the other side of the board.

<h3 tabindex="-1" dir="auto"><a id="user-content-install-dependency" class="anchor" aria-hidden="true" href="#install-dependency"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a>How do I make the Turtle Move?</h3>

Below is a simple piece of code to make to make the turtle move. The numerical values specified in the fuctions tell the turtle what distance it needs to move in which direction.

<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>
turtle_init()
turtle_do({
  turtle_move(20)
  turtle_right(90)
  turtle_move(20)
  turtle_right(90)
  turtle_move(20)
  turtle_right(90)
  turtle_move(20)
  turtle_right(90)
})
</code></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="
turtle_init()
turtle_do({
  turtle_move(20)
  turtle_right(90)
  turtle_move(20)
  turtle_right(90)
  turtle_move(20)
  turtle_right(90)
  turtle_move(20)
  turtle_right(90)
})" tabindex="0" role="button" style="display: inherit;">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
 
 <p align="center" dir="auto">
    <a target="_blank" rel="noopener noreferrer" href="https://github.com/harmansingh1412/Paper-Publishing-Template/blob/main/Images/moving%20turtle.jpg
"><img src="https://github.com/harmansingh1412/Paper-Publishing-Template/blob/main/Images/moving%20turtle.jpg" width="150px" style="max-width: 500%;"></a>
</p>

Addtional functions that can specficy the turtle's movements:

-**turtle_forward** 

-**turtle_backward** 

-**turtle_up** 

-**turtle_down** 

  
<h3 tabindex="-1" dir="auto"><a id="user-content-install-dependency" class="anchor" aria-hidden="true" href="#install-dependency"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a>Turtle Art</h3>

<p dir="auto">To view a more complex drawing that experiments with lines and color see the <a href="https://github.com/harmansingh1412/Paper-Publishing-Template/blob/main/Turtle.Rmd">Turtle.Rmd</a></p>

<p align="center" dir="auto">
    <a target="_blank" rel="noopener noreferrer" href="https://github.com/harmansingh1412/Paper-Publishing-Template/blob/main/Images/turtle_image.jpg"><img src="https://github.com/harmansingh1412/Paper-Publishing-Template/blob/main/Images/turtle_image.jpg" width="500px" style="max-width: 500%;"></a>
</p>

<p dir="auto">To view an attempt to draw a forest using turtle graphics see <a href="https://github.com/harmansingh1412/Paper-Publishing-Template/blob/main/TurtleForest.Rmd">TurtleForest.Rmd</a></p>

<p align="center" dir="auto">
    <a target="_blank" rel="noopener noreferrer" href="https://github.com/harmansingh1412/Paper-Publishing-Template/blob/main/turtle_plot.png"><img src="https://github.com/harmansingh1412/Paper-Publishing-Template/blob/main/turtle_plot.png" width="800px" style="max-width: 500%;"></a>
</p>

## Development
<p dir="auto">See <a href="https://github.com/harmansingh1412/test/blob/main/DEVELOPMENT.md">DEVELOPMENT.md</a></p>

## Citation

## Contact

For any queries, please contact
Harman Singh 
(<a href=mailto:hxs5376@psu.edu>email</a>)
Department of Geography, 
Penn State Univeristy, U.S.A.
