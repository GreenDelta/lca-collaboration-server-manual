<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 4-3-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 4-3-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h2 id="header-4-3">4.3	Expert features</h2>

<h3 id="header-4-3-1">4.3.1	Additional roles</h3>

Additional roles are that of the Data Manager and User Manager. Both can be assigned as such by the Server Administrator.

- Data Manager – A data manger can manage libraries and push data to GLAD[^a]
- User Manager – A user manager can manage users and teams

**Restricted data sets**

These  are protected data sets that require an additional confirmation to commit changes.

**Create users**

Users can be created by accessing the admin area via clicking on the wrench in the top-right corner of the LCA Collaboration Server dashboard.

**Teams**

Individual users can be combined into a team and teams can be added to groups (of repositories). Teams consist of users, and groups contain repositories.  Teams can be added to a repository. Teams are created by accessing the admin area via clicking on the wrench in the top-right corner of the LCA Collaboration Server dashboard (<a href="#Figure 4-11">Figure below</a>).[^b] 

<figure id="Figure 4-11">
	<img src="images/chapter_4/section_3/teams_are_created.png" alt="Image not available">
    <figcaption>Teams are created by accessing the admin area via clicking on the wrench in the top-right corner of the LCA Collaboration Server dashboard</figcaption>
</figure>

[^a]: Global LCA Data Access network (<a href="https://www.unep.org/explore-topics/resource-efficiency/what-we-do/life-cycle-initiative/global-lca-data-access-network"> <u>http://unep-glad.71.ecedi.fr/</u></a>). Feature developed for the USDA.  

[^b]: Please note that only admins can create teams
