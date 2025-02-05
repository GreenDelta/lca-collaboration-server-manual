<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 3-7-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 3-7-" counter(tableCounter) ": ";
    }

    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h2>Using git to update datasets programmatically</h2>

If you want to programmatically update datasets, we recommend to use git in command line to clone the repository, checkout the main branch, make changes to the datasets and then commit and push changes back to the CS via the usual git commands.

The openLCA git repositories are using the following structure:

* Categories as Directories
* JSON-LD files as Type/Category/RefId.json
* Bin file as Type/Category/RefId_bin/file
* Empty categories as Type/Category/.empty
* openlca.json file

The root of the repositories contains the "openlca.json" file, which contains the following information:

```
{
	schemaVersion: int, // The openLCA JSON-LD schema version used in this repository
	libraries: { id: string, url: string }[], // A list of libraries linked in this repository, with an optional url where they can be downloaded
	repositoryClientVersion: int, // A client version the repository is compatible with; it is used to check feature compatibility 
	repositoryServerVersion: int // A server version the repository is compatible with; it is used to check feature compatibility 
}
```

Example:

```
{ schemaVersion: 5, libraries: [], repositoryClientVersion: 6, repositoryServerVersion: 5 }
```

Each dataset committed to the repository will be converted into the openLCA JSON-LD format (https://greendelta.github.io/olca-schema/) and stored in the git repository. The ModelType is used as root directory, followed by the category and the refId as filename, with .json as file extension.
For example the Actor dataset with the ref_id '3e339f63-ae9e-5223-82b4-3c2acc029c64' in the category 'GreenDelta GmbH/Employees' will be stored as:

```
ACTOR/GreenDelta GmbH/Employees/3e339f63-ae9e-5223-82b4-3c2acc029c64.json
```

Some model types allow binary files to be linked, e.g. a Source dataset with the ref_id '6e339f63-ae9e-5223-82b4-3c2acc029c64' in the category 'Publications' might link a document 'document.pdf'. It will be stored the following way:

```
SOURCE/Publications/6e339f63-ae9e-5223-82b4-3c2acc029c64.json
SOURCE/Publications/6e339f63-ae9e-5223-82b4-3c2acc029c64_bin/document.pdf
```

To support committing empty categories an empty file ".empty" will be placed in an empty category:

```
FLOW/Elementary flows/Emissions to air/.empty
```
