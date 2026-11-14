---
layout: workshop      # Цей текст не можна змінювати.
# More detailed instructions (including how to fill these variables for an
# online workshop) are available at
# https://carpentries.github.io/workshop-template/customization/index.html
venue: "Інститут математики НАН України" # brief name of the institution that hosts the workshop without address (e.g., "Euphoric State University")
address: "online"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria"), videoconferencing URL, or 'online'
country: "ua"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes) for the institution that hosts the workshop
language: "uk"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) for the workshop
latitude: "0"        # decimal latitude of workshop venue (use https://www.latlong.net/)
longitude: "0"       # decimal longitude of the workshop venue (use https://www.latlong.net)
humandate: "7-11 грудня 2026 р." # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "11:00 - 14:00 за київським часом"    # human-readable times for the workshop e.g., "9:00 am - 4:30 pm CEST (7:00 am - 2:30 pm UTC)"
startdate: 2026-12-07 # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2026-12-11   # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Олександр Коновалов", "Ірина Раєвська", "Марина Раєвська"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["TBC"] # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["gap.kyiv2026@gmail.com"]  # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes: https://pad.carpentries.org/2026-12-07-kyiv-imath-online # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document (e.g., https://pad.carpentries.org/2026-12-07-kyiv-imath-online)
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

{% comment %} See instructions in the comments below for how to edit specific sections of this workshop template. {% endcomment %}

{% comment %}
HEADER

Edit the values in the block above to be appropriate for your workshop.
If the value is not 'true', 'false', 'null', or a number, please use
double quotation marks around the value, unless specified otherwise.
And run 'make workshop-check' *before* committing to make sure that changes are good.
{% endcomment %}


{% comment %}
8< ============= For a workshop delete from here =============
For a workshop please delete the following block until the next dashed-line
{% endcomment %}

{% comment %}
8< ============================= until here ==================
{% endcomment %}


{% comment %}
Check DC curriculum
{% endcomment %}

{% if site.carpentry == "dc" %}
{% unless site.curriculum == "dc-astronomy" or site.curriculum == "dc-ecology" or site.curriculum == "dc-genomics" or site.curriculum == "dc-geospatial" or site.curriculum == "dc-image" or site.curriculum == "dc-socsci" %}
<div class="alert alert-warning">
Здається, що ви налаштовуєте вебсайт для навчальної програми Data Carpentry, але ви не вказали тип навчальної програми у файлі <code>_config.yml</code> (поточне значення у <code>_config.yml</code>: "<strong>{{ site.curriculum }}</strong>", можливі значення: <code>dc-image</code>, <code>dc-astronomy</code>, <code>dc-ecology</code>, <code>dc-genomics</code>, <code>dc-socsci</code>, or <code>dc-geospatial</code>). Після редагування цього файлу вам потрібно знову запустити <code>make serve</code>, щоб побачити результат цих змін.
</div>
{% endunless %}
{% endif %}

{% comment %}
Перевірте навчальний план SWC
{% endcomment %}

{% if site.carpentry == "swc" %}
{% unless site.curriculum == "swc-inflammation" or site.curriculum == "swc-gapminder" %}
<div class="alert alert-warning">
Здається, що ви налаштовуєте вебсайт для навчального плану Software Carpentry, але не вказали його тип у файлі <code>_config.yml</code> (поточне значення у <code>_config.yml</code>: "<strong>{{ site.curriculum }}</strong>", possible values: <code>swc-inflammation</code>, або <code>swc-gapminder</code>). Після редагування цього файлу вам потрібно знову запустити <code>make serve</code>, щоб побачити результат цих змін.
</div>
{% endunless %}
{% endif %}

{% comment %}
EVENTBRITE

Цей блок містить віджет реєстрації Eventbrite, якщо в заголовку встановлено "eventbrite". Ви можете видалити його, якщо ви не використовуєте Eventbrite, або залишити його, оскільки воно не відображатиметься, якщо поле 'eventbrite' у заголовку не встановлено.
{% endcomment %}
{% if page.eventbrite %}
<strong>Деякі блокувальники реклами блокують вікно реєстрації. Якщо ви не бачите поле реєстрації нижче, перевірте налаштування блокувальника реклами.</strong>
<iframe
  src="https://www.eventbrite.com/tickets-external?eid={{page.eventbrite}}&ref=etckt"
  frameborder="0"
  width="100%"
  height="280px"
  scrolling="auto">
