---
id: 35491273-1a00-432a-8f26-98488908711b
blueprint: page
title: Testimonial
author: 7cd469aa-80ee-43db-911c-a05a879c8683
template: home
seo_title: 'Meta Title'
seo_keywords: 'Meta Keywords'
banner_title: Services
heading: 'Find tranquility and transformation with our spa and beauty services.'
updated_by: 7cd469aa-80ee-43db-911c-a05a879c8683
updated_at: 1724681354
parent: home
content:
  -
    type: set
    attrs:
      id: m0b2nr6f
      values:
        type: inside_page_banner
        banner_image: img/home_gallery/Swedish_Massage.jpeg
        banner_text: Testimonial
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
      id: m0b2o8t6
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
    type: set
    attrs:
      id: m0b2olzk
      values:
        type: services
        title_one: 'Our Services'
        title_two: 'Transform and renew with our comprehensive spa and beauty offerings.'
        button_text: 'More Services'
        button_link: /services
        edit_template: true
        custom_template: |-
          <!-- Services Start -->
              <div class="container-fluid services py-5">. 
                  <div class="container py-5">
                      <div class="mx-auto text-center mb-5" style="max-width: 800px;">
                          <p class="fs-4 text-uppercase text-center text-primary">{{title_one}}</p>
                          <h1 class="display-3">{{titile_two}}</h1>
                      </div>
                      <div class="row g-4">
                          {{collection:services limit="8" as="posts"}}
          {{posts}}
                              <div class="col-lg-6">
                                  <div class="services-item bg-light border-4 border-end border-primary rounded p-4">
                                      <div class="row align-items-center">
                                          <div class="col-8">
                                              <div class="services-content text-end">
                                                  <h3>{{title}}</h3>
                                                  <p>{{short_description}}</p>
                                                  <a href="{{url}}" class="btn btn-primary btn-primary-outline-0 rounded-pill py-2 px-4">{{button_text}}</a>
                                              </div>
                                          </div>
                                          <div class="col-4">
                                              <div class="services-img d-flex align-items-center justify-content-center rounded">
                                                  <img src="{{ glide:image_1 preset="service_thumb" }}" class="img-fluid rounded" alt="{{title}}">
                                              </div>
                                          </div>
                                      </div>
                                  </div>
                              </div>
          {{/posts}}
                              {{/collection:services}}
                          <div class="col-12">
                              <div class="services-btn text-center">
                                  <a href="{{button_link}}" class="btn btn-primary btn-primary-outline-0 rounded-pill py-3 px-5">{{button_text}}</a>
                              </div>
                          </div>
                      </div>
                  </div>
              </div>
              <!-- Services End -->
  -
    type: paragraph
---
