<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 2-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 2-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h1 id="header-2">2.  First steps</h1>

The LCA Collaboration Server (LCA CS) is an open-source tool that is available for free. Therefore, it can be downloaded, installed, and maintained by the user alone, see section 2.1. However, not all users have the IT infrastructure to host their own LCA Collaboration Server or do not want to bother with its installation and operation. For that case, GreenDelta also offers hosting solutions and support, see section 2.2.

This section also explains how to make the link between the openLCA in your machine and the LCA CS, the dashboard of the LCA CS, and the types of users and roles available for this tool.

<h3>Sections</h3>
 
[2.1    Install the LCA Collaboration Server on your server](./chapter_2_1.md)

[2.2    Hosting and further support](./chapter_2_2.md)

[2.3    Getting familiar with the LCA Collaboration Server dashboard](./chapter_2_3.md)

<!--
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[2.3.1 Expanding on the repository dashboard](#header-2-3-1)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[2.3.2 Expanding on the admin area dashboard](#header-2-3-2)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[2.3.3	Groups and user roles](#header-2-3-3)
>