</iframe>
{% endif %}


<h2 id="general">Загальна інформація</h2>

{% comment %}
ВСТУП

Відредагуйте загальний пояснювальний абзац нижче, якщо ви хочете змінити "pitch"
{% endcomment %}

<p>
На цьому семінарі ми будемо викладати роботу з командним рядком UNIX, контроль версій за допомогою Git, та програмування у системі компʼютерної алгебри GAP. Ми будемо використовувати навчальні матеріали від <a href="https://carpentries.org">The Carpentries</a>, які були перекладені на українську мову учасниками <a href="https://ukrainian-carpentries.github.io/">Української Спільноти The Carpentries</a>.
</p>

<p>
Проєкт <strong><a href="https://carpentries.org">The Carpentries</a></strong> складається з <a
href="{{site.swc_site}}">Software Carpentry</a>, <a href="{{site.dc_site}}">Data Carpentry</a>, та
<a href="{{site.lc_site}}">Library Carpentry</a>, які обʼєднують спільноти їх інструкторів, тренерів, супроводжувачів, помічників і прихильників. Вони мають спільну місію — навчати науковців базовим навичкам досліджень за допомогою обчислювальних методів.
<p align="center">
  <em>
  <strong>Хочете дізнатися більше та підтримувати співпрацю з Carpentries?</strong> Carpentries Clippings — це двотижневий інформаційний вісник про Carpentries, де ми ділимося новинами спільноти, оголошеннями про вакансії тощо.
  Зареєструйтеся, щоб отримувати наступні видання та читати наш повний архів: <a href="https://carpentries.org/newsletter/">https://carpentries.org/newsletter/</a>
  </em>
</p>
{% if site.carpentry == "swc" %}
{% include swc/intro.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/intro.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/intro.html %}
{% endif %}

{% if site.pilot %}
Це пілотний семінар, де проходить тестування уроку, який ще розробляється. Автори уроку будуть вдячні за будь-які відгуки, які ви можете надати їм щодо змісту уроку та пропозиції щодо його подальшого вдосконалення.
{% endif %}

{% comment %}
ЦІЛЬОВА АУДИТОРІЯ

Поясніть, хто ваша аудиторія.  (Зокрема, повідомте аудиторії, чи семінар відкритий лише для людей з певної установи).
{% endcomment %}
{% if site.carpentry == "swc" %}
{% include swc/who.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/who.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/who.html %}
{% endif %}

{% comment %}
МІСЦЕЗНАХОДЖЕННЯ

У цьому блоці відображається адреса та посилання на карти, що показують напрямки, якщо було встановлено широту та довготу семінару. Ви можете використовувати https://www.latlong.net/, щоб знайти широту/довготу
адресу.
{% endcomment %}
{% assign begin_address = page.address | slice: 0, 4 | downcase  %}
{% if page.address == "online" %}
{% assign online = "true_private" %}
{% elsif begin_address contains "http" %}
{% assign online = "true_public" %}
{% else %}
{% assign online = "false" %}
{% endif %}
{% if page.latitude and page.longitude and online == "false" %}
<p id="where">
  <strong>Де:</strong>
  {{page.address}}.
  Пошук шляху за допомогою
  <a href="//www.openstreetmap.org/?mlat={{page.latitude}}&mlon={{page.longitude}}&zoom=16">OpenStreetMap</a>
  або
  <a href="//maps.google.com/maps?q={{page.latitude}},{{page.longitude}}">Google Maps</a>.
</p>
{% elsif online == "true_public" %}
<p id="where">
  <strong>Де:</strong>
  онлайн за адресою <a href="{{page.address}}">{{page.address}}</a>.
  Якщо вам потрібен пароль або інша інформація для доступу до тренінгу, інструктор дасть його вам перед семінаром.
