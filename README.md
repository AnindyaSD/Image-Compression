# Image-Compression using Huffman-Encoding

One of the fundamental compression techniques that has been useful in image and video compression standards is Huffman Coding. When using the Huffman Encoding technique on an image, the source symbols might either be the result of an intensity mapping function or the pixel intensities of the image.

The first step of Huffman coding technique is to reduce the input image to a ordered histogram, where the probability of occurrence of a certain pixel intensity value is as - 

prob_pixel = numpix/totalnum

where numpix is the number of occurrence of a pixel with a certain intensity value and totalnum is the total number of pixels in the input Image. 

Let us take a 8 X 8 Image:

![image](https://github.com/AnindyaSD/Image-Compression/assets/93717247/26bcc2f2-147f-4c57-b1a0-446799478bdb)

The pixel intensity values are :

![image](https://github.com/AnindyaSD/Image-Compression/assets/93717247/202e7374-7f65-42d2-b0d7-f192365f3093)

This image contains 46 distinct pixel intensity values, hence we will have 46 unique Huffman code words. It is evident that, not all pixel intensity values may be present in the image and hence will not have non-zero probability of occurrence. From here on, the pixel intensity values in the input Image will be addressed as leaf nodes. Now, there are 2 essential steps to build a Huffman Tree :

Build a Huffman Tree :

-Combine the two lowest probability leaf nodes into a new node.

-Replace the two leaf nodes by the new node and sort the nodes according to the new probability values.

-Continue the steps (a) and (b) until we get a single node with probability value 1.0. We will call this node as root

Average number of bits = 5.343750

Encoded, compressed image output:

Encoded Image :

0111010101000110011101101010001011010000000101111
00010001101000100100100100010010101011001101110111001
00000001100111101010010101100001111000110110111110010
10110001000000010110000001100001100001110011011110000
10011001101111111000100101111100010100011110000111000
01101001110101111100000111101100001110010010110101000
0111101001100101101001010111

