<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 5-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 5-" counter(tableCounter) ": ";
    }
   
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<style>
   #shape {
    width: 350px;
    height: 70px;
    background: CornflowerBlue;
    border-radius: 5%;
    text-align: center;
    padding: 50px 20px 20px 20px;
    font-family: Arial;
    color: white;
   }
</style>

<h1 id="header-5"> 5. Conclusion and Outlook</h1>

The LCA Collaboration Server is an unprecedented software tool and likewise, offers unprecedented opportunities for LCA practitioners and the LCA community. We have two things in our mind and kindly ask for your support!

<h3>Sections</h3>

[5.1    Building a community of best practice - A public repository for LCA models](./chapter_5_1.md)

[5.2    The LCA Collaboration Server as a nexus for LCA data sets](./chapter_5_2.md)

