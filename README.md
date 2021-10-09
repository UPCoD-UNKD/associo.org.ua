# Кто мы?

ГРОМАДСЬКА ОРГАНІЗАЦІЯ “УКРАЇНСЬКИЙ НАРОДНИЙ КОНТРОЛЬ ЗА ДІДЖІТАЛІЗАЦІЄЮ”

https://unkd.com.ua/

Мы - очень "душные" и умеем добиваться своей цели через бюрократические заслоны при помощи цифровых технологий. А еще у нас есть устав, по которому мы имеем право проводить контроль всех цифровых реестров и интерфейсов. В том числе - и государственных!

# Зачем нам это надо?

Мы хотим заставить Министерство Юстиции привести в порядок свой реестр регистрации юридических лиц, а именно - внести контактную информацию для всех государственных учреждений. После этого мы сможем реализовать контроля за выполнением элекронных обращений и предоставить возможность осуществлять эти обращения через интернет в едином окне. Вы сможете отправить обращение в любой государственный орган и получить на него ответ. В дальнейшем мы планируем доработать систему таким образом, что если на запрос не приходит подтверждение действий, а пустая отписка - эскалация в вышестоящую организацию, вплоть до Офиса Президента. Это долгий, но рабочий процесс, который можно и нужно автоматизировать. На систему можно влиять только системным методом.

# Почему мы в этом должны участвовать?

Потому что автоматическая система не устанет высылать обращения чиновникам, проверять их отписки и отправлять все заново, пока не достигнет результатов. А чиновники устанут писать отказы. И им придется выполнять свои прямые обязанности под давлением вышестоящих организаций. Конечно, вы не получите от этого никакого материального вознаграждения. Но есть вещи, которые намного сильнее, и то что мы предлагаем - это народный контроль над исполнениями обращений в государственные органы. Эмоциональное удовлетворение не измерить в деньгах, когда тебе вынуждены отвечать на твои обращения и отчитываться о бюджетных расходах.

## MVP

Минимально полезной версией служит система https://dostup.pravda.com.ua/ через которую можно сделать публичный запрос к открытым данным. К недостаткам такой системы можно отнести отсутствие какой-то автоматизации в эскалации обращений, а еще там слишком мало инстанций в которые можно сделать запрос. Несмотря на эти недостатки - система работает.

## POC

Нами была разработана система, которая интегрирует законодательные требования к формату обращений и обычная система отслеживания заявок (ticket track system), которая отлично себя показала. В качетсве опытного датасета нами была выбрана старая база контактов http://email.court.gov.ua/search и обработаны все устаревшие контакты, по которым были отправлены "письма счастья", с требованием привести контакты в порядок. Результаты себя оправдали - представители власти реагируют на заявки, присылают ответы и даже благодорят за проведенный аудит.

## PROD

Всего найдено около 10000 государственных органов разной степени важности и по каждому мы будем писать обращение, каждое из которых будет автоматически создавать запрос в системе отслеживания заявок. Мы проследим за тем, чтоб все они были обработаны.

#### Ах ты сукин сын, я в деле

Отлично! Тогда давай создадим систему народного контроля за реестрами. У нас уже есть POC, но этого недостаточно. Что мы хотим выпустить в релиз:

* Пользовательский интерфейс для юристов, которые желают поучаствовать в нашем деле. Уж они-то точно знают, как именно написать грамотный ответ, чтоб прищучить ленивого бюрократа.
* Пользовательский интерфейс для подачи заявки от пользователя, который желает решить проблему связанную с его правами при помощи цифровых технологий.
* Пользовательский интерфейс для госслужащих, которым мы даем возможность исправить упущение в нашем, народном реестре. Раз уж МинЮст и МинЦифра ничего в этом направлении не делают.

Как мы будем это делать?

Как всегда - чик-чик и в продакшен. Ну а детальнее - набор микросервисов, на обычных API и етицкой силе, которые смогут реализовать все это.

Метод работы все знают. Пулл реквесты в https://github.com/UPCoD-UNKD/associo.org.ua

