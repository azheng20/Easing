Easing
======

Sandvich

PImage img;
int distX;
int distY;
int targetX;
int targetY;
int x;
int y;
float easing=.1;

void setup() {
  size(600, 600);
  imageMode(CENTER);
  img=loadImage("Sandvich.png");
  smooth();
  x=width/2;
  y=height/2;
}

void draw() {
  background(0);
  fill(255, 0, 255);
  image(img, x, y, 100, 100);
  targetX=mouseX;
  targetY=mouseY;
  distX=targetX-x;
  distY=targetY-y;
  x+=distX*easing;
  y+=distY*easing;
}
