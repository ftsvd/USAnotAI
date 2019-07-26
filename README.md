# USAnotAI
 Organ Classification on Abdominal Ultrasound using Javascript

<a href=https://siim.org/page/siim2019>SIIM 2019</a> Innovation Challenge Winner

<b>Training File:</b> usanotai.html<br>
1. Training images are in \train folder (named as {organ}-00##.png)
2. Test images are in \test folder (named as {organ}-005#.png)
3. Once images are loaded, start training by typing this in the console:<br>
<code>doTrain() //trains one epoch by default</code><br>
<code>doTrain(5) //trains 5 epochs</code>
4. Script will automatically run test images through the trained model at the end of doTrain
5. To output the trained model as JSON.stringify:<br>
<code>doNet()</code><br>

<b>Live Classification:</b> live.html<br>
1. Accepts a video feed from the ultrasound machine into the computer via video capture
2. Crops the video feed to dimensions that the model uses
3. Runs images (every 100ms) through the model and outputs predictions
4. Model is hard-coded as string (from doNet() above)

<b>I wrote this without knowing <i>anything</i> about machine learning, therefore:</b>
1. Epochs are called "repetitions". 
2. My "Test Images" is essentially the validation set. And the live video feed is the actual test set.
3. No evaluation of training and validation losses.
