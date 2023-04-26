[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/fOgSn8sg)

Code Link: https://editor.p5js.org/liamdworkin/sketches/sds6Asd-O

The object of Lab 11 was to paraphrase in coloquial language how we perceived an example of code was done. 
I chose the 'asteroids' game. 
Below is first, the obfuscated code and then my own notes on how the project works. 

(function(j,r){var z=S,l=j();while(!![]){try{var M=parseInt(z(0x1db))/0x1+-parseInt(z(0x1f7))/0x2+-parseInt(z(0x1f1))/0x3*(-parseInt(z(0x1e0))/0x4)+-parseInt(z(0x1e1))/0x5+-parseInt(z(0x1ea))/0x6+parseInt(z(0x1f2))/0x7*(parseInt(z(0x1f0))/0x8)+-parseInt(z(0x1ee))/0x9*(-parseInt(z(0x1fa))/0xa);if(M===r)break;else l['push'](l['shift']());}catch(s){l['push'](l['shift']());}}}(p,0x346f5));function Asteroid(j,l){var Y=S;j?this[Y(0x1e8)]=j[Y(0x1d9)]():this[Y(0x1e8)]=createVector(random(width),random(height));l?this['r']=l*0.5:this['r']=random(0xf,0x32);this[Y(0x1e2)]=p5[Y(0x1d6)][Y(0x1ed)](),this[Y(0x1f6)]=floor(random(0x5,0xf)),this[Y(0x1e5)]=[];for(var M=0x0;M<this[Y(0x1f6)];M++){this[Y(0x1e5)][M]=random(-this['r']*0.5,this['r']*0.5);}this[Y(0x1de)]=function(){var O=Y;this[O(0x1e8)][O(0x1e9)](this[O(0x1e2)]);},this['render']=function(){var e=Y;push(),stroke(0xff),noFill(),translate(this[e(0x1e8)]['x'],this[e(0x1e8)]['y']),beginShape();for(var s=0x0;s<this[e(0x1f6)];s++){var v=map(s,0x0,this['total'],0x0,TWO_PI),Z=this['r']+this[e(0x1e5)][s],n=Z*cos(v),f=Z*sin(v);vertex(n,f);}endShape(CLOSE),pop();},this[Y(0x1f3)]=function(){var K=Y,s=[];return s[0x0]=new Asteroid(this[K(0x1e8)],this['r']),s[0x1]=new Asteroid(this[K(0x1e8)],this['r']),s;},this[Y(0x1d5)]=function(){var X=Y;if(this[X(0x1e8)]['x']>width+this['r'])this[X(0x1e8)]['x']=-this['r'];else this[X(0x1e8)]['x']<-this['r']&&(this[X(0x1e8)]['x']=width+this['r']);if(this[X(0x1e8)]['y']>height+this['r'])this[X(0x1e8)]['y']=-this['r'];else this[X(0x1e8)]['y']<-this['r']&&(this[X(0x1e8)]['y']=height+this['r']);};}function Laser(j,r){var R=S;this['pos']=createVector(j['x'],j['y']),this[R(0x1e2)]=p5[R(0x1d6)][R(0x1f9)](r),this[R(0x1e2)]['mult'](0xa),this[R(0x1de)]=function(){var b=R;this[b(0x1e8)][b(0x1e9)](this[b(0x1e2)]);},this[R(0x1ef)]=function(){var P=R;push(),stroke(0xff),strokeWeight(0x4),point(this['pos']['x'],this[P(0x1e8)]['y']),pop();},this[R(0x1ec)]=function(l){var T=R,M=dist(this[T(0x1e8)]['x'],this[T(0x1e8)]['y'],l[T(0x1e8)]['x'],l[T(0x1e8)]['y']);return M<l['r']?!![]:![];},this[R(0x1f4)]=function(){var h=R;if(this['pos']['x']>width||this[h(0x1e8)]['x']<0x0)return!![];if(this[h(0x1e8)]['y']>height||this['pos']['y']<0x0)return!![];return![];};}function Ship(){var J=S;this[J(0x1e8)]=createVector(width/0x2,height/0x2),this['r']=0x14,this[J(0x1df)]=0x0,this['rotation']=0x0,this[J(0x1e2)]=createVector(0x0,0x0),this[J(0x1f8)]=![],this['boosting']=function(j){var i=J;this[i(0x1f8)]=j;},this['update']=function(){var C=J;this[C(0x1f8)]&&this[C(0x1e6)](),this[C(0x1e8)][C(0x1e9)](this[C(0x1e2)]),this['vel'][C(0x1e3)](0.99);},this[J(0x1e6)]=function(){var c=J,j=p5[c(0x1d6)][c(0x1f9)](this[c(0x1df)]);j[c(0x1e3)](0.1),this[c(0x1e2)][c(0x1e9)](j);},this[J(0x1ec)]=function(j){var d=J,r=dist(this[d(0x1e8)]['x'],this[d(0x1e8)]['y'],j[d(0x1e8)]['x'],j[d(0x1e8)]['y']);return r<this['r']+j['r']?!![]:![];},this[J(0x1ef)]=function(){var D=J;push(),translate(this[D(0x1e8)]['x'],this[D(0x1e8)]['y']),rotate(this[D(0x1df)]+PI/0x2),fill(0x0),stroke(0xff),triangle(-this['r'],this['r'],this['r'],this['r'],0x0,-this['r']),pop();},this[J(0x1d5)]=function(){var W=J;if(this[W(0x1e8)]['x']>width+this['r'])this[W(0x1e8)]['x']=-this['r'];else this[W(0x1e8)]['x']<-this['r']&&(this[W(0x1e8)]['x']=width+this['r']);if(this[W(0x1e8)]['y']>height+this['r'])this[W(0x1e8)]['y']=-this['r'];else this[W(0x1e8)]['y']<-this['r']&&(this[W(0x1e8)]['y']=height+this['r']);},this[J(0x1f5)]=function(j){var m=J;this[m(0x1d7)]=j;},this[J(0x1e4)]=function(){var H=J;this[H(0x1df)]+=this[H(0x1d7)];};}var ship,asteroids=[],lasers=[];function S(j,r){var l=p();return S=function(M,s){M=M-0x1d5;var v=l[M];return v;},S(j,r);}function setup(){createCanvas(windowWidth,windowHeight),ship=new Ship();for(var j=0x0;j<0x5;j++){asteroids['push'](new Asteroid());}}function draw(){var o=S;background(0x0);for(var r=0x0;r<asteroids[o(0x1d8)];r++){ship[o(0x1ec)](asteroids[r])&&console['log'](o(0x1eb)),asteroids[r][o(0x1ef)](),asteroids[r][o(0x1de)](),asteroids[r]['edges']();}for(var r=lasers[o(0x1d8)]-0x1;r>=0x0;r--){lasers[r]['render'](),lasers[r][o(0x1de)]();if(lasers[r][o(0x1f4)]())lasers['splice'](r,0x1);else for(var l=asteroids[o(0x1d8)]-0x1;l>=0x0;l--){if(lasers[r][o(0x1ec)](asteroids[l])){if(asteroids[l]['r']>0xa){var M=asteroids[l][o(0x1f3)]();asteroids=asteroids[o(0x1da)](M);}asteroids[o(0x1dd)](l,0x1),lasers['splice'](r,0x1);break;}}}console['log'](lasers[o(0x1d8)]),ship[o(0x1ef)](),ship[o(0x1e4)](),ship[o(0x1de)](),ship[o(0x1d5)]();}function keyReleased(){var G=S;ship[G(0x1f5)](0x0),ship[G(0x1dc)](![]);}function keyPressed(){var t=S;if(key=='\x20')lasers[t(0x1e7)](new Laser(ship['pos'],ship[t(0x1df)]));else{if(keyCode==RIGHT_ARROW)ship[t(0x1f5)](0.1);else{if(keyCode==LEFT_ARROW)ship['setRotation'](-0.1);else keyCode==UP_ARROW&&ship['boosting'](!![]);}}}function p(){var B=['random2D','11349irkBtf','render','280ooCFCO','1452uKQxlJ','43386oyZHDb','breakup','offscreen','setRotation','total','304190IkOoDn','isBoosting','fromAngle','2180pkmQyz','edges','Vector','rotation','length','copy','concat','298347BHQfSZ','boosting','splice','update','heading','1832IhfrUD','1920310XszYhK','vel','mult','turn','offset','boost','push','pos','add','1565502nGobtl','ooops!','hits'];p=function(){return B;};return p();}

