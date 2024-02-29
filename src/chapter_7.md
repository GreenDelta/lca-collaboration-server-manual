<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 7-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 7-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h1 id="header-7">7.	Privacy </h1>
GreenDelta GmbH honours privacy and backs users in protecting confidential data. The LCA Collaboration Server is an independent application and decisions about where to host data as well as access to data are exclusively taken by its users. With the LCA Collaboration Server, users remain in full control of their data and commit to building their own sovereign IT-infrastructure for collaborative development of LCA studies in a distributed team.