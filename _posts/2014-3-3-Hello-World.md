---
layout: post
title:  "Welcome to Jekyll!"
---

<!-- UIkit CSS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/uikit@3.4.2/dist/css/uikit.min.css" />

<!-- UIkit JS -->
<script src="https://cdn.jsdelivr.net/npm/uikit@3.4.2/dist/js/uikit.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/uikit@3.4.2/dist/js/uikit-icons.min.js"></script>

<form>


{% for question in site.data.quiz1 %}
<div class="uk-h3">{{question.question}}</div>
<div class="uk-grid uk-grid-medium uk-grid-row-large uk-form-controls">
{% for answer in question.answers %}
            <label><input class="uk-radio" type="radio" name="{{question.question| slugify}}" value="{{answer.answer | slugify}}" >{{answer.answer}}</label>
            
{% endfor %}
</div>
{% endfor %}
</form>

