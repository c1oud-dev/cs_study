---
layout: default
title: "CS 정리 – 홈"
sidebar: false
---

<!-- Hero & Category Styles -->
<style>
  /* Hero */
  .hero {
    padding: 3rem 2rem;
    background: #fff;
    text-align: center;
  }
  .hero h1 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
  }
  .hero p {
    font-size: 1.125rem;
    color: #555;
    margin-bottom: 1.5rem;
  }
  .search-input {
    padding: 0.75rem 1rem;
    width: 300px;
    max-width: 100%;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 1rem;
  }

  /* Category Section */
  .category-section {
    max-width: 1000px;
    margin: 2rem auto;
    padding: 0 2rem;
  }
  .category-section h2 {
    font-size: 1.75rem;
    margin-bottom: 1rem;
    text-align: center;
  }
  .category-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
    gap: 1rem;
    justify-items: center;
  }
  .category-card {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    background: #0366d6;
    display: flex;
    align-items: center;
    justify-content: center;
    text-decoration: none;
    color: #fff;
    font-size: 0.9rem;
    text-align: center;
    padding: 1rem;
    transition: background 0.2s;
    line-height: 1.15;     /* 줄바꿈 시 균형 */
    word-break: keep-all;  /* 단어 중간 분리 방지 */
  }
  .category-card:hover {
    background: #0255a5;
  }

  /* Responsive */
  @media (max-width: 600px) {
    .hero { padding: 2rem 1rem; }
    .search-input { width: 100%; }
    .category-grid { grid-template-columns: repeat(auto-fill, minmax(80px, 1fr)); }
    .category-card { width: 80px; height: 80px; font-size: 0.8rem; }
  }
</style>

<!-- Hero Section -->
<section class="hero">
  <h1>CS 개념 학습 자료</h1>
  <p>아래 카테고리에서 학습하고 싶은 주제를 선택하거나 검색해보세요.</p>
  <input type="text" id="category-search" class="search-input" placeholder="카테고리 검색..." />
</section>

<!-- Category Cards -->
<section class="category-section">
  <h2>Category</h2>
  <div class="category-grid" id="category-grid">
    <a href="/cs_study/category/programming_basics.html" class="category-card">기초 프로그래밍</a>
    <a href="/cs_study/category/data_structures_algorithms.html" class="category-card">자료구조와 알고리즘</a>
    <a href="/cs_study/category/internet/index.html" class="category-card">Internet</a>
    <a href="/cs_study/category/language/index.html" class="category-card">Language</a>
    <a href="/cs_study/category/vcs/index.html" class="category-card">VCS</a>
    <a href="/cs_study/category/repo_hosting_services/index.html" class="category-card">Repo Hosting Services</a>
    <a href="/cs_study/category/relational_databases/index.html" class="category-card">Relational Databases</a>
    <a href="/cs_study/category/apis/index.html" class="category-card">APIs</a>
    <a href="/cs_study/category/caching/index.html" class="category-card">Caching</a>
    <a href="/cs_study/category/web_security/index.html" class="category-card">Web Security</a>
    <a href="/cs_study/category/testing/index.html" class="category-card">Testing</a>
    <a href="/cs_study/category/ci_cd/index.html" class="category-card">CI/CD</a>
    <a href="/cs_study/category/databases/index.html" class="category-card">Databases</a>
    <a href="/cs_study/category/scaling_databases/index.html" class="category-card">Scaling Databases</a>
    <a href="/cs_study/category/sw_design_and_architecture/index.html" class="category-card">SW Design & Architecture</a>
    <a href="/cs_study/category/architectural_patterns/index.html" class="category-card">Architectural Patterns</a>
    <a href="/cs_study/category/design_and_development_principles/index.html" class="category-card">Design & Dev Principles</a>
    <a href="/cs_study/category/containerization_and_virtualization/index.html" class="category-card">Containerization vs Virtualization</a>
    <a href="/cs_study/category/message_brokers/index.html" class="category-card">Message Brokers</a>
    <a href="/cs_study/category/search_engines/index.html" class="category-card">Search Engines</a>
    <a href="/cs_study/category/web_servers/index.html" class="category-card">Web Servers</a>
    <a href="/cs_study/category/real_time_data/index.html" class="category-card">Real Time Data</a>
    <a href="/cs_study/category/graphql/index.html" class="category-card">GraphQL</a>
    <a href="/cs_study/category/nosql_databases/index.html" class="category-card">NoSQL Databases</a>
    <a href="/cs_study/category/building_for_scale/index.html" class="category-card">Building for Scale</a>
  </div>
</section>

<!-- Search Script -->
<script>
  document.getElementById('category-search').addEventListener('input', function(e) {
    const filter = e.target.value.toLowerCase();
    document.querySelectorAll('#category-grid .category-card').forEach(card => {
      const text = card.textContent.toLowerCase();
      card.style.display = text.includes(filter) ? 'flex' : 'none';
    });
  });
</script>
