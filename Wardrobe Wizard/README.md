![image](https://github.com/hollydarter/Data-Science-Math/assets/143565143/2818d528-9b4e-4bfb-b199-317f6a26aa20)
# What is the Wardrobe Wizard?
In today's fast-paced world, managing one's wardrobe can be a daunting task. Choosing the right outfit for different occasions, keeping track of clothing items, and planning daily attire can be time-consuming and often frustrating. The Virtual Wardrobe Organizer is a cutting-edge solution designed to simplify the process of managing your clothing collection and enhancing your daily fashion experience.
# Why It Matters:
- Save Time: Say goodbye to the hassle of sifting through your physical closet each morning. Our virtual wardrobe streamlines the outfit selection process.
- Improve Your Style: Receive personalized outfit recommendations and discover new ways to wear your existing clothing items.
- Sustainability: Make better use of your existing clothes, reducing the need for constant fashion purchases and contributing to a more sustainable lifestyle.
# How It Works
Simply upload photos of your clothing items, and our algorithm will categorize them as shirts or pants. Once your wardrobe is digitized, you can start exploring and utilizing its features.
# What is Alexnet and How do we Use It?
Wardrobe Wizard integrates AlexNet, a pioneering convolutional neural network, to elevate the accuracy of our image classification. Developed in 2012, AlexNet excels in discerning intricate patterns and features within images.Think of AlexNet as your wardrobe's style detective. With a vast collection of clothing photos, its job is to swiftly sort them into two categories: shirts and pants. It's the key to making your wardrobe organization quick, precise, and hassle-free. 
## Why AlexNet Matters:
- *Image Classification:* AlexNet is the backbone of our algorithm, precisely distinguishing between shirts and pants in your clothing photos.
- *Feature Extraction:* Its convolutional layers help to accurately distinguish the differences between clothing items.
 ![image](https://miro.medium.com/v2/resize:fit:960/0*pJ3o_2zTTNnixhKH.png)
## How It Works:
- *Upload Images:*
Easily upload clothing photos through the Wardrobe Wizard interface.
- *Automatic Classification:*
AlexNet works behind the scenes, automatically categorizing images into shirts and pants.
- *Effortless Wardrobe Management:*
Leveraging AlexNet ensures the precision and efficiency of our virtual wardrobe organizer, simplifying your wardrobe management experience.
# Data Deck for Alexnet
Our AlexNet model is trained on a meticulously curated dataset to ensure robust and accurate classification of clothing items in WardrobeWiz.
<table>
  <tr>
    <td>
      <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTG0I9-Bno7heabRn7nO6YEPC22BlfmTRQGzA&usqp=CAU" width="200" height="200">
    </td>
    <td>
      Vs
    </td>
    <td>
      <img src="data:image/jpeg;base64,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" width="200" height="200"> 
    </td>
  </tr>
</table> 

## Dataset Composition:
- *Clothing Diversity:* The dataset encompasses a wide variety of clothing items, capturing diverse styles, patterns, and textures representative of real-world wardrobes.
- *Image Variation:* We've included images with different angles, lighting conditions, and backgrounds to enhance the model's ability to differntiate between shirts and pants.

# Collected Data
Wardbrobe Wizard's data deck, composed of 50 images of either shirts or pants. 

<a href="https://docs.google.com/presentation/d/1w-UwMzHvUYb3D-X_rpMsPCt_y8ej8LpBzYM9ql7BFmc/edit#slide=id.g1ea91ee60e5_0_235">Data Deck </a>

# Results
<a href="https://colab.research.google.com/drive/1LW18gelJDEHGanZsYtbeAhaSYfz5FnFa#scrollTo=WANJibeUNghZ" >Alexnet Loaded Slides </a>

Tracking the evolution of our model's performance, the following graphs illustrate the training accuracy (acc_train) and loss throughout multiple training runs

## Accuracy
![image]()
## Loss
![image]()

# Run Summary
- Training accuracy: Achieved an accuracy of -- during training.
- Loss: Recorded a loss value of --.

The elevated training accuracy underscores Wardrobe Wizard's proficiency in picking between shirts and pants. This high level of accuracy positions Wardrobe Wizard as an intelligent solution for refined wardrobe organization. 

# Feature Map
![image](https://user-images.githubusercontent.com/143112521/282343750-baaf59f8-a379-483e-bdd6-95d1d3c7f202.png)

# Future Enhancements
We are continuously working to improve the Virtual Wardrobe Organizer. Future updates may include enhanced outfit recommendations, integration with weather forecasts, and the ability to share your wardrobe with friends or fashion stylists.

