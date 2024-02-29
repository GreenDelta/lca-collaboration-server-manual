<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 6-4-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 6-4-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h2 id="header-6-4">6.4	Contact GreenDelta GmbH </h2>
For further inquiries please contact GreenDelta GmbH. <br>
Tel: +49 30 48 496 – 030 <br>
Fax: +49 30 48 496 – 991 <br>
<a href="mailto: gd@greendelta.com "> gd@greendelta.com</a> <br>
GreenDelta GmbH <br>
Kaiserdamm 13 <br>
14057 Berlin <br>
<a href="https://www.greendelta.com"> <u>www.greendelta.com</u></a>
