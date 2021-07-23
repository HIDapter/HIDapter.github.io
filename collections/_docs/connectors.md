---
permalink: "/connectors/"
---

# Connectors

<table>
    <tr>
        <th>Connector</th>
        <th>Pins</th>
        <th>Width</th>
        <th>Height</th>
        <th>Used by</th>
    </tr>
    {% include get_collection_sorted_docs.md collection="connectors" %}
    {% for connector in sorted_docs %}
    <tr>
        <td><a href="{{ connector.url }}">{{ connector.title }}</a></td>
        <td>{{ connector.pins }}</td>
        <td>{{ connector.width }}</td>
        <td>{{ connector.height }}</td>
        <td>
            <ul>
                {% include get_collection_doc.md collection="protocols" id="db9" %}
                {% for protocol in protocols %}
                <li><a href="{{ protocol.url }}">{{ protocol.title }}</a></li>
                {% endfor %}
            </ul>
        </td>
    </tr>
    {% endfor %}
</table>