</p>
{% elsif online == "true_private" %}
<p id="where">
  <strong>Де:</strong> Цей семінар відбуватиметься онлайн.
  Інструктори нададуть вам інформацію, яка вам знадобиться для того, щоб приєднатися до цієї зустрічі.
</p>
{% endif %}

{% comment %}
ДАТА

Цей блок відображає дату та посилання на Google Calendar.
{% endcomment %}
{% if page.humandate %}
<p id="when">
  <strong>Коли:</strong>
  {{page.humandate}}
  {% include workshop_calendar.html %}
</p>
{% endif %}


<strong>Організатори семінару:</strong>
</p>
<ul>
 <li>	<a href="https://www.imath.kiev.ua/">Інститут математики НАН України (Київ, Україна)</a></li>
 <li>	<a href="https://ukrainian-carpentries.github.io/">Українська Спільнота The Carpentries</a></li>
 <li> <a href="https://www.st-andrews.ac.uk/">Університет Сент-Ендрюса (Сент-Ендрюс, Великобританія)</a></li>
</ul>


{% comment %}
ОСОБЛИВІ ВИМОГИ

Змініть блок нижче, якщо є якійсь особливі вимоги.
{% endcomment %}
<p id="requirements">
  <strong>Вимоги:</strong>
  {% if online == "false" %}
    Слухачі повинні мати з собою ноутбук з операційною системою Mac, Linux або Windows (не планшет, Chromebook тощо), на якому вони мають права адміністратора.
  {% else %}
    Слухачі повинні мати доступ до комп’ютера з операційною системою Mac, Linux або Windows (не планшет, Chromebook тощо), на якому вони мають права адміністратора.
  {% endif %}
  У них має бути встановлено декілька спеціальних програмних пакетів (перелічених  <a href="#setup">тут</a>).
</p>

{% comment %}
ДОСТУПНІСТЬ

Змініть блок нижче, якщо є будь-які перешкоди для доступності або спеціальні інструкції.
{% endcomment %}
<p id="accessibility">
  <strong>Доступність:</strong>
{% if online == "false" %}
  Ми прагнемо зробити цей семінар зручним для всіх. Для офлайн-семінару 
  організатори переконалися, що:
</p>
<ul>
  <li>приміщення пристосоване для інвалідних візків/самокатів;</li>
  <li>наявні облаштовані вбиральні.</li>
</ul>
<p>
  Матеріали будуть надані до початку семінару. Також нотатки з великим шрифтом будуть доступні за потреби, якщо ви заздалегідь попередите про це організаторів. Якщо ми можемо допомогти вам полегшити навчання (наприклад, надати сурдоперекладача або приміщення для лактації), будь ласка, зв'яжіться з нами (використовуючи контактні дані нижче), і ми спробуємо задовольнити вашу потребу.
</p>
{% else %}
  Ми прагнемо створити позитивне та доступне навчальне середовище для всіх.
  Ми не вимагаємо від учасників розкривати будь-яку особисту інформацію, яку ми не потребуємо. Однак ми хочемо допомогти створити інклюзивний, доступний досвід для всіх учасників. Щоб повідомити будь-яку інформацію, яка може бути корисною для того, щоб зробити ваш досвід в Carpentries більш доступним, <a href="mailto:gap.kyiv2026@gmail.com">напишіть нам електронною поштою</a>.
</p>
{% endif %}

{% comment %}
АДРЕСА ЕЛЕКТРОННОЇ ПОШТИ ДЛЯ КОНТАКТІВ

Відобразити контактну адресу електронної пошти, яка вказана у файлі конфігурації.
{% endcomment %}
<p id="contact">
  <strong>Контакт:</strong>
  Будь ласка, напишіть
  {% if page.email %}
  {% for email in page.email %}
  {% if forloop.last and page.email.size > 1 %}
  або
  {% else %}
  {% unless forloop.first %}
  ,
  {% endunless %}
  {% endif %}
  <a href='mailto:{{email}}'>{{email}}</a>
  {% endfor %}
  {% else %}
  to-be-announced
  {% endif %}
  для додаткової інформації.
</p>

