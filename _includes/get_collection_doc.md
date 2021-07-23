<!--
Parameters:
- include.collection
- include.id
Return:
- doc
-->
{% include get_collection.md collection=include.collection %}
{% capture doc_id %}/{{include.collection}}/{{include.id}}{% endcapture %}
{% assign doc = collection.docs | where_exp: "doc", "doc.id == doc_id" | first %}
