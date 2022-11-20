---
title: 'Smooth Kronecker: Solving the Combing Problem in Kronecker Graphs'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Vaastav Anand
  - admin
  - Daniel Margo
  - Margo Seltzer

# Author notes (optional)
author_notes:
  - 'Equal contribution'
  - 'Equal contribution'

date: '2020-07-06T18:07:29-07:00'
doi: "https://doi.org/10.1145/3398682.3399161"

# Schedule page publish date (NOT publication's date).
publishDate: '2017-01-01T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['1']

# Publication name and optional abbreviated publication name.
publication: 
publication_short: 

abstract: Graphs and graph-processing have become increasingly important. This has led to an explosion in the development of graph-processing systems, each of which is evaluated relative to its predecessors. In the absence of a large corpus of real-world graphs, synthetic generators provide an easy way to construct graphs of varying sizes. The most widely used generator is the Kronecker generator. Unfortunately, the Kronecker generator was not designed to produce graphs for benchmarking and when used in this fashion, it is problematic in two ways. First, the fraction of zero-degree vertices scales with the graph size, dramatically reducing the effective size of the connected graph. Second, the generator produces a vertex degree distribution not found in real world settings. We demonstrate these phenomena and present the Smooth Kronecker Generator, which remedies the vertex degree distribution problem without changing the statistical properties of the graph

# Summary. An optional shortened abstract.
summary: Fixing the combed degree distribution in Kronecker graphs

tags: [graph generators, kronecker, benchmarking, graph]

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: ''
url_code: 'https://github.com/dmargo/smooth_kron_gen'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: 'GRADES-SmoothKronecker.pdf'
url_source: ''
url_video: 'https://www.youtube.com/watch?v=5G75VpX9pZs'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
  focal_point: ''
  preview_only: false


# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---