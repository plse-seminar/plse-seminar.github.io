---
layout: default
---

<table>
 <tr>
   <th class="date">Date</th>
   <th class="title">Seminar</th>
   <th class="presenter">Presenter</th>
 </tr>
 {% assign talks = site.data.talks | sort: 'date' | reverse %}
 {% for talk in talks %}
<tr>
  <td>{{ talk.date | date: "%b %d, %Y" }}</td>
  <td>
    <details>
      <summary><a>{{ talk.title }}</a></summary>
      {{ talk.abstract }}
    </details>
  </td>
  <td>{{ talk.presenter }}</td>
</tr>
{% endfor %}
</table>
