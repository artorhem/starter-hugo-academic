---
widget: pages # As of v5.8-dev, 'pages' is renamed 'collection'
headless: true  # This file represents a page section.

# Put Your Section Options Here (title, background, etc.) ...
title: Research
subtitle: ''

# Position of this section on the page
weight: 20

content:
  # Filter content to display
  filters:
    # The folders to display content from
    folders:
      - post
    tag: ''
    category: ''
    publication_type: ''
    author: ''
    featured_only: false
    exclude_featured: false
    exclude_future: false
    exclude_past: false
  # Choose how many pages you would like to display (0 = all pages)
  count: 10
  # Choose how many pages you would like to offset by
  # Useful if you wish to show the first item in the Featured widget
  offset: 0
  # Field to sort by, such as Date or Title
  sort_by: 'Date'
  sort_ascending: false
design:
  # Choose a listing view
  view: compact
  # Choose how many columns the section has. Valid values: '1' or '2'.
  columns: '1'
---

My research is focussed on graph processing systems and graph data management. 
An incredible amount of data can be naturally expressed as graphs, 
and there is a growing need to develop efficient and scalable systems to process and manage such data.
Much research and industry effort has been spent on developing efficient systems for graph processing and graph storage individually, but rarely are they considered together. 
Most graph processing systems are either entirely in-memory or spend much time preprocessing the graph to make out-of-core processing feasible and efficient.
Either way, all systems are designed to be plugged into deep ETL pipelines that extract the graph from a primary source (usually a database) and prepare it for processing. 
Data once extracted become disjoint from the primary source, and any subsequent updates to the primary data source must initiate another round of ETL and preprocessing. 
Moreover, the results of the computation are often discarded and are not used in subsequent rounds of computation.

Ideally, the database used to store the primary data source would also allow fairly performant analytics along with all the rich feature one expects from an ACID compliant transactional store. Relational databases and their SQL interfaces make writing iterative graph algorithms very difficult, a situation often remedied by providing a graph DSL on top of the database (ex. Oracle PGX). Graph databases exist but have not managed to find widespread adoption and are instead relegated to specialized tasks such as fraud detection.

We take a more fundamental approach to tackle this incongruity: *why* do people not use graph databases? In order to answer this question, we take a ground-up approach to understand the relationship between the graph representation on disk, in memory, and how it impacts the performance of popular graph analytics tasks.
We have built a graph database that stores graphs in (currently) three different representations which support fast inserts and range queries to varying extents. This allows us to experiment with different representations, style of algorithm-writing (edge or vertex centric), and the statistical properties of the graph. A clear understanding of these together is essential in designing a system that performs well on both transactional and analytical workloads. 