<p id="who-can-attend">
    <strong>Реєстрація:</strong>
    Реєстрація на семінар The Carpentries (Київ, 2026) завершена.
</p>


<p id="roles">
  <strong>Ролі:</strong>
  Щоб дізнатися більше про ролі учасників семінару (інструктор, помічник, організатор, слухач), зверніться 
  до <a href="https://carpentries.org/workshop_faq/#what-are-the-roles-of-everyone-participating-in-a-workshop">Workshop FAQ</a>.
</p>



{% comment %}
ХТО МОЖЕ БРАТИ УЧАСТЬ?

Якщо ви хочете вказати, хто може відвідати семінар, ви можете скористатися розділом нижче.

Перемістіть тег 'endcomment' над початком наступного
<p> тегу, щоб зробити цей розділ видимим.

Відредагуйте текст відповідно до того, хто може відвідувати семінар. Наприклад:
- Цей семінар відкритий для студентів та співробітників університету ABC.
- Цей семінар відкритий для громадськості.
- Якщо ви зацікавлені в відвідуванні цього семінару, напишіть на me@example.com для отримання подальшої інформації

<p id="who-can-attend">
    <strong>Who can attend?:</strong>
    Цей семінар відкритий для ....
</p>
{% endcomment %}

<hr/>

{% comment%}
КОДЕКС ПОВЕДІНКИ
{% endcomment %}
<h2 id="code-of-conduct">Кодекс поведінки</h2>

<p>
Кожен, хто бере участь у діяльності Carpentries, зобов'язаний дотримуватися <a href="https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html">Кодексу поведінки</a>. У цьому документі також зазначено, як повідомити про інцидент, якщо це необхідно.
</p>

<p class="text-center">
  <a href="https://goo.gl/forms/KoUfO53Za3apOuOK2">
    <button type="button" class="btn btn-info">Повідомити про інцидент, пов'язаний із кодексом поведінки</button>
  </a>
</p>
<hr/>


{% comment %}
Нотатки для співпраці

Якщо ви хочете використовувати Etherpad, перейдіть до

https://pad.carpentries.org/YYYY-MM-DD-site

де 'YYYY-MM-DD-site' є ідентифікатором вашого семінару,
Наприклад, '2015-06-10-esu'.

Зверніть увагу, що у нас також є CodiMD (версія HackMD з відкритим вихідним кодом), доступна за адресою https://codimd.carpentries.org
{% endcomment %}
{% if page.collaborative_notes %}
<h2 id="collaborative_notes">Нотатки для співпраці</h2>

<p>
Ми використовуватимемо цей <a href="{{ page.collaborative_notes }}">спільний документ</a> для спілкування в чаті, створення нотаток і обміну URL-адресами та фрагментами коду.
</p>
<hr/>
{% endif %}


{% comment %}
ОПИТУВАННЯ - НЕ РЕДАГУЙТЕ ПОСИЛАННЯ НА ОПИТУВАННЯ
{% endcomment %}
<h2 id="surveys">Опитування</h2>
<p>Будь ласка, обов'язково заповніть ці опитування до та після семінару.</p>
{% if site.carpentry == "incubator" %}
<p><a href="{{ site.incubator_pre_survey }}">Опитування перед семінаром</a></p>
<p><a href="{{ site.incubator_post_survey }}">Опитування після семінару</a></p>
{% elsif site.incubator_pre_survey or site.incubator_post_survey %}
<div class="alert alert-danger">
УВАГА: ви визначили власні посилання до та/або після опитування для семінару, який не налаштований для The Carpentries Incubator (значення 'curriculum' не встановлено на 'incubator' у '_config.yml'). Будь ласка, закоментуйте поля "incubator_pre_survey" та "incubator_post_survey" у "_config.yml" або, якщо цей семінар проводить урок в Incubator, змініть значення "carpentry" на incubator.
</div>
{% else %}
<p><a href="{{ site.pre_survey }}{{ site.github.project_title }}">Опитування перед семінаром</a></p>
<p><a href="{{ site.post_survey }}{{ site.github.project_title }}">Опитування після семінару</a></p>
{% endif %}

