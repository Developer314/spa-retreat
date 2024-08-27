---
id: 6235f887-68c7-4de6-b370-ecdd87f8f505
blueprint: page
title: Services
author: 7cd469aa-80ee-43db-911c-a05a879c8683
template: home
seo_title: Services
seo_keywords: Services
seo_description: Services
banner_image: img/services/HotStoneMassage_banner.jpeg
banner_title: Services
heading: 'Find tranquility and transformation with our spa and beauty services.'
updated_by: 7cd469aa-80ee-43db-911c-a05a879c8683
updated_at: 1724693182
parent: home
content:
  -
    type: set
    attrs:
      id: m0b9n0uv
      values:
        type: inside_page_banner
        banner_image: img/services/Swedish_Massage_banner.jpeg
        banner_text: 'Our Services'
        edit_template: true
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
      id: m0b9rp28
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
                          {{collection:services limit="25" as="posts"}}
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
                          
                      </div>
                  </div>
              </div>
              <!-- Services End -->
  -
    type: set
    attrs:
      id: m0b1nfsc
      values:
        type: get_appointment
        title_1: 'Get In Touch'
        title_2: 'Get Appointment'
        form_success_message: 'Thanks for your time, Form Submitted Successfully !'
        submit_buttion_text: Submit
        opening_hours_text: 'Opening Hours'
        opening_hours:
          -
            id: m0b1np51
            day: Saturday
            time: '09:00 am – 10:00 pm'
          -
            id: m0b1nqfj
            day: Saturday
            time: '09:00 am – 10:00 pm'
          -
            id: m0b1nrbs
            day: Saturday
            time: '09:00 am – 10:00 pm'
          -
            id: m0b1ntep
            day: Saturday
            time: '09:00 am – 10:00 pm'
          -
            id: m0b1nu8a
            day: Saturday
            time: '09:00 am – 10:00 pm'
          -
            id: m0b1nvk0
            day: Saturday
            time: '09:00 am – 10:00 pm'
        additional_info: "Don't miss out: seasonal discounts available for a limited time!"
        statistics:
          -
            id: m0b1nxqi
            icon: '<i class="fas fa-globe fa-5x text-primary mb-3"></i>'
            title: Clients
            number: '100'
          -
            id: m0b1nz9n
            icon: '<i class="fas fa-globe fa-5x text-primary mb-3"></i>'
            title: Clients
            number: '100'
          -
            id: m0b1o0e7
            icon: '<i class="fas fa-globe fa-5x text-primary mb-3"></i>'
            title: Clients
            number: '100'
        edit_template: true
        custom_template: |-
          <!-- Appointment Start -->
              <div class="container-fluid appointment py-5"> 
                  <div class="container py-5">
                      <div class="row g-5 align-items-center">
                          <div class="col-lg-6">
                              <div class="appointment-form p-5">
                                  <p class="fs-4 text-uppercase text-primary">{{title_1}}</p>
                                  <h1 class="display-4 mb-4 text-white">{{title_2}}</h1>
                                  
                                  {{ form:get_appointment }}
           
              {{ if success }}
                  <div class="text-success">
                      {{ form_success_message }}
                  </div>
              {{ else }}
                 {{ if errors }}
                      <div class="text-danger mb-3">
                          {{ errors }}
                              {{ value }}<br>
                          {{ /errors }}
                      </div>
                  {{ /if }}
                  <div class="row gy-3 gx-4">
                  {{ fields }}
                      
                          
                          {{if input_type == "text"}}
                          <div class="col-lg-6">
                              <input type="{{input_type}}" name="{{handle}}"  class="form-control py-3 border-white bg-transparent text-white" placeholder="{{placeholder}}">
                          </div>
                          {{elseif type=="textarea"}}
                          <div class="col-lg-12">
                              <textarea class="form-control border-white bg-transparent text-white" name="{{handle}}" cols="30" rows="5" placeholder="{{placeholder}}"></textarea>
                          </div>

                          {{elseif type=="select"}}
                          
                              <div class="col-lg-6">
                                  <select class="form-select py-3 border-white bg-transparent" aria-label="{{display}}">
                                      <option selected="">{{display}}</option>
                                      {{ foreach:options }}

                                      <option selected="{{key}}">{{value}}</option>
                                      {{ /foreach:options }}
                                  </select>
                              </div>
                         

                          

                          {{else}}

                          <div class="col-lg-6">
                              <input type="{{input_type}}" name="{{handle}}"  class="form-control py-3 border-white bg-transparent text-white" placeholder="{{placeholder}}">
                          </div>
                          
                          {{/if}}






                  {{ /fields }}
           </div>
                 
                  <input type="hidden" class="hidden" name="{{ honeypot ?? 'honeypot' }}">
           
                
                  <div class="col-lg-12 mt-3">
                      <button type="submit" class="btn btn-primary btn-primary-outline-0 w-100 py-3 px-5">{{submit_buttion_text}}</button>
                  </div>    
                  
                  {{ /if }}
           
          {{ /form:get_appointment }}
                              </div>
                          </div>
                          <div class="col-lg-6">
                              <div class="appointment-time p-5">
                                  <h1 class="display-5 mb-4">{{opening_hours_text}}</h1>
                                  {{opening_hours}}
                                  <div class="d-flex justify-content-between fs-5 text-white">
                                      <p>{{day}}:</p>
                                      <p>{{time}}</p>
                                  </div>
                                  {{/opening_hours}}
                                  <p class="text-dark">{{additional_info}}</p>
                              </div>
                          </div>
                      </div>
                  </div>
                  <!-- Counter Start -->
                  <div class="container-fluid counter-section">
                      <div class="container py-5">
                          <div class="row g-5 justify-content-center">
                              {{statistics}}
                              <div class="col-md-6 col-lg-4 col-xl-4">
                                  <div class="counter-item p-5">
                                      <div class="counter-content bg-white p-4">
                                          {{icon}}
                                          <h5 class="text-primary">{{title}}</h5>
                                          <div class="svg-img">
                                              <svg width="100" height="50">
                                                  <polygon points="55, 10 85, 55 25, 55 25," style="fill: #DCCAF2;"/>
                                              </svg>
                                          </div>
                                      </div>
                                      <div class="counter-quantity">
                                          <span class="text-white fs-2 fw-bold" data-toggle="counter-up">{{number}}</span>
                                          <span class="h1 fw-bold text-white">+</span>
                                      </div>
                                  </div>
                              </div>
                             {{/statistics}}
                          </div>
                      </div>
                  </div>
                  <!-- Counter End -->
              </div>
              <!-- Appointment End -->
  -
    type: paragraph
---
