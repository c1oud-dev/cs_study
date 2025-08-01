---
layout: default
title: "CS 정리 – 홈"
---

<section class="hero">
  <h1>CS 개념 학습 자료</h1>
  <p>아래 카테고리에서 학습하고 싶은 주제를 선택하거나 검색해보세요.</p>
  <input type="text" id="category-search" class="search-input" placeholder="카테고리 검색..." />
</section>

<section class="category-section">
  <h2>Category</h2>
  <div class="category-grid" id="category-grid">
    <a href="/cs_study/category/internet/index.html" class="category-card">Internet</a>
    <a href="/cs_study/category/language/index.html" class="category-card">Language</a>
    <a href="/cs_study/category/vcs/index.html" class="category-card">VCS</a>
    <a href="/cs_study/category/repo_hosting_services/index.html" class="category-card">Repo Hosting Services</a>
    <a href="/cs_study/category/postgresql/index.html" class="category-card">PostgreSQL</a>
    <a href="/cs_study/category/relational_database/index.html" class="category-card">Relational Databases</a>
    <a href="/cs_study/category/apis/index.html" class="category-card">APIs</a>
    <a href="/cs_study/category/caching/index.html" class="category-card">Caching</a>
    <a href="/cs_study/category/web_security/index.html" class="category-card">Web Security</a>
    <a href="/cs_study/category/ci_cd/index.html" class="category-card">CI/CD</a>
    <a href="/cs_study/category/databases/index.html" class="category-card">Databases</a>
    <a href="/cs_study/category/scaling_databases/index.html" class="category-card">Scaling Databases</a>
    <a href="/cs_study/category/architectural_patterns/index.html" class="category-card">Architectural Patterns</a>
    <a href="/cs_study/category/design_and_deploymen_principle/index.html" class="category-card">Design & Dev Principles</a>
    <a href="/cs_study/category/containerization_and_virtualization/index.html" class="category-card">Containerization vs Virtualization</a>
    <a href="/cs_study/category/message_brokers/index.html" class="category-card">Message Brokers</a>
    <a href="/cs_study/category/search_engines/index.html" class="category-card">Search Engines</a>
    <a href="/cs_study/category/web_servers/index.html" class="category-card">Web Servers</a>
    <a href="/cs_study/category/real_time_data/index.html" class="category-card">Real Time Data</a>
    <a href="/cs_study/category/nosql_databases/index.html" class="category-card">NoSQL Databases</a>
    <a href="/cs_study/category/building_for_scale/index.html" class="category-card">Building for Scale</a>
  </div>
</section>

<script>
  // 카테고리 검색 필터
  document.getElementById('category-search').addEventListener('input', function(e) {
    const filter = e.target.value.toLowerCase();
    document.querySelectorAll('#category-grid .category-card').forEach(card => {
      const text = card.textContent.toLowerCase();
      card.style.display = text.includes(filter) ? 'flex' : 'none';
    });
  });
</script>
