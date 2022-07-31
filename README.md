# Autoencoder

An autoencoder is a special type of neural network that is trained to copy its input to its output. For example, given an image of a handwritten digit, an autoencoder first encodes the image into a lower dimensional latent representation, then decodes the latent representation back to an image. An autoencoder learns to compress the data while minimizing the reconstruction error.

![image](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSGir0YoT-cWA_B2XTd76p8g3Kofk3EozWojg&usqp=CAU)

As you can see, an autoencoder typically has the same architecture as a Multi-Layer
Perceptron, except that the number of neurons in the output
layer must be equal to the number of inputs. In this example, there is just one hidden
layer composed of two neurons (the encoder), and one output layer composed of
three neurons (the decoder). The outputs are often called the reconstructions because
the autoencoder tries to reconstruct the inputs, and the cost function contains a
reconstruction loss that penalizes the model when the reconstructions are different
from the inputs.

Autoencoders can have multiple hidden layers. In this case they are called <b>stacked autoencoders</b> (or deep autoencoders).
Adding more layers helps the autoencoder learn more complex codings. That said,
one must be careful not to make the autoencoder too powerful. Imagine an encoder
so powerful that it just learns to map each input to a single arbitrary number (and the
decoder learns the reverse mapping)
