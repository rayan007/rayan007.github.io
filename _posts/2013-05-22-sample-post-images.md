---
layout: post
title: "آموزش جکیل"
excerpt: "Examples and code for displaying images in posts."
tags: [sample post, images, test]
comments: true
---
<body style="direction:rtl">
<div class="wrapper">
        <div itemscope="" itemtype="http://schema.org/Article" class="post">

  <header class="post-header">
    <h1 itemprop="name" class="post-title">آموزش نصب jekyll بر روی ویندوز (قسمت اول)</h1>
    <p class="post-meta">
    <svg height="16px" style="enable-background:new 0 0 32 32;" viewBox="0 0 32 32" width="16px"><g></g><g><g><path d="M16,4c6.617,0,12,5.383,12,12s-5.383,12-12,12S4,22.617,4,16S9.383,4,16,4 M16,0    C7.164,0,0,7.164,0,16s7.164,16,16,16s16-7.164,16-16S24.836,0,16,0L16,0z" style="fill:#BBBBBB;"></path><path d="M21.422,18.578L18,15.152V8h-4.023v7.992c0,0.602,0.277,1.121,0.695,1.492l3.922,3.922    L21.422,18.578z" style="fill:#AAAAAA;"></path></g></g></svg> 
    <span itemprop="datePublished" content="2014-09-30 21:00:00 +0000">چهارشنبه ۹ مهر ۱۳۹۳</span> &nbsp;&nbsp;&nbsp;
	
          <svg height="16px" viewBox="0 0 32 32" width="16px"><title></title><desc></desc><defs></defs><g fill="none" fill-rule="evenodd" stroke="none" stroke-width="1"><g fill="#929292"><path d="M17,11 L15,7 L4.00276013,7 C2.89666625,7 2,7.88967395 2,8.991155 L2,27.008845 C2,28.1085295 2.89971268,29 3.99328744,29 L29.0067126,29 C30.1075748,29 31,28.1073772 31,27.0049107 L31,12.9950893 C31,11.8932319 30.1029399,11 28.9941413,11 L17,11 Z"></path></g></g></svg> tutorial
        
    </p>
  </header>

  <article itemprop="articleBody" class="post-content">
    <div class="container centeralized">
	<img src="../img/jekyll.png" alt="jekyll logo" height="230" width="498">
</div>
<p>همونطور که تو پست قبلی قولش رو داده بودم اینجا قصد دارم یه توضیح و آموزشی در مورد jekyll داشته باشم.امیدوارم که از این برنامه و آموزش اون در اینجا خوشتون بیاد.
یکی از مشکلاتی که jekyll داره و شاید اکثر برنامه های این شکلی دارن اینه که تو ویندوز به درستی کار نمی کنن. در واقع این برنامه ها برای سیستم عامل لینوکس ساخته میشن.
اما همیشه راه ها یا هک هایی وجود داره که میشه این مشکلات رو رفع کرد.</p>

<p>یکی از این هک ها تو وبسایت <a href="http://jekyll-windows.juthilo.com/">jekyll-windows.juthilo.com</a> معرفی شده که من خودم از این روش استفاده می کنم ولی باز هم مشکلاتی داشت که در اینجا روشهای حل اون رو توضیح میدم.
در کل اگه با <a href="http://jekyllrb.com">jekyll</a> آشنایی ندارین می تونین پست «<a href="http://front-end.ir/webdesign/why-i-have-chosen-jekyll/">چرا تصمیم گرفتم از Jekyll استفاده کنم</a>» رو که امیرعباس زحمتش رو کشیده مطالعه کنید. من خودم از طریق همین پست با jekyll آشنا شدم.</p>

