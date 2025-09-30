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
<br/>
<p>Default values for each setting can be specified programmatically before starting the application, see the list at the end of the page</p>

<h2 id="header-8-3-2">8.3.2	Enabled features </h2>
Some of the collaboration server’s advanced features can be disabled, including: Comments, Tasks, Messaging, Public repositories, Notifications, Activities and Tags (<a href="#Figure A-1">jump to figure above</a>).

<h2 id="header-8-3-3">8.3.3	Mail Configuration </h2>
To be able to use notifications, you need to configure an email account to send from. You can use an existing smpt email account (<a href="#Figure A-2">jump to figure above</a>).

<h2 id="header-8-3-4">8.3.4 List of settings for setting default values in application.properties </h2>
<p>The following settings can be set in WEB-INF/classes/application.properties after which a restart is required. They can afterwards still be changed in the UI</p>
cs.settings.default-values.SERVER_SETTING.MESSAGING_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.TASKS_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.COMMENTS_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.RELEASES_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.NOTIFICATIONS_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.USER_REGISTRATION_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.USER_REGISTRATION_APPROVAL_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.CHANGE_LOG_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.DASHBOARD_ACTIVITIES_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.REPOSITORY_ACTIVITIES_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.HOMEPAGE_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.SEARCH_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.USAGE_SEARCH_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.REPOSITORY_TAGS_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.DATASET_TAGS_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.DATASET_TAGS_ON_DASHBOARD_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.DATASET_TAGS_ON_GROUPS_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.DATASET_TAGS_ON_REPOSITORIES_ENABLED={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.DOCKER_INSTALLATION={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.SERVER_NAME={String}<br/>
cs.settings.default-values.SERVER_SETTING.SERVER_URL={String}<br/>
cs.settings.default-values.SERVER_SETTING.REPOSITORY_PATH={String}<br/>
cs.settings.default-values.SERVER_SETTING.LIBRARY_PATH={String}<br/>
cs.settings.default-values.SERVER_SETTING.GLAD_URL={String}<br/>
cs.settings.default-values.SERVER_SETTING.GLAD_API_KEY={String}<br/>
cs.settings.default-values.SERVER_SETTING.GLAD_DATAPROVIDER={String}<br/>
cs.settings.default-values.SERVER_SETTING.HOME_TITLE={String}<br/>
cs.settings.default-values.SERVER_SETTING.HOME_TEXT={String}<br/>
cs.settings.default-values.SERVER_SETTING.MAINTENANCE_MODE={Boolean}<br/>
cs.settings.default-values.SERVER_SETTING.MAINTENANCE_MESSAGE={String}<br/>
cs.settings.default-values.SERVER_SETTING.ANNOUNCEMENT_ID={String}<br/>
cs.settings.default-values.SERVER_SETTING.ANNOUNCEMENT_MESSAGE={String}<br/>
cs.settings.default-values.SERVER_SETTING.LICENSE_AGREEMENT_TEXT={String}<br/>
cs.settings.default-values.SEARCH_SETTING.SCHEMA={String}<br/>
cs.settings.default-values.SEARCH_SETTING.HOST={String}<br/>
cs.settings.default-values.SEARCH_SETTING.PORT={Integer}<br/>
cs.settings.default-values.SEARCH_INDEX.PRIVATE={String}<br/>
cs.settings.default-values.SEARCH_INDEX.PUBLIC={String}<br/>
cs.settings.default-values.SEARCH_INDEX.PRIVATE_USAGE={String}<br/>
cs.settings.default-values.SEARCH_INDEX.PUBLIC_USAGE={String}<br/>
cs.settings.default-values.MAIL_SETTING.USER={String}<br/>
cs.settings.default-values.MAIL_SETTING.PASS={String}<br/>
cs.settings.default-values.MAIL_SETTING.PROTO={String}<br/>
cs.settings.default-values.MAIL_SETTING.HOST={String}<br/>
cs.settings.default-values.MAIL_SETTING.PORT={Integer}<br/>
cs.settings.default-values.MAIL_SETTING.SSL={Boolean}<br/>
cs.settings.default-values.MAIL_SETTING.TLS={Boolean}<br/>
cs.settings.default-values.MAIL_SETTING.DEFAULT_FROM={String}<br/>
cs.settings.default-values.MAIL_SETTING.DEFAULT_REPLY_TO={String}<br/>
cs.settings.default-values.IMPRINT_SETTING.COMPANY={String}<br/>
cs.settings.default-values.IMPRINT_SETTING.CEO={String}<br/>
cs.settings.default-values.IMPRINT_SETTING.STREET={String}<br/>
cs.settings.default-values.IMPRINT_SETTING.ZIP_CODE={String}<br/>
cs.settings.default-values.IMPRINT_SETTING.CITY={String}<br/>
cs.settings.default-values.IMPRINT_SETTING.COUNTRY={String}<br/>
cs.settings.default-values.IMPRINT_SETTING.PHONE={String}<br/>
cs.settings.default-values.IMPRINT_SETTING.FAX={String}<br/>
cs.settings.default-values.IMPRINT_SETTING.EMAIL={String}<br/>
cs.settings.default-values.IMPRINT_SETTING.WEBSITE={String}<br/>
cs.settings.default-values.IMPRINT_SETTING.REGISTRATION={String}<br/>
cs.settings.default-values.IMPRINT_SETTING.VAT={String}<br/>
