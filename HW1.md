/**
 * Class: CECS 174 section 13, Spring 2016
 * Instructor: Alvaro Monge alvaro.monge@csulb.edu
 *
 * HW 1: Simulation of Two Moving Balls 
 * Author 1:  Kristen Mae Hernandez kmaefhernandez@gmail.com
 * Author 2:  Vivian Ta ta.tvivian@yahoo.com
 */
 
 PImage webImg;
 
 float positionX;
 float positionY;
 float positionTwoX;
 float positionTwoY;
 float ballSize;
 float ballTwoSize; 
 float ballRadius; 
 float ballTwoRadius; 
 
 int distance;
 int edgeBallOne;
 int edgeBallTwo;
 
 float velocity;
 
 color ballOne;
 color ballTwo;
 color collideBallOne;
 color collideBallTwo;

 float r;
 float g; 
 float b; 
 float r2;
 float b2;
 float g2; 
 
void setup() {
  size(900, 600);
  background(0);
  
  String url = "http://www.designlovefest.com/wp-content/uploads/downloads/2016/01/patterno.jpg";
  // Load image from a web server
  
  //sets background to image
  webImg = loadImage(url, "jpg");
  image(webImg, 0, 0);
  
  r = random(0,255); 
  g = random(0,255);
  b = random(0,255);
  r2 = random(0,255); 
  g2 = random(0,255);
  b2 = random(0,255);
  ballOne = color(r, g, b);
  ballTwo = color(r2, g2, b2);
  
  ballRadius = random(20,100); 
  ballTwoRadius = random(100,250); 
  ballSize = ballRadius; 
  ballTwoSize = ballTwoRadius; 
 
  ballSize = random(100, 400);
  positionX = random(10, width);
  positionY = random(10, height);
  
  ballTwoSize = random(50, 180);
  positionTwoX = random(10, width);
  positionTwoY = random(10, height);
  
  
 }
 
void draw() {
  noStroke();
  
  //1st Ball
  fill(ballOne);
  ellipse(positionX, positionY, ballSize, ballSize);
  
  //2nd Ball
  fill(ballTwo);
  ellipse(positionTwoX, positionTwoY, ballTwoSize, ballTwoSize);
  
  if (distance <= edgeBallOne + edgeBallTwo) {
    ballOne = color(r, g, b);
    ballTwo = color(r2, g2, b2); 
  }
  
  
}

void keyPressed() {
  
}

void mousePressed() {
  
}
