# Звіт з лабораторної роботи (Work-case 2)
**Дисципліна:** Операційні системи

---
**МІНІСТЕРСТВО ОСВІТИ І НАУКИ УКРАЇНИ** **КИЇВСЬКИЙ ФАХОВИЙ КОЛЕДЖ ЗВ'ЯЗКУ**

**Виконала:** студентка групи БІКС-33 Руда Дарина Сергіївна  
**Перевірила:** викладач Сушанова Вікторія Сергіївна  

**Київ 2026**

---

## 1. Встановлення гіпервізора
Для виконання роботи було обрано гіпервізор II типу — **Oracle VM VirtualBox**. Процес включав базове налаштування середовища для віртуалізації.

## 2. Налаштування віртуальної машини та обладнання
Було виконано наступні кроки з конфігурації:

* **Створення та налаштування VM:**
<img width="1017" height="496" alt="image" src="https://github.com/user-attachments/assets/ca115d6a-b22f-441e-a004-b434052cba8d" />


*Налаштування базових ресурсів віртуальної машини.*

* **Додавання образу та дисків:**
<img width="1025" height="495" alt="image" src="https://github.com/user-attachments/assets/721417eb-c0a4-4d04-b9b0-3c0bedc45cdc" />

*Підключення ISO-образу Fedora до віртуального оптичного привода.*

* **Зовнішні носії (Flash-пам'ятть):**
<img width="954" height="788" alt="image" src="https://github.com/user-attachments/assets/3b41d8ba-e417-4d2d-aea8-f065e5bcf38b" />

*Створення віртуального жорсткого диска (VHD) об'ємом 15 ГБ, який виступає в ролі зовнішнього накопичувача.*

* **Налаштування мережі:**
<img width="746" height="347" alt="image" src="https://github.com/user-attachments/assets/778c44c6-c512-404d-b8d7-60d2d35e1800" />

*Конфігурація Bridged Adapter для прямого підключення до бездротової мережі.*

## 3. Встановлення ОС у базовій конфігурації
Встановлено ОС **Fedora Workstation 43** з графічною оболонкою **GNOME**.

* **Процес встановлення:**
<img width="770" height="708" alt="image" src="https://github.com/user-attachments/assets/88b4177e-130b-4b5d-8aa6-4c09e638913c" />

*Початок процесу розгортання операційної системи.*

* **Етап безпеки:**
<img width="721" height="291" alt="image" src="https://github.com/user-attachments/assets/7edbf085-1ccd-43da-9c4a-f835712efdc8" />

*Етап введення пароля для розшифрування системного розділу.*

* **Фінальний результат:**
<img width="646" height="584" alt="image" src="https://github.com/user-attachments/assets/409d95c6-fb6b-4a4d-b861-c55a47b6ede0" />

*Завантажена оболонка GNOME, готова до роботи.*

## 4. Робота з терміналом та додатковими оболонками
Згідно з завданням, встановлення додаткового ПЗ проводилось через термінал:

* **Оновлення репозиторіїв:**
<img width="773" height="422" alt="image" src="https://github.com/user-attachments/assets/df182328-b1b4-4e3b-9680-70112e76e3cf" />

*Процес завантаження метаданих пакетів у терміналі.*

* **Встановлення Xfce:**
<img width="684" height="478" alt="image" src="https://github.com/user-attachments/assets/12a40174-625e-4b6d-8381-e246bd57eb29" />

*Виконання команди інсталяції групи пакетів Xfce Desktop.*

---

### 4.1. Порівняння графічних оболонок

| Характеристика | GNOME | Xfce |
| :--- | :--- | :--- |
| **Інтерфейс** | Сучасний, мінімалістичний, орієнтований на продуктивність | Класичний, подібний до Windows (панель задач, меню) |
| **Ресурси** | Високе споживання RAM та CPU | Легка оболонка, мінімальне навантаження |
| **Продуктивність** | Плавна анімація, вимагає потужного GPU | Миттєвий відгук, підходить для слабких систем |

---

### Dictionary of English Terms (Словник термінів)

| Term | Translation | Description |
| :--- | :--- | :--- |
| **Hypervisor** | Гіпервізор | Software that creates and runs virtual machines. |
| **Virtual Machine (VM)** | Віртуальна машина | An emulation of a computer system. |
| **Host OS** | Хостова ОС | The primary operating system on the hardware. |
| **Guest OS** | Гостьова ОС | The operating system inside a virtual machine. |
| **Bridged Adapter** | Мережевий міст | Network mode for direct physical network access. |
| **Desktop Environment** | Графічна оболонка | A graphical user interface for the operating system. |

---

### Conclusions (Висновки)

In this laboratory work, I have successfully mastered the skills of working with the **VirtualBox** hypervisor. I learned how to create and configure virtual machines, emulate external storage devices, and set up network connections via Wi-Fi adapters.

During the installation of **Fedora Linux**, I practiced both graphical and terminal-based software management. The process of installing an additional desktop environment (**Xfce**) via the **DNF** package manager allowed me to compare different interfaces. I concluded that GNOME is more suitable for modern user experiences, while Xfce is superior for resource-constrained environments like virtual machines. All tasks of the work-case were completed successfully.
