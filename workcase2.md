# Звіт з лабораторної роботи (Work-case 2)
**Дисципліна:** Операційні системи

---
**МІНІСТЕРСТВО ОСВІТИ І НАУКИ УКРАЇНИ** **КИЇВСЬКИЙ ФАХОВИЙ КОЛЕДЖ ЗВ'ЯЗКУ**

**Виконала:** студентка групи БІКС-33 Руда Дарина Сергіївна  
**Перевірила:** викладач Сушанова Вікторія Сергіївна  

**Київ 2026**

---

## 1. Встановлення гіпервізора
Для виконання лабораторної роботи було обрано **Oracle VM VirtualBox**. Це гіпервізор II типу, який дозволяє запускати гостьові ОС ізольовано від основної системи. В процесі було налаштовано глобальні параметри віртуалізації для підтримки 64-бітних систем.

## 2. Налаштування віртуальної машини та обладнання

Етап конфігурації включає підготовку "заліза" віртуальної машини перед встановленням ОС:

* **Створення носія даних:** Налаштування параметрів віртуального жорсткого диска.
![Створення віртуального диска](image_e53125.png)  
*Процес визначення розміру та формату диска для основної системи. Обрано динамічне розширення для економії місця на хості.*

* **Налаштування мережі:** Забезпечення доступу до Інтернету.
![Налаштування Wi-Fi адаптера](image_e5342b.png)  
*Вибір мережевого мосту (Bridged Adapter) з використанням контролера **MediaTek Wi-Fi 6**. Це дозволяє віртуальній машині отримати власну IP-адресу в мережі Wi-Fi.*

* **Робота з образами:** Підключення інсталяційного диска.
![Додавання ISO образу](image_f00309.png)  
*Монтування ISO-образу Fedora у віртуальний привід. Це критично для початкового завантаження системи.*

* **Конфігурація накопичувачів:**
![Контролери IDE та SATA](image_f00743.png)  
*Використання контролера SATA для основного SSD та IDE для оптичного привода, що забезпечує максимальну сумісність.*

* **Зовнішні носії:** Створення віртуальної "флешки".
![Створення VHD накопичувача](image_f0747d.png)  
*Додавання другого диска формату VHD на 15 ГБ. Це виконує вимогу завдання щодо роботи з зовнішніми носіями інформації.*

## 3. Встановлення ОС у базовій конфігурації

Процес встановлення Fedora 43 супроводжувався налаштуванням безпеки та виправленням помилок завантаження:

* **Шифрування диска (LUKS):**
![Запит пароля розшифрування](image_f00e6f.png)  
*Введення Passphrase для доступу до зашифрованих розділів. Це стандарт безпеки в сучасних дистрибутивах Linux.*

* **Діагностика Emergency Mode:**
![Помилка завантаження системи](image_f020d2.png)  
*Виникнення критичної помилки через відсутність UUID диска. Проблема була вирішена шляхом корекції точок монтування в конфігурації VirtualBox.*

* **Фінальний результат:**
![Робочий стіл Fedora GNOME](image_f0958a.png)  
*Успішний запуск графічної оболонки GNOME. Базова конфігурація включає стандартний набір утиліт та браузер Firefox.*

## 4. Робота з терміналом та додатковими оболонками

Згідно з завданням, було виконано встановлення додаткового ПЗ через CLI (Command Line Interface):

* **Використання DNF5:** Новий менеджер пакетів у Fedora.
![Команди в терміналі](image_f0f387.png)  
*Спроба використання команди `groupinstall`. Система підказала правильний синтаксис для нової версії менеджера пакетів.*

* **Процес встановлення Xfce:**
![Інсталяція графічної оболонки](image_f0fe6e.png)  
*Виконання команди `sudo dnf install @xfce-desktop-environment`. На скріншоті видно процес завантаження метаданих та підготовку списку пакетів для Xfce.*

---

### 4.1. Порівняння графічних оболонок (Benchmark)



| Характеристика | GNOME (Default) | Xfce (Lightweight) |
| :--- | :--- | :--- |
| **Архітектура** | GTK 4, орієнтація на Wayland | GTK 3, стабільна класика |
| **Використання RAM** | Високе (від 1.1 ГБ в спокої) | Низьке (від 500 МБ в спокої) |
| **Налаштування** | Через розширення та Tweaks | Вбудовані інструменти кастомізації |
| **UX/UI** | Планшетний стиль, жести | Традиційна панель та меню "Пуск" |

---

### Dictionary of English Terms (Словник термінів)

| Term | Translation | Description |
| :--- | :--- | :--- |
| **Hypervisor** | Гіпервізор | Software that creates and runs virtual machines. |
| **Bridged Adapter** | Мережевий міст | Network mode for direct physical network access. |
| **VHD (Virtual Hard Disk)** | Віртуальний диск | A file format representing a virtual hard disk drive. |
| **Passphrase** | Парольна фраза | A sequence of words used for disk encryption access. |
| **CLI (Command Line Interface)** | Термінальний інтерфейс | A text-based means of interacting with a computer. |
| **Repository** | Репозиторій | A central location where software packages are stored. |

---

### Conclusions (Висновки)

In this laboratory work, I have successfully mastered the skills of working with the **VirtualBox** hypervisor. I learned how to create and configure virtual machines, emulate external storage devices (VHD), and set up network connections via Wi-Fi adapters using **Bridged** mode.

During the installation of **Fedora Linux**, I practiced both graphical and terminal-based software management. The transition from a broken boot state (**Emergency Mode**) to a working system gave me valuable experience in Linux troubleshooting. The process of installing an additional desktop environment (**Xfce**) via the **DNF5** manager allowed me to compare different interfaces. I concluded that GNOME provides a modern UX, while Xfce is superior for performance-critical tasks in virtualized environments.

---
