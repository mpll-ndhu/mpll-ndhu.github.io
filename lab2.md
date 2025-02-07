
{% assign target_category = "current-master" %}  
{% assign category_images = null %} 
{% for category_data in site.data.images %}
  {% if category_data.category == target_category %}
    {% assign category_images = category_data.students %}
    {% break %}  
  {% endif %}
{% endfor %}



<h2 style="text-align: center">Alumni</h2>

<hr>

<h2 style="text-align: center">Ph.D students</h2>

<div class="gallery">
    {% for student in site.data.students %}
    <div class="student-card">
        <img src="assets/images/{{ student.image_subdirectory }}/{{ student.photo }}" alt="{{ student.name }}">
        <h4>{{ student.name }}</h4>
        <p>Email: <a href="mailto:{{ student.email }}">{{ student.email }}</a></p>
    </div>
    {% endfor %}
</div>

<hr>

<h2 style="text-align: center">Master students</h2>

<div class="gallery">
    {% for student in site.data.students %}
    <div class="student-card">
        <img src="assets/images/{{ student.image_subdirectory }}/{{ student.photo }}" alt="{{ student.name }}">
        <h4>{{ student.name }}</h4>
        <p>Email: <a href="mailto:{{ student.email }}">{{ student.email }}</a></p>
    </div>
    {% endfor %}
</div>

<hr>

<h2 style="text-align: center">Undergraduate students (Independent study)</h2>

<div class="gallery">
    {% for student in site.data.students %}
    <div class="student-card">
        <img src="assets/images/{{ student.image_subdirectory }}/{{ student.photo }}" alt="{{ student.name }}">
        <h4>{{ student.name }}</h4>
        <p>Email: <a href="mailto:{{ student.email }}">{{ student.email }}</a></p>
    </div>
    {% endfor %}
</div>

