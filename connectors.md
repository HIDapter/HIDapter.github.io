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
        <td><a href="{{ connector.url }}">{{ connector.name }}</a></td>
        <td>{{ connector.pins }}</td>
        <td>{{ connector.width }} x {{ connector.height }}</td>
        <td>
            <ul>
                {{% assign protocols = site.collections.protocols | where_exp:"protocol", "protocol.connector == connector.name" %}}
                {% for protocol in protocols %}
                <li><a href="{{ protocol.url }}">{{ protocol.name }}</a></li>
                {% endfor %}
            </ul>
        </td>
    </tr>
    {% endfor %}
</table>
