<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 3-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 3-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h1 id="header-3">3.  How-To: Basic Workflow</h1>

<h3>Sections</h3>

[3.1    The underlying workflow explained](./chapter_3_1.md)

[3.2    Repositories - Create a new repository for your working group](./chapter_3_2.md)

[3.3    How to connect and disconnect your local openLCA to the LCA Collaboration Server](./chapter_3_3.md)

[3.4    Adding data to the connected repository](./chapter_3_4.md)

[3.5    Getting data sets from the repository](./chapter_3_5.md)

[3.6    The workflow is always linear](./chapter_3_6.md)

[3.7    Conflicts](./chapter_3_7.md)

[3.8    Pitfalls](./chapter_3_8.md)

[3.9	Using the API to download a dataset as JSON](./chapter_3_9.md)

[3.10   Using git to update datasets programmatically](.chapter_3_10.md)
