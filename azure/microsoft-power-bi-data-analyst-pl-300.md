---
layout: editorial
---

# Microsoft Power BI Data Analyst (PL-300)

{% tabs %}
{% tab title="Introdction" %}
* **ANALYTICS**: descriptive / diagnostic / predictive / prescriptive / cognitive

| ANALYTICS              | DEFINITION                                                                                                                                                                                                                                               | APPLICATIONS                                                                                                                                                                                                                                                                                    |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| descriptive analytics  | what happened based on historical data                                                                                                                                                                                                                   | <ul><li>KPI(key performance indicators)</li><li>ROI(return on investment)</li><li>organization sales &#x26; financial data report</li></ul>                                                                                                                                                     |
| diagnostic analytics   | <p>why events happened </p><p>-> using findings from descAnlt</p>                                                                                                                                                                                        | <ol><li>Identify anomalies in the data. These anomalies might be unexpected changes in a metric or a particular market.</li><li>Collect data that's related to these anomalies.</li><li>Use statistical techniques to discover relationships and trends that explain these anomalies.</li></ol> |
| predictive analytics   | <p>what will happen in the future </p><p>-> use historical data to identify trends and determine weather they are likely to recur</p>                                                                                                                    | <ul><li>statistical </li><li>machine learning -> neural network / decision tree / regression</li></ul>                                                                                                                                                                                          |
| prescriptive analytics | <p>what actions should be taken to achieve a goal or target </p><p>-> data-driven decision</p>                                                                                                                                                           | <ul><li>machine learning  </li></ul>                                                                                                                                                                                                                                                            |
| cognitive analytics    | <p>draw inferences from existing data and patterns, derive conclusions based on existing knowledge bases, and then add these findings back into the knowledge base for future inferences, a self-learning feedback loop </p><p>-> data to knowledge </p> | <ul><li>machine learning </li></ul>                                                                                                                                                                                                                                                             |

****

* **ROLES**: **** BA / DA / DE / DS / Database Administrator

| ROLE                   | RESPONSIBILITY                                                                                                                                                                                                                                                                                                                              | WORK WITH                                                                                                                                                       |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Business Analyst       | interpreting the data from the visualization                                                                                                                                                                                                                                                                                                |                                                                                                                                                                 |
| Data Analyst           | <p>tuning raw data -> meaningful insights</p><ul><li>profiling, cleaning, and transforming data</li><li>designing and building scalable and effective data models</li><li>enabling and implementing the advanced analytics capabilities into reports</li><li>managing PowerBI (reports, dashboards, workspaces, datasets)</li></ul>         | <ul><li>pertinent stakeholder -> report requirement</li><li>data engineer -> data source collection and analysis</li><li>data administrator -> access</li></ul> |
| Data Engineer          | <ul><li>provision and set up data platform technologies that are on-premises and in the cloud</li><li>manage and secure the flow of data from many sources</li><li>data services seamlessly and securely integrate across data platforms</li><li>data wrangling -> ingesting, transforming, validating, cleaning</li></ul>                  | <ul><li>stakeholder</li><li>alignment with database administrator</li><li>database administrator / BI -> DE</li></ul>                                           |
| Data Scientist         | <ul><li>descAnlt -> EDA(exploratory data analysis)</li><li>predAnlt</li><li>data wrangling and feature engineering</li></ul><p></p>                                                                                                                                                                                                         |                                                                                                                                                                 |
| Databsae Administrator | <ul><li>manage the operation aspects of cloud-native and hybrid data platform solution (built in Azure data services, SQL server)</li><li>overall availability and consistent performance and optimizations of databases solutions</li><li>policies, tools, data backup and recovery plan</li><li>security, access and privileges</li></ul> | <ul><li>stakeholder</li></ul>                                                                                                                                   |

****

* **DATA ANALYSIS PROCESS**: prepare -> model -> visualize -> analyze -> manage  &#x20;

