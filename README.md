# cs
Slider s1;

void setup(){
size(800,800);
s1 = new Slider(width/2,height/2,500,20,0,255);
//s1.x = 400;
}
void draw(){
  rectMode(CENTER);
  background(0);
  s1.drawSlider();
}
class Slider{
  float x;
  float y;
  float xSlider;
  float xSize;
  float ySize;
  float minValue;
  float maxValue;
  float cV;
  
  Slider(float x, float y, float xSize, float ySize, float minValue, float maxValue){
    this.x =x;
    this.y = y;
    this.xSize = xSize;
    this.ySize = ySize;
    this.minValue = minValue;
    this.maxValue = maxValue;
    this.cV = cV;
    this.xSlider = (cV - minValue)/((maxValue-minValue)/xSize);
  
}

void drawSlider(){
  pushMatrix();
  translate(x,y);
  fill (200);
  rect(0,0,xSize,ySize);
  translate (xSlider,0);
  ellipse(0,0*ySize/2,ySize*2,ySize*2);
  popMatrix();

}

  

}
