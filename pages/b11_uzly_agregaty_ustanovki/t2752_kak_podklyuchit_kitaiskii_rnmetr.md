---
title: "Как подключить китайский рН-метр?"
sidebar: ponics_sidebar
---

**serge mat** 01-11-2017

Купил на алиэкспрессе рН-метр. 

![](https://scontent-lga3-1.xx.fbcdn.net/v/t1.0-9/22894123_2024421504455606_1623898933650044895_n.jpg?oh=07c8e944103aa458fe102e89d8c065ea&amp;oe=5A72EB5F)![](https://scontent-lga3-1.xx.fbcdn.net/v/t1.0-9/22893977_2024421517788938_9087116497934870866_n.jpg?oh=0b0b9853e47a3e7d660857cfe2747e5e&amp;oe=5AA3EC0D)

Теперь не знаю, как его подключить. У датчика 6 пинов. Я смог догадаться, что V+ - это для подачи питания, в инструкции сказано, 5V. Два пина G, как я догадываюсь, это общий. Остаются еще три: To, Do, Po. Кто из них кто?

Приводится скетч для ардуино, там указано только:

#define SensorPin 0 //pH meter Analog output to Arduino Analog Input 0

А что именно надо подключить к этому пину не сказано. Зато в конце скетча есть такой момент:

digitalWrite(13, HIGH);

delay(800);

digitalWrite(13, LOW);

Это они для примера, что можно делать что-то еще? 

Это о том, что между измерениями должно быть не меньше 0,8 секунды?

Или еще один пин надо задействовать на вход?

Может кто знает...

Инструкцию на китайском прикладываю.

[б-+·¬ъ¦ч+Lб¬Ardunio PH+л¬¦¦ўT¦+ў¦щ.pdf](https://t.me/ponics_ru_files/18849){:target="_blank"}

**allex_step** 01-11-2017

P0 - аналоговый вход

T0 - TempComp1 (NC)

D0 - TempComp2 (NC)

[http://iarduino.ru/shop/Sensory-Datchiki/datchik-kislotnosti-zhidkosti-rn-metr.html](http://iarduino.ru/shop/Sensory-Datchiki/datchik-kislotnosti-zhidkosti-rn-metr.html){:target="_blank"}


**veresk** 01-11-2017

Po аналоговый выход PH

To тепрературный выход

Do это как сигнализация о том что пш достиг установленного уровня.


**** 01-11-2017

Воооо! У меня такой-же.))

Держи: https://forum.arduino.cc/index.php?topic=336012.0

И не благодари.

В статье все интуитивно понятно, если в английском не силен.

Сия шилда имеет инвертированое вычисление(измерение?).

Нормально работает.


**serge mat** 01-11-2017

Спасибо, стало понятно.

> To тепрературный выход

Температуру тоже можно им замерять? Кто-нибудь пробовал?


**Vad** 01-11-2017

> А что именно надо подключить к этому пину не сказано. Зато в конце скетча есть такой момент:
> 
> digitalWrite(13, HIGH);
> 
> delay(800);
> 
> digitalWrite(13, LOW);
> 
> Это они для примера, что можно делать что-то еще? 
> 
> Это о том, что между измерениями должно быть не меньше 0,8 секунды?

это лампочкоймигайка..

на 13 пине висит светодиод ))


**Vad** 01-11-2017

> Температуру тоже можно им замерять? Кто-нибудь пробовал?

конечно пробовали ))

он немедленно начнет показывать температуру(причем, не земную а на марсе!)

как только вы его сунете в рабочую емкость... с раствором..

а не в стаканчике... ;)


**Пресвятой_ДжимБим** 01-11-2017

Подтверждаю. Температуру на этом шилде не смог ещё измерить никто..


**Пресвятой_ДжимБим** 01-11-2017

> P0 - аналоговый вход
> 
> T0 - TempComp1 (NC)
> 
> D0 - TempComp2 (NC)
> 
> [http://iarduino.ru/shop/Sensory-Datchiki/datchik-kislotnosti-zhidkosti-rn-metr.html](http://iarduino.ru/shop/Sensory-Datchiki/datchik-kislotnosti-zhidkosti-rn-metr.html){:target="_blank"}

Немножко не та шилда. При использовании скетча по ссылке - топикастера ждёт сюрприз)


**Пресвятой_ДжимБим** 01-11-2017

Датчик температуры отдельный ставьте на ардуину. Типа ds18b20. Опираться в вычислениях на него сможете для всех устройств, которым нужна поправка на температуру.


**Vad** 01-11-2017

> Подтверждаю. Температуру на этом шилде не смог ещё измерить никто..

да я не про температуру.. вообще то )


**Пресвятой_ДжимБим** 01-11-2017

 :D


**** 01-11-2017

Ну ваще мощно для домашней установки систему измерений делать. Не, ну я понимаю у Сива тыща литров раствора за день поглощают полтора огурца.. а остальным то зачем?

Для теплички эти агрегаты - в самый раз.

И вообще -

"Домашний сад" рулит!!!)) 


**serge mat** 02-11-2017

Любопытно, но у меня оказалась слишком низкой чувствительность. Мне пришлось внести коэффициент 2,236.

