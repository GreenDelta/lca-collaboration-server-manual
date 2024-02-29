<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 6-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 6-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h1 id="header-6">6. Support and Contact</h1>

<h3>Sections</h3>

[6.1    Prioritised support via the GreenDelta HelpDesk](./chapter_6_1.md)

[6.2    Public support via ask.openLCA.org](./chapter_6_2.md)

[6.3    Demonstration of the LCA Collaboration Server](./chapter_6_3.md)

[6.4    Contact GreenDelta GmbH](./chapter_6_4.md)
