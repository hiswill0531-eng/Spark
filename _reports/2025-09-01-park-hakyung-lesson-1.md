---
title: 박하경
layout: page
---

# 박하경 학생 페이지

[보고서 작성하기]({{ '/report-form.html?student=park-hakyung' | relative_url }})

## 날짜별 보고서
<ul>
{% assign reports = site.reports | where: "student_id", "park-hakyung" | sort: "date" | reverse %}
{% if reports.size > 0 %}
  {% for r in reports %}
    <li>
      <a href="{{ r.url | relative_url }}">{{ r.title }}</a>
      <small>({{ r.date }})</small>
    </li>
  {% endfor %}
{% else %}
  <li>아직 등록된 보고서가 없습니다.</li>
{% endif %}
</ul>