То есть если электрод показывает изменение рН на одну единицу, то на самом деле произошло изменение на две единицы с лишним!

const float k=2.236;

float f;

int Po = 1023-analogRead (pHpin);

f = (float) Po;

f *= k*14./1023.;


**Vad** 02-11-2017

нужно взять две точки ~2 и ~10

запомнить значение ацп... а внутри интерполяция..

и все *???*

делается в 1 строчку ..


**serge mat** 02-11-2017

> нужно взять две точки ~2 и ~10
> 
> запомнить значение ацп... а внутри интерполяция..
> 
> и все *???*
> 
> делается в 1 строчку ..

Не вопрос! 

Просто во всех текстах ни слова не было про коэффициент...


**Vad** 02-11-2017

а нафиг он нужен.. если все само случится..

просто "натянется" диапазон значений АЦП на pH... и все.. никаких коэффициентов.. блин..

понавыдумывают.. потом голову ломают :D


**serge mat** 02-11-2017

> а нафиг он нужен.. если все само случится..
> 
> просто "натянется" диапазон значений АЦП на pH... и все.. никаких коэффициентов.. блин..
> 
> понавыдумывают.. потом голову ломают :D

Видимо я не правильно объяснил.

Если я беру значение АЦП и натягиваю на диапазон от 0 до 14, то получается фигня.

Надо после этого действия еще умножить на коэффициент, подобранный вручную.

Иначе говоря, диапазон получается от 0 до 32 примерно...

Вроде вот так, с коэффициентом показывает что-то похожее на правду.


**Пресвятой_ДжимБим** 02-11-2017

Po = (1023 - analogRead(pHpin)) / 73.07;

Не вставляет? :)


**Пресвятой_ДжимБим** 02-11-2017

Вообще, Вад правильно написал, ограничивай диапазон, а внутри интерполяция. Ибо линейность этого ph-метра такая прям линейнооость.. *Dance*

Тут где-то уже обоссывалась эта тема.


**Cyclamech** 02-11-2017

> Po = (1023 - analogRead(pHpin)) / 73.07;

Шикарный код! В "лучших традициях"! Пеши исчо! *8)*


**Пресвятой_ДжимБим** 02-11-2017

> > Po = (1023 - analogRead(pHpin)) / 73.07;
> 
> 
> 
> Шикарный код! В "лучших традициях"! Пеши исчо! *8)*

:D


**unclef1** 08-12-2017

Протестировал такой. Ниже 3 х вольт по выходу не дает. А так реагирует на разные растворы. Чувствительный даже к дыханию на плату. Собрал свою схему. Совместил с измерением EC. Что по выходу у этой платы должно быть?


**java** 07-04-2019

Всем привет!

Столкнулся с очень странной проблемой. по таблице рН 4 соответствует 1,14 вольт а рН 10 соответственно 2,86. (аналоговый вход на pin)

У моего датчика всё наоборот. И поэтому когда я отпускаю датчик в раствор с рН 4 он показывает 10, а когда в рН 10 то показывает 4. Как можно конвертировать вход с датчика?

void readPH() /*--(Subroutine, reads current value of pH Meter)--------------------------------------------*/

{

for(int i=0; i&lt;10; i++) //получите 10 значений выборки от датчика, чтобы сгладить 

// значение

{ 

pHavg = analogRead(pHpin); //получите чтение от датчика ПЭ-аш и положите в массив

delay(10); //короткая задержка между показаниями

}

for(int i=0; i&lt;9; i++) //сортировка аналоговых значений от малых до больших

{

for(int j=i+1; j&lt;10; j++) 

{

if(pHavg &gt; pHavg[j]) //если значение" i "массива больше значения" j

{

temp = pHavg; //присвоить" i " временной переменной

pHavg = pHavg[j]; //переключить" j "в положение" i"

pHavg[j] = temp; //переключить" i "в положение" j"

}

}

}

avgValue = 0;

for(int i=2; i&lt;8; i++) //возьмите значение всего 6 значений Центрального массива

{

avgValue += pHavg; //get total

}

pHvalue = (float)avgValue*5.0/1024/6; //сопоставьте аналог (0-1023) с милливольтом (0-5).. 

// деление на 6 в среднем

if (negative == 0) //если смещение положительное... см. раздел подпрограмма 

// калибровки.. отрицательный инициализируется как 0

{

pHvalue = (slope*3.5*pHvalue + offset + offset2); //преобразуйте милливольт в значение ПЭ-аш, с 

// положительными смещением и наклоном от 

// калибровки

}

else

{

pHvalue = (slope*3.5*pHvalue - offset + offset2); //преобразуйте милливольт в значение pH с 

// отрицательным смещением и наклоном от калибровки

}

}


**siv237** 08-04-2019

просто 1023 отнять то что на с ацп идет не подойдет?

avgValue=1023-avgValue


**java** 17-04-2019

Нет, пробовал уже по всякому, если изменять эту величину, начинает писать рН -230, или 40, и перестаёт вобще реагировать. Заказал у китайцев другой датчик. ну не должно быть напряжение с датчика наооборот.

