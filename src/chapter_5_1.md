<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 5-1-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 5-1-" counter(tableCounter) ": ";
    }
   
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<style>
   #shape {
    width: 550px;
    height: 40px;
    background: #00468b;
    border-radius: 25px;
    text-align: center;
    padding: 20px 20px 0px 20px;
    font-family: Arial;
    color: White;
   }
</style>

<h2 id="header-5-1">5.1 Building a community of best practice - A public repository for LCA models</h2>

We appreciate that, with the development of the LCA Collaboration Server, the USDA ([section 1.1](./chapter_1_1.md)) gave GreenDelta the opportunity not only to develop an unprecedented piece of Software but also to enhance the capabilities and reach of LCA practitioners worldwide. This is something we appreciate, and we hope that LCA Collaboration Server users do as well. We were wondering how we can contribute something to the LCA community to further promote the application of LCA and Life Cycle Thinking. What GreenDelta came up with is the vision of a public repository of freely available LCA models under the Creative Commons license.[^a]

Often, it is challenging for LCA beginners to develop their first complex LCA model and to our knowledge, no global database for free LCA models exists. GreenDelta wants to address this. Therefore, we encourage you to share your LCA model with us for use in a public open access repository. Users will be able to access the repository directly from openLCA and import existing LCA models for educational purposes.

<center>
<div id="shape">if this sounds interesting, please reach out: <a href="https://www.openlca.org/contact/" style="color:#FFFFFF;"> <u>https://www.openlca.org/contact/</u></a> </div>
</center>

[^a]: <a href="https://creativecommons.org/licenses/"> https://creativecommons.org/licenses/</a>
