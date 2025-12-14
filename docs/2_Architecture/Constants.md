---
title: Constants
layout: default
parent: Kitbot Intro
---
# Constants.java

Constants.java is an important file. This file contains classes whose only job is to hold constants (variables with the static and final keywords).
Below is a more detailed description of what to do in the constants.java file.
```Java
 * The Constants class provides a convenient place for teams to hold robot-wide
 * numerical or boolean
 * constants. This class should not be used for any other purpose. All constants
 * should be declared
 * globally (i.e. public static). Do not put anything functional in this class.
 *
 * <p>
 * It is advised to statically import this class (or one of its inner classes)
 * wherever the
 * constants are needed, to reduce verbosity.
public final class Constants {
```

## Kitbot Drivetrain Constants

While creating the ```DriveTrainSystem``` for the [Kitbot Intro](2.5_KitbotIntro.md) tutorial, the id's for the 4 motors are defined as constants in the ```constants.java``` file.

### Steps:

- Create a ```public static final class DriveConstants {}``` class inside the ```Constants``` class. This will hold all of our drivetrain related constants, and makes importing them easier.
- Inside the ```DriveConstants``` class, create the four id variables:

    ```Java
    public static final int LEFT_LEADER_ID = 1;
    public static final int LEFT_FOLLOWER_ID = 2;
    public static final int RIGHT_LEADER_ID = 3;
    public static final int RIGHT_FOLLOWER_ID = 4;
    ```   
- There is one more constant to create, which is the ```DRIVE_MOTOR_CURRENT_LIMIT```. This constants defines the maximum amount of current (amps) that the code will send to the motor, which prevents damaged the motor or blowing the fuses. The full ```DriveConstants``` class is below:

```Java
public static final class DriveConstants {
    public static final int LEFT_LEADER_ID = 1;
    public static final int LEFT_FOLLOWER_ID = 2;
    public static final int RIGHT_LEADER_ID = 3;
    public static final int RIGHT_FOLLOWER_ID = 4;
    // Prevents too much current from being sent to the motor. 
    public static final int DRIVE_MOTOR_CURRENT_LIMIT = 60;
  }
```
