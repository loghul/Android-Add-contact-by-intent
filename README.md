### EX NO: 03

### DATE: 


# <p align = "center"> Add contact using Android Intent </p>

## AIM:
To Add the contact list using Intent Android Studio.

## EQUIPMENTS REQUIRED:
Android Studio(Min.required Artic Fox)

## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
## activity_main.xml

``` java

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Add Contact"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.711" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="First Name"
        android:textColor="@color/black"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.131"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.202" />

    <TextView
        android:id="@+id/textView2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Last Name"
        android:textColor="@color/black"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.131"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.314" />

    <TextView
        android:id="@+id/textView3"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Phone"
        android:textColor="@color/black"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.121"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.424" />

    <EditText
        android:id="@+id/editTextTextPersonName"
        android:layout_width="254dp"
        android:layout_height="58dp"
        android:ems="10"
        android:inputType="textPersonName"

        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.898"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.188" />

    <EditText
        android:id="@+id/editTextTextPersonName2"
        android:layout_width="254dp"
        android:layout_height="55dp"
        android:ems="10"
        android:inputType="textPersonName"

        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.898"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.303" />

    <EditText
        android:id="@+id/editTextPhone"
        android:layout_width="251dp"
        android:layout_height="59dp"
        android:ems="10"
        android:inputType="phone"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.898"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.412" />

    <TextView
        android:id="@+id/textView4"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Add New contact"
        android:textColor="@color/black"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.135"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.075" />

    <TextView
        android:id="@+id/textView5"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="email"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.127"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.526" />

    <EditText
        android:id="@+id/editTextTextEmailAddress2"
        android:layout_width="248dp"
        android:layout_height="61dp"
        android:ems="10"
        android:inputType="textEmailAddress"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.883"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.517" />

</androidx.constraintlayout.widget.ConstraintLayout>


```

## MainActivity.java
``` java

package com.example.addcontactusingintent;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.os.Bundle;
import android.provider.ContactsContract;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        Button mButton=(Button) findViewById(R.id.button);
        mButton.setOnClickListener(new View.OnClickListener() {

        @Override
        public void onClick(View view){
        Intent intent=new Intent(ContactsContract.Intents.Insert.ACTION);
        intent.setType(ContactsContract.RawContacts.CONTENT_TYPE);

        EditText mFirstname= (EditText) findViewById(R.id.editTextTextPersonName);
        EditText mLastname=(EditText) findViewById(R.id.editTextTextPersonName2);
        EditText mPhone=(EditText) findViewById(R.id.editTextPhone);
        EditText memail=(EditText) findViewById(R.id.editTextTextEmailAddress2);

        intent
                .putExtra(ContactsContract.Intents.Insert.EMAIL,memail.getText())
                .putExtra(ContactsContract.Intents.Insert.EMAIL_TYPE,ContactsContract.CommonDataKinds.Email.TYPE_WORK)
                .putExtra(ContactsContract.Intents.Insert.PHONE,mPhone.getText())
                .putExtra(ContactsContract.Intents.Insert.PHONE_TYPE,ContactsContract.CommonDataKinds.Phone.TYPE_WORK)
                .putExtra(ContactsContract.Intents.Insert.NAME,mFirstname.getText() + " " + mLastname.getText())
                ;
        startActivity(intent);
    }

        });
    }
}
```
## <br/><br/><br/><br/><br/><br/><br/><br/><br/> OUTPUT
![WhatsApp Image 2022-05-02 at 8 10 24 AM](https://user-images.githubusercontent.com/78194419/166188142-9bac5bbc-4d45-4317-853a-2e0303b2cf51.jpeg)
![WhatsApp Image 2022-05-02 at 8 10 24 AM (1)](https://user-images.githubusercontent.com/78194419/166188151-ae6c50c7-8d2d-4657-8c2c-dbff20e0ad87.jpeg)
![WhatsApp Image 2022-05-02 at 8 10 24 AM (2)](https://user-images.githubusercontent.com/78194419/166188160-b948ca76-becb-44c3-a37e-70947718ad08.jpeg)


## RESULT
Thus a Simple Android Application add contact list using intent Android Studio is developed and executed successfully.
