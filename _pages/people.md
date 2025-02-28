---
title: People
permalink: /people/
---

{% assign people_sorted = site.people | sort: 'joined' %}
{% assign role_array = "pi|researcher|alumni" | split: "|" %}

{% for role in role_array %}

{% assign people_in_role = people_sorted | where: 'position', role %}

<!-- Skip section if there's nobody -->
{% if people_in_role.size == 0 %}
  {% continue %}
{% endif %}

<div class="pos_header">
{% if role == 'pi' %}
<h3>Principal Investigator</h3>
{% elsif role == 'researcher' %}
<h3>Researchers</h3>
{% elsif role == 'alumni' %}
<h3>Alumni</h3>
{% endif %}
</div>

{% if role != 'alumni' %}
<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains role %}
      <div class="list-item-people">
        <p class="list-post-title">
          {% if profile.avatar %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
          {% else %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="http://evansheline.com/wp-content/uploads/2011/02/facebook-Storm-Trooper.jpg"></a>
          {% endif %}
          <a class="name" href="{{ site.baseurl }}{{ profile.url }}">{{ profile.name }}</a>
        </p>
      </div>    
    {% endif %}
  {% endfor %}
</div>
<hr>

{% else %}

<br>

| Name | Title | Works | Current |
| :------------- |:-------------| :-----------| :-----------|
| Minho Kim | Intern (2019.3. - 2019.8.) | Mouse behavior segmentation by NN algorithm | |
| Seonmin Kim | Intern (2019.3. - 2019.8.) | RNA-seq data analysis | |
| JeongJae Park | Intern (2019.7. - 2019.8.) | Modeling cerebellar granule cell migration | |
| Ji Yeon Kim | Intern (2019.7. - 2019.8.) | Modeling cerebellar granule cell migration | |
| Jongeun Kim | Intern (2019.9. - 2019.12.) | Calcium imaging analysis algorithm | |
| Hyeseong Byun | Intern (2020.1. - 2020.12.) | Open source equipment building for animal behavior observation | |
| [Ikhwan Jeon]({{site.baseurl}}/people/ikhwan_jeon/) | Intern (2020.3. - 2021.12.) | | |
| [Chanwoo Park]({{site.baseurl}}/people/chanwoo/) | Intern (2021.11. - 2022.3.) |  | |
| [Huihun Kim]({{site.baseurl}}/people/huihun_kim/) | Intern (2021.12. - 2022.2.) | Whole-neuron excitatory/inhibitory balance | |
| [JinMin Hwang]({{site.baseurl}}/people/jinmin_hwang/) | Intern (2022.1. - 2022.1.) | Whole-neuron excitatory/inhibitory balance | |


{% endif %}
{% endfor %}
