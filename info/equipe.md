---
title: Equipe
layout: template
filename: equipe
button: Equipe
type: info
---
![](../assets/images/logo_e2pc.png) 
## Equipe do Projeto  

<div class="container">
    <div class="row text-center">
        {% for pessoa in site.equipe %}
            <div class="col-xl-4 mb-5">
                <div class="bg-white rounded shadow-sm py-5 px-4">
                    {% if pessoa.photo %}
                        <img src="{{ pessoa.photo }}" alt="" width="100" class="img-fluid rounded-circle mb-3 img-thumbnail shadow-sm">
                    {% else %}
                        <img src="/assets/profile-images/default.jpg" alt="" width="100" class="img-fluid rounded-circle mb-3 img-thumbnail shadow-sm">
                    {% endif %}
                    <h5 class="mb-0">{{ pessoa.name }}</h5><span class="small text-muted">{{ pessoa.type }}</span>
                    <span class="small text-muted">{{ pessoa.begin_year }} - {{ pessoa.end_year }}</span>
                    <ul class="social mb-0 list-inline mt-3">
                        {% if pessoa.github %}
                            <li class="list-inline-item">
                                <a href="{{ pessoa.github }}" ><i class="fa fa-github"></i></a>
                            </li>
                        {% endif %}
                        {% if pessoa.linkedin %}
                            <li class="list-inline-item">
                                <a href="{{ pessoa.linkedin }}" ><i class="fa fa-linkedin"></i></a>
                            </li>
                        {% endif %}
                        {% if pessoa.link %}
                            <li class="list-inline-item">
                                <a href="{{ pessoa.link }}" ><i class="fa fa-link"></i></a>
                            </li>
                        {% endif %}
                    </ul>
                </div>
            </div>
        {% endfor %}
    </div>
</div>

Gabriel Maurício Utzig (2021 - )  
Daniel Machado Brasil (2021 - )  
João Vitor Pieczarka da Silva (2020 - )    
Eric Patrick Militão (2020 - )  
Alexandro Luis da Rocha Jr (2019 - )  
Erick Ascencio (2019 - 2020)  
Gabriel Krysa (2018 - 2019)  
Moises Alonso Prestes (2017 - 2020)  
Higor Gardin (2016 - 2019)    
João Vitor Mas Urtado (2016 - 2019)  
Lucas Fernando Didur (2015 - 2017)  
Lucas Padilha (2014 - 2016)  
Lucas Prestes (2013 - 2014)  
Everson Joay (2013 - 2014)  
Paulo Daniel Gonçalves (2012 - 2014)  
Ricardo Henrique Remes de Lima (2012)  
Marcelo Araújo (2012)  
Alexandre Silvestre Ferreira (2012)  
Paulo Roberto Urio (2011)  
Lucas Marcondes Pavelski (2011)  
Alessandro Dias Batista (2011)  
