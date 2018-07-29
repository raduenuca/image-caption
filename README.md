[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/raduenuca/image-caption)

# \<image-caption\>

Adds caption and alt to an image using the Computer Vision API from Microsoft Cognitive Services

```html
<image-caption api-key="Your API Key"
               api-region="Your API Region"
               language="en|ja|pt|zh"
               src="Image URL">
</image-caption>
```

## Prerequisites

To use the Computer Vision API, you need a [subscription key](https://docs.microsoft.com/en-us/azure/cognitive-services/computer-vision/vision-api-how-to-topics/howtosubscribe).

## Demo

<!--
```
<!-- START-HIDDEN-SECTION: Add imports and styling here. -->
<script src="../webcomponentsjs/webcomponents-lite.js"></script>
<link rel="import" href="image-caption.html">
<style is="custom-style">
        .form-style {
            margin: 10px auto;
            max-width: 400px;
            padding: 20px 12px 10px 20px;
            font: 13px "Lucida Sans Unicode", "Lucida Grande", sans-serif;
        }

        .form-style li {
            padding: 0;
            display: block;
            list-style: none;
            margin: 10px 0 0 0;
        }

        .form-style li p {
            margin-top: 0;
            color: #bbb;
            font-style: italic;
            margin-bottom: 2px;
            font-size: xx-small;
        }

        .form-style label {
            margin: 0 0 3px 0;
            padding: 0;
            display: block;
            font-weight: bold;
        }

        .form-style input[type=text], select {
            box-sizing: border-box;
            -webkit-box-sizing: border-box;
            -moz-box-sizing: border-box;
            border: 1px solid #BEBEBE;
            padding: 7px;
            margin: 0;
            -webkit-transition: all 0.30s ease-in-out;
            -moz-transition: all 0.30s ease-in-out;
            -ms-transition: all 0.30s ease-in-out;
            -o-transition: all 0.30s ease-in-out;
            outline: none;
        }

        .form-style input[type=text]:focus,
        .form-style select:focus {
            -moz-box-shadow: 0 0 8px #88D5E9;
            -webkit-box-shadow: 0 0 8px #88D5E9;
            box-shadow: 0 0 8px #88D5E9;
            border: 1px solid #88D5E9;
        }

        .form-style .field-long {
            width: 100%;
        }

        .form-style .field-select {
            width: 100%;
        }

        .form-style input[type=button] {
            background: #4B99AD;
            padding: 8px 15px 8px 15px;
            border: none;
            color: #fff;
        }

        .form-style input[type=button]:hover {
            background: #4691A4;
            box-shadow: none;
            -moz-box-shadow: none;
            -webkit-box-shadow: none;
        }

        .form-style .required {
            color: red;
        }
    </style>
<!-- END-HIDDEN-SECTION: Add the visible part of the demo below. -->
<div class="vertical-section-container centered">
    <h3>image-caption demo</h3>
    <form>
        <ul class="form-style">
            <li><p>Adds caption and alt to an image using the Computer Vision API from Microsoft Cognitive Services</p>
            </li>
            <li>
                <label for="apiKey">Api Key <span class="required">*</span></label>
                <input type="text" id="apiKey" class="field-long"/>
                <p>To use the Computer Vision API, you need a <a
                        href="https://docs.microsoft.com/en-us/azure/cognitive-services/computer-vision/vision-api-how-to-topics/howtosubscribe">subscription key</a>.</p>
            </li>
            <li>
                <label for="apiRegion">Api Region <span class="required">*</span></label>
                <select id="apiRegion" class="field-select">
                    <option value="westus">West US</option>
                    <option value="eastus2">East US 2</option>
                    <option value="westcentralus" selected>West Central US</option>
                    <option value="westeurope">West Europe</option>
                    <option value="southeastasia">Southeast Asia</option>
                </select>
                <p>Your subscription keys are valid for only one of these regions</p>
                <p>If you sign up using the Computer Vision free trial, your subscription keys are valid for the West
                    Central US region</p>
            </li>
            <li>
                <label for="language">Language</label>
                <select id="language" class="field-select">
                    <option value="en">English</option>
                    <option value="ja">日本語</option>
                    <option value="pt">Português</option>
                    <option value="zh">中文简体</option>
                </select>
                <p>Supported languages</p>
            </li>
            <li>
                <label for="imgSrc">Image URL <span class="required">*</span></label>
                <input type="text" id="imgSrc" class="field-long"/>
                <p>Supported image formats: JPEG, PNG, GIF, BMP.</p>
                <p>Image file size must be less than 4MB.</p>
                <p>Image dimensions should be greater than 50 x 50.</p>
            </li>
            <li>
                <input id="processBtn" type="button" value="Process Image"/>
            </li>
        </ul>
    </form>
    <image-caption></image-caption>
</div>
<script>
    const processButton = document.getElementById('processBtn');
    const subscriptionKeyInput = document.getElementById('apiKey');
    const subscriptionRegionInput = document.getElementById('apiRegion');
    const languageSelect = document.getElementById('language');
    const imageSrcInput = document.getElementById('imgSrc');

    const imageCaption = document.getElementsByTagName('image-caption')[0];

    processButton.onclick = (event) => {
        imageCaption.apiKey = subscriptionKeyInput.value;
        imageCaption.apiRegion = subscriptionRegionInput.value;
        imageCaption.language = languageSelect.value;
        imageCaption.src = imageSrcInput.value;
    };
</script>
```
-->

## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your element locally.

## Viewing Your Element

```
$ polymer serve
```

## License

[MIT](https://opensource.org/licenses/MIT)
