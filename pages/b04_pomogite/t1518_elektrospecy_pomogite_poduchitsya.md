---
title: "Электро-спецы, помогите подучиться."
sidebar: ponics_sidebar
---

**Oxy** 15-08-2012

Ситуация такая. Есть несколько аккумуляторов разного размера. Две или три 115 - ки и две 40-ки. 

Если все соединим последовательно, получим суммарную емкость в Ампер\часах и 12вольт, если два из них паралельно, то есть плюс с плюсом, а минус с минусом получим 24 вольта, и непонятно какой запас мощности? я правильно понимаю или нет, потому что последний раз я учил это еще в прошлом веке?

Следующий вопрос.

Стандартное автомобильное зарядное устройство, сколько на него можно повесить аккумуляторов для одновременной зарядки?

Следующий вопрос. У меня есть генератор макс. 3500Вт. У этого генератора помимо стандартных розеток есть две дырочки с надписью 12v. Можно ли с этого выхода заряжать аккумулятор, и сколько их можно повесить на этот выход.

В общем, мне нужно устроить ликбез по аккумуляторам. Чего я хочу: Нашел в продаже солнечную панель на 5 Вт(12v). Например(фантазирую) две панели каким-то непонятным мне пока образом я прикручиваю к двум самым большим батареям и надеюсь, что они заряжаются. Дальше, каким-то образом, снимаю с них 24 вольта. На эту халяву думаю повесить ПЛК и один электроклапан ханновский. И таким образом получу минимально примитивную систему автоматического полива. 

Но вся раскладка по мощностям, вольтажу, и остальной теории пока для меня темнота. 

Плюс еще такой нюанс, что например аккумулятор исчисляется в Ампер часах, а лампочка к примеру в ватах. Правильно ли я понимаю, что в формуле И равно У на Р, сопротивление это и есть ватты потребителя? Приношу извинения за такие тупые вопросы, я в молодости все это знал досконально и даже экспериментировал с папиными аккумуляторами. А сейчас как-то роюсь в голове, но там такая каша.... *crazy*


**а-ну-ка** 15-08-2012

Если все соединим последовательно, получим суммарную емкость в Ампер\часах и 12вольт, если два из них паралельно, то есть плюс с плюсом, а минус с минусом получим 24 вольта, и непонятно какой запас мощности? я правильно понимаю или нет, потому что последний раз я учил это еще в прошлом веке?

Не верно с точностью на оборот.


**Oxy** 15-08-2012

