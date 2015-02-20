# openfl-transform-examples

**THIS REPO IS A WORK IN PROGRESS**

This samples (just one for now) shows the capabilities of the Transformation class included in the **akifox library** (which is my personal haxe develop library)

## Goal

This class (and this example shows how to implement it) aims to provide an easy tool to manage affine transformations using a reliable pivot point.

## Install and try

<code>git clone --recursive https://github.com/yupswing/openfl-transformation-samples.git</code><br/>
<code>cd openfl-transformation-samples</code><br/>
<code>lime test neko</code><br/>

You should get a window with a red square.
- <code>Space<code> to reset the transformations
- Drag to move
- Click to change the pivot point
- Drag+<code>Shift</code> to rotate around the pivot point
- Drag+<code>Alt</code> to scale related to the pivot point
- Drag+<code>Ctrl</code> to skew related to the pivot point (center of the cross is 0,0)
- <code>UP</code> Flip X 
- <code>DOWN</code> Flip Y 
- <code>RIGHT</code> Rotate 15deg
- <code>LEFT</code> Rotate -15deg
- <code>1</code> to <code>9</code> to set the pivot point on the relative anchor point (TOPLEFT, MIDDLELEFT,BOTTOMLEFT,TOPCENTER... BOTTOMRIGHT)

<img src="https://dl.dropboxusercontent.com/u/683344/akifox/git/openfl-transform-sample.png"/>

## Using the Class
**I DON'T RECOMMEND USING IT RIGHT NOW BECAUSE IT'S A WORK IN PROGRESS AND IT WILL CHANGE MAYBE RADICALLY IN THE PROCESS OF BECOMING STABLE**

Once you got a DisplayObject (Sprites, Bitmap...) you can create a Transformation object linked to it.
(Don't use more than one transformation at a given time. I will code this check later on)

<pre>
trf = new Transformation(YOUROBJECT);
trf.setInternalPoint(Transformation.LEFT,Transformation.TOP);
                               
// these are the Pivot Point coordinates (they will not change unless
// you change the pivot point position)
var pivotCoordinates:Point = trf.getAbsolutePoint();

trf.rotate(20); //rotate 20degress clockwise

</pre>

## Finished
- Pivot point managing
- Scale
- Flip
- Rotate

## Working on
- Skew (not reliable right now, still needs work)
- Cleaning and documenting code
- Better README.md when it will become stable.
