<html>
<head>
<style>
html, body, #wrapper {
       width: 100%;
       margin: 0;
       padding: 0;
       border: 0;
       font-family: 'Didact Gothic', sans-serif;
    }
    #wrapper td {
       vertical-align: middle;
       text-align: center;
       max-width: 800px;
    }
   a.PI {
      text-decoration: none;
      padding: 2px 5px 2px 5px;
   }
   a:hover.PI {
      background: black;
      color: white;
   }
   a:visited {
      color: inherit;
   }
   .sedtapp{
      position: fixed;
      bottom: 0;
      left: 50%;
      transform: translate(-50%, 0%)
   }

</style>
<link href="https://fonts.googleapis.com/css?family=Didact+Gothic" rel="stylesheet">       
</head>
<body>
   <table id="wrapper">
      <tr>
         <td><img src="wordmark.png" alt="" style="max-width:60%; margin:50px; height: auto; width: auto;"/></td>
      </tr>
      <tr>
         <td><h1><a href="http://sedtapp.psu.edu/department/directory-detail-g.aspx?q=uum209" class="PI">Dr. McComb</a> &nbsp; &nbsp; <a href="http://sedtapp.psu.edu/department/directory-detail-g.aspx?q=jdm5407" class="PI">Dr. Menold</a></h1></td>
      </tr>
   </table>
   <a href="http://www.sedtapp.psu.edu"><img src="sedtapp.png" class="sedtapp"/></a>

       <table style="border:none ;">
       {% for repository in site.github.public_repositories %}
         <tr>
           <td style="vertical-align: middle; border: none;">
             <h3>
               <a hxref="https://hsdl.github.io/{{ repository.name}}/">
                 {{ repository.name }}
               </a>
             </h3>
           </td> 
           <td style="vertical-align: top; border: none; white-space: nowrap;">
               Language: <code>{{ repository.language }}</code><br/>
               Status: <a href="https://travis-ci.org/HSDL/{{ repository.name }}" style="margin: 0; padding: 0;"> 
               <img src="https://travis-ci.org/HSDL/{{ repository.name }}.svg?branch=master" style="margin: 0; padding: 0;  margin-bottom: -6px"></a><br/>
               Last updated on {{ repository.pushed_at | date_to_string }}
           </td>
           <td style="vertical-align: top; border: none;">
             <span style="font-style: italic">{{repository.description}}</span>
           </td>
         </tr>
       {% endfor %}
       </table>
       
</body>
</html>

