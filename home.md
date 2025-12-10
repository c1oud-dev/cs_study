---
layout: default
title: "CS Note"
sidebar: false
---

<!-- Hero & Category Styles -->
<style>
 /* Hero */
.hero {
  padding: 5rem 2rem;
  background: linear-gradient(135deg, #4f9dff, #6a5af9); /* 그라데이션 배경 */
  color: #fff;
  text-align: center;
  position: relative;
  overflow: hidden;
}
.hero::after {
  content: "";
  position: absolute;
  top: -50px;
  left: -50px;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle at 30% 30%, rgba(255,255,255,0.15), transparent 70%);
  transform: rotate(25deg);
  pointer-events: none;
}

/* 입력/카드가 오버레이 위로 오도록 */
.hero .hero-card,
.hero .search-input {
  position: relative;               /* ← 추가 */
  z-index: 1;                       /* ← 추가 */
}

.hero h1 {
  font-size: 3rem;
  font-weight: 800;
  margin-bottom: 1rem;
}
.hero p {
  font-size: 1.2rem;
  margin-bottom: 2rem;
}
/* Hero inner card (About + Search in one box) */
.hero .hero-card {
  max-width: 900px;
  margin: 0 auto;
  background: rgba(255,255,255,0.12);
  border: 1px solid rgba(255,255,255,0.25);
  border-radius: 16px;
  padding: 2rem 1.5rem;
  box-shadow: 0 10px 30px rgba(0,0,0,0.15);
  backdrop-filter: blur(6px);
}
.hero .hero-card h2 {
  font-size: 1.5rem;
  font-weight: 800;
  margin: 0 0 0.75rem 0;
  color: #fff;
}
.hero .hero-card p {
  margin: 0 0 1.25rem 0;
  color: rgba(255,255,255,0.9);
  line-height: 1.7;
}
.hero .search-wrap {
  display: flex;
  justify-content: center;
  margin-top: 1rem;
}

.search-input {
  padding: 0.85rem 1rem;
  width: 100%;
  max-width: 600px;
  border: none;
  border-radius: 50px;
  font-size: 1rem;
  box-shadow: 0 4px 15px rgba(0,0,0,0.15);
}

