<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 6-3-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 6-3-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h2 id="header-6-3">6.3	Demonstration of the LCA Collaboration Server </h2>
Demonstration videos of the LCA Collaboration Server are available on the openLCA YouTube channel: 
<a href="https://www.youtube.com/c/openLCA"> https://www.youtube.com/c/openLCA </a>. The video below introduces the previous version of the collaboration server. Some aspects of the workflow have changed, but many features are still as shown in the video. 

[![](https://i.ytimg.com/vi/fMQb_D5eU8M/maxresdefault.jpg)](https://www.youtube.com/watch?v=fMQb_D5eU8M&t=2s)

<center>
<h4>click on the image above to access the livestream video recording</h4>
</center>