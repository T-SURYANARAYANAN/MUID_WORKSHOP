# WORKSHOP - Addtion of Two Numbers
## AIM :
Android Application Getting two values and Display the result (Addition Value) in the text box using Android Studio
## Algorithm:
1.Open Android Studio → New Project → Empty Activity.<br>
2.Open activity_main.xml to design the layout.<br>
3.Add a TextView for the heading (“Workshop”).<br>
4.Add two EditText boxes for number inputs.<br>
5.Add a Button to perform the summation.<br>
6.Add a TextView to display the result.<br>
7.In MainActivity.java, handle the button click → get values → calculate add → display result.<br>
## Program:
```text
Developed by : SURYANARAYANAN T
Register Number : 212224040341
```
## activity_main.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">


    <EditText
        android:id="@+id/et1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:ems="10"
        android:hint="Enter The Number"
        android:inputType="text"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.206" />

    <EditText
        android:id="@+id/et2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:ems="10"
        android:hint="Eter The Number"
        android:inputType="text"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/et1"
        app:layout_constraintVertical_bias="0.042" />

    <TextView
        android:id="@+id/tv"
        android:layout_width="208dp"
        android:layout_height="56dp"
        android:hint="Output Will Display Here"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.502"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/et2"
        app:layout_constraintVertical_bias="0.052" />

    <Button
        android:id="@+id/btn1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Add"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.455"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.512" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="128dp"
        android:layout_height="46dp"
        android:fontFamily="casual"
        android:text="WorkShop"
        android:textColor="#FF0000"
        android:textSize="24sp"
        android:textStyle="bold"
        android:typeface="sans"
        app:layout_constraintBottom_toTopOf="@+id/et1"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java :
```java
package com.example.practice;

import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {
    EditText et1,et2;
    TextView tv;
    Button add;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        et1 = findViewById(R.id.et1);
        et2 = findViewById(R.id.et2);
        add = findViewById(R.id.btn1);
        tv = findViewById(R.id.tv);

        add.setOnClickListener(v -> calculate("+"));
    }

    public void calculate(String op) {
        int n1 = Integer.parseInt(et1.getText().toString());
        int n2 = Integer.parseInt(et2.getText().toString());
        int res = 0;
        switch (op) {
            case "+":
                res = n1 + n2;
                break;
            case "-":
                res = n1 - n2;
                break;
            case "*":
                res = n1 * n2;
                break;
            case "/":
                res = n1 / n2;
                break;
        }
        tv.setText(n1 + " " + op + " " + n2 + " = " + res);
    }
}
```
## Output :
#### activity_main.xml
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/447db7f4-d845-400e-bb2c-841b413256cf" /><br>
#### MainActivity.java
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/eca1b4ea-63c8-48aa-80a3-3585ff75e416" /><br>
#### Execution
<img width="369" height="804" alt="image" src="https://github.com/user-attachments/assets/ae0ae6b5-ac55-49c5-8ad3-872e44e1c139" /><br>
## Result :
Thus the Android application takes two numerical inputs from the user and displays their sum in a text box when the "add" button is executed successfully.
