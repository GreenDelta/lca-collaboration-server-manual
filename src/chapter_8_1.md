<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 8-1-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 8-1-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h1 id="header-8-1">8.1 Known issues </h1>

<h2 id="header-8-1-1">8.1.1	Redirected requests </h2>
OpenLCA currently does not support handling redirected requests (e.g. reverse proxy).

<h2 id="header-8-1-2">8.1.2	Fetching deleted data sets </h2>

Fetching deleted data sets that were not used in the local database of the user who commits but that are used in the local database of the user who fetches will lead to broken references e.g.
1.	<i>User A</i> deletes a flow that is not used in the user’s local database and commits the deletion to the LCA Collaboration Server
2.	<i>User B</i> added a new process in the user’s local database and uses the flow as input
3.	When <i>User B</i> then fetches the changes of <i>User A</i>, the flow is deleted locally, but the input in the process still refers to the (now) deleted flow

<p><b><i>Workaround:</b></i> If a user is aware that another user is going to fetch a deletion of a (locally) linked element, modify any field in the element in question (e.g. add a letter in the name and remove it again and save). OpenLCA will track that the model has changed. When fetching the <i>”deletion”</i> a conflict will come up and the user can manually choose to keep the local element. </p>

