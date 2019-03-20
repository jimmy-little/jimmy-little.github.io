---
layout: page
title: 🔍 Search
permalink: /search/
date: 2019-03-20
---

    
<div id="search-container" test-align="cetner">
<input type="text" id="search-input" placeholder="search...">
<ul id="results-container"></ul>
</div>

<script src="{{ site.baseurl }}/assets/scripts/simple-jekyll-search.js"></script>

<script>
window.simpleJekyllSearch = new SimpleJekyllSearch({
searchInput: document.getElementById('search-input'),
resultsContainer: document.getElementById('results-container'),
json: '{{ site.baseurl }}/search/search.json',
searchResultTemplate: '<li><a href="{url}?query={query}" title="{desc}">{title}</a></li>',
noResultsText: 'No results found',
limit: 10,
fuzzy: false,
})
</script>

<!--
<iframe src="https://duckduckgo.com/search.html?width=280&site=cocktailsandcoffee.com&prefill=Search&bgcolor=#a0a0a0&focus=yes&kl=us-en&kav=1&kac=1&kae=d&km=m" style="overflow:hidden;margin:0;padding:0;width:458px;height:40px;" frameborder="0"></iframe>
<p align= "center">
Duck Duck Go is a private search engine that isn't creepy. 
Searching here will only search Cocktails and Coffee and help you find what you're looking for.
</p> 
-->