<p>مزیت مهمی که jekyll داره اینه که می تونین از هاست <a href="http://github.com">github</a> به صورت رایگان برای وبسایت یا وبلاگتون استفاده کنین و تنها با خرید یک دامنه یک وبسایت کامل راه اندازی کنین. این آموزش به سه دسته تقسیم میشه:</p>
<h1>نصب jekyll</h1>
<p>همونطور که تو وبسایت <a href="http://jekyll-windows.juthilo.com/">jekyll-windows.juthilo.com</a> توضیح داده شده اول از همه نیازه که <a href="http://rubyinstaller.org/downloads/">Ruby</a> رو نصب کنیم. با مراجعه به <a href="http://rubyinstaller.org/downloads/">صفحه دانلود ruby</a> نسخه مناسب با کامپیوترمون رو دانلود می کنیم و اونرو نصب می کنیم. توجه کنید که تو مراحل نصب حتما گزینه Add ruby executables to your PATH رو مثل شکل زیر تیک زده باشید. این گزینه باعث میشه از هرجایی به دستورات ruby دسترسی داشته باشیم. البته اگه این گزینه رو تیک نزده باشید می تونین این کار رو دستی انجام بدید.(<a href="https://www.google.com/#q=how+to+add+executables+to+path+in+windows">جستجو کنید</a>)</p>

<div class="container centeralized">
	<img src="../img/ruby-path.png" alt="Ruby Installation" height="399" width="513">
</div>

<p>بعد از نصب Ruby نوبت به نصب Ruby DevKit میرسه که از همون آدرس قبلی قابل دسترسی هست. برای نصب ابتدا محتویات فایل zip رو درون یک پوشه (ترجیحا در root یکی از درایورها) که اسمش بدون فاصله و حروف خاص باشه قرار می دیم. بطور مثال <span class="inline-code">C:\RubyDevKit</span> مکان مناسبی برای نصب Ruby DevKit است. پس از قرار دادن فایلها نوبت به اجرای اونها میرسه. کدهای زیر رو برای نصب DevKit توی command prompt ویندوز وارد می کنیم. دقت کنید که باید توی مسیر همین پوشه ایجاد شده باشیم تا بتونیم محتویاتش رو نصب کنیم.</p>

<div class="highlight"><pre><code class="language-ruby" data-lang="ruby"><span class="ss">C</span><span class="p">:\</span><span class="no">RubyDevKit</span><span class="o">&gt;</span> <span class="n">chcp</span> <span class="mi">1252</span>
<span class="ss">C</span><span class="p">:\</span><span class="no">RubyDevKit</span><span class="o">&gt;</span> <span class="n">ruby</span> <span class="n">dk</span><span class="o">.</span><span class="n">rb</span> <span class="n">init</span>
<span class="ss">C</span><span class="p">:\</span><span class="no">RubyDevKit</span><span class="o">&gt;</span> <span class="n">ruby</span> <span class="n">dk</span><span class="o">.</span><span class="n">rb</span> <span class="n">install</span></code></pre></div>

<p>بعد از اینکه نصب ruby و ruby DevKit تموم شد نوبت به نصب jekyll میرسه. برای نصب jekyll کدهای زیر رو توی command prompt ویندوز وارد کنید.</p>

<div class="highlight"><pre><code class="language-ruby" data-lang="ruby"><span class="n">gem</span> <span class="n">install</span> <span class="n">jekyll</span></code></pre></div>

<p>یکی از مشکلات یا ناسازگاری های jekyll با ویندوز عدم هماهنگی افزونه highlight اون هست که برای حل اون جایگزینی وجود داره. افزونه پیش فرض jekyll برای highlight کردن کدهای درون صفحات، افزونه pygments هست که توی ویندوز اجرا نمیشه و هر دفعه که شما کد رو اجرا کنید پیام خطا میده. برای رفع مشکل highlight از افزونه rouge که با ویندوز سازگاری داره استفاده می کنیم. برای نصب این افزونه کد زیر رو توی command prompt ویندوز وارد کنید.</p>

<div class="highlight"><pre><code class="language-ruby" data-lang="ruby"><span class="n">gem</span> <span class="n">install</span> <span class="n">rouge</span></code></pre></div>

<p>در نهایت هم برای اضافه کردن قابلیت watch (مشاهده تغییرات در آن واحد) به jekyll کد زیر رو وارد می کنیم تا افزونه مورد نظر نصب بشه.</p>

