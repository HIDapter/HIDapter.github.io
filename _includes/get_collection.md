<!--
Parameters:
- include.collection
Return:
- collection
-->
{% assign collection = site.collections | where_exp: "collection", "collection.label == include.collection" | first %}
