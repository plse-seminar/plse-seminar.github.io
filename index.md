---
layout: default
---
<table>
 <tr>
   <th class="date">Date</th>
   <th class="title">Seminar</th>
   <th class="presenter">Presenter</th>
 </tr>
{% assign posts = site.posts | where: 'group',"seminars" | sort:'weight', 'last' %}
{% for post in posts %}
<tr>
  <td>{{ post.date | date: "%b %d, %Y" }}</td>
  <td>
    <details>
      <summary><a>{{ post.title }}</a></summary>
      {{ post.content }}
    </details>
  </td>
  <td>{{ post.presenter }}</td>
</tr>
{% endfor %}
</table>
