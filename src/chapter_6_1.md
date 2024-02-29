<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 6-1-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 6-1-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h2 id="header-6-1">6.1	Prioritised support via the GreenDelta HelpDesk </h2>

For more information about GreenDelta’s support services for openLCA and the LCA Collaboration Server, please refer to: <https://www.openlca.org/helpdesk/>. 
<br>

Support services include:
*	 Hosting of an LCA Collaboration Server (<http://www.openlca.org/lca-collaboration-server-hosting-andservices/>)
*    Support in setting up an LCA Collaboration Server (<a href="https://www.openlca.org/contact/">contact us</a>)
*    Professional training on how to get the best out of the LCA Collaboration Server for your organisation (<a href="https://www.openlca.org/contact/">contact us</a>)