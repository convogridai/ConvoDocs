# WordPress Integration

If you are looking to integrate your website with WordPress, you have 3 options

### Method 1. Include in the Site Footer in your Theme Builder

Theme builders such as Elementor Pro or Divi provide the option to add code to the site footer

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>Elementor Custom Code</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>Divi Theme Options >Integration</p></figcaption></figure>

Simply add the provided script tag to your website’s HTML footer using your theme builder.

```javascript
 <script id="convobot_extension" fallback-to-default="true" right-margin="3vw" bottom-margin="3vh"  src="https://content-beta.convogrid.ai/script/extension.v.0.1.1.min.js"></script>
```

### Method 2. Using a code editor plugin

By using plugins like Code Snippets or WP Code, you will be able to add the snippet directly to the site footer

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption><p>Code Snippets</p></figcaption></figure>

Simply add the script tag to your website’s HTML footer using your code plugin

```javascript
 <script id="convobot_extension" fallback-to-default="true" right-margin="3vw" bottom-margin="3vh"  src="https://content-beta.convogrid.ai/script/extension.v.0.1.1.min.js"></script>
```

### Method 3. Edit the `Functions.php` file in your WP theme (Advanced)

You can also use this PHP script to embed the widget directly into the site through the functions.php file. Make sure to have a child theme to avoid data deletion when updating the theme.

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption><p>Child Theme Functions.php file</p></figcaption></figure>

Add the function below to the file using the theme file editor, or by manually editing the PHP file through your file manager.

{% code title="Functions.php" overflow="wrap" %}
```php
function embed_convobot_script() {
    $script = '<script id="convobot_extension" fallback-to-default="true" right-margin="3vw" bottom-margin="3vh"  src="https://content-beta.convogrid.ai/script/extension.v.0.1.1.min.js"></script>';
    echo $script;
}

add_action( 'wp_footer', 'embed_convobot_script' );
```
{% endcode %}



Looking for styling options? Please refer [.](./ "mention").