/* Recommended Section */
.recommended-section {
  max-width: 1000px;
  margin: 4rem auto;
  text-align: center;
  padding: 0 1.5rem;
}
.recommended-section h2 {
  font-size: 2rem;
  margin-bottom: 2rem;
  color: #333;
}
.recommended-grid {
  display: flex;
  gap: 1.5rem;
  justify-content: center;
  flex-wrap: wrap;
}
.recommended-card {
  background: linear-gradient(135deg, #6a5af9, #4f9dff);
  color: #fff;
  border: none;
  padding: 1.5rem 2rem;
  border-radius: 12px;
  text-decoration: none;
  font-weight: 600;
  font-size: 1.1rem;
  transition: transform 0.25s ease, box-shadow 0.25s ease;
  box-shadow: 0 6px 15px rgba(0,0,0,0.15);
}
.recommended-card:hover {
  transform: translateY(-5px) scale(1.03);
  box-shadow: 0 10px 25px rgba(0,0,0,0.2);
}

/* Category Section */
.category-section {
  max-width: 1100px;
  margin: 4rem auto;
  padding: 0 2rem;
  display: flex;                  /* 추천 학습 + 카테고리 나란히 */
  gap: 2rem;
}
.category-section h2 {
  font-size: 1.5rem;
  margin-bottom: 1rem;
  font-weight: 700;
  color: #444;
  border-left: 5px solid #6a5af9;
  padding-left: 0.75rem;
}

/* 왼쪽 추천 학습 */
.recommended-sidebar {
  flex: 0 0 220px;                /* 고정 폭 */
}
.recommended-sidebar h2 {
  font-size: 1.25rem;
  margin-bottom: 1rem;
  color: #333;
}
.recommended-list {
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
}
.recommended-card {
  background: linear-gradient(135deg, #6a5af9, #4f9dff);
  color: #fff;
  border-radius: 8px;
  padding: 0.9rem 1rem;
  text-decoration: none;
  font-weight: 600;
  font-size: 0.9rem;
  text-align: center;
  transition: transform 0.25s ease, box-shadow 0.25s ease;
  box-shadow: 0 4px 10px rgba(0,0,0,0.15);
}
.recommended-card:hover {
  transform: translateY(-3px) scale(1.02);
  box-shadow: 0 8px 18px rgba(0,0,0,0.2);
}

/* 오른쪽 카테고리 */
.category-grid {
  flex: 1;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(180px, 1fr)); /* 카드 크기 줄임 */
  gap: 1rem;
}
.category-card {
  background: #fff;
  border-radius: 10px;
  padding: 1rem;
  height: 90px;                  /* 크기 줄임 */
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  text-decoration: none;
  color: #333;
  font-size: 0.9rem;
  font-weight: 600;
  box-shadow: 0 3px 8px rgba(0,0,0,0.08);
  transition: all 0.25s ease;
}
.category-card:hover {
  background: #6a5af9;
  color: #fff;
  transform: translateY(-4px);
  box-shadow: 0 8px 20px rgba(0,0,0,0.2);
}

/* Responsive */
@media (max-width: 800px) {
  .category-section { flex-direction: column; }
  .recommended-sidebar { flex: unset; width: 100%; }
  .category-grid { grid-template-columns: repeat(auto-fill, minmax(140px, 1fr)); }
  .category-card { height: 80px; font-size: 0.85rem; }
}

/* 작은 폰: 2~3열 강제 */
@media (max-width: 600px) {
  .category-grid { grid-template-columns: repeat(auto-fill, minmax(130px, 1fr)); } /* ↓ 더 작게 */
}

/* 아주 작은 폰: 최소 120px로 2열 확보 */
@media (max-width: 380px) {
  .category-grid { grid-template-columns: repeat(auto-fill, minmax(120px, 1fr)); }
}

</style>

<!-- Hero Section (About 포함) -->
<section class="hero">
  <h1>CS 개념 학습 자료</h1>
  <p>원하는 주제를 검색하거나 카테고리를 클릭해 학습을 시작하세요.</p>

  <div class="hero-card">
    <h2>About This Site</h2>
    <p>
      CS 면접과 실무에 꼭 필요한 핵심 개념들을 한눈에 정리했습니다.</p>

  <div class="search-wrap">
    <input type="text" id="category-search" class="search-input" placeholder="카테고리 검색..." />
  </div>
  </div>
</section>

<!-- Recommended Section -->
<section class="recommended-section">
  <h2>추천 학습</h2>
  <div class="recommended-grid">
    <a href="/cs_study/category/data_structures_algorithms.html" class="recommended-card">📘 자료구조와 알고리즘</a>
    <a href="/cs_study/category/web_security/index.html" class="recommended-card">🔒 Web Security</a>
    <a href="/cs_study/category/databases/index.html" class="recommended-card">🗄️ Databases</a>
  </div>
</section>

<!-- Category Cards -->
<section class="category-section">
  <h2>면접 대비</h2>
  <div class="category-grid small" id="cs-basic-grid">
    <a href="/cs_study/category/interview/java.html" class="category-card">자바(Java)</a>
   <a href="/cs_study/category/interview/spring.html" class="category-card">스프링(Spring)</a>
   <a href="/cs_study/category/interview/jpa.html" class="category-card">JPA</a>
    <a href="/cs_study/category/interview/data_structures.html" class="category-card">자료구조 (Data Structures)</a>
    <a href="/cs_study/category/interview/algorithms.html" class="category-card">알고리즘 (Algorithms)</a>
    <a href="/cs_study/category/interview/operating_systems.html" class="category-card">운영체제 (Operating Systems)</a>
    <a href="/cs_study/category/interview/computer_networks.html" class="category-card">네트워크 (Computer Networks)</a>
   <a href="/cs_study/category/interview/database.html" class="category-card">데이터베이스 (Database)</a>
   <a href="/cs_study/category/interview/sw_and_architecture.html" class="category-card">소프트웨어 공학 & 아키텍처</a>
   <a href="/cs_study/category/interview/security.html" class="category-card">보안 (Security)</a>
   <a href="/cs_study/category/interview/cloud_and_distributed_systems.html" class="category-card">클라우드 & 분산 시스템</a>
   <a href="/cs_study/category/interview/other.html" class="category-card">DevOps</a>
  </div>
</section>

<!-- Category Cards -->
<section class="category-section">
  <h2>CS 기본 로드맵</h2>
  <div class="category-grid small" id="cs-basic-grid">
    <a href="/cs_study/category/programming_basics.html" class="category-card">기초 프로그래밍</a>
    <a href="/cs_study/category/data_structures_algorithms.html" class="category-card">자료구조와 알고리즘</a>
    <a href="/cs_study/category/object_oriented_programming.html" class="category-card">객체지향 프로그래밍</a>
    <a href="/cs_study/category/system_fundamentals.html" class="category-card">시스템 기초</a>
   <a href="/cs_study/category/database.html" class="category-card">데이터베이스</a>
   <a href="/cs_study/category/web_development.html" class="category-card">웹 개발</a>
  </div>
</section>

<section class="category-section">
  <h2>백엔드 로드맵</h2>
  <div class="category-grid small" id="backend-grid">
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
  document.getElementById('category-search')?.addEventListener('input', function(e) {
    const filter = e.target.value.toLowerCase();
    document.querySelectorAll('.category-card').forEach(card => {
      const text = card.textContent.toLowerCase();
      card.style.display = text.includes(filter) ? 'flex' : 'none';
    });
  });
</script>
