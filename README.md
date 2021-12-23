###### ***Эта документация доступна на русском языке. Если хотите прочитать, прокрутите вниз***
# AccordionRush `English version`

**AccordionRush** - This is a free plugin that allows you to install
accordion inside html markup using pure JavaScript.

## Connection

To get started, you need to download and connect before the closing tag `body`
`accordion-rush.js` file, be sure to check the paths in your project.

```
<body>
    <!-- Плагин подключаем перед основным скриптом-->
    <script src="js/accordion-rush.js"></script>

    <!-- Основной скрипт-->
       <script src="js/script.js" ></script>
</body>
```

## Initialization

We need to create the markup for our accordions.

For the wrapper, you need to set a unique `class` (in our case, it is `.accordion__container`), you also need to set the second unique `class` for the `accordion__item-body` (in our case, it is `accordion__item-body-one`)

we will use these classes during initialization.

(The active class will be applied to the `accordion__item-body` and will be named `accordion__item-active by default`)

```
<div class="accordion__container">
        <div class="accordion__item">
            <div class="accordion__item-title">
                accordion one
            </div>

            <div class="accordion__item-body accordion__item-body-one">
                <div class="content">
                    Lorem ipsum dolor sit amet 
                    consectetur adipisicing elit. Minima ea, 
                    voluptatem amet dicta fugiat architecto nesciunt
                </div>
            </div>
        </div>
    </div>
```

After that, we need to initialize the `accordion__container` and `accordion__item-body-one` in JavaScript

```
new AccordionRush('.accordion__container', {
    itemBody: '.accordion__item-body-one'
})
```

here we use `itemBody` to initialize the `class` `accordion__item-body-one`.
Most importantly, `accordion__item-body-one` was written with a period at the beginning.

## Make some accordions

If you want to make several accordions, then you will need to reproduce the `accordion__item`
together with the class that was specified in `itemBody` (in our case it is `accordion__item-body-one`)

Example:
```
    <div class="accordion__container">

        <div class="accordion__item">
            <div class="accordion__item-title">
                accordion one
            </div>
            <div class="accordion__item-body accordion__item-body-one">
                <div class="content">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                    Minima ea, voluptatem amet dicta fugiat
                    architecto nesciunt pariatur odio atque et tempore facilis neque quas.
                </div>
            </div>
        </div>

        <div class="accordion__item">
            <div class="accordion__item-title">
                accordion two
            </div>
            <div class="accordion__item-body accordion__item-body-one">
                <div class="content">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                    Minima ea, voluptatem amet dicta fugiat
                    architecto nesciunt pariatur odio atque et tempore facilis neque quas.
                </div>
            </div>
        </div>

    </div>
```

## Make two unrelated accordions

If you need to make two accordions that are located in different sections, you will need to make a unique class for the wrapper and the `accordion__item-body`

Example:
```
    <div class="accordion__container-two">

        <div class="accordion__item">
            <div class="accordion__item-title">
                accordion one
            </div>
            <div class="accordion__item-body accordion__item-body-two">
                <div class="content">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                    Minima ea, voluptatem amet dicta fugiat
                    architecto nesciunt pariatur odio atque et tempore facilis neque quas.
                </div>
            </div>
        </div>

        <div class="accordion__item">
            <div class="accordion__item-title">
                accordion two
            </div>
            <div class="accordion__item-body accordion__item-body-two">
                <div class="content">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                    Minima ea, voluptatem amet dicta fugiat
                    architecto nesciunt pariatur odio atque et tempore facilis neque quas.
                </div>
            </div>
        </div>

    </div>
```

JS:
```
new AccordionRush('.accordion__container-two', {
    itemBody: '.accordion__item-body-two'
})
```

## Parameters

* itemBody: 'accordion__item-body-two' - makes it possible to initialize the box with the opening content `accordion__item-body`

* transitionTabs: '300ms ease' - makes it possible to add smoothness when the accordion is opened (ms can be changed as you need, you can also change ease to ease-in-out and other css transitions for animation)

* openAllTabs: true, false - if you enable this parameter, then when the accordion is opened, the others will not close (by default, if you open one, and then the second, the first one will close)

* activeClassTabs: 'example-active' - using this parameter you can change the active class


## Default parameters


If you do not specify any parameters in the `AccordionRush` plugin, the default values will be used:

* activeClassTabs: 'accordion__item-active'
* openAllTabs: false
* itemBody: 'there is no default parameter for it'
* transitionTabs: '700ms ease'






# AccordionRush `Russian version`

**AccordionRush** - Это бесплатный плагин который позволяет реализовать
accordion внутри html разметки используя чистый JavaScript.

