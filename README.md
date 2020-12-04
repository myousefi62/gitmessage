# gitmessage
  <h1 dir="rtl"> نحوه نوشتن توضیحات Commit در git  به شکل استاندارد</h1>

<p dir="rtl">
با حضور مدیر نرم افزار حدید در سازمان و تغییر و تحولاتی که به وجود اومد بیش از پیش به استفاده از git و استانداردهای استفاده از git ملزم شدیم, 
اولین جیزی که باید رعایت کنیم نوشتن توضیحات به شکل استاندارد هست با کمی جستچو در نت به مقالاتی در این رابطه بر خوردم که در زیر لینک ها رو برای مشاهده دوستان میذارم 
 <br />
<dir="rtl"> 
<a href="https://www.radcom.co/fa/blog/webdesign/post/detail/132/%D8%A7%D8%B3%D8%AA%D8%A7%D9%86%D8%AF%D8%A7%D8%B1%D8%AF-%D8%AA%D9%88%D8%B6%DB%8C%D8%AD%D8%A7%D8%AA-Commit-%D8%A8%D8%B1%D8%A7%DB%8C-git">نحوه نوشتن توضیحات Commit در git (استاندارد قالب توضیحات گیت)</a> <br />
 <a href="https://virgool.io/@mmdsharifi/how-to-semantic-git-commit-messages-gvmmqatf6acg">چگونه یک پیغام git commit با معنا بنویسیم؟</a> <br />
 <a href="https://chris.beams.io/posts/git-commit/">How to Write a Git Commit Message</a> <br />
</dir>
<p dir="rtl">
اما با این که مطالب ارایه شده کامل و جامع هست یک مشکل اساسی وجود داره , با توجه به ترافیک کاری که داریم احتمال به خاطر سپاری این قوانین و استاندارد ها نه تنها برای من بلکه برا بیشتر اعضای تیم ممکن نیست و شانس به یاد اوری و رعایت این قوانین نزدیک به صفر هست , بنا بر این تصمیم گرفتم تمامی این قوانین و استانداردهای رو به الگویی تبدیل کنیم تا هر زمانی که دستور  git commit  در ترمینال نوشتم قوانین به شکل یک تمپلیت یاد اور بشه
چیزی که در زیر میبینید نمونه این قالب توضیحات هست .
<br />
 
```# 
# Hey there o/! 
# We just wanted to let you know that we care a great deal about    
# making our git history clean, maintainable and easy to access for 
# all our contributors. Commit messages are very important to us,  
# which is why we have a strict commit message policy in place.     
# Please use the following guidelines to format all your commit     
# messages:
# 
#     <type>(<scope>): <subject>
#     <BLANK LINE>
#     <body>
#     <BLANK LINE>
#     <footer>
# 
# Please note that:
#  - The HEADER is a single line of max. 50 characters that         
#    contains a succinct description of the change. It contains a   
#    type, an optional scope, and a subject
#       + <type> describes the kind of change that this commit is   
#                providing. Allowed types are:
#             * feat (feature)
#             * fix (bug fix)
#             * docs (documentation)
#             * style (formatting, missing semicolons, …)
#             * refactor
#             * test (when adding missing tests)
#             * chore (maintain)
#       + <scope> can be anything specifying the place of the commit    
#                 change
#       + <subject> is a very short description of the change, in   
#                   the following format:
#             * imperative, present tense: “change” not             
#               “changed”/“changes”
#             * no capitalised first letter
#             * no dot (.) at the end
#  - The BODY should include the motivation for the change and      
#    contrast this with previous behavior and must be phrased in   
#    imperative present tense 
#  - The FOOTER should contain any information about Breaking       
#    Changes and is also the place to reference GitHub issues that   
#    this commit closes
# 
# Thank you <3
```
<p dir="rtl"> نمونه کامیت ایجاد شده باید مشابه  توضیحات زیر باشد<br />
 
```
fix(middleware): ensure Range headers adhere more closely to RFC 2616

Add one new dependency, use `range-parser` (Express dependency) to compute
range. It is more well-tested in the wild.

Fixes #2310
```
<p dir="rtl"> مراحل تعریف الگو و استفاده از الگو در دو مرحله انجام میشود  <br />
<h1 dir="rtl">ایجاد فایل الگو</h1>
<p dir="rtl">شما میتوانید از الگویی که من استفاده کردم استفاده کنید الگوی زیر را کپی کرده و در فایلی با نام .gitmessage ذخیره کنید. <br />

```
# Hey there o/! 
# We just wanted to let you know that we care a great deal about    
# making our git history clean, maintainable and easy to access for 
# all our contributors. Commit messages are very important to us,  
# which is why we have a strict commit message policy in place.     
# Please use the following guidelines to format all your commit     
# messages:
# 
#     <type>(<scope>): <subject>
#     <BLANK LINE>
#     <body>
#     <BLANK LINE>
#     <footer>
# 
# Please note that:
#  - The HEADER is a single line of max. 50 characters that         
#    contains a succinct description of the change. It contains a   
#    type, an optional scope, and a subject
#       + <type> describes the kind of change that this commit is   
#                providing. Allowed types are:
#             * feat (feature)
#             * fix (bug fix)
#             * docs (documentation)
#             * style (formatting, missing semicolons, …)
#             * refactor
#             * test (when adding missing tests)
#             * chore (maintain)
#       + <scope> can be anything specifying the place of the commit    
#                 change
#       + <subject> is a very short description of the change, in   
#                   the following format:
#             * imperative, present tense: “change” not             
#               “changed”/“changes”
#             * no capitalised first letter
#             * no dot (.) at the end
#  - The BODY should include the motivation for the change and      
#    contrast this with previous behavior and must be phrased in   
#    imperative present tense 
#  - The FOOTER should contain any information about Breaking       
#    Changes and is also the place to reference GitHub issues that   
#    this commit closes
# 
# Thank you <3
```
<p dir="rtl">در نظر داشته باشید این نام الزامی نیست و شما میتوانید هر نام دیگری را انتخاب کنید.<br />
<h1 dir="rtl">کانفیگ git جهت استفاده از فایل الگو</h1>

<p dir="rtl">برای اینکه به Git بگوییم از فایل الگو استفاده کند (در سطح سراسری ، نه فقط در نسخه فعلی) ، از دستور زیر استفاده کردم:<br />
 
 ```
 git config --global commit.template ~/.gitmessage
 ```
<p dir="rtl">نکته :<br /> ~/.gitmessage نام فایل الگو به همراه ادرس فایل می باشد. <br />
 
 <h1 dir="rtl"> پاورقی کردن</h1>
 <p dir="rtl">
در نظر داشته باشد که الگوی توضیحات به سیاستهای هر سازمان بستگی دارد و این تنها نمونه ای استاندارد هست 
امید وار مفید واقع شده باشد .
