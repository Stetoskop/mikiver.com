---
layout: page
title: Guestbook
permalink: /
---

## Guestbook

Have something to say? Leave a message in the guestbook!
CURRENTLY W.I.P, WILL NOT WORK!

<form method="POST" action="https://staticman-stetoskops-projects.vercel.app/v3/entry/github/Stetoskop/mikiver.com/main/guestbook">
  <input name="fields[name]" type="text" placeholder="Your name" required>
  <textarea name="fields[message]" placeholder="Your message" required></textarea>
  <button type="submit">Submit</button>
</form>

---

### Entries

{% for entry in site.data.guestbook %}
  <div>
    <p><strong>{{ entry.name }}</strong> said:</p>
    <p>{{ entry.message }}</p>
    <p><small>{{ entry.date | date_to_string }}</small></p>
  </div>
  <hr>
{% endfor %}