/* 
There are three interactive assets/sprites of sorts outside of the background: the asteroids, the spaceship, and the particles fired from the spaceship when the space bar is interacted with. 

I'm sure values like 'speed = ...' and possibly 'createSprite = ... (ship)' are also defined at the top in setup for the rest of the code. 

Background is then probably done in the 'draw' function and there are no other grapics/assets other than the background and three sprites. 
*/

//SHIP

/*
My assumption is there is a class for all three of those assets. The first being the spaceship which assumedly has a 'constructor' a 'show' and 'move' or 'update' in the class itself. The 'contructor' element of the class helps define the variables of the sprite such as X, Y used via translate or size used via scale. In the class format they become 'this.X' or 'this.size' in order to differentiate the variables from others. 

Next in the 'show' part of the spaceship class there would be the actual asset that defines the phyiscal look of the sprite. Whatever it is from a single rect to multiple arcs they are defined by the preset variables of the class itself. You can then in the class create a hardcoded version of the sprite, or pass along some form of visuals coded in an array to a single class if to create multiple different looking versions with the same class. My assumption is the spaceship is hardcoded because there's only one and it'd just be easier. 

Finally, the 'move' or 'update' function contains the movement, using this.height/width or height/width and reversing the speed value to keep the spaceship teleporting around the canvas when you go over a boundary. Furthermore, the spaceship's movement is bound to the keys, using 'keyIsDown'. the 'up' arrow makes the ship move forward and the down arrow makes the ship move backwards by applying +/- speed values to it. Whereas the left/right arrow keys make the ship roatate in place for steering.

The ship class is then either assigned to an array such as, "ship1 = []" and called back into the draw function using the 'new' function as the "ship1 = new Ship(this.x, this.y, ....)" Though if the ship is hardcoded this may be an unecessary step as it could just be called back with no added variables using, "Ship.show" and "Ship.update" or "Ship.move" in the draw function, allowing the class to be shown and the movment applied. 
*/

