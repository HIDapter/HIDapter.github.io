# Connectors

<table>
    <tr>
        <th>Connector</th>
        <th>Pins</th>
        <th>Size</th>
        <th>Used by</th>
    </tr>
{% for connector in site.connectors %}
    <tr>
        <td><a href="{{ controller.url }}">{{ connector.name }}</a></td>
        <td>{{ connector.pins }}</td>
        <td>{{ connector.width }} x {{ connector.height }}</td>
        <td></td>
        <!-- <p>{{ connector.content | markdownify }}</p> -->
    </tr>
{% endfor %}
</table>
