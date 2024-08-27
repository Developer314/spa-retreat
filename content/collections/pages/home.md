---
id: home
blueprint: pages
title: Home
template: home
author: 7cd469aa-80ee-43db-911c-a05a879c8683
updated_by: 7cd469aa-80ee-43db-911c-a05a879c8683
updated_at: 1724690783
seo_title: 'Meta Title'
seo_keywords: 'Meta Keywords'
banner_title: Services
heading: 'Find tranquility and transformation with our spa and beauty services.'
content:
  -
    type: set
    attrs:
      id: m0akilyb
      values:
        type: home_gallery
        home_gallery:
          -
            id: m0akf1zx
            background_image: img/home_gallery/antiaging.jpeg
            title_1: 'Relax, Rejuvenate, Renew'
            title_2: 'Anti-Aging Facial'
            description: 'The Anti-Aging Facial rejuvenates skin, reducing fine lines and wrinkles. Customized masks and expert techniques stimulate collagen, revealing a brighter, smoother, and youthful complexion.'
            button_one_text: 'Get Start'
            button_one_link: /
            button_one_target: _self
            button_two_text: 'Order Now'
            button_two_link: /
            button_two_target: _self
            type: new_set
            enabled: true
          -
            id: m0akg8f1
            background_image: img/home_gallery/Swedish_Massage.jpeg
            title_1: 'Relax, Rejuvenate, Renew'
            title_2: 'Swedish Massage'
            description: 'Swedish Massage eases muscle tension, improves circulation, and promotes relaxation. Long strokes, kneading, and gentle pressure soothe the mind and body, melting away stress.'
            button_one_text: 'Get Start'
            button_one_link: /
            button_one_target: _self
            button_two_text: 'Order Now'
            button_two_link: /
            button_two_target: _self
            type: new_set
            enabled: true
          -
            id: m0akh2ff
            background_image: img/home_gallery/Microdermabrasion.jpeg
            title_1: 'Where Wellness Meets Wonder'
            title_2: Microdermabrasion
            description: 'Microdermabrasion exfoliates and resurfaces the skin, reducing fine lines, wrinkles, and hyperpigmentation. Gentle yet effective, it reveals smoother, brighter, and more radiant complexion instantly.'
            button_one_text: 'Get Start'
            button_one_link: /
            button_one_target: _self
            button_two_text: 'Order Now'
            button_two_link: /
            button_two_target: _self
            type: new_set
            enabled: true
        edit_template: true
        custom_template: |-
          <!-- Carousel Start -->
              <div class="container-fluid carousel-header px-0">
                  <div id="carouselId" class="carousel slide" data-bs-ride="carousel">
                      <ol class="carousel-indicators">
                          {{home_gallery}}
                          <li data-bs-target="#carouselId" data-bs-slide-to="{{increment}}" class="{{if first}} active {{/if}}"></li>
                          {{/home_gallery}}
                      </ol>
                      <div class="carousel-inner" role="listbox">

                          {{home_gallery}}
                          <div class="carousel-item {{if first}} active {{/if}}">
                              <img src="{{background_image}}" class="img-fluid" alt="{{title_2}}">
                              <div class="carousel-caption">
                                  <div class="p-3" style="max-width: 900px;">
                                      <h4 class="text-primary text-uppercase mb-3">{{title_1}}</h4>
                                      <h1 class="display-1 text-capitalize text-dark mb-3">{{title_2}}</h1>
                                      <p class="mx-md-5 fs-4 px-4 mb-5 text-dark">{{description}}</p>
                                      <div class="d-flex align-items-center justify-content-center">
                                          <a class="btn btn-light btn-light-outline-0 rounded-pill py-3 px-5 me-4" target="{{button_one_target}}" href="{{button_one_link}}">{{button_one_text}}</a>
                                          <a class="btn btn-primary btn-primary-outline-0 rounded-pill py-3 px-5" target="{{button_two_target}}" href="{{button_two_link}}">{{button_two_text}}</a>
                                      </div>
                                  </div>
                              </div>
                          </div>
                          {{/home_gallery}}
                         
                      </div>
                      <button class="carousel-control-prev" type="button" data-bs-target="#carouselId" data-bs-slide="prev">
                          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                          <span class="visually-hidden">Previous</span>
                      </button>
                      <button class="carousel-control-next" type="button" data-bs-target="#carouselId" data-bs-slide="next">
                          <span class="carousel-control-next-icon" aria-hidden="true"></span>
                          <span class="visually-hidden">Next</span>
                      </button>
                  </div>
              </div>
              <!-- Carousel End -->
  -
    type: set
    attrs:
      id: m0ai6f6u
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
    type: set
    attrs:
      id: m0akit7p
      values:
        type: about_us
        image_1: img/services/Deep_Tissue_Massage_banner.jpeg
        image_2: img/services/Swedish_Massage_banner.jpeg
        youtube_video_link: 'https://www.youtube.com/embed/82eLC8SzEvE?si=8mK_evhU0s9l4i_l'
        title_1: 'About Us'
        title_2: 'Relax, rejuvenate, and refresh with our luxurious spa and beauty treatments.'
        decription_1: 'Welcome to Spa Retreat, your haven for relaxation and rejuvenation. Our expert therapists provide personalized care, using only the finest products and techniques. With a passion for wellness, we create a tranquil atmosphere, tailored to your needs, ensuring a truly unforgettable spa experience. Escape, unwind, and let us pamper you.'
        description_2:
          -
            type: paragraph
            attrs:
              textAlign: left
          -
            type: paragraph
            attrs:
              textAlign: left
            content:
              -
                type: text
                text: "At Retreat, our mission is to provide a tranquil retreat from the stresses of everyday life. Our skilled therapists and luxurious treatments will melt away tension, soothe your mind, and nourish your body. We're dedicated to helping you achieve ultimate relaxation and wellness in a serene and peaceful environment."
        button_text: Explore
        button_link: /services
        edit_template: true
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
        offers:
          -
            id: m0akqg2r
            icon: '<i class="fab fa-gitkraken fa-3x text-primary"></i>'
            title: 'Refer a friend and receive 20% off your next service.'
            description: 'Share the bliss, refer a friend and enjoy 20% off your next!'
          -
            id: m0akqjem
            icon: '<i class="fas fa-gift fa-3x text-primary"></i>'
            title: 'Book 5 services, get the 6th 50% off.'
            description: 'Collect moments of bliss, book 5 services and enjoy 6th at half!'
        description_1:
          -
            type: paragraph
            attrs:
              textAlign: left
            content:
              -
                type: text
                text: 'Welcome to Spa Retreat, your haven for relaxation and rejuvenation. Our expert therapists provide personalized care, using only the finest products and techniques. With a passion for wellness, we create a tranquil atmosphere, tailored to your needs, ensuring a truly unforgettable spa experience. Escape, unwind, and let us pamper you.'
          -
            type: paragraph
            attrs:
              textAlign: left
  -
    type: set
    attrs:
      id: m0aonwk3
      values:
        type: get_appointment
        title_1: 'Get In Touch'
        title_2: 'Get Appointment'
        form_success_message: 'Thanks for your time, Form Submitted Successfully !'
        submit_buttion_text: Submit
        opening_hours_text: 'Opening Hours'
        opening_hours:
          -
            id: m0aoo6vo
            day: Monday
            time: '09:00 am – 10:00 pm'
          -
            id: m0aoo7u8
            day: Tuesday
            time: '09:00 am – 10:00 pm'
          -
            id: m0aoo8mp
            day: Wednesday
            time: '09:00 am – 10:00 pm'
          -
            id: m0aoo9dl
            day: Thursday
            time: '09:00 am – 10:00 pm'
          -
            id: m0aooac9
            day: Friday
            time: '09:00 am – 10:00 pm'
          -
            id: m0aoow4a
            day: Saturday
            time: '09:00 am – 10:00 pm'
          -
            id: m0aoozyj
            day: Sunday
            time: CLOSED
        additional_info: "Don't miss out: seasonal discounts available for a limited time!"
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
        statistics:
          -
            id: m0aovyqf
            icon: '<i class="fas fa-globe fa-5x text-primary mb-3"></i>'
            title: Clients
            number: '900'
          -
            id: m0aow07l
            icon: '<i class="fas fa-spa fa-5x text-primary mb-3"></i>'
            title: 'Worldwide Clients'
            number: '200'
          -
            id: m0aox6c3
            icon: '<i class="fas fa-users fa-5x text-primary mb-3"></i>'
            title: 'Happy Customers'
            number: '500'
  -
    type: set
    attrs:
      id: m0atuwnx
      values:
        type: our_gallery
        title_1: 'Experience Our Excellence'
        title_2: 'See Our Exceptional Services in Action Right Here'
        number_of_items_per_category: 4
        edit_template: false
        custom_template: |-
          <!-- Gallery Start -->
              <div class="container-fluid gallery py-5">
                  <div class="container py-5">
                      <div class="text-center mx-auto mb-5" style="max-width: 800px;">
                          <p class="fs-4 text-uppercase text-primary">{{title_1}}</p>
                          <h1 class="display-4 mb-4">{{title_2}}</h1>
                      </div>
                      <div class="tab-class text-center">
                          <ul class="nav nav-pills d-inline-flex justify-content-center mb-5">
                              <li class="nav-item">
                                  <a class="d-flex mx-2 py-2 border border-primary bg-light rounded-pill active" data-bs-toggle="pill" href="#tab-1">
                                      <span class="text-dark" style="width: 150px;">All Gallery</span>
                                  </a>
                              </li>
                              {{gallery:gallery}}
                              <li class="nav-item">
                                  <a class="d-flex py-2 mx-2 border border-primary bg-light rounded-pill" data-bs-toggle="pill" href="#{{category}}">
                                      <span class="text-dark mx-2" style="width: 150px;">{{category:label}}</span>
                                  </a>
                              </li>
                              {{/gallery:gallery}}
                             
                          </ul>
                          <div class="tab-content">
                              <div id="tab-1" class="tab-pane fade show p-0 active">
                                  <div class="row g-4">
                                      <div class="col-lg-12">
                                          <div class="row g-4">
                                              {{gallery:gallery}}
                                              {{images limit="2"}}
                                              <div class="col-lg-3">
                                                  <div class="gallery-img">
                                                      <img class="img-fluid rounded w-100" src="{{url}}" alt="{{category}}">
                                                      <div class="gallery-overlay p-4">
                                                          <h4 class="text-secondary">{{category}}</h4>
                                                      </div>
                                                      <div class="search-icon">
                                                          <a href="{{url}}" data-lightbox="Gallery-9" class="my-auto"><i class="fas fa-search-plus btn-primary btn-primary-outline-0 rounded-circle p-3"></i></a>
                                                      </div>
                                                  </div>
                                              </div>
                                             {{/images}}
                                              {{/gallery:gallery}}
                                          </div>
                                      </div>
                                  </div>
                              </div>
                              {{gallery:gallery}}
                              <div id="{{category}}" class="tab-pane fade show p-0">
                                  <div class="row g-4">
                                      <div class="col-lg-12">
                                          <div class="row g-4">
                                             
                                             {{images limit="{{number_of_items_per_category}}"}}
                                              <div class="col-lg-3">
                                                  <div class="gallery-img">
                                                      <img class="img-fluid rounded w-100" src="{{url}}" alt="{{category}}">
                                                      <div class="gallery-overlay p-4">
                                                          <h4 class="text-secondary">{{category}}</h4>
                                                      </div>
                                                      <div class="search-icon">
                                                          <a href="{{url}}" data-lightbox="Gallery-9" class="my-auto"><i class="fas fa-search-plus btn-primary btn-primary-outline-0 rounded-circle p-3"></i></a>
                                                      </div>
                                                  </div>
                                              </div>
                                             {{/images}}
                                          </div>
                                      </div>
                                  </div>
                              </div>
                              {{/gallery:gallery}}
                             
                          </div>
                      </div>
          <div class="col-12 py-5">
                                  <div class="services-btn text-center">
                                      <a href="{{button_link}}" class="btn btn-primary btn-primary-outline-0 rounded-pill py-3 px-5">{{button_text}}</a>
                                  </div>
                              </div>
                  </div>
              </div>
              <!-- gallery End -->
        button_text: 'Full Gallery'
        button_link: /gallery
  -
    type: set
    attrs:
      id: m0avq4xj
      values:
        type: pricing
        pricing:
          -
            id: m0avq5uf
            plan_name: BASIC
            currency: dollar
            frequency: month
            price: '100'
            features:
              -
                id: m0avrlp5
                feature: 'Swedish Massage'
              -
                id: m0avrnha
                feature: 'Deep Tissue Massage'
              -
                id: m0avrw3o
                feature: 'Hot Stone Massage'
              -
                id: m0avs2bz
                feature: 'Aromatherapy Massage'
              -
                id: m0avsbev
                feature: 'Sports Massage'
            button_title: Order
            button_link: /contact
            edit_template: false
            custom_template: |-
              <!-- Pricing Start -->
                  <div class="container-fluid pricing py-5">
                      <div class="container py-5">
                          <div class="owl-carousel pricing-carousel">
                              {{pricing}}
                              <div class="pricing-item">
                                  <div class="rounded pricing-content">
                                      <div class="d-flex align-items-center justify-content-between bg-light rounded-top border-3 border-bottom border-primary p-4">
                                          <h1 class="display-4 mb-0">
                                              <small class="align-top text-muted" style="font-size: 22px; line-height: 45px;">{{currency}}</small>{{price}}<small class="text-muted" style="font-size: 16px; line-height: 40px;">/{{frequency}}</small>
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
                             {{/pricing}}
                          </div>
                      </div>
                  </div>
                  <!-- Pricing End -->
            type: new_set
            enabled: true
          -
            id: m0avv7zp
            plan_name: 'FAMILY PLAN'
            currency: dollar
            frequency: month
            price: '200'
            features:
              -
                id: m0avvp6h
                feature: 'Basic Facial'
              -
                id: m0avvw8t
                feature: 'Anti-Aging Facial'
              -
                id: m0avw4xw
                feature: 'Hydrating Facial'
              -
                id: m0avw6cu
                feature: 'Brightening Facial'
              -
                id: m0avwf11
                feature: 'Customized Facial'
            button_title: Order
            button_link: /contact
            type: new_set
            enabled: true
          -
            id: m0avwkye
            plan_name: 'VIP PLAN'
            currency: dollar
            frequency: month
            price: '100'
            features:
              -
                id: m0avwyf6
                feature: 'Salt Scrub'
              -
                id: m0avwzz5
                feature: 'Sugar Scrub'
              -
                id: m0avx5s5
                feature: 'Coffee Scrub'
              -
                id: m0avxb6w
                feature: 'Seaweed Wrap'
              -
                id: m0avxgct
                feature: 'Herbal Wrap'
            button_title: Order
            button_link: /contact
            type: new_set
            enabled: true
          -
            id: m0avxpis
            plan_name: 'GOLD PLAN'
            currency: dollar
            frequency: month
            price: '100'
            features:
              -
                id: m0avy8ex
                feature: Microdermabrasion
              -
                id: m0avye21
                feature: 'Chemical Peel'
              -
                id: m0avyia8
                feature: Microneedling
              -
                id: m0avynme
                feature: 'Laser Hair Removal'
              -
                id: m0avytfi
                feature: 'IPL (Intense Pulsed Light)'
            button_title: Order
            button_link: /contact
            type: new_set
            enabled: true
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
      id: m0axb8wd
      values:
        type: team
        title_1: 'Spa Therapist'
        title_2: 'Expert in Relaxation and Beauty Enhancement Therapies and Treatments'
        members:
          -
            id: m0axbb5x
            name: 'Emily Wilson'
            speciality: 'Wellness Therapist'
            image: img/team/specialist_1.jpeg
            social_media:
              -
                id: m0axbkje
                icon: twitter
                link: 'http://www.facebook.com'
              -
                id: m0axblfm
                icon: facebook-f
                link: 'http://www.facebook.com'
              -
                id: m0axbm3z
                icon: linkedin-in
                link: 'http://www.facebook.com'
              -
                id: m0axbmp8
                icon: instagram
                link: 'http://www.facebook.com'
            edit_template: false
            custom_template: |-
              <!-- Team Start -->
                  <div class="container-fluid team py-5">
                      <div class="container py-5">
                          <div class="text-center mx-auto mb-5" style="max-width: 800px;">
                              <p class="fs-4 text-uppercase text-primary">{{title_1}}</p>
                              <h1 class="display-4 mb-4">{{title_2}}</h1>
                          </div>
                          <div class="row g-4">
                              
                              {{members}}
                              
                              <div class="col-md-6 col-lg-6 col-xl-3">
                                  <div class="team-item">
                                      <div class="team-img rounded-top">
                                          <img src="{{image}}" class="img-fluid w-100 rounded-top bg-light" alt="">
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
                              
                              {{/members}}

                          </div>
                      </div>
                  </div>
                  <!-- Team End -->
            type: new_set
            enabled: true
          -
            id: m0axecj5
            name: 'Charlotte Lee'
            speciality: 'Spa Therapist'
            image: img/team/specialist_2.jpeg
            social_media:
              -
                id: m0axeqmd
                icon: twitter
                link: 'http://www.facebook.com'
              -
                id: m0axerbo
                icon: facebook-f
                link: 'http://www.facebook.com'
              -
                id: m0axerv2
                icon: linkedin-in
                link: 'http://www.facebook.com'
              -
                id: m0axesef
                icon: instagram
                link: 'http://www.facebook.com'
            type: new_set
            enabled: true
          -
            id: m0axezce
            name: 'Abigail Rose'
            speciality: 'Beauty Specialist'
            image: img/team/specialist_3.jpeg
            social_media:
              -
                id: m0axfcof
                icon: twitter
                link: 'http://www.facebook.com'
              -
                id: m0axfdla
                icon: facebook-f
                link: 'http://www.facebook.com'
              -
                id: m0axfe75
                icon: linkedin-in
                link: 'http://www.facebook.com'
              -
                id: m0axfet0
                icon: instagram
                link: 'http://www.facebook.com'
            type: new_set
            enabled: true
          -
            id: m0axfk06
            name: 'Harriet Thompson'
            speciality: 'Skincare Expert'
            image: img/team/specialist_4.jpeg
            social_media:
              -
                id: m0axfx1m
                icon: twitter
                link: 'http://www.facebook.com'
              -
                id: m0axfxu1
                icon: facebook-f
                link: 'http://www.facebook.com'
              -
                id: m0axfytc
                icon: linkedin-in
                link: 'http://www.facebook.com'
              -
                id: m0axfzd1
                icon: instagram
                link: 'http://www.facebook.com'
            type: new_set
            enabled: true
        edit_template: true
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
      id: m0aycnuw
      values:
        type: testimonials
        title_1: Testimonials
        text_2: 'See What our Clients Say!'
        edit_template: true
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
        title_2: 'See What our Clients Say!'
  -
    type: set
    attrs:
      id: m0b8bz0t
      values:
        type: contact_details
        contacts:
          -
            id: m0b8bzzh
            icon: fa-map-marker-alt
            title: Address
            data: 'Trivandrum, Kerala, India'
          -
            id: m0b8c103
            icon: fa-envelope
            title: Address
            data: manup.rav@gmail.com
          -
            id: m0b8c1s1
            icon: fa-phone-alt
            title: Address
            data: '+918907289865'
        google_map: |-
          <iframe class="rounded-top w-100" 
                                      style="height: 450px; margin-bottom: -6px;" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d387191.33750346623!2d-73.97968099999999!3d40.6974881!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89c24fa5d33f083b%3A0xc80b8f06e177fe62!2sNew%20York%2C%20NY%2C%20USA!5e0!3m2!1sen!2sbd!4v1694259649153!5m2!1sen!2sbd" 
                                      loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        follow_us_title: 'Follow Us'
        social_links:
          -
            id: m0b8cqcs
            icon: fa-facebook-f
            url: 'https://www.linkedin.com/company/recolve-314-digital'
          -
            id: m0b8crfd
            icon: fa-twitter
            url: 'https://www.linkedin.com/company/recolve-314-digital'
          -
            id: m0b8csnd
            icon: fa-instagram
            url: 'https://www.linkedin.com/company/recolve-314-digital'
          -
            id: m0b8ctel
            icon: fa-linkedin-in
            url: 'https://www.linkedin.com/company/recolve-314-digital'
        edit_template: false
        custom_template: |-
          <div class="container-fluid pb-5">
              <div class="container py-5">
                  <div class="row g-4 align-items-center">
                      <div class="col-12">
                          <div class="row g-4">
                              {{contacts}}
                              <div class="col-lg-4">
                                  <div class="d-inline-flex bg-light w-100 border border-primary p-4 rounded">
                                      <i class="fas {{icon}} fa-2x text-primary me-4"></i>
                                      <div>
                                          <h4>{{title}}</h4>
                                          <p class="mb-0">{{data}}</p>
                                      </div>
                                  </div>
                              </div>
                              {{/contacts}}
                            
                          </div>
                      </div>
                      <div class="col-12">
                          <div class="rounded">
                              {{google_map}}
                          </div>
                          <div class=" text-center p-4 rounded-bottom bg-primary">
                              <h4 class="text-white fw-bold">{{follow_us_title}}</h4>
                              <div class="d-flex align-items-center justify-content-center">
                                  {{social_links}}
                                  <a href="{{url}}" target="_blank" class="btn btn-light btn-light-outline-0 btn-square rounded-circle me-3"><i class="fab {{icon}}"></i></a>
                                  {{/social_links}}</div>   
                          </div>
                      </div>
                  </div>
              </div>
          </div>
  -
    type: paragraph
---
