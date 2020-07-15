# e-mail service

![app-mockup](email.gif "app-mockup")

### Technology
* HTML
* CSS
* Adobe Photoshop CC 2019


### Create attractive, responsive, HTML Emails, that work in over 30 combinations of the most commonly used email clients
* HTML e-mail are not web pages
* This is because the mount of each HTML is CSS support in each email client varies.
* Since most email clients don’t support a full range of HTML and CSS we need to use tables  which is an older layout structure in order to get our content to work right in all the different clients
* When designing responsive design inside of a browser using strong HTML
* We have the ability to take containers such as div tags and other elements
* And when we resize the browser we can move those individual elements
* Now when a table size changing all of <td> will get smaller
* But we can’t actually change the relationship of the individual <td>
* They’re locked inside of that tables structure so we can’t take one <td> for example and move it independent of all of the other ones.
### Solve the problem
* So to get around this limitation of what we’re going to do is put individual content into full tables that have a single cell inside of them.
* And then when the width changes we’re going to move the entire tables around.

### Setting a DOCTYPE
1. Now some e-mail clients and HTML e-mail services will recommend that you don’t use any doctype
* None
2. Other will recommend you use the XHTML 1.0 transitional in this case HTML need an attribute for the xml name space 
* XHTML 1.0 Transitional
```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 1.0 Transitional//EN" "http://www.w3.org/TR/html11/DTD/xhtml11-transitional.dtd">

<html xmlns="http://www.w3.org/1999/xhtml">
```
3. Other will recommend you use the HTML 4.0 since some email client will actually strip whatever doctype you have.
* HTML 4.01
```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/1999/REC-html401-19991224/strict.dtd">
```

### Troubleshooting want to make the design responsive
* we're going to work on adding some inline CSS styling and ranging the layout and elements based on screen size.
* Now in the document we're all starting from we have a style element up in the heading area.
Let's first add css as 3 media queries.

* So exsample
* Once we get under 510 pixels we're going to set the width to 100 percent.
* Add the important tag and the next we're going to target the <td> inside of the table container

```
@media only screen and (max-width: 510px) {

        table.container { width: 100% !important; }
}
```
* Now we're going to target the image inside of the logo row
* So this is going to do is hide the logo graphic and then replaced the background graphic of the <td> with the medium sized logo
```
 @media only screen and (max-width: 660px) {

        table.container { width: 480px !important; }
                
        td.logo img { display: none; }
        td.logo  { background: #fff url(images/logo_medium.gif) no-repeat 10px 10px; height: 45px; }
}
```

## Dark mode
The CSS selectors are prefers-color-scheme, [data-ogsc], and [data-ogsb] and we will be using these selectors to update the dark mode 

### Enable dark mode in email clients
To tell email or browser clients that dark mode is available in this HTML file, we need to add some lines of code to the <head> and <style> sections.
In the <head> tag where all the <meta> tags are defined, add these lines of code:

```
<meta name="color-scheme" content="light dark">
<meta name="supported-color-schemes" content="light dark">
```
And under the <style> tag add:

```
:root {
color-scheme: light dark;
supported-color-schemes: light dark;
}
```
### Additional Resources
1. <a href="https://www.youtube.com/user/chrisconverse" target="_blank">Chris Converse</a>
2. <a href="https://help.designmodo.com/article/postcards-dark-mode/" target="_blank">Postcards-dark-mode</a>
3. <a href="https://www.freecodecamp.org/news/dark-mode-in-html-email-everything-you-need-to-know/amp/" target="_blank">Freecodecamp</a>



