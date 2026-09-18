---
layout: page
---

# About Me

<img src="/images/yinyao.jpg" class="floatpic">

Here is **Yao Yin (Yin Yao)**.<br>

I am an M.Eng. student in Electronic Information at the [School of Software and Microelectronics](https://ss.pku.edu.cn/) of **Peking University**, advised by [Prof. Wentao Zhang](https://zwt233.github.io/). My interests lie at the intersection of **intelligent software engineering**, **large language models**, and **agentic AI systems**, with a particular focus on reliable AI systems for software modernization and data-centric workflows. Previously, I received my B.Eng. in Software Engineering from **Beihang University**, where I worked on agentic migration from monoliths to deployable microservices and static analysis for application permission security. I have also gained industry experience through internships at **ModelBest** and **Alibaba Cloud**.<br>

## Work Experience

<div class="timeline">
  <div class="timeline-progress" id="timeline-progress"></div>

  <div class="timeline-item timeline-item--current">
    <div class="timeline-dot" style="background: #ffffff;">
      <img src="/images/logo/modelbest.png" alt="Modelbest">
    </div>
    <div class="timeline-card">
      <div class="timeline-header">
        <div class="timeline-role">Algorithm Intern <span class="timeline-sep">|</span> <span class="timeline-company">Modelbest Inc.</span></div>
        <span class="timeline-time">Dec. 2025 - Jun. 2026</span>
      </div>
      <div class="timeline-details">
        Contributed to the early development of OpenMAIC, an open multi-agent interactive classroom project. Focused on prototype design and core feature implementation for AI-generated course content, interactive learning flows, and production-oriented engineering workflows.
      </div>
    </div>
  </div>

  <div class="timeline-item">
    <div class="timeline-dot" style="background: #ffffff;">
      <img src="/images/logo/alibabacloud.svg" alt="Alibaba Cloud">
    </div>
    <div class="timeline-card">
      <div class="timeline-header">
        <div class="timeline-role">Academic Collaboration Intern <span class="timeline-sep">|</span> <span class="timeline-company">Alibaba Cloud Inc.</span></div>
        <span class="timeline-time">Jul. 2025 - Nov. 2025</span>
      </div>
      <div class="timeline-details">
        Conducted research and prototyping for monolith-to-microservices modernization, with a focus on dependency analysis, service decomposition strategies, and code refactoring.
      </div>
    </div>
  </div>

  <!-- <div class="timeline-item">
    <div class="timeline-dot" style="background: #ffffff;">
      <img src="/images/logo/sf.svg" alt="SF Express">
    </div>
    <div class="timeline-card">
      <div class="timeline-header">
        <div class="timeline-role">Software Engineer <span class="timeline-sep">|</span> <span class="timeline-company">SF Express</span></div>
        <span class="timeline-time">May. 2025 - Jul. 2025</span>
      </div>
      <div class="timeline-details">
        Delivered microservice modules for the order management system.
      </div>
    </div>
  </div> -->

  <!-- <div class="timeline-item">
    <div class="timeline-dot" style="background: #ffffff;">
      <img src="/images/logo/boc.svg" alt="Bank of China">
    </div>
    <div class="timeline-card">
      <div class="timeline-header">
        <div class="timeline-role">Software Engineer <span class="timeline-sep">|</span> <span class="timeline-company">Bank of China</span></div>
        <span class="timeline-time">Jul. 2024 - Sep. 2024</span>
      </div>
      <div class="timeline-details">
        Involved in the deployment and fine-tuning of large language models in internal banking systems.
      </div>
    </div>
  </div> -->

  <!-- <div class="timeline-item">
    <div class="timeline-dot" style="background: #ffffff;">
      <img src="/images/logo/szu.svg" alt="Shenzhen University">
    </div>
    <div class="timeline-card">
      <div class="timeline-header">
        <div class="timeline-role">Research Assistant <span class="timeline-sep">|</span> <span class="timeline-company"><a href="https://bdsc.szu.edu.cn/">Big Data Institute, Shenzhen University</a></span></div>
        <span class="timeline-time">2023 - 2024</span>
      </div>
      <div class="timeline-details">
        Supervised by Distinguished Professor <a href="https://dblp.org/pid/h/JoshuaZhexueHuang.html">Joshua Zhexue Huang</a>. Carried out optimizations on data processing and clustering algorithms by leveraging distributed approximate computing techniques.
      </div>
    </div>
  </div> -->

</div>

<script>
(function() {
  var timelineProgress = document.getElementById('timeline-progress');
  var timeline = document.querySelector('.timeline');
  if (!timelineProgress || !timeline) return;

  var items = timeline.querySelectorAll('.timeline-item');

  // IntersectionObserver for in-view class
  if ('IntersectionObserver' in window) {
    var observer = new IntersectionObserver(function(entries) {
      entries.forEach(function(entry) {
        if (entry.isIntersecting) {
          entry.target.classList.add('in-view');
        }
      });
    }, { rootMargin: '0px 0px -15% 0px' });

    items.forEach(function(item, idx) {
      if (idx < 3) {
        // Reveal first 3 immediately on load (still gets the stagger transition)
        item.classList.add('in-view');
      } else {
        observer.observe(item);
      }
    });
  } else {
    items.forEach(function(item) { item.classList.add('in-view'); });
  }

  // Scroll progress bar
  window.addEventListener('scroll', function() {
    var rect = timeline.getBoundingClientRect();
    var totalHeight = timeline.offsetHeight;
    var windowH = window.innerHeight;
    var lineTop = 30;
    var lineBottom = 30;
    var lineHeight = totalHeight - lineTop - lineBottom;

    if (rect.top < windowH && rect.bottom > 0) {
      var scrolled = Math.min(1, Math.max(0, (windowH - rect.top - lineTop) / (totalHeight - lineTop + windowH * 0.4)));
      timelineProgress.style.height = Math.min(scrolled * lineHeight, lineHeight) + 'px';
    }
  }, { passive: true });
})();
</script>

If you are interested in any aspect of me, I am always open to discussions and collaborations. Feel free to reach out to me at - yinyao053 [at] gmail.com

**<font color="#990000">Seeking Software Engineer and Machine Learning roles — AI Infrastructure, Applied AI / Agents, and ML Systems. Feel free to reach out!</font>**

<!-- ---

## Publications

<div class="publications-grid">

  <div class="publication-card">
    <div class="publication-thumb">
      <img src="/images/papers/paper1.svg" alt="Innovative covariance-based framework">
      <a href="https://www.tandfonline.com/doi/abs/10.1080/03610918.2026.2635000" class="publication-overlay" target="_blank" rel="noopener">
        <span>View Paper</span>
      </a>
    </div>
    <div class="publication-info">
      <div class="publication-title">
        <a href="https://www.tandfonline.com/doi/abs/10.1080/03610918.2026.2635000" target="_blank" rel="noopener">Innovative covariance-based framework: symmetry assessment and exponentiality testing under multiplicative distortion measurement Errors</a>
      </div>
      <div class="publication-authors"><strong class="author-highlight">Siming Deng</strong>, Jun Zhang, Jiongtao Zhong</div>
      <div class="publication-conference"><span class="pub-venue">Communications in Statistics - Simulation and Computation, 2026</span> <a href="https://www.tandfonline.com/doi/abs/10.1080/03610918.2026.2635000" target="_blank">[paper]</a></div>
      <div class="publication-details">SCI, first author</div>
    </div>
  </div>

  <div class="publication-card">
    <div class="publication-thumb">
      <img src="/images/papers/paper2.svg" alt="A New Logarithmic Multiplicative Distortion">
      <a href="https://onlinelibrary.wiley.com/doi/10.1002/sam.11708" class="publication-overlay" target="_blank" rel="noopener">
        <span>View Paper</span>
      </a>
    </div>
    <div class="publication-info">
      <div class="publication-title">
        <a href="https://onlinelibrary.wiley.com/doi/10.1002/sam.11708" target="_blank" rel="noopener">A New Logarithmic Multiplicative Distortion for Correlation Analysis</a>
      </div>
      <div class="publication-authors"><strong class="author-highlight">Siming Deng</strong>, Jun Zhang</div>
      <div class="publication-conference"><span class="pub-venue">Statistical Analysis and Data Mining, 2024</span> <a href="https://onlinelibrary.wiley.com/doi/10.1002/sam.11708" target="_blank">[paper]</a></div>
      <div class="publication-details">SCI, JCR: Q1, first author, Top Cited Article - WILEY 2025</div>
    </div>
  </div>

  <div class="publication-card">
    <div class="publication-thumb">
      <img src="/images/papers/paper3.svg" alt="A Revisit to Pearson Correlation Coefficient">
      <a href="https://www.tandfonline.com/doi/full/10.1080/03610918.2024.2333352" class="publication-overlay" target="_blank" rel="noopener">
        <span>View Paper</span>
      </a>
    </div>
    <div class="publication-info">
      <div class="publication-title">
        <a href="https://www.tandfonline.com/doi/full/10.1080/03610918.2024.2333352" target="_blank" rel="noopener">A Revisit to Pearson Correlation Coefficient under Multiplicative Distortions</a>
      </div>
      <div class="publication-authors"><strong class="author-highlight">Siming Deng</strong>, Jun Zhang, Yingcong Huang, Jiongtao Zhong & Xiaozhen Yang</div>
      <div class="publication-conference"><span class="pub-venue">Communications in Statistics - Simulation and Computation, 2024</span> <a href="https://www.tandfonline.com/doi/full/10.1080/03610918.2024.2333352" target="_blank">[paper]</a></div>
      <div class="publication-details">SCI, first author, Highly Cited Paper - Web of Science</div>
    </div>
  </div>

  <div class="publication-card">
    <div class="publication-thumb">
      <img src="/images/papers/paper4.svg" alt="Covariance Ratio under Multiplicative Distortion">
      <a href="https://www.tandfonline.com/doi/full/10.1080/03610926.2023.2295240" class="publication-overlay" target="_blank" rel="noopener">
        <span>View Paper</span>
      </a>
    </div>
    <div class="publication-info">
      <div class="publication-title">
        <a href="https://www.tandfonline.com/doi/full/10.1080/03610926.2023.2295240" target="_blank" rel="noopener">Covariance Ratio under Multiplicative Distortion Measurement Errors</a>
      </div>
      <div class="publication-authors">Jiongtao Zhong, <strong class="author-highlight">Siming Deng</strong>, Jun Zhang & Zhenghui Feng</div>
      <div class="publication-conference"><span class="pub-venue">Communications in Statistics - Theory and Methods, 2023</span> <a href="https://www.tandfonline.com/doi/full/10.1080/03610926.2023.2295240" target="_blank">[paper]</a></div>
      <div class="publication-details">SCI, 2nd-author</div>
    </div>
  </div>

  <div class="publication-card">
    <div class="publication-thumb">
      <img src="/images/papers/paper5.svg" alt="Estimation of Correlation Coefficient">
      <a href="https://www.tandfonline.com/doi/full/10.1080/03610926.2023.2288794" class="publication-overlay" target="_blank" rel="noopener">
        <span>View Paper</span>
      </a>
    </div>
    <div class="publication-info">
      <div class="publication-title">
        <a href="https://www.tandfonline.com/doi/full/10.1080/03610926.2023.2288794" target="_blank" rel="noopener">Estimation of Correlation Coefficient with Monotone Transformation and Multiplicative Distortions</a>
      </div>
      <div class="publication-authors">Jun Zhang, Xuan Yu, <strong class="author-highlight">Siming Deng</strong>, Jiongtao Zhong, Yisheng Zhou & Bingqing Lin</div>
      <div class="publication-conference"><span class="pub-venue">Communications in Statistics - Theory and Methods, 2023</span> <a href="https://www.tandfonline.com/doi/full/10.1080/03610926.2023.2288794" target="_blank">[paper]</a></div>
      <div class="publication-details">SCI, 3rd-author</div>
    </div>
  </div>

</div>

<script>
(function() {
  if ('IntersectionObserver' in window) {
    var observer = new IntersectionObserver(function(entries) {
      entries.forEach(function(entry) {
        if (entry.isIntersecting) {
          entry.target.classList.add('animate-in');
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.08, rootMargin: '0px 0px -40px 0px' });
    document.querySelectorAll('.publication-card').forEach(function(card) {
      observer.observe(card);
    });
  } else {
    document.querySelectorAll('.publication-card').forEach(function(card) {
      card.classList.add('animate-in');
    });
  }
})();
</script> -->

---

## Research Interests

- Agentic AI & Multi-Agent Systems
- Embodied AI & World Models
- Data-Centric AI & LLM Data Systems
- Intelligent Software Engineering
- Large Language Models & AI Infrastructure

I am particularly interested in building reliable agentic systems that connect data, models, and real-world environments, with an emphasis on software engineering workflows, data-centric intelligence, and embodied interaction.

<img src="/images/hello.jpg">

---

## News and Updates

<div class="news-grid">
  <div class="news-card news-card--milestone">
    <div class="news-meta">
      <span class="news-date">June 2026</span>
      <span class="news-tag news-tag--milestone">Academic</span>
    </div>
    <p>Graduated from <strong>Beihang University</strong> with a B.Eng. in Software Engineering and was recognized as an <strong>Outstanding Graduate</strong>.</p>
  </div>

  <div class="news-card news-card--milestone">
    <div class="news-meta">
      <span class="news-date">December 2025</span>
      <span class="news-tag news-tag--milestone">Award</span>
    </div>
    <p>Received the <strong>Excellence Award</strong> of the Ninebot Company Scholarship.</p>
  </div>

  <div class="news-card news-card--milestone">
    <div class="news-meta">
      <span class="news-date">May 2025</span>
      <span class="news-tag news-tag--milestone">Award</span>
    </div>
    <p><strong>HapPermission</strong>, an application-permission analysis framework for HarmonyOS, received the <strong>Gold Award</strong> in the Capital Challenge Cup “Youth Intelligence Future” Special Competition.</p>
  </div>

  <div class="news-card news-card--publication">
    <div class="news-meta">
      <span class="news-date">2025 – 2026</span>
      <span class="news-tag news-tag--publication">Project</span>
    </div>
    <p>Led <strong>Microxpert</strong>, a knowledge-preserving agentic framework for migrating monoliths to deployable microservices, which received the <strong>Third Prize</strong> in Beihang University’s Feng Ru Cup Main Track.</p>
  </div>
</div>

<script>
(function() {
  if ('IntersectionObserver' in window) {
    var observer = new IntersectionObserver(function(entries) {
      entries.forEach(function(entry) {
        if (entry.isIntersecting) {
          entry.target.classList.add('animate-in');
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.08, rootMargin: '0px 0px -60px 0px' });
    document.querySelectorAll('.news-card').forEach(function(card) {
      observer.observe(card);
    });
  } else {
    document.querySelectorAll('.news-card').forEach(function(card) {
      card.classList.add('animate-in');
    });
  }
})();
</script>
