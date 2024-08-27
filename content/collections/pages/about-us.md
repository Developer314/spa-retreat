---
id: 9369caff-d037-49c8-b13a-9917cb3645a3
blueprint: page
title: 'About Us'
author: 7cd469aa-80ee-43db-911c-a05a879c8683
template: home
seo_title: 'Meta Title'
seo_keywords: 'Meta Keywords'
banner_title: Services
heading: 'Find tranquility and transformation with our spa and beauty services.'
updated_by: 7cd469aa-80ee-43db-911c-a05a879c8683
updated_at: 1724680431
parent: home
content:
  -
    type: set
    attrs:
      id: m0b13311
      values:
        type: inside_page_banner
        banner_image: img/our_gallery/body_treatment_1.jpg
        banner_text: 'About Us'
        edit_template: false
        custom_template: |-
          <!-- Header Start -->
          <div class="container-fluid bg-breadcrumb py-5" style="background-image: url({{banner_image}});">
              <div class="container text-center py-5">
                  <h3 class="text-white display-3 mb-4">{{banner_text}}</h1>
                  <ol class="breadcrumb justify-content-center mb-0">
                     
                      {{ nav:breadcrumbs }}
                      <li class="breadcrumb-item {{ if is_current }}active{{ /if }} text-white">
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
      id: m0b18qm4
      values:
        type: about_us
        image_1: img/services/Deep_Tissue_Massage_1.jpeg
        image_2: img/services/HotStoneMassage_2.jpeg
        youtube_video_link: 'https://www.youtube.com/embed/82eLC8SzEvE?si=8mK_evhU0s9l4i_l'
        title_1: 'Contact Us'
        title_2: 'Relax, rejuvenate, and refresh with our luxurious spa and beauty treatments.'
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
        offers:
          -
            id: m0b1a8s6
            icon: '<i class="fab fa-gitkraken fa-3x text-primary"></i>'
            title: 'Refer a friend and receive 20% off your next service.'
            description: 'Share the bliss, refer a friend and enjoy 20% off your next!'
          -
            id: m0b1aaoa
            icon: '<i class="fas fa-gift fa-3x text-primary"></i>'
            title: 'Book 5 services, get the 6th 50% off.'
            description: 'Collect moments of bliss, book 5 services and enjoy 6th at half!'
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
          -
            type: paragraph
            attrs:
              textAlign: left
            content:
              -
                type: text
                text: "At Retreat, our mission is to provide a tranquil retreat from the stresses of everyday life. Our skilled therapists and luxurious treatments will melt away tension, soothe your mind, and nourish your body. We're dedicated to helping you achieve ultimate relaxation and wellness in a serene and peaceful environment."
          -
            type: paragraph
            attrs:
              textAlign: left
            content:
              -
                type: text
                text: "At Retreat, our mission is to provide a tranquil retreat from the stresses of everyday life. Our skilled therapists and luxurious treatments will melt away tension, soothe your mind, and nourish your body. We're dedicated to helping you achieve ultimate relaxation and wellness in a serene and peaceful environment."
          -
            type: paragraph
            attrs:
              textAlign: left
            content:
              -
                type: text
                text: "At Retreat, our mission is to provide a tranquil retreat from the stresses of everyday life. Our skilled therapists and luxurious treatments will melt away tension, soothe your mind, and nourish your body. We're dedicated to helping you achieve ultimate relaxation and wellness in a serene and peaceful environment."
          -
            type: paragraph
            attrs:
              textAlign: left
            content:
              -
                type: text
                text: "At Retreat, our mission is to provide a tranquil retreat from the stresses of everyday life. Our skilled therapists and luxurious treatments will melt away tension, soothe your mind, and nourish your body. We're dedicated to helping you achieve ultimate relaxation and wellness in a serene and peaceful environment."
          -
            type: paragraph
            attrs:
              textAlign: left
            content:
              -
                type: text
                text: "At Retreat, our mission is to provide a tranquil retreat from the stresses of everyday life. Our skilled therapists and luxurious treatments will melt away tension, soothe your mind, and nourish your body. We're dedicated to helping you achieve ultimate relaxation and wellness in a serene and peaceful environment."
          -
            type: paragraph
            attrs:
              textAlign: left
        button_text: Explore
        button_link: /services
        button_target: _self
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
  -
    type: set
    attrs:
      id: m0b271z8
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
    type: paragraph
---
