---
layout: default
title: My lab
permalink: /students/
---

<h2 style="text-align: center">Machine Perception and Learning Laboratory (機器感知暨學習實驗室)</h2>
<hr>

<style>
    .gallery {
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
        justify-content: center;
        padding: 20px;
    }
    .student-card {
        text-align: center;
        padding: 10px;
        border: 1px solid #ddd;
        border-radius: 5px;
        background: #f9f9f9;
        width: 200px;
    }
    .student-card img {
        width: 100%;
        height: auto;
        border-radius: 5px;
    }
</style>
  
{% assign students = null %} 
{% for category_data in site.data.students %}
  
{% if category_data.category == "current-phd" %}
{% assign students = category_data.images %}
<h2 style="text-align: center">PhD students</h2>
<div class="gallery">
    {% if students and students.size > 0 %}
    {% for student in students %}
    <div class="student-card">
        <img src="/assets/images/{{ student.photo }}" alt="{{ student.name }}">
        <h4>{{ student.name }}</h4>
        <!--<p>Email: <a href="mailto:{{ student.email }}">{{ student.email }}</a></p>-->
    </div>
    {% endfor %}
    {% endif %}
</div>
{% endif %}


{% if category_data.category == "current-master" %}
<hr>
<h2 style="text-align: center">Master students</h2>
{% assign students = category_data.images %}
<div class="gallery">
    {% if students and students.size > 0 %}
    {% for student in students %}
    <div class="student-card">
        <img src="/assets/images/{{ student.photo }}" alt="{{ student.name }}">
        <h4>{{ student.name }}</h4>
        <!--<p>Email: <a href="mailto:{{ student.email }}">{{ student.email }}</a></p>-->
    </div>
    {% endfor %}
    {% endif %}
</div>
{% endif %}


{% if category_data.category == "current-undergraduate" %}
<hr>
<h2 style="text-align: center">Undergraduate students (Independent study)</h2>
{% assign students = category_data.images %}
<div class="gallery">
    {% if students and students.size > 0 %}
    {% for student in students %}
    <div class="student-card">
        <img src="/assets/images/{{ student.photo }}" alt="{{ student.name }}">
        <h4>{{ student.name }}</h4>
        <!--<p>Email: <a href="mailto:{{ student.email }}">{{ student.email }}</a></p>-->
    </div>
    {% endfor %}
    {% endif %}
</div>
{% endif %}
{% endfor %}

<h2 style="text-align: center">Alumni</h2>
<hr>

{% assign students = null %} 
{% for category_data in site.data.alumni %}
  
{% if category_data.category == "alumni-phd" %}
{% assign alumni = category_data.images %}

{% if alumni and alumni.size > 0 %}
<hr>
<h2 style="text-align: center">PhD students</h2>
<div class="gallery">
    {% for student in alumni %}
    <div class="student-card">
        <img src="/assets/images/{{ student.photo }}" alt="{{ student.name }}">
        <h4>{{ student.name }}</h4>
        <!--<p>Email: <a href="mailto:{{ student.email }}">{{ student.email }}</a></p>-->
    </div>
    {% endfor %}    
</div>
{% endif %}
{% endif %}

{% if category_data.category == "alumni-master" %}
{% assign alumni = category_data.images %}

{% if alumni and alumni.size > 0 %}
<hr>
<h2 style="text-align: center">Master students</h2>
<div class="gallery">    
    {% for student in alumni %}
    <div class="student-card">
        <img src="/assets/images/{{ student.photo }}" alt="{{ student.name }}">
        <h4>{{ student.name }}</h4>
        {% if student.graduation-year %}
        <h4><i class="fa fa-graduation-cap"></i> {{ student.graduation-year }}</h4>
        {% endif %}
        <!--<p>Email: <a href="mailto:{{ student.email }}">{{ student.email }}</a></p>-->
    </div>
    {% endfor %}    
</div>
{% endif %}
{% endif %}


{% if category_data.category == "alumni-undergraduate" %}
{% assign alumni = category_data.images %}

{% if alumni and alumni.size > 0 %}
<hr>
<h2 style="text-align: center">Undergraduate students (Independent study)</h2>
<div class="gallery">    
    {% for student in alumni %}
    <div class="student-card">
        <img src="/assets/images/{{ student.photo }}" alt="{{ student.name }}">
        <h4>{{ student.name }}</h4>
        <!--<p>Email: <a href="mailto:{{ student.email }}">{{ student.email }}</a></p>-->
    </div>
    {% endfor %}    
</div>
{% endif %}
{% endif %}


{% if category_data.category == "alumni-assistant" %}
{% assign alumni = category_data.images %}

{% if alumni and alumni.size > 0 %}
<hr>
<h2 style="text-align: center">Assistant</h2>
<div class="gallery">    
    {% for assistant in alumni %}
    <div class="student-card">
        <img src="/assets/images/{{ assistant.photo }}" alt="{{ assistant.name }}">
        <h4>{{ assistant.name }}</h4>
        <!--<p>Email: <a href="mailto:{{ assistant.email }}">{{ assistant.email }}</a></p>-->
    </div>
    {% endfor %}    
</div>
{% endif %}
{% endif %}

{% endfor %}

