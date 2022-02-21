## JSON
1. Создать внешний репозиторий c названием JSON\
Заходим на [GitHub](https://github.com/) нажать `+` в `New repository` вводим имя `JSON` нажать `Create repository`

2. Клонировать репозиторий JSON на локальный компьютер\
`cd /Users/igori/Documents/github/HW_1_GitHub`\
`git clone https://github.com/igorlipskii/JSON.git`

3. Внутри локального JSON создать файл “new.json”\
`touch new.json`

4. Добавить файл под гит\
`git add new.json`

5. Закоммитить файл\
`git commit -m "add new file"`

6. Отправить файл на внешний GitHub репозиторий\
`git push`

7. Отредактировать содержание файла “new.json” - написать информацию о себе (ФИО, возраст, количество домашних животных, будущая желаемая зарплата). Всё написать в формате JSON\
`vim new.json`\
`i` — перейти в режим редактирования

```json
{
	"Name": "Igor",
	"Surname": "Lipskii",
	"Age": 33,
	"Pet": "No pets",
	"Salary": {
		"Junior": "80.000 rub",
		"Middle": "190.000 rub",
		"Senior": "320.000+ rub"
		}
}
```
`esc` `:` `wq`

8. Отправить изменения на внешний репозиторий\
`git status` - смотрим какие файлы изменились\
`git add new.json` - файл отслеживается\
`git commit -m  "wrote information about myself` - снимок текущего состояния файла с комментарием `wrote information about myself`\
`git push` - отправляем файл на внешний репозиторий

9. Создать файл preferences.json\
`touch preferences.json`

10. В файл preferences.json добавить информацию о своих предпочтениях (Любимый фильм, любимый сериал, любимая еда, любимое время года, сторона которую хотели бы посетить) в формате JSON\
`vim preferences.json`\
`i` — перейти в режим редактирования

```json
{
	"My preferences": {
		"Film": "John Carter",
		"Series": "La casa de papel",
		"Food": [
			"pasta",
 			"vegetables",
			"meat"
		],
		"Season": "Summer",
		"Place to visit": [
			"USA",
			"Japan",
			"New Zealand"
		]
	}
}

```
`esc` `:` `wq`

11. Создать файл skills.json добавить информацию о скиллах которые будут изучены на курсе в формате JSON\
`vim skills.json`\
`i` — перейти в режим редактирования

```json
{               
        "Skills": {
                "1": "Basic theory (What is testing, bug reports, documentation, types, methods, testing directions, etc.)",
                "2": "What is a client-server architecture.",
                "3": "HTTP Methods of requests to the server.",
                "4": "HTTP server response codes.",
                "5": "Structures of HTTP requests and responses.",
                "6": "What is JSON, XML. Their structure.",
                "7": "API testing via Postman (JS, API autotests).",
                "8": "Removing and reading logs from an external server.",
                "9": "Sniffing http web traffic via Charles and Fiddler.",
                "10": "Dev Tools of web browsers (Google Chrome, FireFox).",
                "11": "VPN (How it works, why you need it, how to use it, tool options).",
                "12": "Mobile testing.",
                "13": "Feature iOS, Android, guidelines.",
                "14": "Building iOS applications on XCode. (Those who do not have a Mac computer, just look).",
                "15": "Building Android applications on Android Studio.",
                "16": "ADB (android device management).",
                "17": "Setting up proxy and vpn on iOS and Android.", 
                "18": "Interception (sniffing) of mobile traffic via Charles and Fiddler on iOS and Android.",
                "19": "Command line (terminal) Linux (copying, creating, viewing, moving files on servers without a graphical interface)",
                "20": "Basics of bash scripting, automation of routine tasks on the server.",
                "21": "Access to remote servers.",
                "22": "SQL basics (Create, Delete, Drop, Insert Into, Select, From, Where, Join).",
                "23": "Postgres database (installation, configuration and use).",
                "24": "Non-relational database Redis (installation, configuration and use).",
                "25": "Load testing in Jmeter.",
                "26": "Scrum development methodology.",
                "27": "Python. (Learning the basics. Creating a client-server application)."
        }
}
```
`esc` `:` `wq`

12. Отправить сразу 2 файла на внешний репозиторий
    > `git add preferences.json skills.json`\
    или `git add {preferences,skills}.json`

    `git status`
    `git commit -m  "add skills and preferences files"`\
    `git push`
    > `git add {preferences,skills}.json && git commit -m "add 2 files and commit and push" && git push` - одной командой делем add, commit, push

13. На веб интерфейсе создать файл bug_report.json\
нажать `add new file` затем `create new file` пишем название файла 

14. Сделать Commit changes (сохранить) изменения на веб интерфейсе\
в `commit new file` пишем `create bug_report` нажимаем `Commit new file`

15. На веб интерфейсе модифицировать файл bug_report.json, добавить баг репорт в формате JSON\
открыть файл, нажать `bug_report.json` нажать `edit this file`

```json
{
    "Project": "Calculator",
    "ID": 88,
    "Summary": "Результат умножения неверен",
    "Description": "Результат равен ожидаемому результату +2",
    "Steps to reproduce": {
	"Step 1": "Открыть сайт https://nuix.github.io/SDET/senior-sdet/stagingCalc/index.html",
	"Step 2": "Нажать цифру 6",
	"Step 3": "Нажать знак умножения",
	"Step 4": "Нажать цифру 3",
	"Step 5": "Нажать знак равно"
    },
    "Actual result": 20,
    "Expected result": 18,
    "Attachments": "https://somup.com/c3nq02TjpH",
    "Severity": "Critical",
    "Priority": "High",
    "Labels": "Smoke",
    "Environment": {
	"Operational system": "macOS Big Sur 11.6.4",
	"Browser version": "Google Chrome 98.0.4758.102"
    },
    "Author": "Igor Lipskii",
    "Test Data": "20.02.2022"
}
```
`esc` `:` `wq`

16. Сделать Commit changes (сохранить) изменения на веб интерфейсе\
пишем в `Commit changes` `update bug_report`

17. Синхронизировать внешний и локальный репозиторий JSON\
`git pull`

## XML
1. Создать внешний репозиторий c названием XML\
Заходим на [GitHub](https://github.com/) нажать `+` в `New repository` вводим имя `XML` нажать `Create repository`

2. Клонировать репозиторий XML на локальный компьютер\
`cd /Users/igori/Documents/github/HW_1_GitHub`\
`git clone https://github.com/igorlipskii/XML.git`

3. Внутри локального XML создать файл “new.xml”\
`touch new.xml`

4. Добавить файл под гит\
`git add new.xml`\
`git status`

5. Закоммитить файл\
`git commit -m "add new xml file"`

6. Отправить файл на внешний GitHub репозиторий\
`git push`

7. Отредактировать содержание файла “new.xml” - написать информацию о себе (ФИО, возраст, количество домашних животных, будущая желаемая зарплата). Всё написать в формате XML

```xml
<?xml version="1.0" encoding="UTF-8"?>
<person>
    <name>Igor</name>
    <surname>Lipskii</surname>
    <age>33</age>
    <pets>no pets</pets>
    <salary>
	<junior>80.000 rub</junior> 
	<middle>190.000 rub</middle>
	<senior>320.000+ rub</senior>
    </salary>
</person>
```

8. Отправить изменения на внешний репозиторий\
`git add new.xml`\
`git commit -m  "wrote information about myself"`\
`git push`

9. Создать файл preferences.xml\
`touch preferences.xml`

10. В файл preferences.xml добавить информацию о своих предпочтениях (Любимый фильм, любимый сериал, любимая еда, любимое время года, сторона которую хотели бы посетить) в формате XML\
`vim preferences.xml`\
`i` — перейти в режим редактирования

```xml
<?xml version="1.0" encoding="UTF-8"?>
<myPreferences>
	<film>John Carter</film>
	<series>La casa de papel</series>
	<food>pasta, vegetables and meat</food>
	<season>Summer</season>
	<placeToVisit>USA, Japan, New Zealand</placeToVisit>
</myPreferences>
```

11. Создать файл skills.xml добавить информацию о скиллах которые будут изучены на курсе в формате XML\
`vim skills.xml`\
`i` — перейти в режим редактирования

```xml
<skills>
        <skills1>Basic theory (What is testing, bug reports, documentation, types, methods, testing directions, etc.)</skills1>
        <skills2>What is a client-server architecture.</skills2>
        <skills3>HTTP Methods of requests to the server.</skills3>
        <skills4>HTTP server response codes.</skills4>
        <skills5>Structures of HTTP requests and responses.</skills5>
        <skills6>What is JSON, XML. Their structure.</skills6>
        <skills7>API testing via Postman (JS, API autotests).</skills7>
        <skills8>Removing and reading logs from an external server.</skills8>
        <skills9>Sniffing http web traffic via Charles and Fiddler.</skills9>
        <skills10>Dev Tools of web browsers (Google Chrome, FireFox).</skills10>
        <skills11>VPN (How it works, why you need it, how to use it, tool options).</skills11>
        <skills12>Mobile testing.</skills12>
        <skills13>Feature iOS, Android, guidelines.</skills13>
        <skills14>Building iOS applications on XCode. (Those who do not have a Mac computer, just look).</skills14>
        <skills15>Building Android applications on Android Studio.</skills15>
        <skills16>ADB (android device management).</skills16>
        <skills17>Setting up proxy and vpn on iOS and Android.</skills17>
        <skills18>Interception (sniffing) of mobile traffic via Charles and Fiddler on iOS and Android.</skills18>
        <skills19>"Command line (terminal) Linux (copying, creating, viewing, moving files on servers without a graphical interface).</skills19>
        <skills20>Basics of bash scripting, automation of routine tasks on the server.</skills20>
        <skills21>Access to remote servers.</skills21>
        <skills22>SQL basics (Create, Delete, Drop, Insert Into, Select, From, Where, Join).</skills22>
        <skills23>Postgres database (installation, configuration and use).</skills23>
        <skills24>Non-relational database Redis (installation, configuration and use).</skills24>
        <skills25>Load testing in Jmeter.</skills25>
        <skills26>Scrum development methodology.</skills26>
        <skills27>Python. (Learning the basics. Creating a client-server application).</skills27>
</skills>
```

12. Сделать коммит в одну строку\
`git status`\
`git add {pefereces,skills}.xml && git commit -m "add and commit 2 files`

13. Отправить сразу 2 файла на внешний репозиторий\
`git status`\
`git push`

14. На веб интерфейсе создать файл bug_report.xml\
нажать `add new file` `create new file` пишем название файла

15. Сделать Commit changes (сохранить) изменения на веб интерфейсе\
в `commit new file` пишем `create bug_report` нажимаем `Commit new file`

16. На веб интерфейсе модифицировать файл bug_report.xml, добавить баг репорт в формате XML\
открыть файл, нажать `bug_report.xml` нажать `edit this file`

```xml
<?xml version="1.0" encoding="UTF-8"?>
<bugReport>
 <project>Calculator</project>
 <id>88</id>
 <summary>Результат умножения неверен</summary>
 <description>Результат равен ожидаемому результату +2</description>
	<stepsToReproduce>
	<step1>Открыть сайт https://nuix.github.io/SDET/senior-sdet/stagingCalc/index.html</step1>
	<step2>Нажать цифру 6</step2>
	<step3>Нажать знак умножения</step3>
	<step4>Нажать цифру 3</step4>
	<step5>Нажать знак равно</step5>
 </stepsToReproduce>
 <actualResult>20</actualResult>
 <expectedResult>18</expectedResult>
 <attachments>https://somup.com/c3nq02TjpH</attachments>
 <severity>Critical</severity>
 <priority>High</priority>
 <labels>Smoke</labels>
 <environment>
	<operationalSystem>macOS Big Sur 11.6.4</operationalSystem>
	<browserVersion>Google Chrome 98.0.4758.102</browserVersion>
 </environment>
 <author>Igor Lipskii</author>
 <testData>20.02.2022</testData>
 </bugReport>
```
17. Сделать Commit changes (сохранить) изменения на веб интерфейсе\
пишем в `Commit changes` `update bug_report`

18. Синхронизировать внешний и локальный репозиторий XML\
`git pull`

## TXT
1. Создать внешний репозиторий c названием TXT\
Заходим на [GitHub](https://github.com/) нажать `+` в `New repository` вводим имя `TXT` нажать `Create repository`

 2. Клонировать репозиторий TXT на локальный компьютер\
`cd /Users/igori/Documents/github/HW_1_GitHub`\
`git clone https://github.com/igorlipskii/TXT.git`

 3. Внутри локального TXT создать файл “new.txt”\
`touch new.txt`

 4. Добавить файл под гит\
`git status`\
`git add new.txt`

 5. Закоммитить файл\
`git commit -m "add new file"`

 6. Отправить файл на внешний GitHub репозиторий\
`git push`

 7. Отредактировать содержание файла “new.txt” - написать информацию о себе (ФИО, возраст, количество домашних животных, будущая желаемая зарплата). Всё написать в формате TXT\
`vim new.json`\
`i` — перейти в режим редактирования

```txt
Name: Igor
Surname: Lipskii
Age: 33
Pet: no pets
Salary: 
    1. Junior - 80.000 rub. 
    2. Middle - 190.000 rub.
    3. Senior - 320.000+ rub.
```
`esc` `:` `wq`

 8. Отправить изменения на внешний репозиторий\
`git add new.txt`\
`git commit -m  "wrote information about myself"`\
`git push`

 9. Создать файл preferences.txt\
`touch preferences.txt`

 10. В файл preferences.txt” добавить информацию о своих предпочтениях (Любимый фильм, любимый сериал, любимая еда, любимое время года, сторона которую хотели бы посетить) в формате TXT\
`vim preferences.txt`\
`i` — перейти в режим редактирования

```txt
My preferences:
	Film: John Carter
	Series: La casa de papel
	Food: pasta, vegetables and meat
	Season: Summer
	Place to visit: USA, Japan, New Zealand
```
`esc` `:` `wq`

 11. Создать файл skills.txt добавить информацию о скиллах которые будут изучены на курсе в формате TXT\
`vim skills.txt`\
`i` — перейти в режим редактирования

```txt
Skills:
        1. Basic theory (What is testing, bug reports, documentation, types, methods, testing directions, etc.).
        2. What is a client-server architecture.
        3. HTTP Methods of requests to the server.
        4. HTTP server response codes.
        5. Structures of HTTP requests and responses.
        6. What is JSON, XML. Their structure.
        7. API testing via Postman (JS, API autotests).
        8. Removing and reading logs from an external server.
        9. Sniffing http web traffic via Charles and Fiddler.
        10. Dev Tools of web browsers (Google Chrome, FireFox).
        11. VPN (How it works, why you need it, how to use it, tool options).
        12. Mobile testing.
        13. Feature iOS, Android, guidelines.
        14. Building iOS applications on XCode. (Those who do not have a Mac computer, just look).
        15. Building Android applications on Android Studio.
        16. ADB (android device management).
        17. Setting up proxy and vpn on iOS and Android.
        18. Interception (sniffing) of mobile traffic via Charles and Fiddler on iOS and Android.
        19. "Command line (terminal) Linux (copying, creating, viewing, moving files on servers without a graphical interface).
        20. "Basics of bash scripting, automation of routine tasks on the server.
        21. "Access to remote servers.
        22. "SQL basics (Create, Delete, Drop, Insert Into, Select, From, Where, Join).
        23. "Postgres database (installation, configuration and use).
        24. "Non-relational database Redis (installation, configuration and use).
        25. "Load testing in Jmeter.
        26. "Scrum development methodology.
        27. "Python. (Learning the basics. Creating a client-server application).
```
`esc` `:` `wq`

 12. Сделать коммит в одну строку\
`git status`\
`git add {preferences,skills}.txt && git commit -m "add and commit 2 files"`

 13. Отправить сразу 2 файла на внешний репозиторий\
`git status`\
`git push`

 14. На веб интерфейсе создать файл bug_report.txt\
нажать `add new file` `create new file` пишем название файла

 15. Сделать Commit changes (сохранить) изменения на веб интерфейсе\
в `commit new file` пишем `create bug_report` нажимаем `Commit new file`

 16. На веб интерфейсе модифицировать файл bug_report.txt, добавить баг репорт в формате TXT\
открыть файл, нажать `bug_report.txt` нажать `edit this file`

```txt
Project: Calculator
ID: 88
Summary: Результат умножения неверен
Description: Результат равен ожидаемому результату +2
    Steps to reproduce:
    Step 1: Открыть сайт https://nuix.github.io/SDET/senior-sdet/stagingCalc/index.html
    Step 2: Нажать цифру 6
    Step 3: Нажать знак умножения
    Step 4: Нажать цифру 3
    Step 5: Нажать знак равно
Actual result: 20
Expected result: 18
Attachments: https://somup.com/c3nq02TjpH
Severity: Critical
Priority: High
Labels: Smoke
Environment:
Operational system: macOS Big Sur 11.6.4
Browser version: Google Chrome 98.0.4758.102
Author: Igor Lipskii
Test Data: 20.02.2022
```
 17. Сделать Commit changes (сохранить) изменения на веб интерфейсе.\
пишем в `Commit changes` `update bug_report`
 18. Синхронизировать внешний и локальный репозиторий TXT\
`git pull`
