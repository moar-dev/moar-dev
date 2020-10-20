---
layout: page
title: Meet the builder
description: 'More information about pricing and shipping'
seo_description:
show_tile: false
nav-menu: false
order: 3
image: 'assets/images/misc/guitar-carve.jpg'
---

<div class="inner">
	<form id="guitar-design-form" method="post" enctype='application/json' name="fields">
      <input placeholder="Guitar name" type="text" id="guitar-name" name="guitar-name">
      <input placeholder="Creator name" type="text" id="creator-name" name="creator-name">
      <input placeholder="Creator Instagram" value="@" type="text" id="creator-instagram" name="creator-instagram">
      <ul class="actions" style="margin-bottom: 0;">
        <li style="width:100%; padding:0;"><input id="save-design" type="submit" value="Save and Submit" class="button fit"/></li>
        <!-- <input type="hidden" name="_next" id="next" value="{{ site.baseurl }}/order-placed" /> -->
      </ul>
    </form>
</div>


<script type="text/javascript">
console.clear();

// sort with _createdTime ??
// var airtable_write_endpoint = "?api_key=";

const data = {
        "records": [
          {
            "fields": {
              "guitar-name": "The Bitch",
              "creator-name": "John",
              "creator-instagram": "Just a test"
            }
          }
        ]
      };

  let axiosConfig = {
    headers: {
        'Authorization': 'Bearer keykx6o2ysAy0m8xs',
        'Content-Type': 'application/json'
    }
  };
axios.post('https://api.airtable.com/v0/appZwoSS7LA9GWVKP/submitted-guitars', data, axiosConfig)
    .then(function (response) {
      // handle success
      console.log(response);
    })
    .catch(function (error) {
      // handle error
      console.log(error);
    })
    .finally(function () {
      // always executed
    });
</script>