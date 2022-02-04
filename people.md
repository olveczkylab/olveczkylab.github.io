---
title: People

permalink: /people/
---
<br/><br/>
{% assign people_sorted = (site.people | sort: 'joined' %}
{% assign people_array = "pi|postdoc|student|others" | split: "|" %}

{% for item in people_array %}

<div class="pos_header">
{% if item == 'postdoc' %}
<h3>Postdoctoral Fellows</h3>
 {% elsif item == 'pi' %}
<h3>Principal Investigator</h3>
 {% elsif item == 'student' %}
<h3>Graduate Students</h3>
 {% elsif item == 'visiting' %}
<h3>Visiting Scholars</h3>
 {% elsif item == 'others' %}
<h3>Others</h3>
 {% elsif item == 'alumni' %}
<h3>Alumni</h3>
{% endif %}
</div>

<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains item %}
    <div class="list-item-people">
      <p class="list-post-title">
        {% if profile.avatar %}
        <a href="{{ site.baseurl }}{{ profile.url }}"><img width="200" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
        {% else %}
        <a href="{{ site.baseurl }}{{ profile.url }}"><img width="200" src="http://evansheline.com/wp-content/uploads/2011/02/facebook-Storm-Trooper.jpg"></a>
        {% endif %}
        <a class="name" href="{{ site.baseurl }}{{ profile.url }}">{{ profile.name }}</a>
      </p>
    </div>    
    {% endif %}
  {% endfor %}
</div>



<hr>
{% endfor %}


| Alumni | Position | Where are they now? |
| :------------- |:-------------| :-----------|
| Dyuti Bhattacharya | Postdoctoral Fellow | 
| Evi Kopelowitz | Postdoctoral Fellow | 
| Claude Wang | Postdoctoral Fellow | Quant Trader in Taiwan
| Yoram Burak | Postdoctoral Fellow | Assistant Professor at Hebrew University
| Adam Kampff| Postdoctoral Fellow | Group Leader at the Champalimaud Foundation
| Sharon Gobes | Postdoctoral Fellow | Assistant Professor at Wellesley College
| Antoniu Fantana | Postdoctoral Fellow | Assistant Professor at Bowling Green State University
| Risa Kawai | Graduate Student in Biophysics | Data Scientist at Facebook
| Rajesh Poddar | Graduate Student in Neuroscience | Algorithmic Trader at Jump Trading
| Raymond Ko | Graduate Student in OEB | Manager, Strategic Pricing and Marketing at T-Mobile
| Timothy Otchy | Graduate Student in Neuroscience | Research Assistant Professor at Boston University
| Farhan Ali | Graduate Student in Biology | Postdoctoral Fellow at Yale 
| Jonathan Garst-Orozco | Graduate Student in Neuroscience | Senior Scientist at Flagship Pioneering
| Alexandre Kempff | Visiting Graduate Student (ENS Paris) | Data Scientist at PandaScore
| Alexis Dubreuil | Visiting Graduate Student (ENS Paris) | 
| Timothy Markman | Undergraduate Research Assistant | Cardiology Fellow at UPenn Perelman School of Medicine (MD, Johns Hopkins Medical School)
| Kate Xie | Undergraduate Research Assistant | Physician (MD, UC Irvine)
