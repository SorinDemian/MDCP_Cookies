## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/ssepty10/MDCP_Cookies/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Cookies

<button onclick="alertCookie()">Show cookies</button> <br>
<button onclick="alertCookieValue()">Show cookie colorDepth</button> <br>
<button onclick="doOnce()">Only once</button> <br>
<button onclick="resetOnce()">Reset only once cookie</button> <br>
<button onclick="checkExists()">color_depth?</button>

<script> 
  document.cookie = "color_depth=" + window.screen.colorDepth; 
  document.cookie = "user_agent=" + navigator.userAgent; 
  
  const cookieValue = document.cookie
  .split('; ')
  .find(row => row.startsWith('color_depth='))
  .split('=')[1];
  
  function alertCookie() { 
    alert(document.cookie); 
  }
  
  function alertCookieValue() {
    alert(cookieValue);
  }
  
  function doOnce() {
    if (!document.cookie.split('; ').find(row => row.startsWith('oneTime'))) {
      alert("~One time offer~");
      document.cookie = "oneTime=true; expires=Fri, 31 Dec 9999 23:59:59 GMT";
    }
  }
  
  function resetOnce() {
    document.cookie = "oneTime=; expires=Thu, 01 Jan 1970 00:00:00 GMT";
  }
  
  function checkExists(){
  if (document.cookie.split(';').some((item) => item.trim().startsWith('color_depth='))) {
    console.log('The cookie "color_depth" exists (ES6)')
    alert('The cookie "color_depth" exists (ES6)');
    }
  }
  
</script>

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/ssepty10/MDCP_Cookies/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
