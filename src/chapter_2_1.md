<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 2-1-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 2-1-" counter(tableCounter) ": ";
    }
    
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h2 id="header-2-1">2.1     Install the LCA Collaboration Server on your server</h2>

With this option the user can use the LCA CS for free, and has to install and maintain it themselves. Here are the steps:

1.	  Download the LCA Collaboration Server from <https://www.openlca.org/download/>
2.    Install a local instance of the LCA Collaboration Server on your server 

      * [Hardware requirements](./chapter_8_4.md) for the LCA Collaboration Server
      *	Installation - follow: <https://www.openlca.org/lca-collaboration-server-2-installation-guide/>
