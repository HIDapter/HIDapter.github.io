# Controllers

{% for controller in site.controllers %}
    <a href="{{ controller.url }}">
        <h2>{{ controller.name }}</h2>
    </a>
    <p>{{ controller.connector.width }} x {{ controller.connector.height }}, {{ controller.connector.pins }} pins</p>
    <p>{{ controller.content | markdownify }}</p>
{% endfor %}
