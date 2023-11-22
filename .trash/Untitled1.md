<< [[2023-11-18]] | [[2023-11-20]] >>
# Last Day
{% set previous_notes = context.previous_notes %} {% for item in previous_notes.to_do_list %} {% if not item.completed %} {{ item.task }} {% endif %} {% endfor %}