Да - да,я уже полазил немного по сайтам, так и чувствовал что туплю. А вот на этой[ ссылке](http://building-forum.ru/energiya/joining-battery.php){:target="_blank"} на картинке номер один, как они посчитали что запас мощности 4 Квт? Ну и остальные нюансы тоже интересуют, сколько можно повесить аккумуляторов на стандартное зарядное устройство. Ну или как посчитать исходя из характеристик зарядки.

Пы.сы, сам играю, сам пою. Умножили вольты на амперы, получили запас в киловат-часах?


**Oxy** 15-08-2012

Короче начитался интернета, аж голова разболелась, прям как перед экзаменом по электротехнике. Понял что ничего не понял.


**Nikolai** 15-08-2012

> Ситуация такая. Есть несколько аккумуляторов разного размера. Две или три 115 - ки и две 40-ки. 
> 
> Если все соединим последовательно, получим суммарную емкость в Ампер\часах и 12вольт, если два из них паралельно, то есть плюс с плюсом, а минус с минусом получим 24 вольта, и непонятно какой запас мощности? я правильно понимаю или нет, потому что последний раз я учил это еще в прошлом веке?

вопрос сложный - пять аккумуляторов, два из них параллельно...

> Следующий вопрос.
> 
> Стандартное автомобильное зарядное устройство, сколько на него можно повесить аккумуляторов для одновременной зарядки?

лучше если один

> Следующий вопрос. У меня есть генератор макс. 3500Вт. У этого генератора помимо стандартных розеток есть две дырочки с надписью 12v. Можно ли с этого выхода заряжать аккумулятор, и сколько их можно повесить на этот выход.

нельзя использовать для зарядки, должно быть ограничение по току

> В общем, мне нужно устроить ликбез по аккумуляторам. Чего я хочу: Нашел в продаже солнечную панель на 5 Вт(12v). Например(фантазирую) две панели каким-то непонятным мне пока образом я прикручиваю к двум самым большим батареям и надеюсь, что они заряжаются. Дальше, каким-то образом, снимаю с них 24 вольта. На эту халяву думаю повесить ПЛК и один электроклапан ханновский. И таким образом получу минимально примитивную систему автоматического полива. 

можно так соединить, только не напрямую. Сходу не скажу, должна быть какая-то развязка батареи от аккумулятора, типа диода и сопротивления.

> Плюс еще такой нюанс, что например аккумулятор исчисляется в Ампер часах, а лампочка к примеру в ватах. Правильно ли я понимаю, что в формуле И равно У на Р, сопротивление это и есть ватты потребителя? Приношу извинения за такие тупые вопросы, я в молодости все это знал досконально и даже экспериментировал с папиными аккумуляторами. А сейчас как-то роюсь в голове, но там такая каша.... *crazy*

У аккумулятора есть вольты (например 12) и амперчасы

вольты умножить на амперчасы и поделить на ватты лампочки (если она на 12 вольт) - получим сколько часов будет гореть лампочка


**orgail** 15-08-2012

и еще поделим пополам, говорят так дольше аккумы служат...


**Vad** 15-08-2012

У меня солнечные батареи стоят с 2008 года. 

освещение в квартире полностью автономно... мне эта тема близка.. и наболевша :)

по аккумуляторам это ко мне! :)

значит так..

исходные данные 

Две или три 115 - ки и две 40-ки

и я так полнял стремимся 24 вольтам? 

(зачем? все равно инвертер нужен.. чтоб 220 делать.. ибо ККЛ от 24 вольт не горят :))

ну и ладно вот ваша схема )) за одно и 12 вольтовая

[![](/imagehost/thumbs/akk.gif)](https://t.me/ponics_ru_files/9352){:target="_blank"}

в любом случае получается 3720 ватт часов (если устроит сок службы акков - 3 раза))

но! разряжать аккумуляторы ниже 30% - сокращает срок службы в РАЗЫ.. то есть при регулярном 30% разряде мы имеем порядка 300-600 циклов(от производителя зависит)

при 50% разряде 150-300 циклов

при 70% всего 50-60!! циклов

а при 100% хватит 2х-3х для того чтоб убить батарею.

заряжать акк нужно током 1/10 емкости 

то есть 40 амперный - 4 ампера 

115 - 11 ампер

всю группу 12 вольтовую по второй схеме = 30 ампер

всю 24вольтовую группу - 15 ампер

кпд кислотного аккумулятора 80% (соотношение полученой энергии при заряде к отданой при разряде)

то есть, если нам в акк нужно залить 100АЧ .. то его нужно заряжать током 10 а в течение 10 часов + еще 20% времени.. 

это я к тому, что ваши 5 ваттные батарейки - своими 0.4 амперами будут заряжать около 1000 часов ))

если у вас их конечно не 20 штук :)

к тому же для автономии, нужно иметь источник тока которого хватило бы для заряда аккумулятора и питания устройства одновременно!

если у вас нагрузка предположим 10 ватт и постоянно подключена (упрощеная схема)

10 ватт при 12 в это ток 0.83A

значит за 24 часа она сьест 240 ватт часов или 19.2 Ампер*Час

такс,теперь, 

световой день, при котором Солнечная батарея будет давать номинальный ток 

(при условии что Вы ее будите поворачивать за солнцем) 

составит летом -8 часов, зимой -4

значит аккумулятор будет работать 20 часов на нагрузку 10 ватт (0.83А).. и 4 часа от солнца 

итого аккумулятор потеряет за ночь 16.6 Ач

