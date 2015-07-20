# PlayerControls
PlayerControls is a modificatin to the three.js script, OrbitControls.js: https://gist.github.com/mrflix/8351020

PlayerControls enables quick and easy access to a 3rd person player controller:

1) "import" three.js library
```html
<script src="js/three.js"></script>
```

2) "import" PlayerControls.js
```html
<script src="js/PlayerControls.js"></script>
```

3) instantiate PlayerControls object ( pass camera and player object as arguments )
```javascript
var controls = new THREE.PlayerControls( camera , player );
```

Keep in mind that player is a mesh or group object with position.x, position.y, etc.. properties

4) update controls in animate function
```javascript
function animate() {

	requestAnimationFrame( animate );

	// other things you do..

	controls.update();
	
	render();

}
```
You can adjust the speed of the player with:
```javascript
controls.moveSpeed = some_number;
```

You can adjust the turn speed with:
```javascript
controls.turnSpeed = some_number;
```