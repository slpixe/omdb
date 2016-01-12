---
artist:  "Ellie Goulding"
works:
  - title: "Missa De beata virgine"
    composer: "Josquin des Prez"
    tracks:
      - title: "Kyrie"
        duration: "4:25"
      - title: "Gloria"
        duration: "9:53"
      - title: "Credo"
        duration: "9:09"
      - title: "Sanctus &amp; Benedictus"
        duration: "7:47"
      - title: "Agnus Dei I, II &amp; III"
        duration: "6:49"
---

#HELOOOO

{% for artist in site.artists %}
  <h2>{{ artist.title }}</h2>
  {% for work in artist.works %}
    <h3>{{ work.title }}</h3>
    <p>Composed by {{ work.composer }}</p>
    <ul>
    {% for track in work.tracks %}
      <li>{{ track.title }} ({{ track.duration }})</li>
    {% endfor %}
    </ul>
  {% endfor %}
{% endfor %}