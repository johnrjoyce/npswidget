# Widget Usage #
The NPS Widget can be embedded in any web page by inserting the following lines in the page:

```
<script type="text/javascript">
   nps_project_id = 3;
   nps_project_name = "My Project";
   nps_background_url = "http://<path_to_background>";
   nps_background_top_url = "http://<path_to_background_top>";
   nps_background_bottom_url = "http://<path_to_background_bottom>";
   nps_border = "y";
   nps_font_color = "336699";
</script>

<script type="text/javascript" src="http://<widgethost>/nps_widget/nps_widget-1.0.js"></script>
```


# Basic Parameters #

  * ps\_project\_id - Project ID
  * ps\_project\_name - Project name descriptor

At a minimum an end user should include both the "nps\_project\_id" and "nps\_project\_name" parameters.

The project ID is the numeric ID value that is associated with the project name in the MySQL database project table.

The project name descriptor is displayed within the text that appears above the NPS recommendation rating scale in the widget. The default text reads: "How likely is it that you would recommend this to a friend or colleague?" But with the project name descriptor parameter specified by the end user, using our example above the text would read: "How likely is it that you would recommend My Project to a friend or colleague?"

# Optional Parameters #

There are several optional parameters that are available to users with version 1.0 of the widget. These parameters are used to specify widget background(s), border and font color.

  * ps\_background\_url - URL of a background image for the entire widget
  * ps\_background\_top\_url - URL of a background image for the top (rating) portion of the widget
  * ps\_background\_bottom\_url - URL of a background image for the bottom (feedback) portion of the widget
  * ps\_border - Solid black border
  * ps\_font\_color - Font color for text
  * ps\_language - Language to use ([more information](WidgetLanguages.md))

The background image size for the entire widget should be at least 219 x 245 pixels. An image for the top portion of the widget should be at least 219 x 68 pixels and for the bottom at least 219 x 177 pixels. These sizes are a guide for when you may want to have a specific, non-repeating image as the background for the entire, top and/or bottom of the widget. If, for example, all you want is a solid blue background for the widget then you only need a very small image of, let's say, 1 x 1 pixels and the image will be repeated to create a background for the specified area of the widget. If the nps\_background\_url parameter is specified along with the top and/or bottom background parameter(s) the nps\_background\_url parameter takes precedence and the top and/or bottom background image(s) will not be displayed.

The border parameter is specified by "y". A value of "y" indicates that a 1 pixel wide solid black border should be displayed. This parameter works in conjunction with the background image parameters. If the border parameter is specified along with a background image parameter then a border will be displayed around the image. If the border parameter is not specified but a background image parameter is specified then no border will be displayed around the background image. Finally, if the border parameter is not specified and no background image parameter is specified as well, then the default light grey border will be displayed around the default white background.

The font color is entered in standard RGB hexadecimal value format.


# Generate Starting Code #

When creating the NPS project via the admin interface, an initial code snippet is provided to use as the basis for the widget deployment. This code can then be modified to customise the widget as required.


# Usage Examples #

This example will set the background of the entire widget to the specified image and display a solid black border.

```
<script type="text/javascript">
   nps_project_id = 3;
   nps_project_name = "My Project";
   nps_background_url = "http://<widgethost>/nps_widget/backgrounds/bubbles.jpg";
   nps_border = "y";
</script>

<script type="text/javascript" src="http://<widgethost>/nps_widget/nps_widget-1.0.js"></script>
```

This example will set the background of the top and bottom portions of the widget to the specified images.

```
<script type="text/javascript">
   nps_project_id = 3;
   nps_project_name = "My Project";
   nps_background_top_url = "http://<widgethost>/nps_widget/backgrounds/green1x1.gif";
   nps_background_bottom_url = "http://<widgethost>/nps_widget/backgrounds/green1x1.gif";
</script>

<script type="text/javascript" src="http://<widgethost>/nps_widget/nps_widget-1.0.js"></script>
```

This example will set the font color to blue. No background or border parameter is specified in this example so the default white background will be displayed along with the default dotted border.

```
<script type="text/javascript">
   nps_project_id = 3;
   nps_project_name = "My Project";
   nps_font_color = "1144cc";
</script>

<script type="text/javascript" src="http://<widgethost>/nps_widget/nps_widget-1.0.js"></script>
```