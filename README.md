# ECS AutoScaling Examples
AutoScaling ECS cluster

This repo contains a CloudFormation stack which creates an ECS cluster with a running nginx service. The following parameters can be adjusted in order to test the autoscaling behavior.

```
  ClusterDesiredCapacity: 1,                  # The number of container instances which should be started
  ClusterMaxSize: 100,                        # The maximum size of the ECS cluster
  ClusterMaxMemoryReservationPercentage: 80,  # The threshold when ASG should scale up
  TaskDesiredCapacity: 1,                     # The number of running nginx tasks
  TaskMemory: 512,                            # The reserved memory for one nginx task
```  

To create the stack open the console and run
```
bundle install
bundle exec rake deploy
``` 
