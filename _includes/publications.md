<h2 id="publications" style="margin: 2px 0px -15px;">Publications</h2>

<div class="publications">
<ol class="bibliography">

<!-- First show selected publications only -->

{% for link in site.data.publications.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if link.image %} 
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% if link.conference_short %} 
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ link.paper }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
    <div class="links">
      {% if link.paper %} 
      <a href="{{ link.paper }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Paper</a>
      {% endif %}
      {% if link.slides %} 
      <a href="{{ link.slide }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Slides</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Page</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.notes %} 
      &nbsp;<strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>

<!-- Show other publications when button clicked -->

{% if site.data.publications.others and site.data.publications.others.size > 0 %}
<div id="more-publications" style="display: none;">
  <ol class="bibliography" start="{{ site.data.publications.main.size | plus: 1 }}">
  
  {% for link in site.data.publications.others %}
  
  <li>
  <div class="pub-row">
    <!-- Don't show image, keep a compact layout -->
    <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
        <div class="title"><a href="{{ link.paper }}">{{ link.title }}</a></div>
        <div class="author">{{ link.authors }}</div>
        <div class="periodical"><em>{{ link.conference }}</em>
        </div>
      <div class="links">
        {% if link.paper %} 
        <a href="{{ link.paper }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Paper</a>
        {% endif %}
        {% if link.slides %} 
        <a href="{{ link.slide }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Slides</a>
        {% endif %}
        {% if link.code %} 
        <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
        {% endif %}
        {% if link.page %} 
        <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Page</a>
        {% endif %}
        {% if link.bibtex %} 
        <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
        {% endif %}
        {% if link.notes %} 
        &nbsp;<strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
        {% endif %}
        {% if link.others %} 
        {{ link.others }}
        {% endif %}
      </div>
    </div>
  </div>
  </li>
  <br>
  
  {% endfor %}
  
  </ol>
</div>

<!-- Button to adjust showed publications -->

<div style="text-align: center; margin: -30px 0px 20px;">
  <span id="toggle-publications" style="font-size:20px; color: #007bff; cursor: pointer; text-decoration: none;">
    See More Publications
  </span>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const toggleBtn = document.getElementById('toggle-publications');
  const morePublications = document.getElementById('more-publications');
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
      morePublications.style.display = 'none';
      toggleBtn.textContent = 'See More Publications';
      isExpanded = false;
    } else {
      morePublications.style.display = 'block';
      toggleBtn.textContent = 'See Fewer Publications';
      isExpanded = true;
    }
  });
});
</script>

{% endif %}

</div>