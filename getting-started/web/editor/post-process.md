---
title: Post-processing
meta_title: Post-processing the editor content | Kendo UI Documentation
meta_description: The documentation guide will show how to post-process the Editor content so that it fits your needs.
slug: gs-web-editor-post-process
relatedDocs: api-web-editor
tags: getting-started,web
ordinal: 3
publish: true
---

# Post-processing the editor content

## Post-processing the editor value before sending it to the server

If the editor is within a `<form>` element, a good moment to post-process its contents is right before the form is posted to the server, in the `submit` event.

### Example - remove all paragraphs before posting to server
    <form>
      <textarea id="comments"></textarea>

      <button type="submit">Submit</button>
    </form>

    <script>
    var comments = $("#comments");

    comments.kendoEditor({ encoded: false });

    $("form").on("submit", function() {
      var value = comments.data("kendoEditor").value();

      // strip all paragraphs
      value = value
        .replace(/<p[^>]*>/g, "")
        .replace(/<\/p>/g, "<br />");

      comments.val(value);
    });
    </script>
