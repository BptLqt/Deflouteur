# Deflouteur
v1.0


A machine learning algorithm that unblur your blur pictures.
This algorithm uses stacked auto-encoders, in order to recreate what would your picture look like if it was clear.
For power processing issues, the pictures will 64x64 images, leading to 4096 nodes in the first layer of the Auto-encoder
The images will be taken on the internet, and will be processing that way :

-> First the pictures will be transform to black and white picture, and stocked in the "original_pictures" folder (RGB in v2.0)

-> Then the images will be blurred and stocked in the "blurred_pictures" folder

-> We'll separate of course a training set from a test set

-> We'll give in entry the blurred pictures to the auto-encoder, the pictures's informations will be processing through the network's nodes, until the output layer. Then will "show" to the AE the wanted output ( the unblurred image ), will calculate the loss, and use gradient descent in order to ajustate the neurons's weights through backpropagation.

-> The auto-encoder will perform many epochs of training (500), throught all images (not mini-batchs)

-> The algorithm will be tested on the test set, in order to see his efficiency on real world applications

The auto-encodeur's numbers of neurons in the hiddens layers will be superior to the number of inputs (and of course outputs), that way the AE will be able to recognize better paterns in the images.
So the information will not be "encoded" or "decoded" like with an common AE.
This process can be used to colorize black and white pictures, with a few changes.
The v2.0 will be able to process RGB images, and much higher image dimensions ( using convolutional and deconvolutional layers )
