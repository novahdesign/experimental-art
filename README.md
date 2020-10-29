function setup() {
  createCanvas(710, 710, WEBGL);
}

function draw() {
  background(250);
  rotateY(frameCount * 0.01);

  for (let j = 0; j < 10; j++) {
    push();
    for (let i = 0; i < 90; i++) {
      translate(
        sin(frameCount * 0.001 + j) * 100,
        sin(frameCount * 0.001 + j) * 100,
        i * 0.1
      );
      rotateZ(frameCount * 0.0002);
      push();
      sphere(30, 6, 2);
      pop();
    }
    pop();
  }
}
