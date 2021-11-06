## Smart Car

![Smart Car](https://s1.cdn.autoevolution.com/images/gallery/SMART-ForTwo-569_6.jpeg)

The basic approach: -

- __Input images/ videos of car, radar, padestrian, lanes, traffic lights, obstacle etc.__

- __GPS and Maps should also be used for better analysis__

______________________________________________________________________________________________________________________________________________________________________________________________

__Car Detection:__ Other cars on the road, either moving or standing should be detected. Car's back, sides, front all images should constitute image set of car detection model.

__Pedestrian Detection:__ Pedestrians can be found on footpath as well as roads. Special care should be taken to not train the algorithm for pedestrian detection only when the pedestrian is standing on the pavement/footpath, model might learn that and ignore the pedestrian on raod.

__Lane Detection:__ This is where the car should move. 

__Traffic Light Detection:__ To stop if the light is red, in a ready state when light is yellow and start moving when light is green. There are 2 fold responsibilities here: 

1. Traffic light detection
2. Which color is it showing.

Both of them are essential for the self-driven car.

__Obstacle Detection:__ Any othe robstacles like a big stone/ fallen tree that may hinder car's movement should be detected.

All the above detections are for avoiding them when the car moves.
______________________________________________________________________________________________________________________________________________________________________________________________

__Trajectory Prediction:__
For cars and pedestrian prediction, predict their trajectory also so that car's motion doesn't hinder with their motion, this is essential to avoid accidents.
If we are able to predict the path a car or person is about to take then motion decisions can be based upon that analysis as well.
______________________________________________________________________________________________________________________________________________________________________________________________

__Motion Planning:__
Combining the insights from all the above, finlly the motion has to be decided like Steer/Acceleration/Break etc.




## Flow Diagram for self-driving car:
![Self_driving_car_approach](https://user-images.githubusercontent.com/35145893/140601677-66d63bbf-e5a8-454e-83c6-66c08728174f.png)

