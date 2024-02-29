<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 1-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 1-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<br>
<center>
<figure id="Figure 1">
	<img src="./images/chapter_1/lca_cs_logo.png" width="410" height="180" alt="Image not available">
</figure>
</center>


<h1>Introduction</h1>


With the general advancement of Life Cycle Assessment (LCA) and the spreading of Life Cycle Thinking (LCT), collaborative work on LCA studies becomes increasingly common e.g. within a company or team at the same location, within a company or team at different locations within multilateral projects (e.g. in research) on an international level and under participation of various entities such as companies, universities or consultancies as well as co-development of an LCA among executing contractors and clients. Moreover, it is becoming increasingly commonplace to use reference data for background processes, elementary flows, impact assessment methods, and other elements of existing LCA models. Often sharing of reference data for updating databases and distribution to users who are (also) distributed comes along with technical issues. In addition, quality assurance and review of LCA models through an external reviewer is of interest for anybody who wants to create a consistent LCA database.

The LCA Collaboration Server, now in version 2.0, is a server application that complements openLCA (the LCA desktop application). It is available for free, and support is available on demand.

Since version 1.7, openLCA accommodates full integration of the LCA Collaboration Server and facilitates the development of LCA studies in distributed teams. The LCA Collaboration Server is not only a milestone for openLCA but offers innovative features and opportunities for LCA practitioners that are unparalleled by any other LCA software.[^a] openLCA users are now able to work simultaneously on an LCA study while tracking each other’s changes along synchronised databases.

<h3>Sections</h3>

[1.1    How can the LCA Collaboration Server be free?](./chapter_1_1.md)

[1.2    What are use cases of the LCA Collaboration Server?](./chapter_1_2.md)


[^a]: Software solutions that offer a functionality close to that of the LCA Collaboration Server may be SimaPro’s multi-user feature from *PRé Sustainability and Soda4LCA from the Karlsruhe Institute of Technology*






