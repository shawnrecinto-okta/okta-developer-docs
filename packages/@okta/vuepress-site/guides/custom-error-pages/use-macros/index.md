---
title: Use Macros
---
The following macros contain the configuration parameters for certain page elements. These macros inject specific content or functionality automatically.

The graphic highlights and numbers the macros in the html editor, and then displays the corresponding number on the error page for each macro and what text or image is affected.

> Note: When you replace a macro with other text, be sure to replace both the brackets and the text.

![Macros on Error Page](/img/custErrorPage.png "Macros on Error Page")

1 <span v-pre>`{{orgName}}`</span> 
This macro controls the org name title that appears on the error page's browser tab. You can make changes to this text by removing the macro and adding your own.

For example:
```javascript
`<title>Your Text Here - {{errorSummary}}</title>`
```

2 <span v-pre>`{{errorSummary}}`</span>
This macro controls the error title text that appears on the error page's browser tab. You can make changes to this text by removing the macro and adding your own.

For example:
```javascript
`<title>{{orgName}} - Your Text Here</title>`
```

> Note: Removing this <span v-pre>`{{errorSummary}}`</span> macro doesn't affect the <span v-pre>`{{errorSummary}}`</span> macro (6) lower on the page.

3 <span v-pre>`{{bgImageUrl}}`</span>
This macro controls the background image of the entire error page. You can configure which background image this macro displays using the **Sign-In Configuration** option accessed by selecting **Customization**, and then **Appearance** from the Developer Console. 
You can also change which background image appears by removing the macro in the HTML editor and adding your own background image URL. 

For example:
`<div class="login-bg-image" style="background-image: url('https://example.com//YourBackgroundImage.png)"></div>`

4 <span v-pre>`{{orgLogo}}`</span>
This macro controls the org logo image that appears. You can configure which org logo this macro displays using the **Organization Logo** option accessed by selecting **Customization**, and then **Appearance** from the Developer Console. You can also change which image appears by removing the macro in the HTML editor and adding your own image URL.

For example:
`<img alt="{{orgName}}" src="https://example.com//SomeOtherImage.png" class="org-logo">`

5 <span v-pre>`{{httpStatusCode}}`</span>
This macro controls the display of the standard HTTP error code, if there is one. If there isn't one, a generic error triangle logo (alert.png) is used instead. You can change this default image.

For example:
`<img alt="{{errorSummary}}" src="https://example.com//yourimage.png" />`

6 <span v-pre>`{{errorSummary}}`</span>
This macro controls the error title text that appears on the error page. You can make changes to this text by removing the macro and adding your own.

For example:
`<h2 class="o-form-title">Error Title Text Here</h2>`

7 <span v-pre>`{{{errorDescription}}}`</span>
This macro controls the display of the error description. You can replace this description by removing the macro and adding your own text.

For example:
`<p class="o-form-explain">There was a problem with your sign-in. Contact your system administrator.</p>`

8 <span v-pre>`{{back}}`</span>
This macro controls the text on the back button. The button takes the user back to the sign-in page when clicked. You can replace the button text by removing the macro and adding your own text.

For example:
 `<a href="/" class="button">Take Me Back!</a>`

9 <span v-pre>`{{technicalDetails}}`</span>
This macro controls the display of additional error codes, if there are any. See [Okta Error Codes](reference/error_codes/) for more information.

<NextSectionLink/>