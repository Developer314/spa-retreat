---
id: 659d2ed7-057f-4c06-842c-2cb048edb4d5
blueprint: service
title: Test
banner_title: 'Spa Service'
short_description: 'Microdermabrasion exfoliates and resurfaces the skin, reducing fine lines, wrinkles, and hyperpigmentation. Gentle yet effective, it reveals smoother, brighter, and more radiant complexion instantly.'
heading: 'Spa Service'
youtube_video_link: 'https://youtu.be/xRwRv8GJXtM?si=n97qSK-sFDMeSowJ'
button_text: 'Order Now'
author: 7cd469aa-80ee-43db-911c-a05a879c8683
seo_keywords: 'Spa Service'
seo_description: 'SEO Description'
updated_by: 7cd469aa-80ee-43db-911c-a05a879c8683
updated_at: 1724692653
content:
  -
    type: set
    attrs:
      id: m0b9gymq
      values:
        type: about_us
        youtube_video_link: 'https://www.youtube.com/embed/82eLC8SzEvE?si=8mK_evhU0s9l4i_l'
        title_1: 'Contact Us'
        title_2: 'Relax, rejuvenate, and refresh with our luxurious spa and beauty treatments.'
        button_text: Explore
        button_link: /services
        edit_template: false
        custom_template: |-
          <!-- About Start -->
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
                              <p class="fs-4 text-uppercase text-primary">{{title_1}}</p>
                              <h1 class="display-4 mb-4">{{title_2}}</h1>
                             {{description_1}}
                             <div class="row g-4">
                              {{offers}}

                              <div class="col-md-6">
                                  <div class="d-flex align-items-center">
                                      {{icon}}
                                      <div class="ms-4">
                                          <h5 class="mb-2">{{title}}</h5>
                                          <p class="mb-0">{{description}}</p>
                                      </div>
                                  </div>
                              </div>
                              {{/offers}}

                          </div>
                        
                          {{description_2}}
                             <a href="{{button_link}}" class="btn btn-primary btn-primary-outline-0 rounded-pill py-3 px-5" target="{{button_target}}">{{button_text}}</a>
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
                          <h5 class="modal-title" id="exampleModalLabel">{{title_2}}</h5>
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
          <!-- About End -->
  -
    type: paragraph
---
