---
id: 95868cc0-02e6-4ae9-81f3-0e61fcc56907
blueprint: page
title: Pricing
author: 7cd469aa-80ee-43db-911c-a05a879c8683
seo_title: 'Meta Title'
seo_keywords: 'Meta Keywords'
banner_title: Services
heading: 'Find tranquility and transformation with our spa and beauty services.'
updated_by: 7cd469aa-80ee-43db-911c-a05a879c8683
updated_at: 1724680995
template: home
parent: home
content:
  -
    type: set
    attrs:
      id: m0b281bi
      values:
        type: inside_page_banner
        banner_image: img/home_gallery/Swedish_Massage.jpeg
        banner_text: 'Our Pricing Plans'
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
      id: m0b2fzqw
      values:
        type: pricing
        edit_template: true
        custom_template: |-
          <!-- Pricing Start -->
              <div class="container-fluid pricing py-5"> 
                  <div class="container py-5">
                      <div class="owl-carousel pricing-carousel">
                          {{pricing:pricing}}
                          <div class="pricing-item">
                              <div class="rounded pricing-content">
                                  <div class="d-flex align-items-center justify-content-between bg-light rounded-top border-3 border-bottom border-primary p-4">
                                      <h1 class="display-4 mb-0">
                                          <small class="align-top text-muted" style="font-size: 22px; line-height: 45px;">{{currency:label}}</small>{{price}}<small class="text-muted" style="font-size: 16px; line-height: 40px;">/{{frequency:label}}</small> 
                                      </h1>
                                      <h5 class="text-primary text-uppercase m-0">{{plan_name}}</h5>
                                  </div>
                                  <div class="p-4">
                                      {{features}}
                                      <p><i class="fa fa-check text-primary me-2"></i>{{feature}}</p>
                                      {{/features}}
                                      <a href="{{button_link}}" class="btn btn-primary btn-primary-outline-0 rounded-pill my-2 px-4">{{button_title}}</a>
                                  </div>
                              </div>
                          </div>
                        {{/pricing:pricing}}
                      </div>
                  </div>
              </div>
              <!-- Pricing End -->
  -
    type: set
    attrs:
      id: m0b2ip3t
      values:
        type: get_appointment
        title_1: 'Get In Touch'
        title_2: 'Get Appointment'
        form_success_message: 'Thanks for your time, Form Submitted Successfully !'
        submit_buttion_text: Submit
        opening_hours_text: 'Opening Hours'
        opening_hours:
          -
            id: m0b2ivra
            day: Saturday
            time: '09:00 am – 10:00 pm'
          -
            id: m0b2ix4y
            day: Saturday
            time: '09:00 am – 10:00 pm'
          -
            id: m0b2ixwx
            day: Saturday
            time: '09:00 am – 10:00 pm'
          -
            id: m0b2iyus
            day: Saturday
            time: '09:00 am – 10:00 pm'
          -
            id: m0b2izr0
            day: Saturday
            time: '09:00 am – 10:00 pm'
          -
            id: m0b2j19t
            day: Saturday
            time: '09:00 am – 10:00 pm'
        additional_info: "Don't miss out: seasonal discounts available for a limited time!"
        statistics:
          -
            id: m0b2j37b
            icon: '<i class="fas fa-globe fa-5x text-primary mb-3"></i>'
            title: Clients
            number: '100'
          -
            id: m0b2j49a
            icon: '<i class="fas fa-globe fa-5x text-primary mb-3"></i>'
            title: Clients
            number: '100'
          -
            id: m0b2j5fe
            icon: '<i class="fas fa-globe fa-5x text-primary mb-3"></i>'
            title: Clients
            number: '100'
        edit_template: false
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
