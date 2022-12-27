---
title: Equipe
layout: template
filename: equipe
button: Equipe
type: info
---

{% assign todos_equipe = site.equipe | sort:"end_year", "last" | reverse %}
![](../assets/images/logo_e2pc.png) 

## Equipe do Projeto  
<div class="container">
    <div class="row text-center">
        {% for pessoa in todos_equipe %}
            <div class="col-xl-4 mb-5">
                <div class="align-items-center d-flex dis flex-column px-4 py-5 rounded shadow-sm h-100" style="background-color: #f5f5f5 !important;">
                    {% if pessoa.photo %}
                        <img src="/assets/profile_images/{{ pessoa.photo }}.jpg" alt="" width="100" class="img-fluid rounded-circle mb-3 img-thumbnail shadow-sm">
                    {% else %}
                        <img src="/assets/profile_images/default.jpg" alt="" width="100" class="img-fluid rounded-circle mb-3 img-thumbnail shadow-sm">
                    {% endif %}
                    <h5 class="mb-0">{{ pessoa.name }}</h5>
                    <p class="mb-0 small text-muted align-center">{{ pessoa.type }}</p>
                    {% if pessoa.end_year %}
                        <p class="small text-muted">{{ pessoa.begin_year }} - {{ pessoa.end_year }}</p>
                    {% else %}
                        <p class="small text-muted">{{ pessoa.begin_year }} - Atualmente</p>
                    {% endif %}
                    <ul class="social mb-0 list-inline mt-3">
                        {% if pessoa.github %}
                            <li class="list-inline-item">
                                <a href="{{ pessoa.github }}" target="_blank"><i class="fa fa-github"></i></a>
                            </li>
                        {% endif %}
                        {% if pessoa.linkedin %}
                            <li class="list-inline-item">
                                <a href="{{ pessoa.linkedin }}" target="_blank"><i class="fa fa-linkedin"></i></a>
                            </li>
                        {% endif %}
                        {% if pessoa.link %}
                            <li class="list-inline-item">
                                <a href="{{ pessoa.link }}" target="_blank"><i class="fa fa-link"></i></a>
                            </li>
                        {% endif %}
                        {% if pessoa.bitbucket %}
                            <li class="list-inline-item">
                                <a href="{{ pessoa.bitbucket }}" target="_blank"><i class="fa  fa-bitbucket"></i></a>
                            </li>
                        {% endif %}
                    </ul>
                </div>
            </div>
        {% endfor %}
    </div>
</div>
