---
id: 9a5469a2-670a-4c9f-9c55-7775db44c27c
blueprint: page
title: 'Search Results'
author: 7cd469aa-80ee-43db-911c-a05a879c8683
template: default
seo_title: 'Meta Title'
seo_keywords: 'Meta Keywords'
updated_by: 7cd469aa-80ee-43db-911c-a05a879c8683
updated_at: 1724736287
parent: home
content:
  -
    type: set
    attrs:
      id: m0bx4w7g
      values:
        type: inside_page_banner
        banner_image: img/home_gallery/Swedish_Massage.jpeg
        banner_text: 'Search Results'
        edit_template: false
        custom_template: |-
          <!-- Header Start -->
          <div class="container-fluid bg-breadcrumb py-5" style="background-image: url({{banner_image}});">
              <div class="container text-center py-5">
                  <h3 class="text-white display-3 mb-4">{{banner_text}}</h1>
                  <ol class="breadcrumb justify-content-center mb-0">
                     
                      {{ nav:breadcrumbs }}
                      <li class="breadcrumb-item {{ if is_current }} active {{ /if }} text-white">
                          <a href="{{ url }}">{{ title }}</a>
                      </li>
                      {{ /nav:breadcrumbs }}


                  </ol>    
              </div>
          </div>
          <!-- Header End -->
  -
    type: set
    attrs:
      id: m0bzd6o1
      values:
        type: search_result
        image_1: img/our_gallery/body_treatment_4.jpg
        image_2: img/services/HotStoneMassage_2.jpeg
        youtube_video_link: 'https://www.youtube.com/embed/82eLC8SzEvE?si=8mK_evhU0s9l4i_l'
        title: 'Search Result found for {{get:q}}'
        edit_template: true
        custom_template: |-
          <!-- Search Start --> 
            <div class="container-fluid about py-5">
              <div class="container py-5">
                  <div class="row g-5 align-baseline">
                      <div class="col-lg-5">
                          <div class="video">
                              <img src="{{ glide:image_1 preset="service_image_1" }}" class="img-fluid rounded" alt="{{title}}">
                              <div class="position-absolute rounded border-5 border-top border-start border-white" style="bottom: 0; right: 0;;">
                                  <img src="{{ glide:image_2 preset="service_image_2" }}" class="img-fluid rounded" alt="{{title}}" style="width: 300px; height: 200px;">
                              </div>
                              <button type="button" class="btn btn-play" data-bs-toggle="modal" data-src="{{youtube_video_link}}" data-bs-target="#videoModal">
                                  <span></span>
                              </button>
                          </div>
                      </div>
                      <div class="col-lg-7">
                          <div>

                              <h2>{{title}}</h2>
                          
                              {{ search:results index="default" }}
                              {{ if no_results }}
                                  <p>No results found for {{ get:q }}.</p>
                              {{ else }}
                                 <p> <a href="{{ url }}">
                                      <p>{{ title }}</p>
                                      <p>{{ description | truncate:180 }}</p>
                                  </a>
          </p>
                              {{ /if }}
                          {{ /search:results }}
                          
                          
                          </div>
                        
                      </div> 
                  </div>
              </div>
          </div>
          <!-- Modal Video -->
           
          <div class="modal fade" id="videoModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
              <div class="modal-dialog">
                  <div class="modal-content rounded-0">
                      <div class="modal-header">
                          <!--<h5 class="modal-title" id="exampleModalLabel">{{title_2}}</h5>-->
                          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                      </div>
                      <div class="modal-body">
                          <!-- 16:9 aspect ratio -->
                          <div class="ratio ratio-16x9">
                              <iframe class="embed-responsive-item" src="" id="video" allowfullscreen allowscriptaccess="always"
                                  allow="autoplay"></iframe>
                          </div>
                      </div>
                  </div>
              </div>
          </div>
          <!-- Search End -->
  -
    type: paragraph
---
