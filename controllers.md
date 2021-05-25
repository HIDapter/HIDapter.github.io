# Controllers

<table>
    <tr>
        <th>Controller</th>
        <th>Connector pins</th>
        <th>Connector size</th>
    </tr>
{% for controller in site.controllers %}
    <tr>
    <td><a href="{{ controller.url }}">{{ controller.name }}</a></td>
    <td>{{ controller.connector.pins }}</td>
    <td>{{ controller.connector.width }} x {{ controller.connector.height }}</td>
    <!-- <p>{{ controller.content | markdownify }}</p> -->
    </tr>
{% endfor %}
</table>
