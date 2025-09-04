// Copyright 2014 The Flutter Authors. All rights reserved.
// Use of this source code is governed by a BSD-style license that can be
// found in the LICENSE file.

import 'package:flutter/material.dart';
import 'package:flutter/widgets.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Proyecciones Financieras',
      home: Scaffold(
        appBar: AppBar(title: Text('Proyecciones financieras'), backgroundColor: Colors.blueAccent),
        body: Padding(
          padding: const EdgeInsets.all(16.0),
          child: Column(
            crossAxisAlignment: CrossAxisAlignment.start,
            children: [
              campoTexto('Símbolo de moneda (\$, €, £)'),
              campoTexto('Cantidad total invertida por los propietarios', hint: '0'),
              campoTexto('Cantidad total necesaria', hint: '0'),
              campoTexto(
                'Beneficios proyectados',
                hint: 'Cuánto dinero ingresará vendiendo productos/servicios',
              ),
              campoTexto(
                'Balance proyectado',
                hint: 'Estimación futura de activos, pasivos y capital',
              ),
              campoTexto(
                'Flujo de efectivo proyectado',
                hint: 'Inversiones y desinversiones previstas en el proyecto',
              ),
              campoTexto('Uso de los fondos', hint: 'Cómo se gastarán los fondos'),
              campoTexto(
                'Estrategia de salida',
                hint: 'Plan para abandonar el negocio si es necesario',
              ),
            ],
          ),
        ),
      ),
    );
  }

  Widget campoTexto(String label, {String hint = ''}) {
    return Padding(
      padding: const EdgeInsets.only(bottom: 16.0),
      child: Column(
        crossAxisAlignment: CrossAxisAlignment.start,
        children: [
          Text(label, style: TextStyle(fontSize: 16, fontWeight: FontWeight.bold)),
          TextField(
            decoration: InputDecoration(
              hintText: hint,
              border: OutlineInputBorder(),
              contentPadding: EdgeInsets.symmetric(horizontal: 10, vertical: 8),
            ),
          ),
        ],
      ),
    );
  }
}
# m_gonzalez_septiembre
