
osc(15).color(0.5,0.1,0.5).rotate(0.1, .1).modulate(osc(1).rotate(0.03).add(o0, 0.1)).add(osc(20,0.01,1).color(0,0.8,1)).out(o0)
osc(50,0.05, 0.7).color(1,0.7,0.5).diff(o0).modulate(o1,0).out(o1)
osc(2).color(1,0.7,0.5).diff(o0).modulate(o1,0).out(o1)
osc(0.7, 2, 3, 0.5).color(1,0.7,0.5).diff(o0).modulate(o1,0).out(o1)


render(o1)
