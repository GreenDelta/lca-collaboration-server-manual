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

<h2>Using the API to download a dataset as JSON</h2>

If you want to access datasets that are not released, you need to call the login API to optain the value of the JSESSIONID cookie from the response header and add it as a cookie to each subsequent call. You can omit this step if you are trying to access a publicly available dataset:

```
curl -s -i -X POST https://example-url.com/ws/public/login \
        -H 'Content-Type: application/json' \
        -d '{"username":"your_username","password":"your_password"}'
```

Next you can call the browse API to obtain the JSON of a specific dataset, the url is constructed using the repository group, repository name, the type of dataset and the refId: /ws/public/browse/{group}/{repo}/{modelType}/{refId}, e.g.:

```
curl -s -X GET https://example-url.com/ws/public/browse/group/repo/PROCESS/ab12dfa3-3297-9360-999a-33d166fed26a \
        --cookie "JSESSIONID=43E4CFD98E627C4C189C40D4B4FAE2C6"
```

If instead you want to obtain a package ready to import into openLCA, containing the dataset and including references, you can call the download API to prepare a package, the url is: /ws/public/download/json/prepare/{group}/{repo}/{modelType}/{refId}, it will return a token with which you need to call the download url /ws/public/download/{token}

```
curl -s -X GET https://example-url.com/ws/public/download/json/prepare/group/repo/PROCESS/ab12dfa3-3297-9360-999a-33d166fed26a \
        --cookie "JSESSIONID=43E4CFD98E627C4C189C40D4B4FAE2C6"

curl -s -X GET https://example-url.com/ws/public/download/json/ba51eac4-1569-3345-112b-a417aadef1b3 \
        --output ab12dfa3-3297-9360-999a-33d166fed26a.zip \
        --cookie "JSESSIONID=43E4CFD98E627C4C189C40D4B4FAE2C6"
```

To terminate the session, you can call the logout endpoint:
```
curl -s -X POST https://example-url.com/ws/public/logout \
        --cookie "JSESSIONID=43E4CFD98E627C4C189C40D4B4FAE2C6"

