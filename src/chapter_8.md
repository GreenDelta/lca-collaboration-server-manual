<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 8-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 8-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h1 id="header-8">8. Appendix</h1>

<h3>Sections</h3>

[8.1    Known Issues](./chapter_8_1.md)

[8.2    Installation of the LCA Collaboration Server](./chapter_8_2.md)

[8.3    Configuration](./chapter_8_3.md)

[8.4    Hardware and Software requirements](./chapter_8_4.md)