если расчитывать аккумулятор то это 55 ач ... при 30% разряде как раз грубо получим 20 ач 

итого нам нужно получить с нее 19 амперчасов для восполнения растраченой энергии аккумулятором + его КПД и питать нагрузку, еще 3.32 Ач.

всего за 4 часа батарея должна дать 19+3.3=22.3 Ач

рабочий ток 22.3\4часа =5.57Ампера 

соответствует мощности солнечной батареи 66 ватт!

округляем до 100.. чтоб можно было восполнять с запасом на пасмурный день... (2 дня солнца нет - за 4 дня солнца акк зарядится)

итого...

для круглосуточной работы нагрузки в 10 ватт нужна солнечная панель 100 ватт ))

скажете - ну это ты взял зимний вариант... летом день длинее.. там хватит и 50 ватт..

нонсенс - но не хватит ))

солнечная батарея дает тот ток который на ней написан при 25(!!) градусах цельсия :)

при меньшей температуре дает БОЛЬШИЙ ток.. 

а при большей температуре ток падает..

причем давольно таки... ощутимо ))

особенно когда на улице +47 на солнце.. и сама панель греется не кисло... итого 60 градусов как с куста )

ну и ток в половину меньше..

а зимой наоборот... ток выше.. из за низкой температуры... но день короче..

кувшинчик и дудочка :)


**Oxy** 15-08-2012

Вот яркий пример красивого и точного ответа на криво и тупо сформулированный вопрос. Я перед этим в нете начитался немного теории, и это дало возможность мне понять все что ты написал. Теперь буду низайше *sos* просить не покидать меня на этой стезе а довести дело до ума на практике. А по ходу дела я буду уточнять конкретные данные реалий.

1. Световой день и зимой и летом тут 12 часов. Возможно на час-два длиннее, но я в 6 утра не хочу выскакивать из постели для замеров. Я пользуюсь маленькой панелькой которая дает мне свет и заряжает мобилу, купил наборчег по случаю в намибии за 70баксов. Очень спасает. Так вот в солнечный день на прямом солнце при вертикальном падении света на пластину она дает 9вольт, а в пасмурную погоду, я замерял на закате в 6 вечера она все равно работает и дает 6,5 вольт. Это сейчас когда зимний период. С сентября начнется лето и облака пропадут на 6 месяцев. 

2. По поводу влияния температуры пластины на КПД я в курсе и это очень прискорбно, нагреваться до 60 градусов будет наверняка. Но надо провести дополнительные эксперименты, возможно размещать пластины не на прямом солнце а под деревьями на продуваемом участке. Тут когда нет облачности солнце шпарит так, что даже от отраженного света прячешься. По этой же причине и нет особой необходимости крутить панель за солнцем. хотя нужно конечно же. Я солнечные очки не могу снять даже в пасмурную погоду - глаза режет.

3. Имеющиеся аккумуляторы не новые а бу, и наверняка неплохо ушатанные, ведь ими пользовались негры. Я вернусь на фазенду и проведу диагностику батарей и заодно уточню сколько там точно у кого каких ампер часов. И на основании этой ревизии уже можно будет чего-то расчитывать.

4. Я не выгребаю вручную каждый час готовить 300 литров раствора и проводить полив, по сути весь день только на это и уходит. Так как полив у меня гравитационный - самотеком, то мне на первое время достаточно чтоб ПЛК просто по графику открывала электромагнитный клапан, который и работает на 24 вольтах. Я не намерен насиловать эти батареи по полной программе. Если эта схема себя оправдает то можно будет подключить и второй электроклапан, так сказать для второй зоны полива. Не хочу томаты и огурцы кормить одним и тем же раствором. То есть в принципе можно обойтись и без инвертора, потому что накачивать воду в поливочный бак я буду генератором, все таки 3,5 кило, плюс есть нульцевый генератор на 6,5 кило аварийный так сказать. До сих пор я гонял ноут именно на маленьком генераторе - за 12 часов хавает около 4 литров бензы которая по 70 центов, то есть день погонять в NFS стоит чуть меньше 3 баксов.