<div class="highlight"><pre><code class="language-ruby" data-lang="ruby"><span class="n">gem</span> <span class="n">install</span> <span class="n">wdm</span></code></pre></div>

<p>حالا برنامه ما به طور کامل نصب شده و ما می تونیم ازش استفاده کنیم. بطور مثال کدهای زیر یک وبسایت demo در شاخه <span class="inline-code">D:\</span> میسازه و بعد اون رو برای مشاهده روی آدرس <span class="inline-code">http://localhost:4000</span> قابل دسترس می کنه.</p>

<div class="highlight"><pre><code class="language-ruby" data-lang="ruby"><span class="n">jekyll</span> <span class="kp">new</span> <span class="n">demo</span>
<span class="n">cd</span> <span class="n">demo</span>
<span class="n">jekyll</span> <span class="n">serve</span> <span class="o">-</span><span class="n">w</span></code></pre></div>

<p>اگر در مرحله سوم با اجرای کد <span class="inline-code">jekyll serve -w</span> با مشکل برخوردید باید تنظیمات برنامه رو تغییر بدین. به مسیر <span class="inline-code">D:\demo</span> رفته و فایل <span class="inline-code">_config.yml</span> رو با notepad باز کنید. در این فایل تنظیمات وبسایت demo ذخیره شده. به آخر فایل خط زیر رو اضافه کنید که نشون میده ما میخوایم از rouge استفاده کنیم.</p>

<div class="highlight"><pre><code class="language-html" data-lang="html">highlighter: rouge</code></pre></div>

<p>jekyll تنظیمات بسیار زیادی داره که می تونید تموم اونها رو توی وبسایت رسمی <a href="http://jekyllrb.com">jekyll</a> مشاهده کنید. تو قسمت documentation این سایت تمام ساختار jekyll به سادگی توضیح داده شده که می تونید از اونها استفاده کنید.</p>

<p>در پست بعدی قصد دارم در مورد اتصال github و jekyll بنویسم. خوشحال میشم نظرتون رو در مورد این پست بدونم.</p>

<ul><h3>نکات مهم</h3>
<li>jekyll از زبان نشانه گذاری yaml برای پست ها استفاده می کنه. استفاده از این زبان خیلی خیلی ساده هست و شما فقط کافیه از مثال ها برای یادگیری اون استفاده کنید.</li>
<li>ساختار پوشه ها کاملا مشخصه ولی نکته ای که این وسط مهمه اینه که وبسایت کامل شده و ترجمه شده نهاییتون در پوشه _site ذخیره میشه.</li>
<li>زمانی که از کد <span class="inline-code">jekyll serve -w</span> استفاده می کنید. برنامه در حالت اجرا میمونه و به تغییراتتون توجه می کنه تا اون رو سریع ترجمه کنه و خروجی رو روی پورت 4000 بهتون نشون بده. تنها تغییراتی که به صورت آنی اعمال نمیشه، تغییراتی هست که روی فایل <span class="inline-code">_config.yml</span> انجام می دین. برای اعمال این تغییرات کافیه jekyll رو متوقف کنید و بعد دوباره اون رو اجرا کنید.</li>
</ul>

<p><a href="http://iakrami.ir/tutorial/installing-jekyll-on-windows-part2.html">آموزش نصب jekyll بر روی ویندوز (قسمت دوم)</a></p>

