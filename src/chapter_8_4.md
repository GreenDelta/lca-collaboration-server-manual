<style>
    /* initialise the counter */
    body { counter-reset: figureCounter;
    counter-reset: h1counter h2counter h3counter h4counter h5counter h6counter;
     }
    /* increment the counter for every instance of a figure even if it doesn't have a caption */
    figure { counter-increment: figureCounter; text-align: center}
    /* prepend the counter to the figcaption content */
    figure figcaption:before {
        content: "Figure 8-4-" counter(figureCounter) ": "
    }
    /* increment the counter for every instance of a table even if it doesn't have a caption */
    table { counter-increment: tableCounter; }
    /* prepend the counter to the figcaption content */
    caption:before {
        content: "Table 8-4-" counter(tableCounter) ": ";
    }
    
    /* create padding between table cells*/
    th, td {
        padding: 15px;
    }
</style>

<h2 id="header-8-4">8.4	Hardware and Software requirements </h2>

<h2 id="header-8-4-1">8.4.1	Requirements for openLCA </h2>

* Windows / macOS / Linux
    * 1 GB RAM (for analysing product systems with 2,500 processes, such as ecoinvent 2)
    * &gt;3 GB RAM (for analysing product systems such as ecoinvent 3)
    * 6 GB RAM (for analysing product systems such as ecoinvent 3.4 or Psilca for social LCA)
    * 500 MB free hard disk space + space for databases (e.g. ecoinvent 3 requires 250MB)

<h2 id="header-8-4-2">8.4.2	Requirements for the LCA Collaboration Server </h2>
<br><b>Minimum:</b></br>
<br>CPU: DualCore CPU or better </br>
<br>RAM (Elasticsearch/LCA CS): 2GB/2GB </br>
<br>Disk: HDD (the required disk space depends mostly on the amount of data you want to be able to host; the application itself only requires &lt;100MB) Recommended: </br>
<br>CPU: QuadCore CPU or better</br>
<br>RAM (Elasticsearch/LCA CS): 4GB/8GB</br>
<br>Disk: SSD4</br>

<b>Software requirements:</b></br>
<br>The LCA Collaboration Server is a web application based on Java Servlet. We recommend the use of Tomcat 8 in combination with Java 8. Most testing has been done under use of this configuration (for both Windows 10 and Ubuntu/Debian Linux).</br>
<br>The LCA Collaboration Server depends on Elasticsearch. Since version 6 it does not support JVM internal local nodes. Therefore, Elasticsearch must be installed and run separately.</br>