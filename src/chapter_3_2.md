<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 3-1-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 3-1-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h2 id="header-3-2">3.2	Repositories - Create a new repository for your working group</h2>

Go to Repository  in the main menu. Click  <img src="images/chapter_3/section_2/plus.png" alt="Image not available" width="30" height="25"> to create or import a new repository. There are several ways to upload the database the user wants to work with to the repository in the Collaboration Server:

<ol>
    <li>Create new repository and commit the database from openLCA (section 3.4)</li>
    <li>Import JSON-LD file from a previously exported JSON-LD file from the desired database in openLCA.</li>
    <li>Import repository – this option imports a previously exported repository zip file (e.g. from another CS, or maybe a backup file)</li>
</ol>

It is very important that all of the users that will be using the repository have the same version of the database that is uploaded to the repository. Users can also create a new database in their openLCA and ‘pull’ the database in the repository.

When creating a repository, it is possible to limit the repository’s maximum size on the server (0 = unlimited). For more about the repository board, see [section 2.3.1](./chapter_2_3.md). 
