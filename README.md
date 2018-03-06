# Итак, вам нужен инпут
Данное руководство содержит исчерпывающие инструкции по выбору элементов веб-форм.

![so-you-need-an-input](https://raw.githubusercontent.com/pfrankov/so-you-need-an-input/master/so-you-need-an-input.png)

#### Ситуация
Вы — дизайнер, который с уважением относится к своим коллегам по фронту и к пользователям вашего веб-приложения.  
Перед вами непростая задача: спроектировать форму. Если вы нормальный, адекватный человек — вы терпеть не можете проектировать формы. Фронтендер ненавидит эти формы верстать. Бекендер ненавидит их валидировать. А пользователь, в свою очередь, ненавидит их заполнять.

## Как спроектировать форму правильно?
### Начнём с аксиом
- Любое обучение интерфейсу имеет цену в реальных деньгах;
- Лучший интерфейс — это отсутствие интерфейса;
- Отличный интерфейс — это знакомый интерфейс;
- Компоненты интерфейса должны быть максимально знакомыми, а поведение — ожидаемым;
- Сложно придумать что-то лучше, чем использовать стандартные компоненты операционной системы;
- Меньше нестандартных компонентов → быстрее разработка, дешевле поддержка;
- Меньше форма → больше вероятность её заполнения;
- Сыр пахнет грязными носками.

Теперь, когда вы потеряли бдительность, самое время разобрать несколько вариантов типичных полей:

### Имя пользователя
```
→ Любой текст
	→ Текста может быть больше,
	  чем 80 символов?
		→ Нет
			→ Текст
      
<input type="text" />
```
<img width="143" alt="login" src="https://user-images.githubusercontent.com/584632/37020922-acfbb112-212e-11e8-8358-897063c28916.png">
_Информация для программистов на HTML:_ Понятное дело, `type` инпутов нужно подбирать по смыслу: если нужен *email* — потрудитесь проставить именно этот тип.

### Пароль
```
→ Любой текст
	→ Текста может быть больше,
	  чем 80 символов?
		→ Нет
			→ Текст
      
<input type="password" />
```
<img width="138" alt="password" src="https://user-images.githubusercontent.com/584632/37020924-ad171f06-212e-11e8-998b-4f6eaed0029f.png">

### Пол
```
→ Выбор из фиксированных значений
	→ Множественный выбор
	  или возможность
	  отмены?
		→ Нет
			→ < 5 вариантов
				→ Радио-кнопка
      
<input type="radio" />
```
<img width="215" alt="sex" src="https://user-images.githubusercontent.com/584632/37020925-ad364fca-212e-11e8-80c5-180a46afca8e.png">


## Правильные ответы на правильные вопросы
#### А когда использовать слайдер?
Никогда не используйте слайдер.

#### Но как же я буду ограничивать пользователя, чтобы он специально не ввёл некорректные данные?
Для этого вы будете использовать валидацию полей на клиенте и на сервере.

#### Что ещё за «Комбобокс»?
Смесь селекта и инпута. Инпут используется для поиска. 

#### Чипсы?
Chips. Типа теги такие.

## Контрибуция
Фил фри ту фок!
