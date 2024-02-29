<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 4-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 4-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h1 id="header-4">4. Features</h1>

<h3>Sections</h3>

[4.1    Basic features](./chapter_4_1.md)

[4.2    Advanced features](./chapter_4_2.md)

[4.3    Expert features](./chapter_4_3.md)
