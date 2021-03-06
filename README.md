### What is it? ###
Some Pipeline Steps and Endpoints for Sitecore Data Exchange Framework.

### What does it do? ###

Dual Purpose:
- It's a demo project hopefully illustrating how to setup your own custom DEF Pipelines, Endpoints, and Pipeline Steps
- It's a working proof of concept project that takes an External data feed (in this case RSS) and, using the `BaseIndexable` class, writes the external feed to an index for later consumption

### What do I need for it? ###

- Sitecore
- Sitecore DEF: https://dev.sitecore.net/Downloads/Data_Exchange_Framework.aspx
- The package (in `Sitecore Packages`).  Has been tested on 8.1, 8.2, and should work on 9 (given the correct DEF installs)


### What do I need if for? ###

- The example in the project uses a RSS feed for an example external datasource, but a real-world use case would be pulling in job details form an external job application service such as Kenexa
- The idea behind the `Index Endpoint` is to bring in a mostly-read-only datastore without bringing it in to the content tree.  Using an index in this fashion allows you to still use the `ContentSearch` api

### How do I use it ###
Should be as easy as:

1. Install the package in `Sitecore Packages`  _OR_

1. Clone, download, whatever, just get these files to your computer

1. Bring the source code into your project

1. Install the package to _at least_ get the Items.

1. Run the Pipeline Batch at `/sitecore/system/Data Exchange/DEFIndexer/Pipeline Batches/Process RSS Pipeline` 

Screenshot: 

The Pipeline Batch

![alt text](https://github.com/vandsh/sitecore-defindexer/raw/master/defScreenshot1.png "The Pipeline Batch")

The Tags pulled in from the RSS feed

![alt text](https://github.com/vandsh/sitecore-defindexer/raw/master/defScreenshot2.png "The Associated Tags")