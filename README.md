# jquery-squarecam

## Description
Creates two control buttons on the desired div: 'Start' opens the webcama and 'Capture' gets the current webcam image and crops it with the same height and witdh, according to the 'size' parameter.

## Mandatory requirements
* [jQuery](https://jquery.com/)

## Installation
Include script *after* the jQuery library:

```html
<script src="/path/to/jquery-squarecam.js"></script>
```

## Usage

Apply the **jSquarecam()** function to the desired div, passing the target image identifier as first parameter and setting the required configuration options:

```javascript
$("#map_div_id").jSquarecam( 'img_id', { options } );
```


## Configuration Options

### `size`
(Integer). Width/Height (in pixels) for the webcam target. Default value: `400`,

### `btStartMsg`
String to be shown in the start button. Defaut value: `Start WebCam`.

### `btCaptureMsg`
String to be shown in then capture button. Defaut value: `Capture`.

### `hideImage`
Set to `true` if you want to hide the image object while webcam is on. Default value: `false`.


## Example

```html

	<!-- HTML -->

    <div id="squarecam"></div>
    <img id="imagecam" />

    <!-- SCRIPTS -->

    <script type="text/javascript">

		$(function() {

		    $("#squarecam").squarecam( 
		        'imagecam', 
		        {
		          size:         200,
		          btStartMsg:   '<span class="glyphicon glyphicon-camera" aria-hidden="true"></span>',
		          btCaptureMsg: '<span class="glyphicon glyphicon-ok" aria-hidden="true"></span>',
		          hideImage:    true,
		        } 
		    );

		});

	</script>
```

## License
Released under the [MIT license](https://opensource.org/licenses/MIT).
