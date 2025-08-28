---
layout: page
title: Guestbook
permalink: /
---

## Guestbook

Have something to say? Leave a message in the guestbook!

<form method="POST" action="https://staticman-2ih4.onrender.com/v2/entry/Stetoskop/mikiver.com/main/guestbook">
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