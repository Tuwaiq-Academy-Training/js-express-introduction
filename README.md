

محتوى الملف:

- ماهو middleware
- ماهو rest api
- ماهو Localhost
-  ماهو nodemon
-  ماهو Callback Functions



## ماهو middleware
ال Middleware هو وسيط يستخدم عادة للقيام بمعالجة البارامترات قبل ارسالها للدوال المعالجة الاخرى مثل get وpost وput وdelete

يستقبل يصل الى request وresponse وايضا next

المثال التي يطبع لك وقت كل عملية تمت

      router.use(function (req, res, next) {
       console.log('Time:', Date.now())
       next()
       })
 دالة next تستخدم لتمرير البارامترات


يستخدم مطورو البرامج Middleware لدمج مكونات البرامج المختلفة في تطبيقات أخرى. يوفر Middleware واجهة برمجة تطبيقات (API) قياسية لإدارة المدخلات والمخرجات المطلوبة للبيانات من المكون. الارتباط الداخلي بالمكون مخفي عن المستخدم. يستخدم المطورون واجهات برمجة التطبيقات لطلب الخدمات التي يحتاجون إليها من مكونات البرامج. 

## ماهو rest api

تعد API، أو واجهة برمجة التطبيقات، مجموعة من القواعد التي تحدد كيفية اتصال أو تواصل التطبيقات أو الأجهزة مع بعضها البعض. وتعد REST API واجهة برمجة تطبيقات تتوافق مع مبادئ تصميم REST، أو النمط التصميمي لنقل حالة التمثيل. لهذا السبب، يشار أحيانا إلى واجهات برمجة تطبيقات REST API باسم RESTful APIs‏.


![image](https://cdn-ajfbi.nitrocdn.com/GuYcnotRkcKfJXshTEEKnCZTOtUwxDnm/assets/static/optimized/rev-2888e70/wp-content/uploads/2020/01/rest-768x580.png)

#### كيف تعمل واجهة برمجة تطبيقات REST؟

- الحصول على طلب لجلب البيانات
- ضع طلب لتغيير حالة البيانات (مثل كائن أو ملف أو كتلة)
- طلب POST  لإنشاء البيانات
- حذف طلب

##  ماهو Localhost

##   ماهو nodemon
ال nodemon هي أداة تساعد في تطوير تطبيقات node حيث أنها تراقب التغييرات على الملفات التي تقع ضمن شجرة الملف الجذر للمشروع وتعيد بناء التطبيق في كل مرة وإظهار التعديلات.

يمكنك تثبيت nodemon محليا على مستوى المشروع أو بشكل عام على مستوى النظام "هنا لاتضطر لثبيته في كل مشروع"

      npm install -g nodemon




##  ماهو Callback Functions

فى جافا سكريبت، الـfunctions هى كائنات "objects". ومن خواص الـobjects انه يمكن تمرريها للـfunctions كـparameters

وسبب هذه الخاصية يمكن تمرر الـfunctions كـparameters لـfunctions اخرى وعمل تنفيذ للـfunctions المررة داخل الـfunction الحاوية لهم. هل يبدو الامر معقد قليلا؟ لنشاهد مثال للتوضيح:

     function print(callback) {
       callback();
      }
      
#### لما الحاجة للـCallback Functions

تقوم جافاسكريبت بتشغيل الاكواد البرمجية بالتتابع اى بترتيب من أعلى إلى أسفل. ومع ذلك ، هناك بعض الحالات التي يتم فيها تشغيل الكود (أو يجب تشغيله) بعد حدوث شيء آخر وليس بشكل تسلسلي. وهذا ما يسمى بالبرمجة غير المتزامنة "asynchronous programming".

تحرص الـCallbacks من أن الـfunctions لن تعمل قبل اكتمال المهمة ولكنها ستعمل مباشرة بعد اكتمال المهمة. وبالتالى تساعد هذه الخاصية فى كتابة اكواد جافاسكريبت غير متزامن "asynchronous" وتبقينا في مأمن من المشاكل والأخطاء.

في جافاسكريبت ، يمكن إنشاء callback function بتمريرها كـparameters لـfunctions أخرى، ثم إعادة استدعائها بعد حدوث شيء ما أو اكتمال بعض المهام. دعونا نرى كيف...
     
