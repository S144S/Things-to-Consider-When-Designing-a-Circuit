# Things to Consider When Designing a Circuit
According to my experience, these are 20 points that are good to pay attention to when designing a circuit:

1. In PCB design, first, place the components which have a certain place on the board.
2. Always use the component datasheet as the reference for your design. (most of the datasheets have circuit design examples for different use)
3. for the microcontroller circuit, development boards like Arduino, NodeMCU, Blue pill, and ... can really help. (most of their design are available on the internet)
4. The shorter traces, The better performance, and also try to keep routes in one layer.
5. Consider your PCB manufacturer's minimum requirement(such as min trace width, min clearance, min hole size, and ...) for your design.
6. Print your PCB design on paper before ordering it, in this way you can check footprints and placements. (this will take you less than an hour but can save more than one day)
7. Choose the best width for traces. you can use any trace width calculator but I recommend Saturn PCB Toolkit.
8. For the power route, you can choose a wider trace than the minimum calculated width but don't do this for the signal route, it's better to keep the signal route as minimum as calculated.
9. Also choosing the Via dimension is an important step (Saturn PCB Toolkit has via calculator too).
10. Avoid making 90&deg; traces, the best angle for the not straight traces is 45&deg;.
11. Use Vias to transfer the heat of routes. (but not too much and not near the IC's pad)
12. Add rules for your design and be sure to use DRC to check them, good rules always help you.
13. Place decoupling capacitors closest place to the IC and if you use Via for them, power vias should be close together.
14. It's better to draw more important routes. (sensitive routes, routes that must be short, routes that must be on one layer, and ...) 
15. In MCU's circuits always consider MCU's pins that have extra notifications. (e.g. input only, make it pull up, don't use it, and ...)
16. It is better if the parallel routes are as far away from each other as possible to reduce the cross-coupling effect.
17. it's better to place relevant parts (e.g. power section) near each other, it helps to reduce EMI.
18. It's better to design the relevant part circuits in separate schematic sheets, it can help you manage and debug better.
19. it's better to make your library for keeping the most used parts.
20. I recommend adding some extra parts to your circuit, for example, if you have doubt if a path needs pull up resistor or not, just add the resistor, if at last, you'll not need it you'll not montage it, and also decoupling capacitors and... .