//ASTEROID

/*  
The asteroids work very much the same, however, my guess is they either are hardcoded as well and looped in an array to create multiple iterations from the same single class of the asteroid or they are done in the same manner as the ship, requiring multiple separate arrays like "asteroid1 = [], asteroid2 = [],..." of which they are then each called back separately in the draw function using "show.asteroid1", and "show.asteroid2", etc... 

The major difference in the "move" aspect of the asteroid class comes down the random movement they utilize. There is no conditional statement that defines the movement as a key bind or input and instead they seemingly float around randomly. Here it is most likely that "this.speed" in the class variable is somewhat randomized as far as initial direction, being limited to the canvas by this.x/this.y location and width/height interaction. They move randomly, but reverse the value of their movement (+ to - or - to +) when the interact with the boundaries and their own x/y value is 'too far' over the boundary. 

Likely the asteroids sprite is not hardcoded in the class but taken from arrays as they have some level of random look to each asteroid, unlike the ship and particles which always appear the same.
*/

//PARTICLES

/*
The particles most likely are also a class. They have a constructor, show, and move/update, containing their constructor class for variables and then either a hardcoded design or leaving variables that allow for change to be applied in the draw function in 'show' part of the class. 

As far as movement goes. The 'x/y' position of the particles is likely linked to the 'sprite.X' and 'sprite.Y' position, being given positive acceleration from wherever the ship sprite is facing, and beginning their existence at the x/y of the ship itself.

The speed of the particles, defined in 'move' or 'update' is most likely the 'ship.speed' combined with a numerical variable like 5 or something to make it appear faster but congruent with the ship itself. 

Finally, the particles don't need to be looped for placement even though there are multiple iterations of them and that is because you're using a conditional to spawn them when the 'spacekey' IsPressed. Each space key defines a single particle spawning, allowing for a simple method of creating multiple particles. Also the particles unlike the ship and asteroids do have collision but don't have boundaries, as the goal is to have them collide and dissappear or move off screen, not remaining as bouncing bullets all over the canvas. 

The collision is most likely done in a collision, coniditonal function, using 'dist()' of the 'asteroid' and 'particle' class. If dist(ast.x, ast.y, part.x, part.y) -> equating to if the x/y value of the asteroid and the x/y value of the particles are the same, then they 'collide' which in the conditional would change the asset of the asteroid to multiple, smaller asteroids, most likely defined in a class almost the same as the prospective first 'Asteroid' class. The conditional also likely yields a 'noStroke' or 'noFill' or some more complicated form of deleting the particle once it has interacted and collided as it does not continue. It isn't using 'hsla' to judge collision amounts as the asteroid breaks apart instead upon collision and the particle purely disappears. 
*/

//GAMEPLAY CHANGES

/*
1. Add collision between the 'ship' and 'asteroids'. It's not very fun w/o some danger and it assuredly wouldn't be hard for the game developer to hybridize the code that makes the particle disappear when it collides with an asteroid the same for the ship + asteroid when the ship takes 'damage'

2. With collision added, add some form of 'life' system. Create a class spawning 3 hearts in the upper corner and when collision between the ship/asteroid class is detected a conditional takes a single life away. When all three are gone, the game is over. 

3. Finally, my third gameplay change is to add 'random()' speed into the movement of the asteroids. They all move the same speed and at all sizes have the same 'this.speed' in 'move' whereas the game would be harder and more fun with varying speeds.
*/

//AESTHETIC CHANGES

/*
1. I would first add a 'stars' class in, define their move and show functions as well as constructors to only have them move ever so slightly, and to have no collision so they don't change interactivity and serve the function of providing a more detailed background. Using an array and for loop I could call back like 20 little stars that while not static don't move much to add an element of 'space' to the background. 

2. I would add a title image, and 'game over' screen. Just a quick title image that displays text for a set period of when the game is initiated. (The game can still even be played, just everytime you refresh the game itself, a little "Welcome to Space" would play. It could also include movement instructions) Alternatively, I'd add a little 'game over' that played when all three hearts/lives are exhausted. These could be done simply, with conditionals. Maybe the 'game over' and black screen needs a class to create a large blank image superceding everything but I believe it can be done entirely with conditionals. If all three hearts are exhausted, display 'game over' while 'ship' and 'particle' are given noStroke/noFill. (The most simple way I could imagine it.)

3. Add some color and texture. I personally really like the classic arcade, 2D design of asteroids and games like pong. However, for the purpose of our assignment here I'd use HSL on the stars I added to make them semi transparent little specks in the 'show' function, add in a random colors array "asteroidcolors = []" using full transparency on the asteroids to give them randomized color options of like gray, gold, silver, etc... and finally for the ship itself I'd try and give it a little flame animation using 'framedelay' and small addition to the hardcoded visuals of the ship of a single rocket burner visual. 
*/
