# coin-recognition
Algorithm that detects hungarian coin types on basic images using template matching and radius matching

Working principle:
  1. Detect edges on the input images using Laplacian transform, filter out noise
  2. Find circles within the edges
  3. Do template matching for each coin found, the templates are the sample coin images
  4. From all the coins it selects the one where the mean difference between the best match and other matches is the most, in other words the coin it has the highest confidence identifying correctly
  5. Using the reference coin it tries to predict the others by the ratio of their respective radius'
  
Conclusion:
  Coins are hard to distinguish using only a colored image, they're more suited for humans to recognize them by their texture and weight
  Texture is hard to capture in average lighting conditions
  Even the size of the coins are similar
