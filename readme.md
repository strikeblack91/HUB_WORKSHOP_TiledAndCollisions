# Tiled

Tiled is a 2D map level editor with which you can create 2D map for RPG, platformers and others games.\
Tiled is highly flexible. It can be used to create maps of any size, with no restrictions on the number of layers or assets that can be used.\
It can also generate files with different informations about the created map.\
\
Today we are going to use JSON files, to generate some collisions in C, that you could use for your RPG for example.

## Step. 1

[Download Tiled](https://www.mapeditor.org/)

## Step. 2

Create a Tileset by using the assets into the **./assets** directory.\
*(Feel free to use your own assets)*

## Step. 3

Create a map with your differents Tileset.\
*(Here a tips: You should create a layer wich should only contain the objects that you can collide with.)*

## Step. 4

Export you map as PNG. Now you can use your map in your game ! **GG.**

# Python

We know that Tiled can generate JSON files with severals information about the layers, so we will use these informations to create an array of collisions in C !\
Let's use Python, which is a very easy programming language.

## Step. 1

With Tiled, export a JSON file of your map.

## Step. 2

Create a Python script which is going to open a JSON file and print the differents names of the layers.\
[Here a full tutoriel to parse JSON files with Python](https://fr.lmgtfy.com/?q=open%20json%20file%20python)

## Step. 3

Now that you know how to parse a JSON file, create a C file by using your script, and write something inside.

## Step. 4

Create an algorithm which is going to parse the JSON file, take the data and transform them into a C array, in a C file.

# Collision in C\CSFML

Let's do some simple math calculs to use our array of collision. It's really easy.

## Step. 1

Create a main, and put your map as background, by using CSFML.

## Step. 2

Export a sprite into your program, which is going to be your character.\
Then create some event to make your character movable.

## Step. 3

Create a function which is going to parse the array and detect collisions and use it.\
Below, an exemple of how could be the prototype of the function, and a math calculation to know where you are in the array.\

```c
bool isCollision(enum E_DIRECTION direction, sfVector2f sprite_position);
```

```c
int x = position.x / 16 /*(size of a tile)*/;
int y = position.y / 16;
```

## Step. 4

Try your program, and fixed it until it works.

# Conclusion

Now your know how to use Tiled, parse JSON files with Python and how make collisions in C.\
Go make better game than me now !\
\
[MyRPG | Epitech 2023](https://www.youtube.com/watch?v=AFMPK4B1MVs)