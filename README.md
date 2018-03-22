# Visualisation-with-TensorBoard
So what is TensorBoard and why would we want to use it? TensorBoard is a suite of web applications for inspecting and understanding your TensorFlow runs and graphs. TensorBoard currently supports five visualizations: scalars, images, audio, histograms, and graphs. The computations you will use in TensorFlow for things such as training a massive deep neural network, can be fairly complex and confusing, TensorBoard will make this a lot easier to understand, debug, and optimize your TensorFlow programs.
If we give the graph a name by typing 
with tf.name_scope("MyOperationGroup"): 
and give the graph a scope like this with tf.name_scope("Scope_A"):. when you re-run your TensorBoard you will see something very different. The graph is now much more easier to read, and you can see that it all comes under the graph header
The basic script

import tensorflow as tf
with tf.name_scope("MyOperationGroup"):
    with tf.name_scope("Scope_A"):
        a = tf.add(1, 80, name="Add_these_numbers")
        b = tf.multiply(a, 3)
    with tf.name_scope("Scope_B"):
        c = tf.add(2, 5, name="And_These_ones")
        d = tf.multiply(c, 6, name="Multiply_these_numbers")

with tf.name_scope("Scope_C"):
    e = tf.multiply(5, 50, name="B_add")
    f = tf.div(c, 6, name="B_mul")
g = tf.add(b, d)
h = tf.multiply(g, f)
i = tf.add(h,1)


with tf.Session() as sess:
        writer = tf.summary.FileWriter("output", sess.graph)
        print(sess.run(i))
        writer.close()


If you were going to run the TensorBoard now, with
 tensorboard --logdir=path/to/logs/directory, you would see that in your given directory you get a folder named ‘output’. 
http://localhost:6006, If you navigate to the ip address in your terminal, It will take you to your TensorBoard, Then if you click graphs you will see your graph.
