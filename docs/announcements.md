---
title: 📢 Announcements
layout: default
nav_order: 1
---

# Announcements

These are the latest announcements for Hack-A-Bot 2025.

---

{% assign sorted_announcements = site.announcements | sort: "date" | reverse %}
{% for post in sorted_announcements %}

{% assign post_day = post.date | date: "%-d" %}

<div style="display: flex; justify-content: space-between; align-items: center; margin-top: 0.25em;">
  <h3 style="margin: 0;">
    {% if post_day == "29" %}
      Day 1 — {{ post.date | date: "%A, %B %-d at %-I:%M %p" }}
    {% elsif post_day == "30" %}
      Day 2 — {{ post.date | date: "%A, %B %-d at %-I:%M %p" }}
    {% else %}
      {{ post.date | date: "%A, %B %-d at %-I:%M %p" }}
    {% endif %}
  </h3>
  <span style="font-size: 1em;">📌</span>
</div>

<h4 style="margin-bottom: 0.2em;">
  {{ post.title }}<br/>
  By: {{ post.author }}
</h4>

{{ post.content }}

---

{% endfor %}