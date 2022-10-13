# autonomous-car-simulation
This is an autonomous car simulation project using genetic algorithm (GA) with feed forward artificial neural networks (ANN) on Unity 3D.

An ANN model trained by GA is used as the car's control system which sets throttle, brake and steering angle parameters as output. The network obtained as a result of training leads the vehicle to move successfully in an unknown environment. The artificial neural networks model used in the project is as follows.


<img src="https://user-images.githubusercontent.com/21012336/195501082-c139c176-2588-4994-bf15-5ddd3bedf10c.png" alt="drawing" width="400"/>

A certain number of neural networks are generated with this architecture and random weight and bias values. Each network is used to drive a car. All the cars are put on the track at the same time and they run on the track without interacting with each other. They do not collide, and their sensors do not detect one another.


Network inputs are car sensor values and outputs are controls of car’s direction and acceleration (1). Also, each one of these networks is a chromosome of the GA. Each weight and bias in the network correspond to a gene of the chromosomes. The fitness of a chromosome is determined by how well the car performs on the track. The purpose is to improve the fitness of the chromosomes over the generations and pick the best one performing the task which is driving the car on the given track in the final generation.

The neural networks used for driving the cars were trained by Genetic Algorithm. The use of the genetic algorithm in learning was carried out as follows: Firstly, a population size was determined. This determined the number of ANNs created, so that their weights could be assigned. These networks are represented as a series of weights and biases. Each of these sequences represent a chromosome in the GA and converted to a neural network before attaching to a car. 

The fitness of the chromosomes was calculated as the cube of the number of checkpoints the vehicle reached. The reason behind this choice was once subsequent checkpoint reached by the vehicle, it has a greater impact on the chromosome's fitness than the previous checkpoint. If vehicle hits the walls during the trial, or do not reach a new checkpoint within ten seconds, it will return to the starting point for new trial.

<img src="https://user-images.githubusercontent.com/21012336/195501773-8cb43b87-3846-4e93-9ca4-9391c197ab05.png" alt="drawing" width="400"/>

<img src="https://user-images.githubusercontent.com/21012336/195501911-d7d46515-4a5a-4020-ad05-4ebf6f6c5802.png" alt="drawing" width="400"/>

<img src="https://user-images.githubusercontent.com/21012336/195501933-111b69d1-3404-4fc8-b314-db00132bbfd9.png" alt="drawing" width="400"/>

The results were as below where displays axis is the number of generations, and y axis shows the cube roots of the fitness values.

<img src="https://user-images.githubusercontent.com/21012336/195502183-25304fac-3e60-465c-8a5c-7ecfe91886b1.png" alt="drawing" width="400"/>
