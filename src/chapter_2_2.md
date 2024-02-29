<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 2-2-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 2-2-" counter(tableCounter) ": ";
    }
    
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h2 id="header-2-2">2.2 Hosting and further support</h2>

If the user wants to start using the tool directly without having to install or maintain it, GreenDelta can host the user’s server. The hosting plans are described in this <a href="#Figure 2-1">figure</a>, and it can be purchased in openLCA Nexus: <https://nexus.openlca.org/service/LCA%20Collaboration%20Server%20Hosting>.

For users and administrators of the LCA Collaboration Server who wish to receive guaranteed and prioritised professional support in handling their LCA Collaboration Server, GreenDelta offers paid support via the GreenDelta HelpDesk: <https://nexus.openlca.org/service/openLCA%20Support%20(help%20desk)>. Public user-to-user support is available via <https://ask.openlca.org/>.

<figure id="Figure 2-1">
	<img src="images/chapter_2/section_2/options_offered.png" alt="Image not available">
	<figcaption>Hosting options offered for the LCA Collaboration Server <nobr style="font-size: 12px"> 1  </nobr> </figcaption>
</figure>


[^a]: <a href="https://www.openlca.org/wp-content/uploads/2019/11/GreenDelta___Hosting_and_Services.pdf"> <u>https://www.openlca.org/wp-content/uploads/2019/11/GreenDelta___Hosting_and_Services.pdf</u></a> 
