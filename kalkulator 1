package com.example.latihan1;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {
    EditText val1, val2;
    TextView result;
    Button tambahButton, kurangButton, bagiButton, kaliButton;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        val1 = findViewById(R.id.val1);
        val2 = findViewById(R.id.val2);
        result = findViewById(R.id.tvhasil);
        tambahButton = findViewById(R.id.buttontambah);
        kurangButton = findViewById(R.id.buttonkurang);
        bagiButton = findViewById(R.id.buttonbagi);
        kaliButton = findViewById(R.id.buttonkali);

        tambahButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                hitungan( '+');
            }
        });

        kurangButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                hitungan('-');
            }
        });

        bagiButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                hitungan('/');
            }
        });

        kaliButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                hitungan('*');
            }
        });
    }

    private void hitungan(char operator) {
        double value1 = Double.parseDouble(val1.getText().toString());
        double value2 = Double.parseDouble(val2.getText().toString());
        double hasil = 0;

        switch (operator) {
            case '+':
                hasil = value1 + value2;
                break;
            case '-':
                hasil = value1 - value2;
                break;
            case '/':
                hasil = value1 / value2;
                break;
            case '*':
                hasil = value1 * value2;
                break;
        }

        String formattedResult = hasil % 1 == 0 ? String.valueOf((int) hasil) : String.valueOf(hasil);
        result.setText(formattedResult);
    }
}

