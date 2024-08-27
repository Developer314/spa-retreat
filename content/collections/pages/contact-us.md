---
id: 9d818816-efaa-40f1-84c6-f3fabab55d64
blueprint: page
title: 'Contact Us'
author: 7cd469aa-80ee-43db-911c-a05a879c8683
template: home
seo_title: 'Meta Title'
seo_keywords: 'Meta Keywords'
banner_title: Services
heading: 'Find tranquility and transformation with our spa and beauty services.'
updated_by: 7cd469aa-80ee-43db-911c-a05a879c8683
updated_at: 1724690697
parent: home
content:
  -
    type: set
    attrs:
      id: m0b5s805
      values:
        type: inside_page_banner
        banner_image: img/our_gallery/facial_treatment_8.jpg
        banner_text: 'Contact Us'
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
      id: m0b5t0mi
      values:
        type: contact_form
        title: 'Contact Us'
        description: "Get in touch with us! Fill out our contact form below to inquire about our services, schedule an appointment, or share your feedback. We'll respond promptly to your message. Please provide your name, email, and a brief message, and we'll be happy to assist you further."
        form_heading: 'Do You have Any Questions?'
        edit_template: true
        custom_template: |2
           <!-- Contact Start -->
             <div class="container-fluid contact py-5" style="background: var(--bs-primary);">
              <div class="container pt-5">
                  <div class="row g-4 align-items-center">
                      <div class="col-lg-6">
                          <div class="text-center">
                              <h1 class="display-3 text-white mb-4">{{title}}</h1>
                              <p class="text-white fs-4">{{description}}</p>
                          </div>
                      </div>
                      <div class="col-lg-6">
                          <div class="contact-form rounded p-5">
                              {{ form:contact_us }}
                                  <h1 class="display-6 mb-4">{{form_heading}}</h1>

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





                                  <div class="row gx-4 gy-3">
                                      {{ fields }}

                                      {{if type=="textarea"}}
                                      <div class="col-12">
                                          <textarea class="form-control bg-white border-0 py-3 px-4" name="{{handle}}" rows="4" cols="10" placeholder="{{placeholder}}"></textarea>
                                      </div>

                                      {{else}}
                                      <div class="col-xl-6">
                                          <input type="{{input_type}}" name="{{handle}}" class="form-control bg-white border-0 py-3 px-4" placeholder="{{placeholder}}{{ if validate | contains:required }}*{{/if}}">
                                      </div>


                                      {{/if}}


                                                                 
                                      {{ /fields }}
                                      <div class="col-12">
                                          <button class="btn btn-primary btn-primary-outline-0 w-100 py-3 px-5" type="submit">Submit</button>
                                      </div>
                                  </div>
                                  {{/if}}
                              {{ /form:contact_us }}
                          </div>
                      </div>
                  </div>
              </div>
          </div>
        form_success_message: 'Form Submitted Successfully'
  -
    type: set
    attrs:
      id: m0b89gfk
      values:
        type: contact_details
        contacts:
          -
            id: m0b89i4w
            icon: fa-map-marker-alt
            title: Address
            data: 'Trivandrum, Kerala, India'
          -
            id: m0b89kdp
            icon: fa-envelope
            title: 'Mail Us'
            data: manup.rav@gmail.com
          -
            id: m0b8acgq
            icon: fa-phone-alt
            title: Telephone
            data: '+918907289865'
        google_map: |-
          <iframe class="rounded-top w-100" 
                                      style="height: 450px; margin-bottom: -6px;" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d387191.33750346623!2d-73.97968099999999!3d40.6974881!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89c24fa5d33f083b%3A0xc80b8f06e177fe62!2sNew%20York%2C%20NY%2C%20USA!5e0!3m2!1sen!2sbd!4v1694259649153!5m2!1sen!2sbd" 
                                      loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        follow_us_title: 'Follow Us'
        social_links:
          -
            id: m0b8as0f
            icon: fa-facebook-f
            url: 'https://www.linkedin.com/company/recolve-314-digital'
          -
            id: m0b8atmh
            icon: fa-twitter
            url: 'https://www.linkedin.com/company/recolve-314-digital'
          -
            id: m0b8auld
            icon: fa-instagram
            url: 'https://www.linkedin.com/company/recolve-314-digital'
          -
            id: m0b8aw23
            icon: fa-linkedin-in
            url: 'https://www.linkedin.com/company/recolve-314-digital'
        edit_template: true
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
