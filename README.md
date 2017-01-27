# Man In The Pi Castle

## Overview

A Pi Day project for a chess playing robot.  It will be broken down into a set of services that will perform different operations as part of the game of chess. 

## Services

Services should all be implemented as an API and be documented in their respective repositories.

The service definitions are as follows:

### Path Service

A service that creates a cartesian path for the robot to follow.  Basically a 2D to 3D move conversion service

#### Inputs:

* Board dimension configuration file
* Board Move

#### Output:

* An action for the Movement Service to perform.  This should be an x,y,z coordinate, grab, or release.

### Movement Service

Actually controls the robot and causes it to move along the path.

#### Inputs: 

* An Action (See definitions below)

#### Output:

* Causes the robot arm to make the specified action

### Chess Service

Plays chess.  Will most likely use an external API or service to do the chess algorithms.

#### Input: 

* The move that the opposing player makes

#### Output: 

* A board move that is fed to the Path Service

## Definitions

Board Move: A set of two board positions, such as A5, B7.  The start should be the first, and the end should be the second

Chess Move: A Chess Notation Move

Action: One of three: x,y,z coordinate, grab, or release
