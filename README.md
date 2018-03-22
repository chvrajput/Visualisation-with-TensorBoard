# Visualisation-with-TensorBoard
So what is TensorBoard and why would we want to use it? TensorBoard is a suite of web applications for inspecting and understanding your TensorFlow runs and graphs. TensorBoard currently supports five visualizations: scalars, images, audio, histograms, and graphs. The computations you will use in TensorFlow for things such as training a massive deep neural network, can be fairly complex and confusing, TensorBoard will make this a lot easier to understand, debug, and optimize your TensorFlow programs.
If we give the graph a name by typing 
with tf.name_scope("MyOperationGroup"): 
and give the graph a scope like this with tf.name_scope("Scope_A"):. when you re-run your TensorBoard you will see something very different. The graph is now much more easier to read, and you can see that it all comes under the graph header.

If you were going to run the TensorBoard now, with
 tensorboard --logdir=path/to/logs/directory, you would see that in your given directory you get a folder named ‘output’. 
http://localhost:6006, If you navigate to the ip address in your terminal, It will take you to your TensorBoard, Then if you click graphs you will see your graph.
