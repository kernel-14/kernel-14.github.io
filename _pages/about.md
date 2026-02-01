---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<head>
    <link rel="stylesheet" href="bootstrap.min.css">
    <script>var clicky_site_ids = clicky_site_ids || []; clicky_site_ids.push(101296995);</script>
    <script async src="//static.getclicky.com/js"></script>    
    <style>
	:root {
	  --theme-color: #EC707D; /* 确保这是一个有效的颜色 */
	  --venue-bg-color: rgb(108, 149, 181);
	}
	    
	g {
		color: #aaaaaa
	}

	 pt {
		/* color:chocolate; */
		/* color:#c50e0e; */
		color: var(--title-color);
		/* color:tomato; */
		font-weight: 500;
	}

	 em {
		font-style: italic;
	}

	 venue {
		/* background-color:royalblue; */
		/* background-color:rgb(80, 80, 80); */
		/* background-color: #d1a7a7; */
		/* background-color: #ca3737; */
		background-color: #EC707D;
		/* background-color: rgb(217, 229, 244); */
		/* color: rgb(16, 68, 158); */
		color: #ffffff;
		/* font-family: 'Nunito'; */
		font-size: 70%;
		font-weight: bold;
		line-height: 170%;
		/* padding-left: 1em;
		padding-right: 1em; */
		margin-right: 0.25em;
		width: 5em;
		display:inline-block;
		text-align: center;
		/* border-color: #ffffff; */
		border-width: 0px;
		border-style: none;
		border-radius: 0.1rem;
		/* -webkit-box-shadow:0 2px 5px 0 rgba(0,0,0,0.16),0 2px 10px 0 rgba(0,0,0,0.12);
		box-shadow:0 2px 5px 0 rgba(0,0,0,0.16),0 2px 10px 0 rgba(0,0,0,0.12); */
		/* border-radius: 4px; */
		/* -webkit-box-shadow:inset 0px 0px 0px 0.25em #fff;
	    -moz-box-shadow:inset 0px 0px 0px 0.25em #fff;
	    box-shadow:inset 0px 0px 0px 0.25em #fff; */
		/* border: #ffffff; */
		height: 1.7em;
		vertical-align:text-bottom;
		margin-bottom: 0.1em;
		/* letter-spacing: 0.1cap; */
	}

	 venue1 {
		/* background-color:royalblue; */
		/* background-color:rgb(80, 80, 80); */
		/* background-color: #d1a7a7; */
		/* background-color: #ca3737; */
		background-color: var(--venue-bg-color);
		/* background-color: rgb(217, 229, 244); */
		/* color: rgb(16, 68, 158); */
		color: #ffffff;
		/* font-family: 'Nunito'; */
		font-size: 70%;
		font-weight: bold;
		line-height: 170%;
		/* padding-left: 1em;
		padding-right: 1em; */
		margin-right: 0.25em;
		width: 5em;
		display:inline-block;
		text-align: center;
		/* border-color: #ffffff; */
		border-width: 0px;
		border-style: none;
		border-radius: 0.1rem;
		/* -webkit-box-shadow:0 2px 5px 0 rgba(0,0,0,0.16),0 2px 10px 0 rgba(0,0,0,0.12);
		box-shadow:0 2px 5px 0 rgba(0,0,0,0.16),0 2px 10px 0 rgba(0,0,0,0.12); */
		/* border-radius: 4px; */
		/* -webkit-box-shadow:inset 0px 0px 0px 0.25em #fff;
	    -moz-box-shadow:inset 0px 0px 0px 0.25em #fff;
	    box-shadow:inset 0px 0px 0px 0.25em #fff; */
		/* border: #ffffff; */
		height: 1.7em;
		vertical-align:text-bottom;
		margin-bottom: 0.1em;
		/* letter-spacing: 0.1cap; */
	}
 
	.filter {
		color: var(--color);
		background-color: #fff;
		border: var(--border);
		border-style: solid;
		border-radius: 0.2rem;
		border-width: 1.5px;
		transition: all .3s;
		touch-action: manipulation;
		font-size: 80%;
		line-height: 120%;
		/* width: 5em; */
	}
	
	.filter:focus {
		color: #171e29;
	}
	  
	  .filter:hover {
		border-color: var(--theme-color);
		color: white;
		background-color: var(--theme-color);
		fill: var(--theme-color);
	  }
	  
	  .filter:active {
		border-color: var(--theme-color);
		color: var(--theme-color);
		fill: var(--theme-color);
	  }
	  
	.button-59 {
	  align-items: center;
	  background-color: #fff;
	  border: 1px solid #dadada;
	  box-sizing: border-box;
	  color: #000000;
	  cursor: pointer;
	  display: inline-block; /* 修改为 inline-block */
	  fill: #000;
	  font-family: 'Nunito';
	  font-size: 0.7rem;
	  height: 1.1rem;
	  justify-content: center;
	  line-height: 1.3;
	  min-width: 60px; /* 增加最小宽度 */
	  outline: 0;
	  padding: 0 10px; /* 增加左右内边距 */
	  text-align: center;
	  text-decoration: none;
	  transition: color .3s, background-color .3s, border-color .3s; /* 限制过渡范围 */
	  user-select: none;
	  -webkit-user-select: none;
	  touch-action: manipulation;
	  margin-right: 0.2em;
	  border-radius: 0.2rem;
	}
	
	.button-59:hover {
	  border-color: var(--theme-color);
	  color: #fff;
	  fill: var(--theme-color);
	  background-color: var(--theme-color);
	  text-decoration: none;
	}
	
	.button-59:active {
	  border-color: var(--theme-color);
	  color: #fff;
	  fill: var(--theme-color);
	  background-color: var(--theme-color);
	}
	
	@media (min-width: 768px) {
	  .button-59 {
	    padding-left: 5px;
	    padding-right: 5px;
	  }
	}
    </style>
    <script>
        try{
            if (window.screen.width < 700) {
                setActiveStyleSheet("jemdoc_mobile.css"); 
            } 
            else if(/iPad/i.test(navigator.userAgent)){ 
                setActiveStyleSheet("jemdoc.css"); 
            } 
            else{
                setActiveStyleSheet("jemdoc.css"); 
            } 
        } 
        catch(e){} 
	
        function setActiveStyleSheet(filename){
            document.write("<link href="+filename+" rel=stylesheet>");
        }

        function checkFilter(type, li) {
            if (type == "All") {
                return true
            }
            else if (type == "First-authored") {
                res = li.getAttribute("first_authored")
                return res
            }
            else {
                cate = li.getAttribute("category")
                if (!cate) {
                    return false
                }
                items = cate.split(',')
                for (j = 0; j < items.length; j++) {
                    console.log(items[j])
                    if (type.toUpperCase() == items[j].toUpperCase()) {
                        return true
                    }
                }
                return false
            }
        }

        function filterPub(type) {
            ul = document.getElementById("publications")
            li = ul.getElementsByTagName("li")
            for (i = 0; i < li.length; i++) {
                if (!checkFilter(type, li[i])) {
                    li[i].style.display = "none";
                }
                else {
                    li[i].style.display = ""
                }
            }
            // change the button color
            bts = document.getElementsByClassName("filter")
            for (k = 0; k < bts.length; k++) {
                if (bts[k].textContent == type) {
                    bts[k].style.setProperty("--color", "#000")
                    bts[k].style.setProperty("--border", "#000")
                    // bts[k].style.color = "#000"
                }
                else {
                    bts[k].style.setProperty("--color", "#a0a0a0")
                    bts[k].style.setProperty("--border", "#d3d3d3")
                    // bts[k].style.color = "#a0a0a0"
                }
            }
        }

    </script>

    <script>
        // import data from './bibtex.json' assert { type: 'json' };

        function getBibTex(key) {
            prompt("You can copy the text manually.", data[key]);
        }
    </script>
