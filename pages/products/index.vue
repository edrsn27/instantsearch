<template>
  <div class="container-fluid">
    <ais-instant-search :search-client="searchClient" index-name="products">
      <div class="row">
        <div class="col-3">
          <h6>Category</h6>
          <ais-refinement-list attribute="category.name" />
          <h6>Manufacturer</h6>
          <ais-refinement-list attribute="manufacturer" />
          <h6>Model</h6>
          <ais-refinement-list attribute="model" />
          <h6>Type</h6>
          <ais-refinement-list attribute="type" />
        </div>
        <div class="col-9">
          <ais-search-box />
          <br />
          <ais-hits>
            <template slot="item" slot-scope="{ item }">
              <h3><ais-highlight :hit="item" attribute="name" /></h3>

              <img
                height="100"
                width="150"
                :src="item.image"
                class="rounded float-left"
                alt="..."
              />
              <!-- <img src="..." class="rounded float-right" alt="..."> -->
            </template>
          </ais-hits>
          <ais-pagination />
        </div>
      </div>
    </ais-instant-search>
  </div>
</template>

<script>
import algoliasearch from "algoliasearch/lite";

export default {
  data() {
    return {
      searchClient: algoliasearch(
        process.env.ALGOLIA_APP_ID,
        process.env.ALGOLIA_API_KEY
      ),
      currentRefinement: ""
    };
  },
  head() {
    return {
      link: [
        {
          rel: "stylesheet",
          href:
            "https://unpkg.com/instantsearch.css@7.1.0/themes/algolia-min.css"
        }
      ]
    };
  }
};
</script>