5. Ну и фотка современной африканской лучины которая очень ярко освещает мои тоскливые одинокие ночи:

Внешний вид коробки:

[![](/imagehost/thumbs/3069.jpg)](https://t.me/ponics_ru_files/9353){:target="_blank"}

Как упаковано

[![](/imagehost/thumbs/3070.jpg)](https://t.me/ponics_ru_files/9354){:target="_blank"}

Че внутри, аккумулятор встроенный на 6500 милиампер.

[![](/imagehost/thumbs/3072tst.jpg)](https://t.me/ponics_ru_files/9355){:target="_blank"}[![](/imagehost/thumbs/3077.jpg)](https://t.me/ponics_ru_files/9356){:target="_blank"}

В общем, не пожалел ни капли, что купил, очень практичная и крутая вещь. За такой кит набор тут в сельской местности могут и гопстопнуть :-X


**Vad** 16-08-2012

четр возьми, я совсем забыл в каких широтах ты обитаешь!:)

солнечные батареи это как раз для твоих широт!!!!

отвечу на все вопросы.. не покидаю.. помогу.

если у вас там есть почта какая нибудь - помогу найти, выбрать рассчитать. солнечные панельки подешевле но с доставкой не знаю даже что у вас...

располагать в тени нет смысла.. пусть жарятся! им это в кайф )) при ваших уровнях инсоляции и продолжительности дня - да тьфу на эти 20% которые сьест нагрев панелей..

а если нет недостатка в воде, то можно панели поливать сверху водой.. (насосик махонький) они будут охлаждаться.. а стекшей водой.. можно мыть руки.. или .. ну не знаю.. будет горячая вода еще! ))

а можно и не париться.. повторяю в ваших широтах можно пренебреч всем.))

это тут у нас каждый лучик экономишь ))

с маленькими панельками не советую связываться.. они классная вещь для мобилы ноута.. и прочей микротехники.. но не для аккумуляторов в 300 амперчасов ))

ПОСТРОИМ ТЕБЕ СОЛНЕЧНУЮ ЭЛЕКТРОСТАНЦИЮ! :)

для расчета мне нужно:

1 какой самый мощный потребитель будет подключен, и сколько он будет работать времени в сутки.

2 какая нагрузка будет подключена непрерывно (если циклическая работа - то мощьность и время работы в сутки) по подробнее.

3 сколько дней в неделю бывает облачно

4 пиковая температура на солнце (самая максимальная за весь период)


**Nikolai** 16-08-2012

Вопрос, сколько надо электричества чтобы управлять открытием клапана? В наших краях продается устройство для дачных теплиц, которое тоже по графику открывает клапан, а дальше - самотеком. Так это устройство вообще работает от батареек.

Может так статься что у вас аккумулятора будет на месяц хватать - так стоит ли тогда городить зарядку от солнечных батарей?


**Alex123** 16-08-2012

Ханну и ПЛК можно совершенно спокойно повесить на одну пару одинаковых аккумуляторов, соединенных последовательно (24 вольта). Если удастся найти инвертор, преобразующий 12вольт в 24, то через него можно повесить и на один акумулятор. Для автомобильного аккумулятора ханна и ПЛК это семечки. Солнечная панель, конечно, будет заряжать аккумулятор, но очень медленно. Но т.к. аккумулятор будет разряжаться достаточно слабо, то панель будет просто поддерживать заряд аккума на уровне 12 вольт - она ведь будет подключена на постоянной основе. При последовательной соединении аккумов можно было бы подключить панель через таймер, который бы переключал ее с одного аккума на другой, скажем каждый час. Вообще, для полноты картины желательно увидеть весь алгоритм работы ПЛК и Ханны. 


**ALB** 16-08-2012

а сколько срок службы солнечных панелей в условиях африки ? может ну их нафиг эти провода - хватит солнышка и батареек для работы всей машинерии ?

