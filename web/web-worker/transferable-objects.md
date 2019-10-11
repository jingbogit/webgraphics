---
description: Avoid cloning data when passing large data among threads.
---

# Transferable objects

#### Documentations:

* [https://developer.mozilla.org/en-US/docs/Web/API/Worker/postMessage](https://developer.mozilla.org/en-US/docs/Web/API/Worker/postMessage)
* [https://developer.mozilla.org/en-US/docs/Web/API/Transferable](https://developer.mozilla.org/en-US/docs/Web/API/Transferable)
* [https://developer.mozilla.org/en-US/docs/Web/API/ImageBitmap](https://developer.mozilla.org/en-US/docs/Web/API/ImageBitmap) 

#### 

#### Example:

May use ImageBitmap for textures. Store ImageBitmap in worker. When main thread retrieved the ImageBitmap, it can be sync converted to texture by:  
 `// onLoad callback  
function ( imageBitmap ) {  
 var texture = new THREE.CanvasTexture( imageBitmap );  
 var material = new THREE.MeshBasicMaterial( { map: texture } );  
}`

{% embed url="https://developer.mozilla.org/en-US/docs/Web/API/ImageBitmap" %}

{% embed url="https://threejs.org/docs/\#api/en/loaders/ImageBitmapLoader" %}



#### 

#### Performance:

{% embed url="https://www.joji.me/en-us/blog/performance-issue-of-using-massive-transferable-objects-in-web-worker" %}



![compability](../../.gitbook/assets/image%20%2818%29.png)

