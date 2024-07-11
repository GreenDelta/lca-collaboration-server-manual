<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 8-3-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 8-3-" counter(tableCounter) ": ";
    }
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h2 id="header-8-3">8.3	Configuration </h2>
We have prepared a configuration guide on openLCA.org - <a href="https://www.openlca.org/lca-collaboration-server-2-configuration-guide/"> Configuration Guide</a>. Also you can find some settings described below.

<p><b>Changing settings in the web application</b></p>

<figure id="Figure A-1">
	<img src="images/chapter_8/section_3/enabled_features.png" alt="Image not available">
    <figcaption>Admin area basic settings and enabled features</figcaption>
</figure>

<figure id="Figure A-2">
	<img src="images/chapter_8/section_3/mail_configuration.png" alt="Image not available">
    <figcaption>Admin area mail configuration and imprint</figcaption>
</figure>

<h2 id="header-8-3-1">8.3.1 Basic Settings </h2>
<br><b>Servername:</b> The Server name, used for two-factor-authentication (optional)</br> 
<br><b>Server base url:</b> The base url used when linking pages in the notification emails</br>
<br><b>Repositories root directory:</b> In this directory, the repository data sets will be stored, this will need extended disk space, depending on the amount of data sets committed.</br>
<br><b>Root directory for library id files:</b> In this directory, configured library data set ref ids will be stored</br>
<br><b>Glad service base url:</b> The base url to an external GLAD service</br>
<br><b>Glad service api key:</b> To push data set descriptors to the GLAD service, an API key is required, which can be set here.</br>
<br><b>Elasticsearch cluster:</b> The cluster name of your elasticsearch installation (default: elasticsearch)</br>
<br><b>Elasticsearch server url:</b> The host address of the elasticsearch installation (default: localhost)</br>
<br><b>Elasticsearch index name:</b> The name of the elasicsearch index used for this collaboration server instance (default: lca- collaboration)</br>

<h2 id="header-8-3-2">8.3.2	Enabled features </h2>
Some of the collaboration server’s advanced features can be disabled, including: Comments, Tasks, Messaging, Public repositories, Notifications, Activities and Tags (<a href="#Figure A-1">jump to figure above</a>).

<h2 id="header-8-3-3">8.3.3	Mail Configuration </h2>
To be able to use notifications, you need to configure an email account to send from. You can use an existing smpt email account (<a href="#Figure A-2">jump to figure above</a>).
