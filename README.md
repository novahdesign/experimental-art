
let t = 0; // time variable

function setup() {
  createCanvas(1000, 1000);
  noStroke();
  fill(1000, 1400, 700);
}

function draw() {
  background(20, 60); // translucent background (creates trails)

  // make a x and y grid of ellipses
  for (let x = 0; x <= width; x = x + 10) {
    for (let y = 0; y <= height; y = y + 14) {
      // starting point of each circle depends on mouse position
      const xAngle = map(mouseX, 0, width, -4 * PI, 4 * PI, true);
      const yAngle = map(mouseY, 0, height, -4 * PI, 4 * PI, true);
      // and also varies based on the particle's location
      const angle = xAngle * (x / width) + yAngle * (y / height);

      // each particle moves in a circle
      const myX = x + 90 * cos(6 * PI * t + angle);
      const myY = y + 120 * sin(2 * PI * t + angle);

      ellipse(myX, myY, 2.3); // draw particle
    }
  }

  t = t + 0.003; // update time
}
