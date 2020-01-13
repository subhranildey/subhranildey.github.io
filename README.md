# glegoux.com

I use [GitHub Pages](https://pages.github.com/) with Jekyll to render this website available at https://glegoux.com .
Related resources for the articles are in another repository: https://github.com/glegoux/articles-glegoux-com .

<table>
  <tr>
    <td>
        <img src="https://github.com/glegoux/glegoux.github.io/blob/master/static/img/glegoux-com.jpg?raw=true"
             alt="glegoux.com blof" />
    </td>
  </tr>
</table>

### Technical stack

This source code generates static web pages, that are served by a static web server.

- Web Static Server: GitHub.com
- Static Site Generator: Jekyll - https://jekyllrb.com with plugins: 
  - https://pages.github.com/versions
- Templating Language: Liquid - https://shopify.github.io/liquid
- Text-to-HTML Conversion: Markdown - https://daringfireball.net/projects/markdown
- CSS Extension: Sass - https://sass-lang.com
- JavaScript Library: JQuery - https://jquery.com
- JavaScript for Mathematics: Mathjax - https://www.mathjax.org
- Toolkit for HTML, CSS and JS: Bootstrap - https://getbootstrap.com
- Data-interchange format: JSON - http://www.json.org and YAML - https://yaml.org

### Monitoring & Checher

- Health Checker: http://status.glegoux.com
- TLS/SSL Certificate Checker: https://www.digicert.com/help
- Page Speed Checker: https://developers.google.com/speed/pagespeed/insights

### Known issues

- The url https://www.glegoux.com has an invalid TLS/SSL certificate, using wildcard certificate is undadvised and there is a GitHub open issue https://github.com/isaacs/github/issues/1675 
- The contents of iframe are not translated (see https://glegoux.com/contact/email page)
- The iframes are not resized when completing a web form for example (see https://glegoux.com/contact/email page)
- The static web server shows the list of its content (see https://glegoux.com/website)
- URL without end of slash are preferred else you could have 404 HTTP response (see https://glegoux.com/home/)

### References

- https://help.github.com/categories/customizing-github-pages
- https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll
