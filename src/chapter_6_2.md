<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 6-2-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 6-2-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h2 id="header-6-2">6.2	Public support via ask.openLCA.org </h2>

<a href="https://ask.openlca.org" style="color: #000000;">Ask.openlca.org</a> is a question-and-answer (Q&A) website on Life Cycle Assessment and the support platform for openLCA, openLCA nexus and the LCA Collaboration Server. We encourage users to use <a href="https://ask.openlca.org"><u>ask.openlca.org</u></a> for non-confidential support requests. However, with <a href="https://ask.openlca.org" style="color: #000000;">ask.openlca.org</a> we are building a public knowledge platform for all LCA practitioners regardless of what software they use or LCA-related questions they may have. Contact us via email for confidential support requests or resort to one of GreenDelta’s <a href="https://www.openlca.org/helpdesk"> <u>service contracts</u></a> for prioritised support via the GreenDelta HelpDesk.