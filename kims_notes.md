basic each loop with an if-statement to limit row by index:

<div class="container">
  	<div class="row">
  		{{ each about_us_photos as picture sort by picture.sort_order }}
  		{{ if {index} % 3 == 1 && $count != 1 }}
  	</div>
  	<div class="row">
  		{{ end-if }}
  		<div class="col-md-4">
  			<img src ="{{ picture.about_us_photo.getImage() }}" alt="{{picture.title}} photo">
  			<p class="large">{{ picture.photo_title }}</p>
  			<p>{{ picture.photo_description }}</p>
  		</div>
  		{{ end-each }}
  	</div>
  </div>
</div>

<dataset name="starter_field_options" name_friendly="Form Settings - Starter Field Options" parent_item="">
    <fields>
      <text name="option_name" name_friendly="Option Name" required="1" list="1">
    </fields>
</dataset>
  <dataset name="field_types" name_friendly="Form Setting - Field Types" parent_item="">
  </dataset>

  
