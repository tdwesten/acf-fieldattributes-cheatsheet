# Fields attributes cheatsheet
This is a overview of all default attributes associated with the different ACF(pro) fields. This Cheatsheet is quite handy when creating ACF fields with the [StoutLogic Acf Builder](https://github.com/StoutLogic/acf-builder).

Last update: 07-11-2017
ACF version: 5.6.4

Full description about registering ACF Fields for PHP is available her: [Register fields via PHP](https://www.advancedcustomfields.com/resources/register-fields-via-php/)

## Construct Group

### Default group attributes and group construction
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

## Fields

### Default field attributes
```php
$default_attributes = [
	'name' => 'field_name',
	'label' => 'Field name',
	'key' => 'key_field_name', // This one gets generated randomly, so in most cases there is no need to set this.
	'prepend' => '',
	'append' => '',
	'wrapper' => [
		'width' => '100%',
		'class' => '',
		'id' => '',
	],
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
```php
$group->addText('field_name', $attributes);
```
### Textarea
```php
$attributes = [
    'default_value' => '',
    'new_lines'	 => 'wpautop' || 'br' || '', // wpautop adds paragraphs automatically, br saves enters, '' won't add any formatting 
    'maxlength' => '',
    'placeholder' => '',
    'rows' => ''
];
```
```php
$group->addTextarea('field_name', $attributes);
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
```php
$group->addNumber('field_name', $attributes);
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
```php
$group->addEmail('field_name', $attributes);
```
### Url
```php
$attributes = [
    'default_value' => '',
    'placeholder' => '',
];
```
```php
$group->addUrl('field_name', $attributes);
```
### Password
```php
$attributes = [
    'placeholder' => '',
    'prepend' => '',
    'append' => '',
];
```
```php
$group->addPassword('field_name', $attributes);
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
```php
$group->addRange('field_name', $attributes);
```
### Wysiwyg Editor
```php
$attributes = [
    'tabs' => 'all' || 'visual' || 'text',
    'toolbar' => 'full' || 'basic',
    'media_upload' => 1,
    'default_value' => '',
    'delay' => 0
];
```
```php
$group->addWysiwyg('field_name', $attributes);
```
### oEmbed
```php
$attributes = [
    'width' => '',
    'height' => '',
];
```
```php
$group->addOembed('field_name', $attributes);
```
### Image
```php
$attributes = [
    'return_format' => 'array' || 'id' || 'url',
    'preview_size' => 'thumbnail',
    'library' => 'all' || 'uploadedTo',
    'min_width' => 0,
    'min_height' => 0,
    'min_size' => 0,
    'max_width' => 0,
    'max_height' => 0,
    'max_size' => 0,
    'mime_types' => '' // e.g. 'jpg,jpeg,png'
];
```
```php
$group->addImage('field_name', $attributes);
```
### File
```php
$attributes = [
    'return_format' => 'array' || 'id' || 'url',
    'library' => 'all' || 'uploadedTo',
    'min_size' => 0,
    'max_size' => 0,
    'mime_types' => ''
];
```
```php
$group->addFile('field_name', $attributes);
```
### Gallery (Pro)
```php
$attributes = [
    'library' => 'all' || 'uploadedTo',
    'min' => 0,
    'max' => 0,
    'min_width' => 0,
    'min_height' => 0,
    'min_size' => 0,
    'max_width' => 0,
    'max_height' => 0,
    'max_size' => 0,
    'mime_types' => '',
    'insert' => 'append' || 'prepend',
];
```
```php
$group->addGallery('field_name', $attributes);
```
### Link
```php
$attributes = [
	'return_format'	=> 'array' || 'id',
];
```
```php
$group->addLink('field_name', $attributes);
```
### Post Object
```php
$attributes = [
    'post_type' => string || array(), // Use string for one post_type, array for multiple post_types
    'taxonomy' => 'taxonomy-slug:item-slug' || ['taxonomy-slug:item-slug'], // Use string for one taxonomy, array for multiple taxonomies
    'allow_null' => 0,
    'multiple' => 0,
    'return_format' => 'object' || 'id',
    'ui' => 1,
];
```
```php
$group->addPostObject('field_name', $attributes);
```
### Page Link
```php
$attributes = [
    'post_type'	=> string || array(), // Use string for one post_type, array for multiple post_types
    'taxonomy' => 'taxonomy-slug:item-slug' || ['taxonomy-slug:item-slug'], // Use string for one taxonomy, array for multiple taxonomies
    'allow_null' => 0,
    'multiple' => 0,
    'allow_archives' => 1,
];
```
```php
$group->addPageLink('field_name', $attributes);
```
### Relationship
```php
$attributes = [
    'post_type'	=> string || array(), // Use string for one post_type, array for multiple post_types
    'taxonomy' => 'taxonomy-slug:item-slug' || ['taxonomy-slug:item-slug'], // Use string for one taxonomy, array for multiple taxonomies
    'min' => 0,
    'max'  => 0,
    'filters' => array('search', 'post_type', 'taxonomy'),
    'elements' => array('featured_image'),
    'return_format' => 'object' || 'id',
];
```
```php
$group->addRelationship('field_name', $attributes);
```
### Taxonomy
```php
$attributes = [
    'taxonomy' => string,
    'field_type' => 'checkbox' || 'multi_select' || 'radio' || 'select',
    'multiple' => 0,
    'allow_null' => 0,
    'return_format' => 'id' || 'object',
    'add_term' => 1,
    'load_terms' => 0,
    'save_terms' => 0
];
```
```php
$group->addTaxonomy('field_name', $attributes);
```
### User
```php
$attributes = [
    'role' => array() // array with user roles,
    'multiple' => 0,
    'allow_null' => 0,
];
```
```php
$group->addUser('field_name', $attributes);
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
```php
$group->addSelect('field_name', $attributes);
```
### Checkbox
```php
$attributes = [
    'layout' => 'vertical' || 'horizontal',
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
```php
$group->addCheckbox('field_name', $attributes);
```
### Radio
```php
$attributes = [
    'layout' => 'vertical' || 'horizontal',
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
```php
$group->addRadio('field_name', $attributes);
```
### True / False
```php
$attributes = [
    'default_value' => 0,
    'message' => '',
    'ui' => 0,
    'ui_on_text' => '',
    'ui_off_text' => '',
];
```
```php
$group->addTrueFalse('field_name', $attributes);
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
```php
$group->addGoogleMap('field_name', $attributes);
```
### Date Picker
```php
$attributes = [
    'display_format' => 'd/m/Y',
    'return_format' => 'd/m/Y',
    'first_day' => 1
];
```
```php
$group->addDatePicker('field_name', $attributes);
```
### Time Picker
```php
$attributes = [
    'display_format' => 'g:i a',
    'return_format' => 'g:i a',
];
```
```php
$group->addTimePicker('field_name', $attributes);
```
### Date Time Picker
```php
$attributes = [
    'display_format' => 'd/m/Y g:i a',
    'return_format' => 'd/m/Y g:i a',
    'first_day' => 1
];
```
```php
$group->addDateTimePicker('field_name', $attributes);
```
### Color Picker
```php
$attributes = [
    'default_value'	=> 0,
];
```
```php
$group->addColorPicker('field_name', $attributes);
```
### Message
```php
$attributes = [
    'message' => '', // Can also be added to the function, see below
    'esc_html' => 0,
    'new_lines' => 'wpautop',
];
```
```php
$group->addMessage('field_name', 'message', $attributes);
```
### Tab
```php
$attributes = [
    'placement'	=> 'top',
    'endpoint' => 0
];
```
```php
$group->addTab('field_name', $attributes);
```
### Group
```php
$attributes = [
    'sub_fields' => array(),
    'layout' => 'block'
];
```
```php
$group->addGroup('field_name', $attributes);
```
### Repeater
```php
$attributes = [
    'sub_fields' => array(),
    'min' => 0,
    'max' => 0,
    'layout' => 'table' || 'row' || 'block',
    'button_label' => '',
    'collapsed' => 'sub_field_name' // Shows the specified sub field when a repeater row is collapsed.
];
```
```php
$group
	->addRepeater('field_name', $attributes)
	// Repeater fields
	->endRepeater();
```
**Layouts**

The repeater fields can be shown in 3 different ways in the admin. 

- `Table`: all sub fields will be shown on one line. Works great with a few sub fields. 
- `Row`: all sub fields will be shown underneath each other, but you can’t control the width, like normal fields. 
- `Block`: the sub fields are shown just like other fields are visible. You can control the wrapper width as well. Works best for more complex repeaters. 

### Flexible Content
```php
$attributes = [
    'layouts' => array(),
	'min' => '',
    'max' => '',
	'button_label'=> "Add Row",
];
```
```php
$group
	->addFlexibleContent('field_name', $attributes)
	->addLayout('layout_name', $layout_aatributes)
	->addLayout($other_group);
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

### Custom field
```php
$group->addField('field_name', 'field_type', $default_attributes);
```

**Example: Gravity Forms field**
```php
$group->addField('form', 'gravity_forms_field', $default_attributes);
```

## Conditional logic
You can add conditional logic to a field by adding some array checks.

**Simple example**
```php
'conditional_logic' => [
	[
		[
			'field' => 'field_name',
			'operator' => '==',
			'value' => '1',
		],
	],
];
```

**Example with multiple fields any**
```php
'conditional_logic' => [
	[
		[
			'field' => 'field_name',
			'operator' => '==',
			'value' => '1',
		],
	],
	[
		[
			'field' => 'other_field_name',
			'operator' => '==',
			'value' => '1',
		],
	],
],
```

**Example with multiple fields all**
```php
'conditional_logic' => [
	[
		[
			'field' => 'field_name',
			'operator' => '==',
			'value' => '1',
		],
		[
			'field' => 'other_field_name',
			'operator' => '==',
			'value' => '1',
		],
	],
],
```

## Reuse fields
Whenever you want to reuse fields, you can make a new FieldsBuilder containing all the fields you want to reuse. With the `->addFields($fields)` function you can implement the field in other field groups.

Example: 
```php
$reused_fields = new FieldsBuilder( 'reused_fields' );
$reused_fields
	->addText( 'text_field' )
	->addTextarea( 'textarea_field' );
	
$sample_group_one = new FieldsBuilder( 'sample_group_one' );
$sample_group_one
	->addFields( $reused_fields )
	->addImage( 'sample_image_field' )
	->setLocation('post_type' == 'page' );

$sample_group_two = new FieldsBuilder( 'sample_group_two' );
$sample_group_two
	->addText( 'sample_text_field' )
	->addFields( $reused_fields )
	->setLocation('post_type' == 'post' );
```	

# Hide WordPress fields
It is possible to hide WordPress fields when adding the 'hide on screen' option to a group. Important note: this only works when `hide_on_screen` is added to the first field group on the admin page. Use `menu_order` in the group attributes to set the order of the field groups.

```php
$group->setGroupConfig('hide_on_screen', [
	'the_content',
	'permalink',
	'excerpt',
	'custom_fields',
	'discussion',
	'comments',
	'revisions',
	'slug',
	'author',
	'format',
	'page_attributes',
	'featured_image',
	'categories',
	'tags',
	'send-trackbacks',
]);
```

