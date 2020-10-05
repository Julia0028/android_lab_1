# Лабораторная работа №1. Layouts

### Цели

- Ознакомиться со средой разработки Android Studio;
- Изучить основные принципы верстки layout с использованием View и ViewGroup;
- Изучить основные возможности и свойства LinearLayout;
- Изучить основные возможности и свойства ConstraintLayout;

### Задачи


#### Задача 1. LinearLayout
---
**Задание**: создать layout ресурсы для следующих макетов экрана с использованием LinearLayout.

*Рис 1.1 Макет экрана 1. Вариант 18*

![image](https://github.com/Julia0028/android_lab_1/blob/master/report_lab_1/1.png)

*Рис 1.2 Макет экрана 2. Вариант 5*

![image_2](https://github.com/Julia0028/android_lab_1/blob/master/report_lab_1/2.png)

**Решение:**

*Рис 1.3 Макет экрана 1. Вариант 18*

![image_4](https://github.com/Julia0028/android_lab_1/blob/master/report_lab_1/4.png)

*Рис 1.4 Макет экрана 2. Вариант 5*

![image_5_1](https://github.com/Julia0028/android_lab_1/blob/master/report_lab_1/5_1.png)

- LinearLayout - макет, который выравнивает всех дочерних элементов в одном направлении: горизонтально или вертикально. Все дочерние элементы LinearLayout располагаются один за другим, поэтому в вертикальном списке будет только один дочерний элемент на строку, независимо от того, насколько они широки, а горизонтальный список будет иметь высоту только в одну строку (высота самого высокого дочернего элемента плюс внутренний отступ). LinearLayout учитывает внешние отступы между дочерними элементами и выравнивание по правому краю, центру или левому краю каждого дочернего элемента.
- Layout_weight - атрибут, который назначает вес дочерним отдельным элементам, тем самым определяет их "важность" в контексте пространства. Элементы будут заполнять экран в пропорциях от объявленного веса. 
- Gravity - атрибут, который задает позиционирование содержимого внутри объекта.
- Layout_gravity - атрибут, который задает позиционирование относительно внешнего контейнера. 
- Orientation - направление, по которому макет выравнивает дочерних элементов. Может быть "horizontal" и "vertical".
- Layout_height - атрибут, задающий высоту элемента.
- Layout_width - атрибут, задающий ширину элемента. 

**Альтернативное решение:**

*Рис 1.5 Макет экрана 1. Вариант 18*

![image_3](https://github.com/Julia0028/android_lab_1/blob/master/report_lab_1/3.png)

Использовались элементы space для создания промежутков между компонентами макета и несколько linearLayout с разными направлениями. 


#### Задача 2. ConstraintLayout
---
**Задание:** решить задачу 1 (обе подзадачи) с использованием ConstraintLayout.

**Решение:**

*Рис 2.1 Макет экрана 1. Вариант 18*

![image_6](https://github.com/Julia0028/android_lab_1/blob/master/report_lab_1/6.png)

*Рис 2.2 Макет экрана 2. Вариант 5*

![image_7_1_1](https://github.com/Julia0028/android_lab_1/blob/master/report_lab_1/7_1_1.png)

- ConstraintLayout - контейнер, который позволяет гибко размещать и изменять размер виджетов. ConstraintLayout позволяет создавать большие и сложные макеты с плоской иерархией представлений. Чтобы определить позицию элемента, нужно задать, как
минимум, одно ограничение для каждой оси. 
- Layout_constraintDimensionRatio - используя это ограничение макета, мы
можем определить одно измерение вида (высота или ширина) как отношение
другого измерения.
- Layout_constraintHorizontal_weight, layout_constraintVertical_weight - аналог layout_weight в LinearLayout. То есть представление с наибольшим значением веса получает наибольшее количество места; представления с одинаковым весом занимают одинаковое количество места.
- Guideline  - направляющие, позволяющие разделить пространство на точное значение (выраженное в процентах или dp). Невидимы для пользователей приложения. 


#### Задача 3. ConstraintLayout
---
**Задание:** создайть layout ресурс для следующего макета экрана с использованием ConstraintLayout.

*Рис 3.1 Макет экрана. Вариант 18*

![image_9](https://github.com/Julia0028/android_lab_1/blob/master/report_lab_1/9.png)

**Решение:** 

*Рис 3.2 Макет экрана. Вариант 18*

![image_8](https://github.com/Julia0028/android_lab_1/blob/master/report_lab_1/8.png)


### Выводы
В процессе выполнения данной лабораторной работы в среде разработки Android Studio изучены основы вёрстки layout с использованием View (элементы интерфейса) и ViewGroup (может содержать другие View). Также изучены основные возможности и свойства LinearLayout и ConstraintLayout. Для строгого представления элементов можно использовать LinearLayout, а для сложной вёрстки, где может понадобиться «привязывание» элементов друг к другу или родителям, необходимо использовать ConstraintLayout.


### Приложение
**task_1_1.xml**
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="horizontal"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <LinearLayout
        android:layout_width="wrap_content"
        android:layout_height="match_parent"
        android:orientation="vertical">

        <Space
            android:layout_width="wrap_content"
            android:layout_height="0dp"
            android:layout_weight="2" />

        <EditText
            android:id="@+id/editTextTextPersonName2"
            android:layout_width="wrap_content"
            android:layout_height="0dp"
            android:layout_weight="1"
            android:ems="10"
            android:inputType="textPersonName" />
    </LinearLayout>

    <LinearLayout
        android:layout_width="wrap_content"
        android:layout_height="match_parent"
        android:orientation="vertical">

        <Space
            android:layout_width="wrap_content"
            android:layout_height="0dp"
            android:layout_weight="1" />

        <TextView
            android:id="@+id/textView6"
            android:layout_width="wrap_content"
            android:layout_height="0dp"
            android:layout_weight="1"
            android:text="TextView" />

        <Space
            android:layout_width="wrap_content"
            android:layout_height="0dp"
            android:layout_weight="1" />
    </LinearLayout>

    <LinearLayout
        android:layout_width="wrap_content"
        android:layout_height="match_parent"
        android:orientation="vertical">

        <Button
            android:id="@+id/button4"
            android:layout_width="wrap_content"
            android:layout_height="0dp"
            android:layout_weight="1"
            android:text="Button" />

        <Space
            android:layout_width="wrap_content"
            android:layout_height="0dp"
            android:layout_weight="2" />
    </LinearLayout>
</LinearLayout>
```
**task_1_1_v_2.xml**
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <Button
        android:id="@+id/button2"
        android:layout_width="wrap_content"
        android:layout_height="0dp"
        android:layout_gravity="end"
        android:layout_weight="1"
        android:text="Button" />

    <RadioButton
        android:id="@+id/radioButton"
        android:layout_width="wrap_content"
        android:layout_height="0dp"
        android:layout_gravity="center"
        android:layout_weight="1"
        android:text="RadioButton" />

    <TextView
        android:id="@+id/textView2"
        android:layout_width="wrap_content"
        android:layout_height="0dp"
        android:layout_gravity="bottom"
        android:layout_weight="1"
        android:text="TextView" />

</LinearLayout>
```
**task_1_2.xml**
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:orientation="horizontal"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <TextView
        android:id="@+id/textView"
        android:layout_width="50dp"
        android:layout_height="match_parent"
        android:text="TextView" />

    <Button
        android:id="@+id/button"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_weight="1"
        android:text="Button" />

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="50dp"
        android:layout_height="match_parent"
        tools:srcCompat="@tools:sample/avatars" />
</LinearLayout>
```
**task_2_1.xml**
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <Switch
        android:id="@+id/switch2"
        android:layout_width="wrap_content"
        android:layout_height="0dp"
        android:text="Switch"
        app:layout_constraintBottom_toTopOf="@+id/guideline"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <ImageView
        android:id="@+id/imageView3"
        android:layout_width="wrap_content"
        android:layout_height="0dp"
        app:layout_constraintBottom_toTopOf="@+id/guideline3"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="@+id/guideline"
        tools:srcCompat="@tools:sample/avatars" />

    <ProgressBar
        android:id="@+id/progressBar2"
        style="?android:attr/progressBarStyle"
        android:layout_width="wrap_content"
        android:layout_height="0dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="@+id/guideline3"
        app:layout_constraintVertical_bias="0.0" />

    <androidx.constraintlayout.widget.Guideline
        android:id="@+id/guideline"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        app:layout_constraintGuide_percent="0.33068782" />

    <androidx.constraintlayout.widget.Guideline
        android:id="@+id/guideline3"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        app:layout_constraintGuide_percent="0.6600529" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
**task_2_2.xml**
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent">


    <Button
        android:id="@+id/button"
        android:layout_width="0dp"
        android:layout_height="0dp"
        android:text="Button"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toStartOf="@+id/imageView"
        app:layout_constraintStart_toEndOf="@+id/textView"
        app:layout_constraintTop_toTopOf="parent" />

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="0dp"
        android:layout_height="0dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="@+id/textView"
        app:layout_constraintTop_toTopOf="parent"
        android:layout_marginLeft="362dp"
        tools:srcCompat="@tools:sample/avatars" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="0dp"
        android:layout_height="0dp"
        android:text="TextView"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        android:layout_marginRight="362dp" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
**task_3.xml**
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <androidx.constraintlayout.widget.ConstraintLayout
        android:layout_width="0dp"
        android:layout_height="0dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintDimensionRatio="1:1"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent">

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/guideline9"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            app:layout_constraintGuide_percent="0.6005472" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/guideline8"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            app:layout_constraintGuide_percent="0.4" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/guideline12"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            app:layout_constraintGuide_percent="0.70861834" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/guideline13"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            app:layout_constraintGuide_percent="0.5" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/guideline2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="vertical"
            app:layout_constraintGuide_percent="0.2" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/guideline5"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="vertical"
            app:layout_constraintGuide_percent="0.6" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/guideline11"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            app:layout_constraintGuide_percent="0.9" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/guideline4"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="vertical"
            app:layout_constraintGuide_percent="0.4" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/guideline6"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="vertical"
            app:layout_constraintGuide_percent="0.8" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/guideline10"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            app:layout_constraintGuide_percent="0.8002736" />

        <androidx.constraintlayout.widget.Guideline
            android:id="@+id/guideline7"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            app:layout_constraintGuide_percent="0.2" />

        <TextView
            android:id="@+id/textView4"
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:text="TextView"
            app:layout_constraintBottom_toTopOf="@+id/guideline8"
            app:layout_constraintEnd_toStartOf="@+id/guideline2"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="parent" />

        <ImageButton
            android:id="@+id/imageButton"
            android:layout_width="0dp"
            android:layout_height="0dp"
            app:layout_constraintBottom_toTopOf="@+id/guideline10"
            app:layout_constraintEnd_toStartOf="@+id/guideline2"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="@+id/guideline8"
            tools:srcCompat="@tools:sample/avatars" />

        <RadioGroup
            android:layout_width="0dp"
            android:layout_height="0dp"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toStartOf="@+id/guideline5"
            app:layout_constraintHorizontal_bias="0.527"
            app:layout_constraintStart_toStartOf="@+id/guideline2"
            app:layout_constraintTop_toTopOf="@+id/guideline10" />

        <Switch
            android:id="@+id/switch4"
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:text="Switch"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="@+id/guideline6"
            app:layout_constraintTop_toTopOf="@+id/guideline9" />

        <EditText
            android:id="@+id/editTextTextPersonName"
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:ems="10"
            android:inputType="textPersonName"
            android:text="Name"
            app:layout_constraintBottom_toTopOf="@+id/guideline9"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="@+id/guideline5"
            app:layout_constraintTop_toTopOf="@+id/guideline8" />

        <CheckBox
            android:id="@+id/checkBox2"
            android:layout_width="0dp"
            android:layout_height="0dp"
            android:text="CheckBox"
            app:layout_constraintBottom_toTopOf="@+id/guideline7"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="@+id/guideline5"
            app:layout_constraintTop_toTopOf="parent" />

    </androidx.constraintlayout.widget.ConstraintLayout>

</androidx.constraintlayout.widget.ConstraintLayout>
```