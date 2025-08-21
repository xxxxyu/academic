---
layout: homepage
---

## About Me

I am a 4th year Ph.D. student at **[Institute for AI Industry Research (AIR), Tsinghua University](https://air.tsinghua.edu.cn/en/)**, advised by **[Dr. Yunxin Liu](https://yunxinliu.github.io/)**. Prior to this, I received my B.E. degree from **[Department of Electronic Engineering, Tsinghua Univeristy](https://www.ee.tsinghua.edu.cn/en/)** in 2022.

My research interests include mobile computing, machine learning systems, and large language models (LLMs). I enjoy doing system research and solving pratical challenges. I am currently focused on **<u>building efficient agentic AI systems on edge platforms via system optimization.</u>**

Occasionally sharing thoughts about research, development, etc. See **[Xyu's Blog](https://xxxxyu.github.io/blog)**.

Feel free to contact: **<lixiangy22@mails.tsinghua.edu.cn>**.

<!-- ## Research Interests

- **Computer Vision:** image recognition, image generation, video captioning
- **Machine Learning:** meta-learning, incremental learning, transfer learning -->

## News

<div id="news-list" markdown="1">
- **[Aug. 2025]** Paper "An Empirical Study of LLM Reasoning Ability Under Strict Output Length Constraint" is accepted to **[EMNLP 2025](https://2025.emnlp.org)** main conference. Congrats to **[Yi Sun](https://scholar.google.com/citations?user=8YHqdcMAAAAJ)**! **[[Paper]](https://arxiv.org/pdf/2504.14350v3)** **[[Page]](https://time-is-up.github.io)**
- **[Jul. 2025]** Paper "Squeezer: Efficient Multi-DNN Inference for Edge Video Analytics via Cross-Model Scheduling" is accepted to IEEE Transactions on Mobile Computing. Congrats to Xiang Wang! **[[Paper]](https://ieeexplore.ieee.org/document/11096018)**
- **[Nov. 2024]** I presented **[FlexNN](https://dl.acm.org/doi/pdf/10.1145/3636534.3649391)** at **[MobiCom 2024](https://www.sigmobile.org/mobicom/2024/)**, Washington, D.C., USA. **[[Slides]](https://github.com/xxxxyu/FlexNN/blob/main/assets/FlexNN-MobiCom.pdf)**
</div>
<div id="more-news" style="display: none;" markdown="1">
- **[Apr. 2024]** **[FlexNN](https://dl.acm.org/doi/pdf/10.1145/3636534.3649391)** is awarded 4 badges in the artifact evaluation. **[[Code]](https://github.com/xxxxyu/FlexNN)**
- **[Jan. 2024]** Our position & survey paper "Personal LLM Agents: Insights and Survey about the Capability, Efficiency and Security" is released. **[[Paper]](https://arxiv.org/abs/2401.05459)** **[[Page]](https://github.com/MobileLLM/Personal_LLM_Agents_Survey)**
- **[Nov. 2023]** Our paper "FlexNN: Efficient and Adaptive DNN Inference on Memory-Constrained Edge Devices" is accepted to **[MobiCom 2024](https://www.sigmobile.org/mobicom/2024/)**. Thanks to all coauthors!
</div>

<div style="text-align: center; margin: 0px 0px 20px;">
  <span id="news-toggle-btn" style="font-size:20px; color: #007bff; cursor: pointer; text-decoration: none;">
    See More News
  </span>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const toggleBtn = document.getElementById('news-toggle-btn');
  const moreNews = document.getElementById('more-news');
  let isExpanded = false;

  // Add hover effects
  toggleBtn.addEventListener('mouseenter', function() {
    toggleBtn.style.textDecoration = 'underline';
  });
  
  toggleBtn.addEventListener('mouseleave', function() {
    toggleBtn.style.textDecoration = 'none';
  });

  toggleBtn.addEventListener('click', function() {
    if (isExpanded) {
      moreNews.style.display = 'none';
      toggleBtn.textContent = 'See More News';
      isExpanded = false;
    } else {
      moreNews.style.display = 'block';
      toggleBtn.textContent = 'See Less News';
      isExpanded = true;
    }
  });
});
</script>

{% include_relative _includes/publications.md %}

{% include_relative _includes/services.md %}
