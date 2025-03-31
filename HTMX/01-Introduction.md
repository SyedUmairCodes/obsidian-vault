# Introduction to HTMX

HTMX is a JavaScript library that extends HTML and allows you to add new attributes to HTML elements so that you won't need JavaScript. It allows you add new abilities to common HTML elements or change the default behavior of these components.

HTMX primarily deals in HTTP requests using AJAX, sending requests and then rendering the content received. HTMX is a decoupled front-end framework just like React and Vue but it focuses on updating the UI using AJAX rather using components to display data.

In a full-stack app, HTMX is almost useless if you don't have a tight back-end and the requests it makes require HTML to be returned as the response which is not always the case in a full-stack app.

The attributes that HTMX provides us with start with the `hx-` prefix and can be added to any HTML element.