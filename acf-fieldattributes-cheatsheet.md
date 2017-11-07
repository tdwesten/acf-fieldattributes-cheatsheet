# Fields attributes cheatsheet
This is a overview of all default attributes associated with the different ACF(pro) fields. This Cheatsheet is quite handy when creating ACF fields with the [StoutLogic Acf Builder](https://github.com/StoutLogic/acf-builder).

Last update: 27/09/2017
ACF version: 5.6.2

### Default field attributes
```php
$default_attributes = [
	'name' => 'field_name',
	'label' => 'Field name',
	'key' => 'key_field_name', // This one gets generated randomly, so in most cases there is no need to set this.
];
```

### Text field
```php
$attributes = [
    'default_value' => '',
    'maxlength' => '',
    'placeholder' => '',
    'prepend' => '',
    'append' => ''
];
```
### Textarea
```php
$attributes = [
    'default_value' => '',
    'new_lines'	 => '',
    'maxlength' => '',
    'placeholder' => '',
    'rows' => ''
];
```
### Number
```php
$attributes = [
    'default_value' => '',
    'min' => '',
    'max' => '',
    'step' => '',
    'placeholder' => '',
    'prepend' => '',
    'append' => ''
];
```
### Email
```php
$attributes = [
    'default_value' => '',
    'placeholder' => '',
    'prepend' => '',
    'append' => ''
];
```
### Url
```php
$attributes = [
    'default_value' => '',
    'placeholder' => '',
];
```
### Password
```php
$attributes = [
    'placeholder' => '',
    'prepend' => '',
    'append' => '',
];
```
### Range
```php
$attributes = [
    'default_value' => '',
    'min' => '',
    'max' => '',
    'step' => '',
    'prepend' => '',
    'append' => ''
];
```
### Wysiwyg Editor
```php
$attributes = [
    'tabs' => 'all',
    'toolbar' => 'full',
    'media_upload' => 1,
    'default_value' => '',
    'delay' => 0
];
```
### oEmbed
```php
$attributes = [
    'width' => '',
    'height' => '',
];
```
### Image
```php
$attributes = [
    'return_format' => 'array',
    'preview_size' => 'thumbnail',
    'library' => 'all',
    'min_width' => 0,
    'min_height' => 0,
    'min_size' => 0,
    'max_width' => 0,
    'max_height' => 0,
    'max_size' => 0,
    'mime_types' => ''
];
```
### File
```php
$attributes = [
    'return_format'	=> 'array',
    'library' => 'all',
    'min_size' => 0,
    'max_size' => 0,
    'mime_types' => ''
];
```
### Gallery (Pro)
```php
$attributes = [
    'library' => 'all',
    'min' => 0,
    'max' => 0,
    'min_width' => 0,
    'min_height' => 0,
    'min_size' => 0,
    'max_width' => 0,
    'max_height' => 0,
    'max_size' => 0,
    'mime_types' => '',
    'insert' => 'append'
];
```
### Link
```php
$attributes = [
	'return_format'	=> 'array',
];
```
### Post Object
```php
$attributes = [
    'post_type' => array(),
    'taxonomy' => array(),
    'allow_null' => 0,
    'multiple' => 0,
    'return_format'	=> 'object',
    'ui' => 1,
];
```
### Page Link
```php
$attributes = [
    'post_type'	=> string || array(), // Use string for one post_type, array for multiple post_types
    'taxonomy' => array(),
    'allow_null' => 0,
    'multiple' => 0,
    'allow_archives' => 1
];
```
### Relationship
```php
$attributes = [
    'post_type'	=> string || array(), // Use string for one post_type, array for multiple post_types
    'taxonomy' => array(),
    'min' => 0,
    'max'  => 0,
    'filters' => array('search', 'post_type', 'taxonomy'),
    'elements' => array(),
    'return_format' => 'object'
];
```

### Taxonomy
```php
$attributes = [
    'taxonomy' => 'category',
    'field_type' => 'checkbox',
    'multiple' => 0,
    'allow_null' => 0,
    'return_format' => 'id',
    'add_term' => 1,
    'load_terms' => 0,
    'save_terms' => 0
];
```
### User
```php
$attributes = [
    'role' => '',
    'multiple' => 0,
    'allow_null' => 0,
];
```
### Select
```php
$attributes = [
    'multiple' => 0,
    'allow_null' => 0,
    'choices' => [
    	[ 'value' => 'Label', ]
    ],
    'default_value'	=> 'value',
    'ui' => 0,
    'ajax' => 0,
    'placeholder' => '',
    'return_format'	=> 'value'
];
```
### Checkbox
```php
$attributes = [
    'layout' => 'vertical',
    'choices' => [
    	[ 'value' => 'Label', ]
    ],
    'default_value' => 'value',
    'allow_custom' => 0,
    'save_custom' => 0,
    'toggle' => 0,
    'return_format' => 'value'
];
```
### Radio
```php
$attributes = [
    'layout' => 'vertical',
    'choices' => [
    	[ 'value' => 'Label', ]
    ],
    'default_value' => 'value',
    'other_choice' => 0,
    'save_other_choice'	=> 0,
    'allow_null' => 0,
    'return_format' => 'value'
];
```
### True / False
```php
$attributes = [
    'default_value'	=> 0,
    'message' => '',
    'ui' => 0,
    'ui_on_text' => '',
    'ui_off_text' => '',
];
```
### Google Map
```php
$attributes = [
    'height' => '',
    'center_lat' => '',
    'center_lng' => '',
    'zoom' => ''
];
```
### Date Picker
```php
$attributes = [
    'display_format' => 'd/m/Y',
    'return_format' => 'd/m/Y',
    'first_day' => 1
];
```
### Date Time Picker
```php
$attributes = [
    'display_format' => 'd/m/Y g:i a',
    'return_format' => 'd/m/Y g:i a',
    'first_day' => 1
];
```
### Time Picker
```php
$attributes = [
    'display_format' => 'g:i a',
    'return_format' => 'g:i a',
];
```
### Color Picker
```php
$attributes = [
    'default_value'	=> 0,
];
```
### Color Picker
```php
$attributes = [
    'default_value'	=> 0,
];
```
### Message
```php
$attributes = [
    'message' => '',
    'esc_html' => 0,
    'new_lines' => 'wpautop',
];
```
### Tab
```php
$attributes = [
    'placement'	=> 'top',
    'endpoint' => 0
];
```
### Group
```php
$attributes = [
    'sub_fields' => array(),
    'layout' => 'block'
];
```
### Repeater
```php
$attributes = [
    'sub_fields' => array(),
    'min' => 0,
    'max' => 0,
    'layout' => 'table',
    'button_label' => '',
    'collapsed' => ''
];
```
### Flexible Content
```php
$attributes = [
    'layouts' => array(),
	'min' => '',
    'max' => '',
	'button_label'=> "Add Row",
];
```
### Clone
Not supported via a arrow function [https://github.com/StoutLogic/acf-builder/issues/37].
```php
$attributes = [
    'clone' => '',
    'prefix_label' => 0,
    'prefix_name' => 0,
    'display' => 'seamless',
    'layout' => 'block'
];
```

# Field group config
Apart from the specific fields there are some default setting for the entire group: 

### GroupConfig
```php
$group = new Fieldsbuilder('name', [
    'key' => 'custom_name',
    'title' => 'Name',
    'style' => 'default' || 'seamless',
    'position' => 'normal' || 'acf_after_title' || 'side',
    'menu_order' => 0,
    'label_placement' => 'top' || 'left',  
    'instruction_placement' => 'label' || 'field', // Place label below label or below field
]);
```
