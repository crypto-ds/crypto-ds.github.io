#### Instructor

{% assign professors = site.staffers | where: 'role', 'Professor' %}
{% for staffer in professors %}
{{ staffer }}
{% endfor %}

{% assign teaching_fellows = site.staffers | where: 'role', 'Teaching Fellow' %}
{% assign num_teaching_fellows = teaching_fellows | size %}

{% if num_teaching_fellows != 0 %}

#### Teaching Fellow

{% for staffer in teaching_fellows %}
{{ staffer }}
{% endfor %}
{% endif %}

{% assign course_assistants = site.staffers | where: 'role', 'Course Assistant' %}
{% assign num_course_assistants = course_assistants | size %}

{% if num_course_assistants != 0 %}

#### Course Assistant

{% for staffer in course_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}
