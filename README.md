# Cartoonization

![house](./images/house.jpg)
![paja](./images/paja_kuca_5000_20210821_203506_image.png)    


 There are many methods that can cartonify picture. One of those methods include usage of neural networks and neural style transfer technique using cartoon pictures as style images.
 Idea behind this technique is to have separated images, one that contains content (shape, objects...) and the other that contains style (colours, textures...) , and *combine* them into one image. Combining includes applying layer upon layer on of style image on content image.
 We use vgg19 pretrained neural network to extract specific layers and use them to define content and style of newly generated image. To extract style from an image, we use multiple layers to define textures that will be transfered. Unlike style, content of an image is extracted from one specific layer.  
 Im mathematical terms, this process is an optimization process and in this notebook we use stochastic gradient descent as an optimization method.
 Loss function is derived into two separate loss functions (content loss and style loss), but because this is style transfer, the most important thing is that the resulting image is appealing for the viewer. This techique is also used to create new images using famous paintings.
 
 | Content | Style | Combination |
 |---------|-------|-------------|
 | ![kitten](./images/kitten.jpg) | ![picaso](./images/picaso.jpg)| ![kitten_picaso](./images/picaso_mace_5000_20210810_114531_image.png)|
 
 | Content | Style | Combination |
 |---------|-------|-------------|
 | ![kitten](./images/kitten.jpg) | ![picaso](./images/picaso.jpg)| ![kitten_picaso](./images/picaso_kitten_800_20210821_200303_image.png)|
 
 
 | Content | Style | Combination |
 |---------|-------|-------------|
 | <img src="./images/iri.jpg" width="400" height="400"> | ![picaso](./images/picaso.jpg)| ![iri_picaso](./images/picaso_iri2_5000_20210812_182108_image.png)|
 
 
 #### Cartoon images
 
 Beside monitoring loss function, important parameters are:
 - layers that we use to extract features of an image
 - weight that are used to balance influences of style and content of new image
 - learning rate of gradient descent

Choosing this parameters we generate very different and interesting images
 
 | Content | Style | Combination |
 |---------|-------|-------------|
 | ![house](./images/house.jpg) | ![garfield](./images/garfield.jpeg)| ![house_gar](./images/gar_kuca_5000_20210819_201548_image.png)|
 
 
 | Content | Style | Combination |
 |---------|-------|-------------|
 | ![house](./images/house.jpg) | ![garfield](./images/garfield.jpeg)| ![house_gar](./images/gar_kuca_5000_20210820_211815_image.png)|
 
 
 
 | Content | Style | Combination |
 |---------|-------|-------------|
 | ![house](./images/house.jpg) | ![donald](./images/paja.jpeg)| ![house_gar](./images/paja_kuca_5000_20210821_203506_image.png)|
 
 
  #### Cartoon images
Papers and tutorials used to create this project are listed in resources.md  
Requirements are listed in requirements.txt
