---
permalink: /
title: "Orlando Ferrari's Homepage"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<!-- *Website under construction, more contents will be updated (publications, teachings, and detailed information about me) after a few days/weeks. -->
---
# I'm Orlando Ferrari! (Yes, Ferrari is my last name)

<figure style="display: block; max-width: 500px;">
  <img src='/images/wm_caricature.png' alt="Caricature of Orlando Ferrari writing mathematical equations on a board">
  <figcaption>My caricature, commissioned from <a href="https://vgen.co/PawpleNeko">pawpleneko</a>!</figcaption>
</figure>

A freshman dual-degree Master's math student at the University of Padova and Dauphine-PSL University for the [MAPPA curriculum](https://mappa.math.unipd.it). Currently has research interests in analysis, particularly in **differential equations, functional analysis, calculus of variations, and measure theory**. In addition to my mathematical interest, I have over four years of experience in mathematics education as a tutor.

{% assign all_content = site.posts %}

{% if site.projects %}
  {% assign all_content = all_content | concat: site.projects %}
{% endif %}

{% if site.talks %}
  {% assign all_content = all_content | concat: site.talks %}
{% endif %}

{% if site.papers %}
  {% assign all_content = all_content | concat: site.papers %}
{% endif %}
{% if site.teaching %}
  {% assign all_content = all_content | concat: site.teaching %}
{% endif %}

{% assign sorted_content = all_content | sort: 'date' | reverse %}

<hr style="opacity: 0.5; margin: 2em 0; border-top: 2px solid #ccc;">

<section class="recent-posts">
  <h2 style="margin-top: 0;">Latest Updates</h2>
  
  <ul style="list-style-type: none; padding-left: 0;">
    
    {% for item in sorted_content limit:3 %}
      <li style="margin-bottom: 1.5em;">
        
        <span class="post-meta">
          {{ item.date | date: "%B %d, %Y" }} 
          <strong style="text-transform: uppercase; font-size: 0.85em; opacity: 0.7;">
            [{{ item.collection }}]
          </strong>
        </span>
        
        <h3 style="margin-top: 0.5em; margin-bottom: 0.5em;">
          <a class="post-link" href="{{ item.url | relative_url }}">{{ item.title }}</a>
        </h3>
        
        {% if item.description %}
          <div style="margin-top: 0; font-size: 0.95em;">
            {{ item.description | markdownify }}
          </div>
        {% endif %}

        {% unless forloop.last %}
          <hr style="opacity: 0.2; margin: 1.5em 0;">
        {% endunless %}
        
      </li>
    {% endfor %}
  </ul>
</section>

<hr style="opacity: 0.5; margin: 2em 0; border-top: 2px solid #ccc;">

<img src='/images/IMC_2023.jpg'>

Prior to my undergraduate years until my 3rd year for my Bachelor's degree, I am focused to math olympiads, and it was my main source of interest to mathematics (funfact: I didn't win often before going to uni). My highest achievement at this time was being able to represent Indonesia for the [30th International Mathematics Competition](https://imc-math.org.uk) at Blagoevgrad, Bulgaria.

<img src='/images/FinalThesis_2025.jpg'>

Starting in my final year (7th semester) as an undergraduate student, I am pursuing other means to love mathematics by striving for its beauty. During the work of my thesis, I was captivated by how we can apply mathematical results from one field--which is topology--to another field--that is, order structure--which produced an interesting problem, which was the content of [my thesis](https://etd.repository.ugm.ac.id/penelitian/detail/249432). Hence, I am more into learning various topics that somehow may unify to a spectacular result (hopefully).

<img src='/images/Wisudapic_2025.jpg'>



