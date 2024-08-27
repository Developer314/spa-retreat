---
id: 6f11c21a-7b2f-4bd3-acbf-95ca64e29949
blueprint: page
title: Gallery
author: 7cd469aa-80ee-43db-911c-a05a879c8683
seo_title: 'Meta Title'
seo_keywords: 'Meta Keywords'
banner_title: Services
heading: 'Find tranquility and transformation with our spa and beauty services.'
updated_by: 7cd469aa-80ee-43db-911c-a05a879c8683
updated_at: 1724681740
template: home
parent: home
content:
  -
    type: set
    attrs:
      id: m0b2s15c
      values:
        type: inside_page_banner
        banner_image: img/home_gallery/antiaging.jpeg
        banner_text: 'Image Gallery'
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
      id: m0b2smf2
      values:
        type: our_gallery
        title_1: 'Experience Our Excellence'
        title_2: 'See Our Exceptional Services in Action Right Here'
        number_of_items_per_category: 20
        edit_template: true
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
                                              {{images limit="20"}}
                                              <div class="col-lg-3">
                                                  <div class="gallery-img">
                                                      <img class="img-fluid rounded w-100" src="{{url}}" alt="{{category}}">
                                                      <div class="gallery-overlay p-4">
                                                          <h4 class="text-secondary">{{category}}</h4>
                                                      </div>
                                                      <div class="search-icon">
                                                          <a href="{{url}}" data-lightbox="gallery_item" class="my-auto"><i class="fas fa-search-plus btn-primary btn-primary-outline-0 rounded-circle p-3"></i></a>
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
                                                          <a href="{{url}}" data-lightbox="gallery_item" class="my-auto"><i class="fas fa-search-plus btn-primary btn-primary-outline-0 rounded-circle p-3"></i></a>
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

                  </div>
              </div>
              <!-- gallery End -->
        button_text: 'Full Gallery'
        button_link: /gallery
  -
    type: paragraph
---
