"# AgenCarro
"Projeto Calculadora de Gasolina
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    private TextView textResultado;
    private EditText editKm;
    private EditText editKml;
    private EditText editVg;




    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);


        textResultado = findViewById(R.id.textResultado);
        editKm        = findViewById(R.id.editKm);
        editKml       = findViewById(R.id.editKml);
        editVg        = findViewById(R.id.editVg);


    }

    public void calculargasolina(View view){

        double km = Double.parseDouble(editKm.getText().toString());
        double kml = Double.parseDouble(editKml.getText().toString());
        double vg = Double.parseDouble(editVg.getText().toString());
        double resultado = km * vg / kml;

        textResultado.setText("Valor em R$: " + resultado);

        }

    }