## Подключение

Для начала работы необходимо скачать и подключить перед закрывающимся тегом `body`
файл `accordion-rush.js`, обязательно проверьте пути в своем проекте.

```
<body>
    <!-- Плагин подключаем перед основным скриптом-->
    <script src="js/accordion-rush.js"></script>

    <!-- Основной скрипт-->
       <script src="js/script.js" ></script>
</body>
```


## Инициализация

Нам необходимо создать разметку для наших аккордеонов.

Для обертки необходимо задать уникальный `class` (в нашем случае это  `.accordion__container`)
ещё потребуется задать вторым уникальный `class` для `accordion__item-body` (в нашем случае это  `accordion__item-body-one`)

эти классы мы будем использовать при инициализации. 

(Активный класс будет наносится на `accordion__item-body` и будет называться по умолчанию `accordion__item-active`)
```
<div class="accordion__container">
        <div class="accordion__item">
            <div class="accordion__item-title">
                accordion one
            </div>

            <div class="accordion__item-body accordion__item-body-one">
                <div class="content">
                    Lorem ipsum dolor sit amet 
                    consectetur adipisicing elit. Minima ea, 
                    voluptatem amet dicta fugiat architecto nesciunt
                </div>
            </div>
        </div>
    </div>
```

После этого нам нужно инициализировать `accordion__container` и `accordion__item-body-one` в JavaScript

```
new AccordionRush('.accordion__container', {
    itemBody: '.accordion__item-body-one'
})
```

тут мы с помощью `itemBody` инициализируем `class` `accordion__item-body-one`. 
Самое главное `accordion__item-body-one` была написана с точкой в начале.


## сделать несколько аккордеонов

Если Вы хотите сделать несколько аккордеонов, то Вам надо будет размножить `accordion__item` 
вместе с классом который указали в `itemBody` (в нашем случае это `accordion__item-body-one`)

Пример:

```
    <div class="accordion__container">

        <div class="accordion__item">
            <div class="accordion__item-title">
                accordion one
            </div>
            <div class="accordion__item-body accordion__item-body-one">
                <div class="content">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                    Minima ea, voluptatem amet dicta fugiat
                    architecto nesciunt pariatur odio atque et tempore facilis neque quas.
                </div>
            </div>
        </div>

        <div class="accordion__item">
            <div class="accordion__item-title">
                accordion two
            </div>
            <div class="accordion__item-body accordion__item-body-one">
                <div class="content">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                    Minima ea, voluptatem amet dicta fugiat
                    architecto nesciunt pariatur odio atque et tempore facilis neque quas.
                </div>
            </div>
        </div>

    </div>
```


## Сделать два несвязанных аккордеона

Если вам требуеться сделать два аккордеона которые будут расположены в разных секциях, 
Вам нужно будет сделать уникальный класс для обертки и `accordion__item-body`

Пример:
```
    <div class="accordion__container-two">

        <div class="accordion__item">
            <div class="accordion__item-title">
                accordion one
            </div>
            <div class="accordion__item-body accordion__item-body-two">
                <div class="content">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                    Minima ea, voluptatem amet dicta fugiat
                    architecto nesciunt pariatur odio atque et tempore facilis neque quas.
                </div>
            </div>
        </div>

        <div class="accordion__item">
            <div class="accordion__item-title">
                accordion two
            </div>
            <div class="accordion__item-body accordion__item-body-two">
                <div class="content">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                    Minima ea, voluptatem amet dicta fugiat
                    architecto nesciunt pariatur odio atque et tempore facilis neque quas.
                </div>
            </div>
        </div>

    </div>
```

JS:
```
new AccordionRush('.accordion__container-two', {
    itemBody: '.accordion__item-body-two'
})
```



## Параметры

* itemBody: 'accordion__item-body-two' - дает возможность инициализировать бокс с открывающимся контентом `accordion__item-body`

* transitionTabs: '300ms ease' - дает возможность добавить плавность при открытии аккордеона
(ms можно изменить как вам требуется, также можно изменить ease на ease-in-out и 
другие css переходы для анимации)

* openAllTabs: true, false - если включить этот параметр, то при открытие аккордеона 
другие не будет закрываться (по умолчанию если открыть один, а потом второй, то первый закроется)

* activeClassTabs: 'example-active' - с помощью этого параметра можно изменить активный класс


## Параметры по умолчанию

Если в плагине `AccordionRush` не указать какие либо параметры, будут применяться значения по умолчанию:

* activeClassTabs: 'accordion__item-active'
* openAllTabs: false
* itemBody: 'для него параметра по умолчанию нету'
* transitionTabs: '700ms ease'