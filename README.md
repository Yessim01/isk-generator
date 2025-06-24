# isk-generator
Веб-приложение для создания исковых заявлений с помощью простой формы ввода данных.
<!DOCTYPE html><html lang="ru">
<head>
  <meta charset="UTF-8" />
  <title>Генератор исковых заявлений</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-50 min-h-screen flex flex-col">
  <!-- Шапка сайта -->
  <header class="bg-blue-600 text-white p-4 shadow-md">
    <h1 class="text-center text-2xl font-bold">Генератор исковых заявлений</h1>
  </header>  <!-- Основной контейнер -->  <main class="flex-1 p-8 grid lg:grid-cols-2 gap-8">
    <!-- Раздел О генераторе -->
    <section class="bg-white rounded-2xl shadow-xl p-6 space-y-4">
      <h2 class="text-xl font-semibold text-blue-600">О генераторе</h2>
      <p class="text-gray-700">Этот генератор помогает быстро создавать типовые исковые заявления. Введите свои данные, а сайт сгенерирует готовый текст для подачи в суд.</p>
      <p class="text-gray-700">Подходит для студентов юридических факультетов и начинающих юристов для тренировки навыков составления процессуальных документов.</p>
    </section><!-- Форма для генерации -->
<section class="bg-white rounded-2xl shadow-xl p-6 space-y-4">
  <h2 class="text-xl font-semibold text-blue-600">Сформировать заявление</h2>
  <form id="claim-form" class="space-y-4">
    <input id="fio-istca" class="w-full p-2 border rounded" placeholder="ФИО истца" required />
    <input id="address-istca" class="w-full p-2 border rounded" placeholder="Адрес истца" required />
    <input id="fio-otvetchika" class="w-full p-2 border rounded" placeholder="ФИО ответчика" required />
    <textarea id="sut-pretenzii" class="w-full p-2 border rounded" placeholder="Суть претензии" required></textarea>
    <input id="summa-iska" class="w-full p-2 border rounded" placeholder="Сумма иска" required type="number" min="0" />
    <button class="w-full bg-blue-600 text-white p-2 rounded hover:bg-blue-700" type="submit">Сгенерировать заявление</button>
  </form>
</section>

<!-- Раздел результата -->
<section class="bg-white rounded-2xl shadow-xl p-6 space-y-4 lg:col-span-2">
  <h2 class="text-xl font-semibold text-blue-600">Ваше заявление</h2>
  <textarea id="result" class="w-full p-2 border rounded h-64" readonly></textarea>
</section>

  </main>  <!-- Подвал сайта -->  <footer class="bg-blue-600 text-white p-4 text-center text-sm">
    © 2025 Генератор исковых заявлений — учебный проект студента-юриста
  </footer>  <script>
    const form = document.getElementById('claim-form');
    const result = document.getElementById('result');
    form.addEventListener('submit', (e) => {
      e.preventDefault();
      const fioIstca = document.getElementById('fio-istca').value;
      const addressIstca = document.getElementById('address-istca').value;
      const fioOtvechika = document.getElementById('fio-otvetchika').value;
      const sutPretenzii = document.getElementById('sut-pretenzii').value;
      const summaIska = document.getElementById('summa-iska').value;

      const text = В суд\n\nИстец: ${fioIstca}, адрес: ${addressIstca}\nОтветчик: ${fioOtvechika}\n\nИСКОВОЕ ЗАЯВЛЕНИЕ\n\nЯ, ${fioIstca}, предъявляю иск к ${fioOtvechika} в связи с тем, что ${sutPretenzii}, в результате чего мне причинён ущерб в размере ${summaIska} тенге.\n\nПрошу суд:\n1. Рассмотреть настоящее заявление.\n2. Взыскать с ответчика сумму ущерба в размере ${summaIska} тенге.\n3. Возместить судебные расходы.\n\nДата: ____________\nПодпись: ____________\n;
      result.value = text;
    });
  </script></body>
</html>
# 🧑‍⚖️ Генератор исковых заявлений

*Учебный проект для студентов-юристов.*  
Это мини-сайт с генератором типовых исковых заявлений по шаблонам.

---

## 🎯 Описание
Данный проект помогает быстро создавать текст исковых заявлений для тренировки навыков составления юридических документов.  
Пользователь вводит свои данные (ФИО, суть претензии, сумма иска), а сайт подставляет их в готовый шаблон.

---

## 🧭 Как использовать
1. Открой сайт по ссылке (будет доступна после активации GitHub Pages).
2. Заполни поля с информацией об истце, ответчике и сути претензии.
3. Нажми «Сгенерировать заявление» — текст появится ниже.
4. Скопируй готовый текст для тренировки или использования в учебных целях.

---

## 🛠 Технологии
- HTML5
- Tailwind CSS для оформления
- Простая логика на JavaScript для подстановки данных

---

## 📄 Лицензия
Этот проект пока не имеет лицензии — использовать можно для учебных целей.

---

## 🤝 Контакты
Например:  
Если у вас есть вопросы или предложения — напишите мне на ( esaserikbaevv@gmail.com ).
