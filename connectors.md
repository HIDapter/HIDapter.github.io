# Connectors

<table>
    <tr>
        <th>Connector</th>
        <th>Pins</th>
        <th>Size</th>
        <th>Used by</th>
    </tr>
{% for controller in site.controllers %}
    <tr>
        <td><a href="{{ controller.url }}">{{ controller.name }}</a></td>
        <td>{{ controller.connector.pins }}</td>
        <td>{{ controller.connector.width }} x {{ controller.connector.height }}</td>
        <td></td>
        <!-- <p>{{ controller.content | markdownify }}</p> -->
    </tr>
{% endfor %}
</table>
