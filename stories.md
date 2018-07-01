---
layout: page
title: Stories
---

<div role="main" class="container">
  <div class="row">
    <div class="col-md-8 blog-main">
      <table class="table table-hover">
        <thead>
        </thead>
        <tbody>
        {% for post in site.posts %}
          <tr>
           <td></td>
           <td class="light">{{ post.date | date: "%b %d, %Y" }} </td>
           <td class="title"><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></td>
          </tr>
        {% endfor %}
        </tbody>
      </table>
    </div>

    <aside class="col-md-4 blog-sidebar">
      <p class="light">Interviews and stories of local heroes of cats - vets, activists, volunteers etc.
        For suggestions, please write to <a href='mailto:rohit@yadav.cloud'>rohit@yadav.cloud</a>.
      </p>
      <h4>Categories</h4>
      {% for category in site.categories %}
          {% capture category_name %}{{ category | first }}{% endcapture %}
          <a href="categories#{{ category | first | slugize }}">
              {{ category | first }}
          </a> ({{ site.categories[category_name] | size }})<br/>
      {% endfor %}
    </aside>
  </div>
</div>

Questions spec: (under change/review)
- Photo of person and interview tags?
- Who are you, and what do you do?
- Are you owned by any pet cats?
- Your thoughts about adopting vs buying?
- Any advise or thoughts for the readers?
- What would be your dream cat?
- How should people reach you?

