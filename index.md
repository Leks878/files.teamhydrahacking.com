---
# Front matter
---
<html lang="en-US">
 <body>
 
    <ul class="list  list--repos">
        <li class="item  item--repo">
            <a href="#">Team Hydra Hacking Docs & Resources</a>
        </li>
    </ul>
 
 <html>
  <body>
    <script>
      (async () => {
        const response = await fetch('https://api.github.com/repos/:user/:repo/contents/');
        const data = await response.json();
        let htmlString = '<ul>';
        for (let file of data) {
          htmlString += `<li><a href="${file.path}">${file.name}</a></li>`;
        }
        htmlString += '</ul>';
        document.getElementsByTagName('body')[0].innerHTML = htmlString;
      })()
    </script>
  <body>
</html>
