# Ex.No:2B To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
1. Start the application.
2. Create a new Android project in Android Studio.
3. Design the first screen with:
4. One EditText to accept a number.
5. One Button labeled FACTORIAL.
6. Create a second activity to display the result.
7. In MainActivity, read the number entered by the user.
8. Create an Explicit Intent to open SecondActivity.
9. Pass the entered number to SecondActivity using putExtra().
10. In SecondActivity, receive the number using getIntent().getStringExtra().
11. Convert the received value into an integer.
12. Calculate the factorial of the number using a for loop.
13. Display the factorial result in a TextView.
14. Run the application.
15. Verify that the second screen displays the correct factorial.
16. Stop the application.




## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
Developed by: SAKTHIVEL S
Registeration Number : 212223220090
*/
```
### MainActivity.java:
```
package com.example.explicitintent;

import android.content.Intent;
import android.os.Bundle;
import android.widget.Button;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        EdgeToEdge.enable(this);
        setContentView(R.layout.activity_main);

        Button btnGo = findViewById(R.id.btnGo);
        btnGo.setOnClickListener(v -> {
            Intent intent = new Intent(MainActivity.this, SecondActivity.class);
            startActivity(intent);
        });
    }
}
```
### activity_main.xml
````
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#121212"
    tools:context=".MainActivity">

    <!-- Title -->
    <TextView
        android:id="@+id/textView1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/first_activity_title"
        android:textSize="24sp"
        android:textColor="@android:color/white"
        android:textStyle="bold"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginTop="100dp"/>

    <!-- Button -->
    <Button
        android:id="@+id/btnGo"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/go_to_other"
        app:layout_constraintTop_toBottomOf="@id/textView1"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginTop="50dp"/>
</androidx.constraintlayout.widget.ConstraintLayout>
````

### MainActivity2.java
````
package com.example.explicitintent;

import android.content.Intent;
import android.os.Bundle;
import android.widget.Button;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;

public class SecondActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        EdgeToEdge.enable(this);
        setContentView(R.layout.activity_second);

        Button btnGoBack = findViewById(R.id.btnGoBack);
        btnGoBack.setOnClickListener(v -> {
            Intent intent = new Intent(SecondActivity.this, MainActivity.class);
            startActivity(intent);
        });
    }
}
````

### activity_main2.xml
````
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#121212"
    tools:context=".SecondActivity">

    <!-- Title -->
    <TextView
        android:id="@+id/textView2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/second_activity_title"
        android:textSize="24sp"
        android:textColor="@android:color/white"
        android:textStyle="bold"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginTop="100dp"/>

    <!-- Button -->
    <Button
        android:id="@+id/btnGoBack"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/go_to_home"
        app:layout_constraintTop_toBottomOf="@id/textView2"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginTop="50dp"/>
</androidx.constraintlayout.widget.ConstraintLayout>
````
## OUTPUT

#### View page 1:
<img width="1884" height="1063" alt="Screenshot 2026-08-06 143156" src="https://github.com/user-attachments/assets/114df5d1-72e6-4ebe-a854-fe8e0a68fab9" />


#### View page 2:
<img width="1907" height="1066" alt="Screenshot 2026-08-06 143202" src="https://github.com/user-attachments/assets/bcdda80a-6e66-4ebc-96e1-b64b99c242be" />




## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.


