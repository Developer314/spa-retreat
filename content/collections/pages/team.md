---
id: 29d59eed-cb48-42b1-82a7-b023db02ede6
blueprint: page
title: Team
author: 7cd469aa-80ee-43db-911c-a05a879c8683
template: home
seo_title: 'Meta Title'
seo_keywords: 'Meta Keywords'
banner_title: Services
heading: 'Find tranquility and transformation with our spa and beauty services.'
updated_by: 7cd469aa-80ee-43db-911c-a05a879c8683
updated_at: 1724681192
parent: home
content:
  -
    type: set
    attrs:
      id: m0b2lwv5
      values:
        type: inside_page_banner
        banner_image: img/services/Swedish_Massage_banner.jpeg
        banner_text: 'Our Team'
        edit_template: false
        custom_template: |-
          <!-- Header Start -->
          <div class="container-fluid bg-breadcrumb py-5" style="background-image: url({{banner_image}});">
              <div class="container text-center py-5">
                  <h3 class="text-white display-3 mb-4">{{banner_title}}</h1>
                  <ol class="breadcrumb justify-content-center mb-0">
                     
                      {{ nav:breadcrumbs }}
                      <li{{ if is_current }} class="breadcrumb-item active text-white"{{ /if }}>
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
      id: m0b2mje3
      values:
        type: team
        title_1: 'Spa Therapist'
        title_2: 'Expert in Relaxation and Beauty Enhancement Therapies and Treatments'
        edit_template: false
        custom_template: |-
          <!-- Team Start -->
              <div class="container-fluid team py-5"> 
                  <div class="container py-5">
                      <div class="text-center mx-auto mb-5" style="max-width: 800px;">
                          <p class="fs-4 text-uppercase text-primary">{{title_1}}</p>
                          <h1 class="display-8 mb-4">{{title_2}}</h1>
                      </div>
                      <div class="row g-4">
                          
                          {{members:members}}
                          
                          <div class="col-md-6 col-lg-6 col-xl-3">
                              <div class="team-item">
                                  <div class="team-img rounded-top">

                                      <img src="{{ glide:image preset="team_member" }}"  class="img-fluid w-100 rounded-top bg-light" alt="">
                                  </div>
                                  <div class="team-text rounded-bottom text-center p-4">
                                      <h3 class="text-white">{{name}}</h3>
                                      <p class="mb-0 text-white">{{speciality:label}}</p>
                                  </div>
                                  <div class="team-social">
                                      {{social_media}}
                                      <a class="btn btn-light btn-light-outline-0 btn-square rounded-circle mb-2" target="_blank" href="{{link}}"><i class="fab fa-{{icon}}"></i></a>
                                     {{/social_media}}
                                  </div>
                              </div>
                          </div>
                          
                          {{/members:members}}

                      </div>
                  </div>
              </div>
              <!-- Team End -->
  -
    type: set
    attrs:
      id: m0b2mwvq
      values:
        type: testimonials
        title_1: Testimonials
        title_2: 'See What our Clients Say!'
        edit_template: false
        custom_template: |-
          <!-- Testimonial Start --> 
              <div class="container-fluid testimonial py-5">
                  <div class="container py-5">
                      <div class="text-center mx-auto mb-5" style="max-width: 800px;">
                          <p class="fs-4 text-uppercase text-primary">{{title_1}}</p>
                          <h1 class="display-4 mb-4 text-white">{{title_2}}</h1>
                      </div>
                      <div class="owl-carousel testimonial-carousel">

                          {{testimonials:testimonials}}


                          <div class="testimonial-item rounded p-4">
                              <div class="row">
                                  <div class="col-4">
                                      <div class="d-flex flex-column mx-auto">
                                          <div class="rounded-circle mb-4" style="border: dashed; border-color: var(--bs-white);">
                                              <img src="{{ glide:image preset="client_image" }}" class="img-fluid rounded-circle" alt="{{name}}">
                                          </div>
                                          <div class="text-center">
                                              <h4 class="mb-2 text-primary">{{name}}</h4>
                                              <p class="m-0 text-white">{{profession}}</p>
                                          </div>
                                      </div>
                                  </div>
                                  <div class="col-8">
                                      <div class="position-absolute" style="top: 20px; right: 25px;">
                                          <i class="fa fa-quote-right fa-2x text-secondary"></i>
                                      </div>
                                      <div class="testimonial-content">
                                          <div class="d-flex mb-4">
                                              
                                              
                                             
                                          </div>
                                          <p class="fs-5 mb-0 text-white">{{testimonial_data}}</p>
                                      </div>
                                  </div>
                              </div>
                          </div>
                          {{/testimonials:testimonials}}

                      </div>
                  </div>
              </div>
              <!-- Testimonial End -->
  -
    type: paragraph
---
