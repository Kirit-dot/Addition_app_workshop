# Addition_app_workshop

## AIM:

To develop a application to add two numbers and get the result using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## PROGRAM:
```
/*
Program to display animation operation”.
Developed by: KIRIT LULLA
Registeration Number : 212225230139
*/
```
activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView1"
        android:layout_width="150dp"
        android:layout_height="48dp"
        android:layout_marginStart="10dp"
        android:layout_marginTop="52dp"
        android:gravity="center_vertical"
        android:textSize="16sp"
        app:layout_constraintEnd_toStartOf="@+id/first_number"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <EditText
        android:id="@+id/first_number"
        android:layout_width="150dp"
        android:layout_height="48dp"
        android:layout_marginTop="52dp"
        android:ems="10"
        android:inputType="number"
        android:textSize="16sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toEndOf="@+id/textView1"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/textView2"
        android:layout_width="150dp"
        android:layout_height="48dp"
        android:layout_marginStart="10dp"
        android:layout_marginTop="8dp"
        android:gravity="center_vertical"
        android:textSize="16sp"
        app:layout_constraintEnd_toStartOf="@+id/second_number"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView1" />

    <EditText
        android:id="@+id/second_number"
        android:layout_width="175dp"
        android:layout_height="48dp"
        android:layout_marginTop="4dp"
        android:layout_marginEnd="10dp"
        android:ems="10"
        android:inputType="number"
        android:textSize="16sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toEndOf="@+id/textView2"
        app:layout_constraintTop_toBottomOf="@+id/first_number" />

    <Button
        android:id="@+id/button"
        android:layout_width="139dp"
        android:layout_height="57dp"
        android:layout_marginTop="84dp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView2" />


    <TextView
        android:id="@+id/result"
        android:layout_width="150dp"
        android:layout_height="40dp"
        android:layout_marginTop="88dp"
        android:gravity="center"
        android:textSize="16sp"
        android:visibility="gone"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toStartOf="@+id/result_value"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/button"
        app:layout_constraintVertical_bias="0.006" />

    <TextView
        android:id="@+id/result_value"
        android:layout_width="150dp"
        android:layout_height="40dp"
        android:gravity="center"
        android:textSize="16sp"
        android:visibility="gone"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toEndOf="@+id/result"
        app:layout_constraintTop_toTopOf="@+id/result" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
MainActivity.java
```
package com.example.additionapp;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {

    EditText number1,number2;
    Button Add_button;
    TextView temp,result;
    int ans=0;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Assiging the values to variables
        number1=(EditText) findViewById(R.id.first_number);
        number2=(EditText) findViewById(R.id.second_number);
        Add_button=(Button) findViewById(R.id.button);
        result=(TextView) findViewById(R.id.result_value);
        temp=(TextView) findViewById(R.id.result);

        Add_button.setOnClickListener(new View.OnClickListener() {
            public void onClick(View v){
                double num1 = Double.parseDouble(number1.getText().toString());
                double num2 = Double.parseDouble(number2.getText().toString());
                // add both number and store it to sum
                double sum = num1 + num2;
                // set it ot result textviewe
                result.setText(Double.toString(sum));

                temp.setVisibility(View.VISIBLE);
                result.setVisibility(View.VISIBLE);
            }
        });
    }
}
```

## OUTPUT:-

<img width="1917" height="1076" alt="Screenshot 2026-08-25 142659" src="https://github.com/user-attachments/assets/9ee672e2-9e7d-4158-bf6d-b4bd6bb1bb42"/>

## RESULT:-

Developed an app to add two numbers using Android Studio.
