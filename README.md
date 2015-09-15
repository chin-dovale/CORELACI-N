# CORELACI-N
Ejercicio de correlación (visualización, comparación y relación de datos)

String semana[]= {"lunes", "martes","miercoles",
"jueves", "viernes", "sábado", "domingo"};
int horas[]={6,8,3,7,9,10,6};
float tazas[]={1.5,2,3.7,2,1,0,0.5};

PFont chin;


void setup(){
  
  size (1000,450);
  
  chin=loadFont("CenturyGothic-20.vlw");
  textFont (chin,20);
  
  smooth(10);
  
}

void draw(){

background(255);
for(int blue=0; blue<7; blue=blue + 1){
  
    //dias de la semana
  
  fill(125);
  text(semana[blue],150+(blue*100),110);
  
  
    //horas de sueño (gráfica)
  noFill();
  stroke(20,200,80);
  ellipse(180+(blue*100),200, horas[blue]*10, horas[blue]*10);

 
  //horas de sueño (texto)
  fill(20,200,80);
  text(horas[blue],180+(blue*100), 280+ horas[blue]);

 
  //tazas de café
  noFill();
  stroke(200,0,80);
  ellipse(180+(blue*100),200, tazas[blue]*10, tazas[blue]*10);
  
  fill(200,0,80);
  text(tazas[blue],180+(blue*100), 320+ tazas[blue]);


fill(125);

text("Cantidad de horas dormidas en la semana vs cantidad de tazas de café al día",125, 400);


}



}
