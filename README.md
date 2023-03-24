// mi primer semaforo creado en el curso diseño de interfaz electronica mediante arduino
// clase 2
// impartido por aaron montoya moraga
// marzo 2023
// diseñador jota-pe-ge
// processing 4.1.1
// made in FAU

// variable para almacenar tiempo
int tiempoActual = 0;

// variable para colores en tiempo
int tiempoRojo = 5;
int tiempoAmarillo = 2;
int tiempoVerde = 8;

// variable colores
color rojo = color(255, 0, 0);
color amarillo = color(255, 255, 0);
color verde = color(0, 255, 0);

void setup() {
  //size(800, 400);
  fullScreen();
  background(255, 0, 0);
  noCursor();
}

void draw() {
  ellipse(mouseX, mouseY, 80, 80);
  tiempoActual = millis();
  tiempoActual = tiempoActual / 1000;
  println(tiempoActual);

  if (tiempoActual < tiempoRojo) {
    background(rojo);
  } else if (tiempoActual < tiempoRojo + tiempoAmarillo) {
    background(amarillo);
  } else if (tiempoActual < tiempoRojo + tiempoAmarillo + tiempoVerde) {
    background(verde);
  }
}