</head>

<span class='anchor' id='about-me'></span>

# 👤 Biography
I am **Kernel**, a [Your Position] at **[Your Institution]**. [Add your brief introduction here].

Feel free to reach out for any form of communication or collaboration!

<div class="highlight-blocks">
  <div class="highlight-block">
    <h3>🔬 Research Interests</h3>
    <ul>
      <li>[Research Interest 1]</li> 
      <li>[Research Interest 2]</li>
      <li>[Research Interest 3]</li>
    </ul>
  </div>

  <div class="highlight-block">
    <h3>☎️ Contact Info</h3>
    <ul>
      <li><strong>Address:</strong> [Your Address]</li>
      <li><strong>Email:</strong> <email>[your-email@example.com]</email></li>
      <li><strong>WeChat:</strong> [Your WeChat ID]</li>
	  <li>Feel free to contact me!</li>
    </ul>
  </div>

</div>

# 🎓 Education
- **[Your University]** ([Start Year]-[End Year]) [Degree] in [Major]
- **[Your University]** ([Start Year]-[End Year]) [Degree] in [Major]
<br>

# 🔥 News
<div id="news" class="w3-container w3-margin-top-2 w3-cursive">
	  <div style="height:200px; width:100%; overflow:auto;">
        <p>[MM.YYYY] 🎉 [Your news item 1]</p>
        <p>[MM.YYYY] 🎓 [Your news item 2]</p>
        <p>[MM.YYYY] 🏆 [Your news item 3]</p>
	  </div>
	</div>
 
<br>

# 📝 Publications
## 📒 Selected publications/preprints

**[Paper Title 1]**
- **Kernel**, [Co-authors]
- [Conference/Journal Name], [Year]
- [[Paper]](#) [[Code]](#)

**[Paper Title 2]**
- **Kernel**, [Co-authors]
- [Conference/Journal Name], [Year]
- [[Paper]](#) [[Code]](#)



# 🥇 Honors and Awards
- *(YYYY)*: &nbsp;[Award Name]
- *(YYYY)*: &nbsp;[Award Name]
- *(YYYY)*: &nbsp;[Award Name]

<span class='anchor' id='services'></span>

# 💼 Academic Services

#### Conference Reviewer
- [Conference Name] [Year]

#### Teaching
- [Course Name], [Institution], [Year]

<br>

<span class='anchor' id='miscellaneous'></span>

# 😄 Miscellaneous

- [Add your hobbies and interests here]
- [Add more personal information here]

<br>

<!-- <div style="text-align: center;"> -->
<div style="width: 20%; position:relative; left:40%">
  <script type="text/javascript" id="clstr_globe" src="//clustrmaps.com/globe.js?d=TexC6zB_7AOUKNMMshe4U4igIY-rca8pyS5kiQ7N6C8"></script>
    <!-- 地图小部件代码结束 -->
</div>

