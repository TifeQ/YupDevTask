# YupDevTask
A java file with features such as editText, TextView, Toast, Snackbar and AlertDialog


package com.example.andriod.yupdev1;

import android.content.DialogInterface;
import android.os.Build;
import android.support.design.widget.Snackbar;
import android.support.v7.app.AlertDialog;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.text.Editable;
import android.text.TextWatcher;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import android.widget.Toast;

import static android.R.attr.button;
import static android.icu.lang.UCharacter.GraphemeClusterBreak.T;

//import static com.example.andriod.yupdev1.R.id.nameField;


public class MainActivity extends AppCompatActivity {


    int textlength = 0;
    EditText editText;
    TextView textView;
    TextView name;
    TextView getTextView;
    AlertDialog.Builder alertDialog;
    Toast toast;
    Snackbar snackbar;
    String name1;
    Button button;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        Button button;


        // allows the user to set text
        TextView nameField = (TextView) findViewById(R.id.text_field);
        nameField.setText(("Hi, welcome to Yupdev group"));


        // allows the user to edit/enter text
        EditText editText = (EditText) findViewById(R.id.editText);
        nameField.getText();
    }


    public void submit(View view) {
        AlertDialog.Builder builder = new AlertDialog.Builder(this);
        builder.setPositiveButton("CONTINUE", new DialogInterface.OnClickListener() {
            @Override
            public void onClick(DialogInterface dialog, int which) {
                // This shows when the user clicks continue
                Snackbar.make(getCurrentFocus(), " You are now good to go", Snackbar.LENGTH_SHORT).show();
            }
        });
        // This occurs when the user cancels the option
        builder.setNegativeButton("Cancel", new DialogInterface.OnClickListener() {
            @Override
            public void onClick(DialogInterface dialog, int which) {
                Toast.makeText(MainActivity.this, "You have to click continue", Toast.LENGTH_SHORT).show();
            }
        });
        
        // Ask if the user wants to continue with option 
        builder.setMessage("Do you want to continue");
        builder.show();


    }




    }
