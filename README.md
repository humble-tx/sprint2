# Sprint 2: Disturbed Terrarium

> **AI Use Disclaimer:** English is not my first language. I initially developed my ideas and reflections in Chinese. To improve clarity and readability, I used AI tools to assist with translating and refining the English version of the text. The concepts, project experiences, and reflections presented in this document are based on my own work and understanding.

### Team Information

Group members:

- Tian Xu 
- Yang Jiaqi 
- Ying Luo
- Zhang XuanHao

 My main contribution to this project was in the early concept discussion stage, where the group decided to shift the project direction from a direct "hand-controls-visuals" interaction towards the "disturbance in an ecosystem" concept based on More-than-human Design.

 
### Project Overview

*Disturbed Terrarium* is an interactive digital ecosystem made in TouchDesigner. A built-in camera tracks the participant's hand through a MediaPipe component. The hand-position data changes the movement and spread of point-cloud plant forms.

The project is connected to **More-than-human Design**. The hand is not treated as a controller giving direct commands. Instead, it becomes a disturbance inside an ecosystem. A small movement can affect the whole plant group and cause it to separate, spread, or reorganise. This shows how human actions can create wider changes inside a connected natural system.

### Interaction

The participant places a hand in front of the camera. MediaPipe detects the hand landmarks inside TouchDesigner. Selected and filtered hand-position channels are used to control the point-cloud plants.

When there is little movement, the plants stay close together and their forms are still recognisable. When the participant moves their hand, the particles spread across the environment. When the disturbance ends, the system can move towards a calmer state again.

```text
Camera
-> MediaPipe hand tracking
-> selected and filtered CHOP channels
-> point-cloud plant movement
-> Render TOP and Bloom TOP
```

### Technical Details

The project uses a laptop, built-in camera, display screen, TouchDesigner, a MediaPipe component, CHOP and TOP processing, and an imported OBJ model.

An original plant model was created and then simplified — the first version had too many surfaces and was too heavy for real-time use, so it was reduced and converted into a point-based structure inside TouchDesigner.

The blue **File SOP** imports the plant model. The purple **Movie File In TOP** imports its texture. If the texture node shows a yellow warning symbol, its file path needs to be relocated to the PNG file in the same project folder.

[TouchDesigner project](./sprint2_touchdesigner/sprint2.toe)  
[Plant model](./sprint2_touchdesigner/disturbed_terrarium_plant.obj)  
[Plant texture](./sprint2_touchdesigner/disturbed_terrarium_texture.png)

### Media

The first screenshot shows the calm state. The yellow and pink point-cloud plants remain grouped and recognisable.

![Calm ecosystem](./media/photos/interaction-state-1-calm.png)

The second screenshot shows the disturbed state. Hand movement causes the point-cloud plants to spread and reorganise.

![Disturbed ecosystem](./media/photos/interaction-state-2-disturbed.png)

These setup photos show the laptop, built-in camera, hand gestures, and the TouchDesigner system running in real time.

![Open-hand interaction setup](./media/photos/setup-open-hand.png)
![Pinch-gesture interaction setup](./media/photos/setup-pinch-gesture.png)
![Dispersed plant response setup](./media/photos/setup-dispersed-response.png)

The demo video shows the hand-tracking interaction and the change between the grouped and dispersed states.

[Demo video](./media/disturbed-terrarium-demo.mp4)

### Process Reflection

My main involvement in this project was in the early stage, in the group discussion about which direction to take. At that stage, we talked about moving away from a straightforward "hand controls the visuals" idea, towards something closer to More-than-human Design — where the hand acts as a disturbance inside a system rather than a controller giving direct commands. Looking at the finished prototype, I think this shift was the right call: the calm and disturbed states make the ecosystem feel like it has its own behaviour, rather than just reacting to a user's input one-to-one.

For future sprints, I'd want to set up a clearer individual task for myself from the start, even within a shared concept.

### Demo Day Notes

*Disturbed Terrarium* is a camera-controlled digital plant ecosystem. The participant places a hand in front of the camera and moves it through the interaction area. MediaPipe tracks the hand, and the point-cloud plants separate, spread, or reorganise.

The hand does not directly control each plant. It acts as a disturbance inside a connected ecosystem. The project shows how one small human action can create a wider system-level response.
