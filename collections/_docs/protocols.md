---
permalink: "/protocols/"
---

# Protocols

<table>
    <tr>
        <th>Protocol</th>
        <th>Connector</th>
        <th>Voltage</th>
    </tr>
    {% include get_collection_sorted_docs.md collection="protocols" %}
    {% for protocol in sorted_docs %}
    <tr>
        <td><a href="{{ protocol.url }}">{{ protocol.title }}</a></td>
        {% include get_collection_doc.md collection="connectors" id=protocol.connector %}
        {% assign connector = doc %}
        <td>
        {% if connector %}
            <a href="{{ connector.url }}">{{ connector.title }}</a>
        {% endif %}
        </td>
        <td>{{ protocol.voltage }}</td>
    </tr>
    {% endfor %}
</table>