| PROCESS                                    |                                                                                                                                                                                                                                                                 |
| ------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| prepare: profiling, cleaning, transforming | <p>raw data -> trusted &#x26; understandable information</p><ul><li>integrity of data</li><li>converting data structure</li><li>making data more readable</li><li>how to connect data with decisions</li><li>privacy and security -> anonymizing data</li></ul> |
| model                                      | <ul><li>defining and creating relationship of tables</li><li>defining metrics and adding custom calculations</li><li>report more accurate / data explored faster &#x26; efficient / maintenance</li><li>critical / iterative </li></ul>                         |
| visualize                                  | <ul><li>report -> actions / decisions / behaviors of org</li><li>understand the problem -> filter data ->small and concise data story</li><li>AI / ML built in powerBI</li></ul>                                                                                |
| analyze                                    | <ul><li>interpreting information disolayed on report</li><li>find insights / identify patterns and trends / predict outcomes  </li><li>AI built in powerBI</li></ul>                                                                                            |
| manage                                     | <ul><li>managing components:  report / dashboard / workspace / dataset...</li><li>access control / reduce data silos / certify</li></ul>                                                                                                                        |



* **MICROSOFT POWER BI**: data visualization
  * **common flow**
    1. Bring data into Power BI Desktop, and create a report.
    2. Publish to the Power BI service, where you can create new visualizations or build dashboards.
    3. Share dashboards with others, especially people who are on the go.
    4. View and interact with shared dashboards and reports in Power BI Mobile apps.
  * **building blocks**&#x20;
    * _visualizations_ -> 图表
    * _datasets_ -> filtered / from different source/ connector&#x20;
    * _reports_ -> a collection of visualizations that appear together on one or more pages 动态
    * _dashboards_ -> a collection of visuals that you can share with others. Often, it's a selected group of visuals that provide quick insight into the data or story you're trying to present 静态
    * _tiles_ -> a single visualization on a dashboard
    * _app_ -> is a collection of preset, ready-made visuals and reports that are shared with an entire organization.
    * The _canvas_ -> the area in the center of the Power BI service -> show available sours of data: Microsoft Excel files, databases, or Microsoft Azure data, (software service ,SaaS)Salesforce, Facebook, Google Analytics, and more.
{% endtab %}

{% tab title="Prepare Data" %}
* **GET DATA FROM FILES**
* **source**

|                         |                                                   |                                                                                                                                                                                                                                                                                                                                                                                                               |
| ----------------------- | ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| flat file (.csv .xlsx)  | excel                                             | <p>source:</p><p>-- local -> data load into Power BI dataset / change on local file nor reflected</p><p>-- OneDrive for business -> synchronized</p><p>-- OneDrive - Personal -> synchronized</p><p>-- SharePoint - Team Sites -> synchronized / connect: specify a URL or connect to the root folder.</p>                                                                                                    |
| RDB                     | SQL Server                                        | <p>import: </p><p>-- import -> login windows / database / Microsoft account -> select data load / transform </p><p>-- advanced option -> SQL statement</p>                                                                                                                                                                                                                                                    |
| NoSQL DB                | more -> Azure Cosmos DB                           | <p>transform: </p><p>-- login -> select data -> edit </p><p>--select the <strong>Expander</strong> button to the right side of the <strong>Column1</strong> header, which will display the context menu with a list of fields. Select the fields that you want to load into Power BI Desktop, clear the <strong>Use original column name as prefix</strong> checkbox, and then select <strong>OK</strong></p> |
| online services         | more -> online services -> SharePoint Online List | you'll be asked for your SharePoint URL                                                                                                                                                                                                                                                                                                                                                                       |
| Azure Analysis Services |                                                   |                                                                                                                                                                                                                                                                                                                                                                                                               |

* **storage mode**
  * **import ->** create a local Power BI copy of your datasets from your data source / Data refreshes can be scheduled or on-demand
  * **DirectQuery ->** do not save local copies of your data / your data will not be cached / query the specific tables that you will need by using native Power BI queries / create direct connection to data source / always viewing most up-to-date data / use for security and large dataset
  * **Dual ->** you can identify some data to be directly imported and other data that must be queried / efficiency
{% endtab %}

{% tab title="Model Data" %}
## #ModelData
{% endtab %}

{% tab title="Visualize Data" %}
## #VisualizeData
{% endtab %}

{% tab title="Data Analysis" %}
## #DataAnalysis
{% endtab %}
{% endtabs %}

##
