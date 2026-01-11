---
layout: default
title: 文章归档
permalink: /archive
---

<div class="archive-page">
  <h1>文章归档</h1>
  <p>按时间顺序查看所有文章</p>
  
  {% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}
  
  {% for year in posts_by_year %}
  <div class="archive-year">
    <h2>{{ year.name }}年</h2>
    <ul class="archive-list">
      {% for post in year.items %}
      <li class="archive-item">
        <time datetime="{{ post.date | date: '%Y-%m-%d' }}" class="archive-date">
          {{ post.date | date: "%m月%d日" }}
        </time>
        <a href="{{ site.baseurl }}{{ post.url }}" class="archive-title">
          {{ post.title }}
        </a>
      </li>
      {% endfor %}
    </ul>
  </div>
  {% endfor %}
</div>

<style>
.archive-page {
  max-width: 700px;
  margin: 0 auto;
}

.archive-page > h1 {
  font-size: 2.5rem;
  margin-bottom: 0.5rem;
}

.archive-page > p {
  color: var(--text-light);
  margin-bottom: 3rem;
}

.archive-year {
  margin-bottom: 3rem;
}

.archive-year h2 {
  font-size: 1.8rem;
  margin-bottom: 1rem;
  color: var(--text-color);
  border-bottom: 2px solid var(--border-color);
  padding-bottom: 0.5rem;
}

.archive-list {
  list-style: none;
  padding-left: 0;
}

.archive-item {
  display: flex;
  gap: 1.5rem;
  padding: 0.75rem 0;
  border-bottom: 1px solid var(--border-color);
  align-items: baseline;
}

.archive-item:last-child {
  border-bottom: none;
}

.archive-date {
  color: var(--text-light);
  font-size: 0.9rem;
  white-space: nowrap;
  min-width: 80px;
}

.archive-title {
  color: var(--text-color);
  text-decoration: none;
  flex: 1;
  transition: color 0.3s ease;
}

.archive-title:hover {
  color: var(--primary-color);
}

@media (max-width: 768px) {
  .archive-item {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .archive-date {
    min-width: auto;
  }
}
</style>