:-\ по крайней мере все расчёты надо сделать.

PS и плотность электролита для африки тоже вроде меньше должна быть - пластины в аккумуляторах дольше служить будут :-\


**Vad** 16-08-2012

> поддерживать заряд аккума на уровне 12 вольт

сперва 14.2, а потом по достижение 14.2 скидывать до 13.7

иначе кирдык .. перезаряд разрушение положительного электрода, выкипание воды из электролита...

это вам так просто говорить, согревши литр водички для чайка.. в электрочайнике, удобно расположившись под кондиционером, включив настольную лампу и телевизор.. - та.. поствь батарейки .. или Хана и плк - семечки :)

а у человека ВООБЩЕ НЕТ ЭЛЕКТРИЧЕСТВА... СОВСЕМ...

и грех не воспользоваться халявой.. 

и лампочками... 2мя,3мя.. ноутом.. телефоном... радио.. телевизором даже.. русскоязычным спутниковым тв.. почему нет?

можно даже и кондиционером... 

особенно когда день 12 часов.. ё-мое.. :) 

ночью там прохладно?

какая температура?


**Alex123** 16-08-2012

В ваших краях очень класно бы работал такой вариант. Концентрирующий пораболический солнечный коллектор нагревает воду до состояния пара, который подается в паровой двигатель, вращающий генератор. Скачивал на Ютубе видеоролик с показом данного процесса - примитивный паровой двигатель вращал генератор на 4квт, от которого работала болгарка.


**Vad** 16-08-2012

> а сколько срок службы солнечных панелей в условиях африки ? 

ну наверное не меньше чем в космосе ))

там по крайней мере не летают космические камни... и не пробивают насквозь.. ))

кусок кремния служит 25 лет при этом снижения эффективности до 80%

то есть.. через 25 лет.. к 100 ваттам нужно будет докинуть еще 20 ваттну панельку ))

но думаю реальнее цифра 10 лет... за это время обязательно что то случится ))

пьяный негр на нее упадет.. или ее сгрызут шакалы))


**Vad** 16-08-2012

> В ваших краях очень класно бы работал такой вариант. Концентрирующий пораболический солнечный коллектор нагревает воду до состояния пара, который подается в паровой двигатель, вращающий генератор. Скачивал на Ютубе видеоролик с показом данного процесса - примитивный паровой двигатель вращал генератор на 4квт, от которого работала болгарка.

тут уже нужна система слежения за солнцем...

куча механических деталей.. зачем??

*???*


**Alex123** 16-08-2012

> > В ваших краях очень класно бы работал такой вариант. Концентрирующий пораболический солнечный коллектор нагревает воду до состояния пара, который подается в паровой двигатель, вращающий генератор. Скачивал на Ютубе видеоролик с показом данного процесса - примитивный паровой двигатель вращал генератор на 4квт, от которого работала болгарка.
> 
> 
> 
> тут уже нужна система слежения за солнцем...
> 
> куча механических деталей.. зачем??
> 
> *???*

Халява, сэр ! :D :D


**Vad** 16-08-2012

ничесе халява..

в СБ ниче не крутится, не движется, не обслуживается, не сломается..

и стоит дешевле )) чем паровой котел, коллектор, и иже с им


**ALB** 16-08-2012

в данном случае кпд парового котла будет меньше - нужно преобразовать свет в температуру , воду в пар , давление пара в поступательное движение поршней, движение поршней во вращение ротора генератора и только оттуда получить электричество, а ещё не забыть систему смазки этих самых поршней и прочей гадости , конденсатор для отработанного пара, удаление накипи из котла *Wall* .

а солнечная батарея - поставил и забыл - ни смазки ни воды не надо - смахнул пыль раз в несколько месяцев и снова забыл - вот где халява то *8)*


**Oxy** 16-08-2012

Всем спасибо за участие, так как тема себя исчерпала, и вылилась в логичную следующую, тут закрываемся, открываемся в узлах и агрегатах.


