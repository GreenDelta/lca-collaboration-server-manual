<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 4-1-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 4-1-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h2 id="header-4-1">4.1 Basic features</h2>

<h3 id="header-4-1-1">4.1.1 Commit history</h3>

A history of all commits is available in openLCA via right-click on a database <i>Repository > Show in history</i> (<a href="#Figure 4-2">Figure below</a>) and via the LCA Collaboration Server dashboard (<a href="#Figure 4-1">Figure below</a>).

<figure id="Figure 4-1">
	<img src="images/chapter_4/section_1/commits_in_the_LCA_Collaboration_Server_dashboard.png" alt="Image not available">
    <figcaption>History of commits in the LCA Collaboration Server dashboard</figcaption>
</figure>

<br>

<figure id="Figure 4-2">
	<img src="images/chapter_4/section_1/commits_in_openLCA.png" alt="Image not available">
    <figcaption>History of commits in openLCA</figcaption>
</figure>

<h3 id="header-4-1-2">4.1.2 Download of whole repositories or selected datasets</h3>

The download feature allows to download individual versions (commits) of a repository as <i>JSON-LD</i> or <i>ILCD</i> (<a href="#Figure 4-3">Figure below</a>) files. It is also possible to download individual datasets from the Collaboration Server.

<figure id="Figure 4-3">
	<img src="images/chapter_4/section_1/download_and_export.png" alt="Image not available">
    <figcaption>Download and export of data sets</figcaption>
</figure> 