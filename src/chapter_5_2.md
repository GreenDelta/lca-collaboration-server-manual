<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 5-2-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 5-2-" counter(tableCounter) ": ";
    }
  
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h2 id="header-5-2">5.2	The LCA Collaboration Server as a nexus for LCA data sets</h2>

Currently, LCA practitioners must download LCA data sets for openLCA via the web browser[^a] and import them into openLCA. This procedure is not too complicated, but the LCA Collaboration Server offers an opportunity to even further simplify the importing of LCA data sets into openLCA. In the long-term, GreenDelta would like to offer commercial and non-commercial LCA data sets directly via the LCA Collaboration Server.

[^a]: <a href="http://nexus.openlca.org/"> http://nexus.openlca.org/</a>
