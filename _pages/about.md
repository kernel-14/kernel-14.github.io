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
 I am a first-year master student at **Peking University**, where I am co-supervised by [**Wentao Zhang**](https://zwt233.github.io/) and [**Weinan E**](https://scholar.google.com/citations?user=i2mOt14AAAAJ&hl=en) at [**AAIS**](https://www.aais.pku.edu.cn/). I also closely work with [**Renrui Zhang**](https://scholar.google.com/citations?hl=en&user=YlL3xN4AAAAJ&view_op=list_works&sortby=pubdate). Previously, I had a wonderful time at [**Tiktok**](https://www.tiktok.com/explore) and [**MSRA**](https://www.microsoft.com/en-us/research/lab/microsoft-research-asia/), serving as research intern. More about my experience can be found in [CV](assets/Ruichuan_An_new.pdf).

**Many kind people helped me in my journey.** If you want to talk more about research or seek advice that I might be able to provide, please no hesitation to reach out. My MBTI type is **ENFJ**(233), feel free to drop me an Email for any form of communication or collaboration! 

📌 We have several academic intern positions at **DCML Lab (Peking University)**. We actively work on **Data-Centric AI** and **Vision-Language Model**. If you like what we do, don't hesitate to contact me. I currently lead a research group of master's and undergraduate students at Peking University. I am proud to have helped many of them secure **top-tier** labs and internships. You can find more details in [Mentorship](#mentorship).

  <div class="highlight-block">
    <h3>🫡 Motivation: "Why do I do research?"</h3>
    <ul>
      <li> To have the chance collaborating with global talents, I enjoy brainstorming and learning from people with different background. </li>
      <li> For the sheer fun and joy of discovery. The three keywords I'm pursuing are <strong>Insight</strong> |  <strong>Innovation</strong> | <strong>Independence</strong>. </li>
      <li> I hope my research could decorate individual's daily life one day. Even if it’s just a ripple, I want to leave a mark on this world.</li>
    </ul>
  </div>

<div class="highlight-blocks">
  <div class="highlight-block">
    <h3>🔬 AI Researcher</h3>
    <ul>
      <li>Current Interests focus on <strong>Unified Model</strong> and <strong>Reasoning</strong></li> 
      <li>Unified Model: Build Unified Representation and Make Understanding and Generation truly benefits each other.</li>
      <li>Reasoning: Think with (generated) image/ video, better adaptation to the real world environments.</li>

    </ul>
  </div>

  <div class="highlight-block">
    <h3>☎️ Contact Info</h3>
    <ul>
      <li><strong>Address:</strong> <a href="https://www.google.com/maps/place/%E5%BE%AE%E8%BD%AF%E4%BA%9A%E6%B4%B2%E7%A0%94%E7%A9%B6%E9%99%A2/@39.977248,116.3321331,17z/data=!3m1!4b1!4m6!3m5!1s0x35f053f0ab311e9f:0x4a43f1f260da036c!8m2!3d39.977244!4d116.337004!16s%2Fg%2F1tg4jk1c?entry=ttu&g_ep=EgoyMDI1MDMxMi4wIKXMDSoASAFQAw%3D%3D">Peking University, Beijing, China</a></li>
      <li><strong>Email:</strong> <email>arctanxarc[AT]gmail.com</email></li>
      <li><strong>WeChat:</strong> arc2002822</li>
	  <li>Do <strong>not</strong> fell embarrassed to contact me.</li>
    </ul>
  </div>

</div>

# 🎓 Educations
- <img src="images/pku_.png" style="width: 20px;height: auto;display: inline-block;vertical-align: middle"> **Peking University** (2025.09-2027.09) M.S. in Mathematics
- <img src="images/xjtu_.png" style="width: 20px;height: auto;display: inline-block;vertical-align: middle"> **Xi'an Jiaotong University** (2021.09-2025.06) B.Eng. in Software Engineering
<br>

# 🔥 News
<div id="news" class="w3-container w3-margin-top-2 w3-cursive">
	  <div style="height:200px; width:100%; overflow:auto;">
        <p>[09.2025] 🎉 Three papers <strong>UniCTokens</strong>, <strong>PAM</strong> and <strong>A-CFG</strong> were accepted by <strong>NIPS 2025</strong> (CCF-A), I have two (co-)first author papers! </p>
        <p>[09.2025] 🎓 I joined Peking University and pursuing master's degree. </p>
        <p>[03.2025] 🏆 I was awarded the <strong>Outstanding Graduate</strong> by XJTU.</p>
	    <p>[02.2025] 🎉 One paper <strong>MOVE-KD</strong> was accepted by <strong>CVPR 2025</strong> (CCF-A), congratulations to Jiajun.</p>
	    <p>[12.2024] 🎉 One paper <strong>Draw and Understand</strong> was accepted by <strong>ICLR 2025</strong>, congratulations to Weifeng.</p>
        <p>[06.2024] 🎉 One paper <strong>SSD-LLM</strong> was accepted by <strong>ECCV 2024</strong>, I am the co-first author, see you in Milano.</p>
        <p>[05.2024] 🎉 One paper <strong>GDAD</strong> was accepted by <strong>KDD 2024</strong> (CCF-A), congratulations to Renhong.</p>
	  </div>
	</div>
 
<br>

# 📝 Publications
## 📒 Selected publications/preprints
<div class='paper-box'><div class='paper-box-image'><div><div class="badge">NIPS'2025</div><img src='images/fig1_final-1.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**UniCTokens: Boosting Personalized Understanding and Generation via Unified Concept Tokens**

- **Ruichuan An**, Sihan Yang, Renrui Zhang, Zijun Shen, Ming Lu, Gaole Dai, Hao Liang, Ziyu Guo, Shilin Yan, Yulin Luo, Bocheng Zou, Chaoqun Yang, Wentao Zhang
- Conference on Neural Information Processing Systems, 2025.
- [[Paper]](https://arxiv.org/pdf/2505.14671?) [[Code, 100+ Stars🌟]](https://github.com/arctanxarc/UniCTokens)
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">NIPS'2025</div><img src='images/PAM_teaser-1.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Perceive Anything: Recognize, Explain, Caption, and Segment Anything in Images and Videos**

- Weifeng Lin*, Xinyu Wei\*, **Ruichuan An\***, Tianhe Ren, Tingwei Chen, Renrui Zhang, Ziyu Guo, Wentao Zhang, Lei Zhang, Hongsheng Li
- Conference on Neural Information Processing Systems, 2025.
- [[Paper]](https://arxiv.org/pdf/2506.05302) [[Code, 300+ Stars🌟]](https://github.com/Perceive-Anything/PAM)
</div>
</div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">ECCV'2024</div><img src='images/eccv_arc.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**LLM as Dataset Analyst: Subpopulation Structure Discovery with Large Language Model**

- Yulin Luo*, **Ruichuan An\***, Bocheng Zou, Yiming Tang, Jiaming Liu, Shanghang Shang
- European Computer Vision Conference, 2024.
- [[Paper]](https://arxiv.org/abs/2405.02363) [[Code]](https://github.com/llm-as-dataset-analyst/SSDLLM)
</div>
</div>



# 🥇 Honors and Awards
- *(2025)*: &nbsp;Outstanding Graduate.
- *(2024)*: &nbsp;Rising Star of the Year (5/2233) Highest personal honors in college.
- *(2024, 2023, 2022)*: &nbsp;XJTU Outstanding Student*3
- *(2023)*: &nbsp;Huawei Scholarship 10k CNY, only awarded to 3 undergraduate students in XJTU per year.

<span class='anchor' id='services'></span>

# 💼 Mentorship and Services

#### Conference reviewer
- ICLR 2025, NIPS 2025, ICCV 2025, ICRA 2025, FM@ICLR 2025

#### Mentorship
- Sihan Yang, XJTU -> PKU, Internship: [**Kuaishou, Kling**](https://github.com/KlingTeam), [**Tiktok**](https://www.tiktok.com/)
- Kai Zeng, TJU -> PKU, Internship: [**XiaoMi**](https://www.mi.com/sg/), [**Tiktok**](https://www.tiktok.com/)

<br>

<span class='anchor' id='miscellaneous'></span>

# 😄 Miscellaneous
<!-- <div class="highlight-blocks">
  <div class="highlight-block">
    <h3>❤️ Family</h3>
    <ul>
      <img src="images/qiaoqiao.jpg" alt="family Image" style="display: block; margin: auto; max-width: 100%; height: auto;">
     <br>
	    <li>I have a beautiful girlfriend, <a href='https://scholar.google.com/citations?user=G_BypiwAAAAJ&hl=zh-CN&oi=ao'>Ziqi Qiao</a>, who is also a Ph.D. student at Peking University. We also own an adorable cat 🐱 named QiuQiu. He brings us tremendous fun and happiness.</li>
    </ul>
  </div>
  
  <div class="highlight-block">
    <h3>🧑‍🤝‍🧑 Friends</h3>
    <ul>
	<img src="images/friends.png" alt="friend Image" style="display: block; margin: auto; max-width: 100%; height: auto;">
      <br>
	    <li>Here are some of my closest academic friends: <a href='https://liujiaming1996.github.io/'>Jiaming Liu</a>, <a href='https://scholar.google.com/citations?user=SgeV4NkAAAAJ&hl=zh-CN&oi=ao'>Yulin Luo</a>, <a href='https://gumpest.github.io/'>Yuan Zhang</a>, and Gaole Dai from PKU; <a href='https://scholar.google.com/citations?hl=zh-CN&user=Vl1X_-sAAAAJ'>Xiaowei Chi</a> from HKUST; <a href='https://wuchenrui.github.io/'>Chenrui Wu</a> from ZJU&SFU; <a href='https://yilijin.github.io/'>Yili Jin</a> from McGill.</li>
    </ul>
  </div>
  
  <div class="highlight-block">
    <h3>😄 Hobbies</h3>
    <ul>
	<img src="images/football_new.png" alt="hobby Image" style="display: block; margin: auto; max-width: 100%; height: auto;">
      <br>
	    <li>I am a crazy basketball 🏀 & football ⚽️ fan. I enjoy the games of Kevin Durant 🕷️ and Kyrie Irving 🧙. I also wholeheartedly pledge my allegiance to Chelsea Football Club, KTBFFH! 💙</li>
    </ul>
  </div>
</div>

<br> -->

<!-- <div style="text-align: center;"> -->
<div style="width: 20%; position:relative; left:40%">
  <script type="text/javascript" id="clstr_globe" src="//clustrmaps.com/globe.js?d=TexC6zB_7AOUKNMMshe4U4igIY-rca8pyS5kiQ7N6C8"></script>
    <!-- 地图小部件代码结束 -->
</div>