<hr/>


{% comment %}
РОЗКЛАД

Покажіть розклад семінару.

Невеликі зміни в розклад можна внести, змінивши "schedule.html", який знаходиться в папці "_includes" для вашого типу семінару ("swc", "lc" або "dc"). Відредагуйте пункти та час у таблиці відповідно до своїх планів. Ви також можете змінити поля "1-й день" і "2-й день" на фактичні дати або дні тижня.

  Для більших змін порожній шаблон для 4-денного семінару
  (корисний, наприклад, для онлайн-викладання) можна знайти в розділі
  `_includes/custom-schedule.html`.
  Додайте до цього файлу час і те, чого ви будете навчати.
  Ви також можете додати рядки до таблиці, якщо хочете розбити розклад далі.
  Щоб використовувати цей користувацький розклад тут, замініть блок коду під   заголовком Розклад`<h2>` нижче на `{% include custom-schedule.html %}`.
  {% endcomment %}

<h2 id="schedule">Розклад (можливі невеликі зміни)</h2>

{% if site.carpentry == "swc" %}
{% include swc/schedule.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/schedule.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/schedule.html %}
{% elsif site.carpentry == "incubator" %}
Цей семінар проводить урок у [The Carpentries Incubator](https://carpentries-incubator.org/).
Будь ласка, перевірте [домашню сторінку уроку]({{ site.incubator_lesson_site }}) щоб отримати список розділів уроку та приблизний час.
{% endif %}

{% comment %}
Відредагуйте або замініть текст вище, якщо ви хочете додати таблицю розкладу.
Перегляньте вміст файлу _includes/custom-schedule.html для прикладу побудови однієї з цих таблиць розкладу.
{% endcomment %}

{% if site.pilot %}
Урок, який викладається на цьому семінарі, є пілотним, і точний розклад ще не встановлений. Семінар містиме регулярні перерви. Будь ласка, [зв'яжіться з організаторами семінару](#contact), якщо ви хочете отримати більше інформації про запланований розклад.
{% endif %}

<hr/>


{% comment %}
НАЛАШТУВАННЯ

Видаліть недоречні розділи з інструкцій налаштування.  Кожен розділ знаходиться всередині 'div' без будь-яких класів, щоб полегшити пошук початку і кінця.

Це ще одне місце, де люди часто роблять помилки, тому, будь ласка, перегляньте свій сайт перед тим, як зробити фіксацію, і переконайтеся, що ви також запустили 'інструменти/перевірку'.
{% endcomment %}

<h2 id="setup">Налаштування</h2>

<p>
  Для участі у семінарах
  {% if site.carpentry == "swc" %}
  Software Carpentry
  {% elsif site.carpentry == "dc" %}
  Data Carpentry
  {% elsif site.carpentry == "lc" %}
  Library Carpentry
  {% endif %}
  вам знадобиться доступ до програмного забезпечення, яке наведено нижче.
  Крім того, вам знадобиться сучасний веббраузер.
</p>
<p>
  Ми склали список типових проблем, які виникають під час встановлення програмного забезпечення, як довідник для інструкторів. Він може вам знадобитися на вікі-сторінці 
  <a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Проблеми конфігурації та рішення</a>.
</p>
<p>
  Окрім того, ви можете скористуватися новішіми версіями інструкцій з налаштування (наприклад, з використанням Windows Subsystem for Linux v2 у сучасних версіях Windows), які знаходяться у 
  <a href="https://carpentries.github.io/workshop-template/#setup">англомовній версії шаблону сторінки семінару The Carpentries</a>.
</p>

{% comment %}
Це інструкція з встановлення інструментів, які використовуються під час семінару.
{% endcomment %}

{% if site.carpentry == "swc" %}
{% include swc/setup.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/setup.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/setup.html %}
{% elsif site.carpentry == "incubator" %}
Будь ласка, перевірте сторінку "Налаштування"
[на сайті уроку]({{ site.incubator_lesson_site }}), щоб отримати інструкції, яких слід дотримуватися, щоб отримати програмне забезпечення та дані, які вам знадобляться для проходження уроку.
{% endif %}
