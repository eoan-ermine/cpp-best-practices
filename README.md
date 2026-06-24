# C++ Best Practices

## curl

1. **[Automatic Builds](https://curl.se/dev/builds.html)** — скрипт, который автоматически собирает curl и отправляет на заданную почту информацию о сборке: собралось или не собралось, какие ошибки, с какими опциями собиралось. Далее на [отдельной страничке](https://curl.se/dev/builds.html) все успешные и неуспешные билды высвечиваются (автоматически извлекается из писем, присланных по почте).
2. **[Test Clutch](https://github.com/dfandrich/testclutch/)** — у curl [развернут инстанс](https://testclutch.curl.se/) Test Clutch, системы, агрегирующей результаты сборок, проходящих на различных CI (AppVeyor, CircleCI, Github Actions) и отображающей их результаты (а также подведенную статистику на их основе) в красивом виде.
3. **[Daily Snapshots](https://curl.se/snapshots/)** — ежедневно выкладываются исходники curl, Docker образ (с окружением для сборки) и артефакты сборки библиотеки под различные платформы (Windows, MacOS, Linux MUSL/glibc).
4. **[GitStats](https://curl.se/gitstats/)** — портал, визуализирующий активность в git репозитории.
5. **[Дашборд](https://curl.se/dashboard.html)** с ежедневно обновляемыми графами: средняя цикломатическая сложность, количество коммитов в неделю, размер страницы man, количество репортов на HackerOne, количество issues на GitHub и так далее.
6. **[Mailing list](https://lists.haxx.se/listinfo/curl-commits) и [RSS-фид](https://github.com/curl/curl/commits/master.atom)** для новых коммитов.
7. **Запрет опасных функций** вроде atoi, strncpy, энфорсящийся на этапе сборки [скриптом](https://github.com/curl/curl/blob/master/scripts/checksrc.pl).
8. **[Ежегодный опрос](https://curl.se/docs/survey/)** пользователей о том, как они пользуются библиотекой: какие фичи используют и т.д.

## LLVM

1. **[LLVM Weekly](https://llvmweekly.org/)** — еженедельная рассылка про наиболее видные коммиты, новые RFC и прочее.
2. **[Dockerfile для сборки LLVM](https://llvm.org/docs/Docker.html)** — не готовые образы, образ надо самостоятельно собрать.
3. **Интеграционные тесты** с помощью [lit](https://llvm.org/docs/CommandGuide/lit.html).
4. **[Система отслеживания производительности](https://llvm.org/docs/lnt/)**: регрессий и улучшений. Однако будто довольно вялая: мало машин и довольно редко гоняется.
5. LLVM имеет **[фаззеры для некоторых проектов](https://llvm.org/docs/FuzzingLLVM.html)**, которые гоняются в CI.
