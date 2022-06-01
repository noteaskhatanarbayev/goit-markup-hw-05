# goit-markup-hw-05

«A1» В корне проекта есть папка images с изображениями.

«A2» Все векторные изображения (иконки) собраны в SVG-спрайт icons.svg, который лежит в папке images.

«A3» Все векторные изображения оптимизированы.

«A4» В корне проекта есть папка css с файлами стилей.

«A5» Все стили написаны в одном файле styles.css, который находится в папке css.

«A6» В названиях файлов нет заглавных букв, пробелов и транслита, только буквы и слова английского языка.

«A7» Исходный код отформатирован при помощи Prettier.

«A8» Все изображения и текстовый контент взяты из макета.

«A9» На всех HTML-страницах подключен нормализатор стилей modern-nomalize.

«A10» Код написан следуя руководству.

Разметка
«B1» Для всех иконок используется векторная графика в формате svg.

«B2» SVG-иконки экспортированы правильно. При экспорте выбрана «группа», а не сам вектор.

«B3» Все иконки из SVG-спрайта добавлены в HTML при помощи тегов <svg> и <use>

«B4» Размеры иконок взяты из макета и заданы элементу <svg> в HTML-файле.

«B5» В блоке Контактов в шапке, добавлены иконки конверта и телефона.

«B6» В секции Преимуществ добавлены иконки.

«B7» В секции Команды добавлены иконки соцсетей.

«B8» В секции Клиентов добавлены иконки компаний.

«B9» В футере добавлены иконки соцсетей.

Оформление
«C1» Большое изображение с эффектом затемнения (под хедером) выполнено как фон. Для затемнения используется многослойный фон с градиентом.

«C2» Фоновое изображение в блоке под хедером не растягивается шире своего оригинального размера 1600рх.

«C3» В карточках секции Наша команда есть постоянный эффект тени.

«C4» В карточках страницы Портфолио есть эффект тени при ховере в любом месте карточки.

«C5» В фильтре (список кнопок) страницы Портфолио есть эффект тени при ховере или фокусе на кнопки.

«C6» При ховере или фокусе, иконки должны переходить в активное состояние - изменять цвет, если это указано в макете.
Проект
«A1» Все стили написаны в одном файле styles.css, который находится в папке css.

«A2» Исходный код отформатирован при помощи Prettier.

«A3» Все изображения и текстовый контент взяты из макета.

«A4» На всех HTML-страницах подключен нормализатор стилей modern-nomalize.

«A5» Код написан следуя руководству.

«A6» Скрипт модального окна подключен в HTML отдельным файлом modal.js.

Разметка
«B1» Выполнена HTML-разметка всех элементов макета.

«B2» Теги использованы согласно их семантического смысла.

Оформление
«C1» Для всех эффектов ховера и фокуса (цвет, фон, тень) сделаны переходы. Время - 250ms, функция распределения времени - cubic-bezier(0.4, 0, 0.2, 1).

«C2» В переходах и анимациях явно указаны анимируемые свойства. Нигде нет значения all.

«C3» В секции Чем мы занимаемся текст с фоном спозиционирован поверх изображения.

«C4» В главной навигации, при помощи псевдоэлемента ::after, сделано подчёркивание ссылки текущей страницы (на которой сейчас находится пользователь).

«C5» Синий оверлей с текстом на карточках страницы Портфолио появляется при ховере в любом месте карточки.

«C6» Синий оверлей в карточках страницы Портфолио выезжает снизу, как показано на видео.

card overlay preview
«C7» У псевдоэлементов нет текстового контента в свойстве content. Они использованы исключительно для декоративного оформления.

Модальное окно
«D1» Выполнена разметка и оформление «бекдропа» (тёмного полупрозрачного фона) модального окна.

«D2» «Бекдроп» заполняет 100% высоты и ширины вьюпорта браузера и фиксирован в нём.

«D3» Выполнена разметка и оформление модального окна.

«D4» Модальное окно вертикально и горизонтально спозиционировано посередине бекдропа.

«D5» Выполнена разметка и оформление кнопки закрытия модального окна в верхнем правом углу.

«D6» Изначально модальное окно и бекдроп скрыты при помощи класса is-hidden на бекдропе, в селекторе которого используются свойства visibility, opacity и pointer-events.

«D7» Если убрать с бекдропа класс is-hidden - появляется бекдроп и модальное окно.

«D8» Появление и скрытие модального окна анимировано при помощи перехода с произвольным эффектом, например scale или translate, и opacity.

Открытие/закрытие модального окна
Модальное окно с формой заявки открывается по клику на кнопку "Заказать услугу". Для того чтобы скрипт сработал необходимо добавить в разметку специальные атрибуты, по которым скрипт ищет элементы:

data-modal-open - на кнопку открытия модального окна.
data-modal-close - на кнопку закрытия модального окна.
data-modal - на бекдроп модального окна.
После чего, перед закрывающим тегом body добавить тег script со ссылкой на файл скрипта для модально окна. Можно посмотреть видео-инструкцию.

<body>
  <!-- Вся твоя разметка, включая разметку модалки -->

  <!-- Ставим перед закрывающим тегом body -->
  <script src="./js/modal.js"></script>
</body>

Скрипт который необходимо скопировать и вставить в файл modal.js.

(() => {
const refs = {
openModalBtn: document.querySelector("[data-modal-open]"),
closeModalBtn: document.querySelector("[data-modal-close]"),
modal: document.querySelector("[data-modal]"),
};

refs.openModalBtn.addEventListener("click", toggleModal);
refs.closeModalBtn.addEventListener("click", toggleModal);

function toggleModal() {
refs.modal.classList.toggle("is-hidden");
}
})();
