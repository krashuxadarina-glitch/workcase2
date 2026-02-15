# Звіт з лабораторної роботи (Work-case 2)
**Дисципліна:** Операційні системи

---
**МІНІСТЕРСТВО ОСВІТИ І НАУКИ УКРАЇНИ** **КИЇВСЬКИЙ ФАХОВИЙ КОЛЕДЖ ЗВ'ЯЗКУ**

**Виконала:** студентка групи БІКС-33 Руда Дарина Сергіївна  
**Перевірила:** викладач Сушанова Вікторія Сергіївна  

**Київ 2026**

---

## 1. Встановлення гіпервізора
Для виконання роботи було обрано гіпервізор II типу — **Oracle VM VirtualBox**. Процес встановлення включав завантаження дистрибутива з офіційного сайту та базове налаштування середовища для віртуалізації.

## 2. Налаштування віртуальної машини та обладнання
Було виконано наступні кроки з конфігурації:
* **Створення VM:** Створено віртуальну машину з назвою `Fedora_Minimal`.
* **Обладнання:** Виділено 2 ГБ оперативної пам'яті та 2 віртуальні процесори.
* **Мережа:** Налаштовано мережевий адаптер у режимі **Bridged Adapter** (Мережевий міст) для підключення до точки Wi-Fi через контролер хоста (MediaTek Wi-Fi 6).
* **Зовнішні носії:** Для імітації роботи з Flash-пам'яттю було створено додатковий віртуальний диск формату **VHD** об'ємом 15 ГБ.

## 3. Встановлення ОС у базовій конфігурації
Встановлено ОС **Fedora Workstation 43** з графічною оболонкою **GNOME**. 
* Проведено розмітку диска.
* Створено обліковий запис користувача.
* Підтверджено успішне завантаження робочого столу.

## 4. Робота з терміналом та додатковими оболонками
Для виконання четвертого пункту було використано термінальний ввід-вивід:
1. **Minimal configuration:** Продемонстровано завантаження системи та роботу через CLI (Command Line Interface).
2. **Встановлення GNOME:** Графічну оболонку було інтегровано в систему за допомогою менеджера пакетів.
3. **Встановлення Xfce:** Виконано встановлення додаткової легкої оболонки командою:
   ```bash
   sudo dnf group install "Xfce Desktop"
### 4. Порівняння графічних оболонок

| Характеристика | GNOME | Xfce |
| :--- | :--- | :--- |
| **Інтерфейс** | Сучасний, мінімалістичний, орієнтований на продуктивність | Класичний, подібний до традиційних ОС (Windows-like) |
| **Ресурси** | Високе споживання системних ресурсів (RAM/GPU) | Мінімальне використання RAM, легкість системи |
| **Продуктивність** | Вимагає апаратного прискорення для плавної анімації | Висока швидкість роботи навіть на слабких віртуальних машинах |

---

### Dictionary of English Terms (Словник термінів)

| Term | Translation | Description |
| :--- | :--- | :--- |
| **Hypervisor** | Гіпервізор | Software that creates and runs virtual machines. |
| **Virtual Machine (VM)** | Віртуальна машина | An emulation of a computer system. |
| **Host OS** | Хостова ОС | The primary operating system installed on the physical hardware. |
| **Guest OS** | Гостьова ОС | The operating system installed inside a virtual machine. |
| **Snapshot** | Знімок системи | A saved state of a virtual machine at a specific point in time. |
| **Bridged Adapter** | Мережевий міст | A network mode that connects VM directly to the physical network. |
| **Desktop Environment** | Графічна оболонка | A graphical user interface for the operating system. |
| **Repository** | Репозиторій | A storage location from which software packages are retrieved. |

---

### Conclusions (Висновки)

In this laboratory work, I have successfully mastered the skills of working with the **VirtualBox** hypervisor. I learned how to create and configure virtual machines, emulate external storage devices, and set up network connections via Wi-Fi adapters.

During the installation of **Fedora Linux**, I practiced both graphical and terminal-based software management. The process of installing an additional desktop environment (**Xfce**) via the **DNF** package manager allowed me to compare different interfaces. I concluded that GNOME is more suitable for modern user experiences, while Xfce is superior for resource-constrained environments like virtual machines. All tasks of the work-case were completed successfully.
