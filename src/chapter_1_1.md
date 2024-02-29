<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 1-1-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 1-1-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h2 id="header-1-1">1.1     How can the LCA Collaboration Server be free?</h2>

The LCA Collaboration Server was developed by GreenDelta with support from the United States Department of Agriculture (USDA), creator of the LCA Digital Commons[^a]. Without support from the USDA, GreenDelta would not be able to offer the LCA Collaboration Server for free and GreenDelta regards this as a great chance to return a favour to the LCA community and support Life Cycle Thinking (LCT). Check-out conclusion and outlook on section 5 to see what we have in 
mind.

[^a]: <a href="https://www.lcacommons.gov/"> <u>https://www.lcacommons.gov/</u></a> 