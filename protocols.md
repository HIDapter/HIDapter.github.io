---
title: Protocols
has_children: true
---
# Protocols

<table>
    <tr>
        <th>Protocol</th>
        <th>Connector</th>
        <th>Voltage</th>
    </tr>
    {% for protocol in site.protocols %}
    <tr>
        <td><a href="{{ protocol.url }}">{{ protocol.title }}</a></td>
        {% assign connector = site.collections.connectors[protocol.connector] %}
        <td><a href="{{ connector.url }}">{{ protocol.connector }} - {{ connector }} - {{ connector.title }}</a></td>
        <td>{{ protocol.voltage }}</td>
    </tr>
    {% endfor %}
</table>
