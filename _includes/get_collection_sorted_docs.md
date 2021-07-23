<!--
Parameters:
- include.collection
Return:
- sorted_docs
-->
{% include get_collection.md collection=include.collection %}
{% assign sorted_docs = collection.docs | sort: 'title' %}
