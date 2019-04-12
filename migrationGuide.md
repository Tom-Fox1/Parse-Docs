# Migration Guide
This is a guide to outline the process of migrating content from the old docs to here for anyone wishing to contribute.

The most important point to be aware of is that the new docs have a unified format with one set of copy across all the client SDKs. Notes realting to a specific SDK can be added, such as to mention that a feature is not implemented on all of the SDKs, however a universal explanation should be used where possible.

## Formatting
Please follow the formatting conversions for specific markdown elements between the old and new docs.

### Headers
✅ No changes necessary

    # Level 1 Header
    ## Level 2 Header
    ### Level 3 Header

Note that only level 1 and 2 headers will appear in the table of contents. Unlike in the existing docs which shows level 1, 3 and 3.

### Paragraph Text
✅ No changes necessary

For normal text, just type your paragraph on a single line.

    This is some paragraph text. Exciting, no?

Make sure the lines above and below your paragraph are empty.

### Code Samples

For code samples:

❗️Significant changes needed

In the existing docs code samples for multiple languages are enclosed with html which is no longer needed:

__Before:__

```
<div class="language-toggle">
	<pre><code class="bash">
	curl -X PUT \
	  -H "X-Parse-Application-Id: <span class="custom-parse-server-appid">${APPLICATION_ID}</span>" \
	  -H "X-Parse-Master-Key: ${MASTER_KEY}" \
	  -d "{\"params\":{\"winningNumber\":43}}"
	  <span class="custom-parse-server-protocol">https</span>://<span class="custom-parse-server-url">YOUR.PARSE-SERVER.HERE</span><span class="custom-parse-server-mount">/parse/</span>config
	</code></pre>
	
	<pre><code class="javascript">
  var request = require('request');
  return request({
    method: 'PUT',
    url: Parse.serverURL + '/config',
    headers: {
      'X-Parse-Application-Id': Parse.applicationId,
      'X-Parse-Master-Key': Parse.masterKey
    },
    json: true,
    body: {
      params: { winningNumber: 43 }
    }
  })
	</code></pre>
</div>
```

__After:__

```
	```bash
	curl -X PUT \
	  -H "X-Parse-Application-Id: <span class="custom-parse-server-appid">${APPLICATION_ID}</span>" \
	  -H "X-Parse-Master-Key: ${MASTER_KEY}" \
	  -d "{\"params\":{\"winningNumber\":43}}"
	  <span class="custom-parse-server-protocol">https</span>://<span class="custom-parse-server-url">YOUR.PARSE-SERVER.HERE</span><span class="custom-parse-server-mount">/parse/</span>config
	```

	```javascript
  var request = require('request');
  return request({
    method: 'PUT',
    url: Parse.serverURL + '/config',
    headers: {
      'X-Parse-Application-Id': Parse.applicationId,
      'X-Parse-Master-Key': Parse.masterKey
    },
    json: true,
    body: {
      params: { winningNumber: 43 }
    }
  })
	```
```

Code samples will appear in the dark area to the right of the main text. We recommend positioning code samples right under headers in your markdown file.

For the full list of supported languages, see [rouge](https://github.com/jneen/rouge/wiki/List-of-supported-languages-and-lexers).

### Code Annotations

For code annotations:

    > This is a code annotation. It will appear in the area to the right, next to the code samples.

Code annotations are essentially the same thing as paragraphs, but they'll appear in the area to the right along with your code samples.

### Formatting code annotations (right column) with its explanation (center column)

In order to correctly format the code in the right column with the text in the center column the code snippet should go first, e.g.
```
    # My Title

    ## My Subtitle

    ```csharp
        Code snippet
    ```

    ```java
        Code snippet
    ```

    ```php
    <?php
        Code snippet
    ?>
    ```

    ```ruby
    #Code snippet
    ```

    Whatever that goes in the center column. Lorem ipsum
```
Putting the content for the center column first and the code snippet afterwards will cause the code snippet to be aligned with the last line of the center column, if the code snippet goes first, then the code is aligned with the first line of the center column.

### Tables

Slate uses PHP Markdown Extra style tables:

```markdown
Table Header 1 | Table Header 2 | Table Header 3
-------------- | -------------- | --------------
Row 1 col 1 | Row 1 col 2 | Row 1 col 3
Row 2 col 1 | Row 2 col 2 | Row 2 col 3
```

Note that the pipes do not need to line up with each other on each line.

If you don't like that syntax, feel free to use normal html `<table>`s directly in your markdown.

### Formatted Text

    This text is **bold**, this is *italic*, this is an `inline code block`.

You can use those formatting rules in tables, paragraphs, lists, wherever, although they'll appear verbatim in code blocks.

### Lists

    1. This
    2. Is
    3. An
    4. Ordered
    5. List

    * This
    * Is
    * A
    * Bullet
    * List

### Links

    This is an [internal link](#error-code-definitions), this is an [external link](http://google.com).

### Notes and Warnings

You can add little highlighted warnings and notes with just a little HTML embedded in your markdown document:

    <aside class="notice">
    You must replace `meowmeowmeow` with your personal API key.
    </aside>

Use `class="notice"` for blue notes, `class="warning"` for red warnings, and `class="success"` for green notes.

### Need Help?

If you have trouble with any of the syntax, or if it's confusing, let us know by filing an issue. Thanks!
