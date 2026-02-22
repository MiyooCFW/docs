<!DOCTYPE html>
<html>
  <body>
    <script>
      (async () => {
        const response = await fetch('https://api.github.com/repos/MiyooCFW/cores/contents/cores/musl/latest');
        const data = await response.json();
        let htmlString = '<ul>';
        
        for (let file of data) {
          htmlString += `<li style="margin-bottom:16px;"><a href="${file.download_url}"><span style="font-size: 1.5em;">${file.name}</span><br>(sha256=${file.sha})</a></li>`;
        }
        htmlString += '</ul>';
        htmlString += `<button style="padding-left: 30px; margin-right: 1020px; cursor: pointer;" onclick="history.back()"><span style="font-size: 1.5em;"> ⟵Previous</span></button>`;
        document.getElementsByTagName('body')[0].innerHTML = htmlString;
      })()
    </script>
  <body>
</html>