<p><a href="http://iakrami.ir/tutorial/installing-jekyll-on-windows-part3.html">آموزش نصب jekyll بر روی ویندوز (قسمت سوم)</a></p>

  </article>

  <footer>
  	<ul class="tags">
  	
		<li class="tag">آموزش</li>
  	
		<li class="tag">وبسایت</li>
  	
		<li class="tag">jekyll</li>
  	
		<li class="tag">tutorial</li>
  	
		<li class="tag">windows</li>
  	
		<li class="tag">ویندوز</li>
  	
  	</ul>
  </footer>

   <div id="disqus_thread"><iframe verticalscrolling="no" horizontalscrolling="no" src="http://disqus.com/embed/comments/?base=default&amp;version=d074862f091cd9585b295f3979a4eb15&amp;f=iakrami&amp;t_u=http%3A%2F%2Fiakrami.ir%2Ftutorial%2Finstalling-jekyll-on-windows-part1.html&amp;t_d=%D8%A2%D9%85%D9%88%D8%B2%D8%B4%20%D9%86%D8%B5%D8%A8%20jekyll%20%D8%A8%D8%B1%20%D8%B1%D9%88%DB%8C%20%D9%88%DB%8C%D9%86%D8%AF%D9%88%D8%B2%20(%D9%82%D8%B3%D9%85%D8%AA%20%D8%A7%D9%88%D9%84)&amp;t_t=%D8%A2%D9%85%D9%88%D8%B2%D8%B4%20%D9%86%D8%B5%D8%A8%20jekyll%20%D8%A8%D8%B1%20%D8%B1%D9%88%DB%8C%20%D9%88%DB%8C%D9%86%D8%AF%D9%88%D8%B2%20(%D9%82%D8%B3%D9%85%D8%AA%20%D8%A7%D9%88%D9%84)&amp;s_o=default" style="width: 1px ! important; min-width: 100% ! important; border: medium none ! important; overflow: hidden ! important; height: 0px ! important;" title="Disqus" tabindex="0" scrolling="no" allowtransparency="true" name="dsq-app2" id="dsq-app2" frameborder="0" width="100%"></iframe><div style="overflow: hidden;" dir="ltr"><div style="height: 52px; width: 54px; margin: 0px auto; overflow: hidden; position: relative; box-sizing: border-box;" class="disqus-loader-bubble"><div class="disqus-loader-spinner" style="box-sizing: border-box; width: 26px; height: 26px; position: absolute; top: 13px; left: 15px; border-width: 3px; border-style: solid; border-color: rgba(51, 54, 58, 0.4) transparent; border-radius: 13px; transform-origin: 50% 50% 0px;"></div></div><p align="center">Disqus seems to be taking longer than usual. <a href="#" onclick="DISQUS.reset({reload: true}); return false;">Reload</a>?</p></div></div>
    <script type="text/javascript">
        /* * * CONFIGURATION VARIABLES: EDIT BEFORE PASTING INTO YOUR WEBPAGE * * */
        var disqus_shortname = 'iakrami'; // required: replace example with your forum shortname

        /* * * DON'T EDIT BELOW THIS LINE * * */
        (function() {
            var dsq = document.createElement('script'); dsq.type = 'text/javascript'; dsq.async = true;
            dsq.src = '//' + disqus_shortname + '.disqus.com/embed.js';
            (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(dsq);
        })();
    </script>
    <noscript>Please enable JavaScript to view the <a href="http://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
    

</div>

      </div>






<div class="page-content">
      <div class="wrapper">
        <div itemscope="" itemtype="http://schema.org/Article" class="post">

  <header class="post-header">
    <h1 itemprop="name" class="post-title">آموزش نصب jekyll بر روی ویندوز (قسمت دوم)</h1>
    <p class="post-meta">
    <svg height="16px" style="enable-background:new 0 0 32 32;" viewBox="0 0 32 32" width="16px"><g></g><g><g><path d="M16,4c6.617,0,12,5.383,12,12s-5.383,12-12,12S4,22.617,4,16S9.383,4,16,4 M16,0    C7.164,0,0,7.164,0,16s7.164,16,16,16s16-7.164,16-16S24.836,0,16,0L16,0z" style="fill:#BBBBBB;"></path><path d="M21.422,18.578L18,15.152V8h-4.023v7.992c0,0.602,0.277,1.121,0.695,1.492l3.922,3.922    L21.422,18.578z" style="fill:#AAAAAA;"></path></g></g></svg> 
    <span itemprop="datePublished" content="2014-10-04 11:00:00 +0000">شنبه ۱۲ مهر ۱۳۹۳</span> &nbsp;&nbsp;&nbsp;
	
          <svg height="16px" viewBox="0 0 32 32" width="16px"><title></title><desc></desc><defs></defs><g fill="none" fill-rule="evenodd" stroke="none" stroke-width="1"><g fill="#929292"><path d="M17,11 L15,7 L4.00276013,7 C2.89666625,7 2,7.88967395 2,8.991155 L2,27.008845 C2,28.1085295 2.89971268,29 3.99328744,29 L29.0067126,29 C30.1075748,29 31,28.1073772 31,27.0049107 L31,12.9950893 C31,11.8932319 30.1029399,11 28.9941413,11 L17,11 Z"></path></g></g></svg> tutorial
        
    </p>
  </header>

  <article itemprop="articleBody" class="post-content">
    <div class="container centeralized">
	<img src="../img/jekyll_github.png" alt="jekyll and github logo" height="230" width="600">
</div>
<p>در قسمت دوم آموزش نصب jekyll، نحوه اتصال این برنامه به یک صفحه github و طریقه پیکربندی اون رو توضیح خواهم داد. در اینجا نکته ای که بسیار اهمیت داره نحوه پیکربندی برنامه تو ویندوز هست.
چون اجرای jekyll روی ویندوز با تنظیمات پیش فرض github به دلیل ناسازگاری افزونه هایی مثل pygments پیغام خطا میده.</p>

<p><a href="http://iakrami.ir/tutorial/installing-jekyll-on-windows-part1.html">آموزش نصب jekyll بر روی ویندوز (قسمت اول)</a></p>

<h1>ایجاد حساب github</h1>
<p>بعد از ثبت نام در وبسایت <a href="http://github.com">github</a>، در منو بالا New Repository رو انتخاب کرده و یک <a href="http://git-scm.com/book/en/Getting-Started-Git-Basics">مخزن</a> ایجاد کنید. در قسمت نام مخزن، عبارت <span class="inline-code">username.github.io</span> رو وارد کنید (بجای username نام کاربری خودتون رو بنویسید). ما بقی تنظیمات را در حالت پیش فرض قرار دهید.</p>

<p>سپس با استفاده از نرم افزار github در ویندوز از مخزن خود clone بگیرید و اونو تو یک فولدر بریزید <a href="https://help.github.com/articles/adding-repositories-with-github-for-windows/">(آموزش)</a>.</p>

<p>خب حالا نوبت به jekyll میرسه. در اینجا باید یک وبسایت جدید با jekyll تو همون مسیر ایجاد کنید. به طور مثال اگه مسیر مخزن شما <span class="inline-code">C:\username.github.io</span> باشه کد زیر رو وارد می کنید.</p>

<div class="highlight"><pre><code class="language-ruby" data-lang="ruby"><span class="n">jekyll</span> <span class="kp">new</span> <span class="ss">C</span><span class="p">:\</span><span class="n">username</span><span class="o">.</span><span class="n">github</span><span class="o">.</span><span class="n">io</span></code></pre></div>

<p>تنظیمات مربوط به وبسایتتون که شامل نام و توضیحات و … میشه رو تو فایل <span class="inline-code">_config.yml</span> وارد کنید. بعد از تغییر دادن محتویات این فایل اون رو تو همین مسیر با نام جدید مثلا <span class="inline-code">win_config.yml</span> کپی کنید. تو فایل جدید کد زیر رو به انتهای فایل اضافه کنید.</p>

<div class="highlight"><pre><code class="language-text" data-lang="text">highlight: rouge</code></pre></div>

<p>دلیل ایجاد این فایل و اضافه کردن این خط اینه که می خوایم برنامه تو ویندوز با فایل تنظیمات دوم اجرا بشه تا مشکلی برای اون پیش نیاد ولی موقع آپلود و قرار گرفتن روی سرور فایل اصلی اجرا بشه.</p>

<p>اگر دقت کنید یک فایل با نام <span class="inline-code">.gitignore</span> توی مسیر اصلی مخزنتون وجود داره. اونرو باز کنید و اسم فایل دوم رو بهش اضافه کنید. این فایل مشخص می کنه که چه فولدرها و فایلهایی از کامپیوترتون به سرور آپلود نشه. احتمالا فولدر <span class="inline-code">_site</span> قبلا به این فایل اضافه شده.</p>

<p>بعد از اینکه تموم این تنظیمات رو انجام دادید می تونید با jekyll وبسایت خودتون رو بسازید و اونرو بعد از هر بار commit کردن تو آدرس username.github.io ببینید.</p>

<ul><h3>نکات مهم</h3>
<li>تنظیمات زیر در github بعد از هر بار اجرا بازنویسی می شن و شما نمی تونین این تنظیمات رو به هیچ شکلی عوض کنید:

<div class="highlight"><pre><code class="language-text" data-lang="text">highlighter: pygments
safe: true
lsi: false
github: [Repository metadata]</code></pre></div>

</li>
<li>تنظیم source رو به هیچ وجه دستکاری نکنید.</li>
<li>چون jekyll در github به صورت safe بالا میاد پس هیچ افزونه اضافی رو برای jekyll نمی تونید اضافه کنید.</li>
<li>لیست تنظیمات jekyll در <a href="http://jekyllrb.com/docs/configuration/">این صفحه</a> موجود است.</li>
</ul>

<p>در پست بعد اتصال دامنه به github رو آموزش خواهم داد. لطفا نظرات و سوالاتتون رو در مورد این پست در قسمت نظرات عنوان کنید.</p>

<p><a href="http://iakrami.ir/tutorial/installing-jekyll-on-windows-part3.html">آموزش نصب jekyll بر روی ویندوز (قسمت سوم)</a></p>

  </article>

  <footer>
  	<ul class="tags">
  	
		<li class="tag">آموزش</li>
  	
		<li class="tag">وبسایت</li>
  	
		<li class="tag">jekyll</li>
  	
		<li class="tag">tutorial</li>
  	
		<li class="tag">windows</li>
  	
		<li class="tag">ویندوز</li>
  	
		<li class="tag">github</li>
  	
		<li class="tag">گیت</li>
  	
  	</ul>
  </footer>

   <div id="disqus_thread"><iframe src="http://disqus.com/embed/comments/?base=default&amp;version=d074862f091cd9585b295f3979a4eb15&amp;f=iakrami&amp;t_u=http%3A%2F%2Fiakrami.ir%2Ftutorial%2Finstalling-jekyll-on-windows-part2.html&amp;t_d=%D8%A2%D9%85%D9%88%D8%B2%D8%B4%20%D9%86%D8%B5%D8%A8%20jekyll%20%D8%A8%D8%B1%20%D8%B1%D9%88%DB%8C%20%D9%88%DB%8C%D9%86%D8%AF%D9%88%D8%B2%20(%D9%82%D8%B3%D9%85%D8%AA%20%D8%AF%D9%88%D9%85)&amp;t_t=%D8%A2%D9%85%D9%88%D8%B2%D8%B4%20%D9%86%D8%B5%D8%A8%20jekyll%20%D8%A8%D8%B1%20%D8%B1%D9%88%DB%8C%20%D9%88%DB%8C%D9%86%D8%AF%D9%88%D8%B2%20(%D9%82%D8%B3%D9%85%D8%AA%20%D8%AF%D9%88%D9%85)&amp;s_o=default" style="width: 1px ! important; min-width: 100% ! important; border: medium none ! important; overflow: hidden ! important; height: 0px ! important;" title="Disqus" tabindex="0" scrolling="no" allowtransparency="true" name="dsq-app2" id="dsq-app2" frameborder="0" width="100%"></iframe></div>
    <script type="text/javascript">
        /* * * CONFIGURATION VARIABLES: EDIT BEFORE PASTING INTO YOUR WEBPAGE * * */
        var disqus_shortname = 'iakrami'; // required: replace example with your forum shortname

        /* * * DON'T EDIT BELOW THIS LINE * * */
        (function() {
            var dsq = document.createElement('script'); dsq.type = 'text/javascript'; dsq.async = true;
            dsq.src = '//' + disqus_shortname + '.disqus.com/embed.js';
            (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(dsq);
        })();
    </script>
    <noscript>Please enable JavaScript to view the <a href="http://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
    

</div>

      </div>
    </div>
</body>