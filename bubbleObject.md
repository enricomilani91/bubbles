class Bubble {
  constructor(_x, _y, _r = 50) {
    this.x = _x;
    this.y = _y;
    this.r = _r;
    this.brigthness = 0;
  }
  
  changeColor(brigth) {
    this.brigthness = brigth;
  }
  
    contains(px, py) {
      let d = dist(px, py, this.x, this.y);
      if (d < this.r) {
        return true;
      } else {
        return false;
      }
    }
  move() {
    this.x = this.x + random(-5, 5);
    this.y = this.y + random(-5, 5);
  }

  show() {
    stroke(255);
    strokeWeight(4);
    fill(this.brigthness, 125);
    ellipse(this.x, this.y, this.r*2);
  }
}
