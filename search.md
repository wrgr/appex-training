---
layout: default
title: Search
---

<input type="text" id="search-input" placeholder="Search..." style="width:100%;padding:8px;"/>
<ul id="results-container"></ul>

<script src="https://cdnjs.cloudflare.com/ajax/libs/simple-jekyll-search/1.7.4/simple-jekyll-search.min.js"></script>
<script>
  SimpleJekyllSearch({
    searchInput: document.getElementById('search-input'),
    resultsContainer: document.getElementById('results-container'),
    json: '{{ '/search.json' | relative_url }}'
  });
</script>
