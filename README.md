# QTM350
Description of how to replicate our final project of using AWS Rekognition

## Objectives
We hypothesized that wearing glasses and/or masks would impair the effectiveness of AWS Rekognition on recognizing human faces. More specifically, we believe that wearing masks would make it much more difficult for the machine to detect whether one is smiling, and wearing masks and/or glasses would affect Rekognition's ability to predict the emotions of the faces.

So we did a controlled experiment using photos of our group members, where everything is the same within each set of photos except wearing masks and/ or glasses or not.

## Data
All data used has been uploaded to a public S3 bucket on AWS named "qtm350-final-project." If there are any access issues, we have also uploaded our photo data under "Photos" folder on this github page. We took 4 photos of each of our group members. One with glasses, one with mask, one with both glasses and mask, and one with neither.

1: no mask, no glasses
2: no mask, with glasses
3: with mask, no glasses
4: with mask, with glasses

Note: we have included our code that created an S3 bucket and moved photos to this bucket.

## Code
Our annotated codes are under "QTM350_Final_Project.ipynb" file, where we looked at facial attributes of whether one's smiling, whether one's wearing glasses, and one's emotion using Rekognition. We also found similarities among faces of the same person using Rekognition.

## Conclusion
In the "Smile" attribute, we found that wearing glasses and/ or mask impaired Rekognition's ability to detect smiles. In peng's example, where Peng smiled in all four photos, Rekognition only detected the smile in the photo with neither glasses nor mask. 
In the "Glasses" attribute, we found that Rekognition is tempted to recognize faces with only masks on as having glasses on, since a lot of photos ended with a 3: with mask, no glasses were classified as "True" for "Glasses" feature.
In the "Emotion" attribute, we can also see the effects of wearing masks on Rekognition, since many photos numbered 3 and 4: with mask, no glasses and with mask, with glasses, respectively, were mistakenly detected as "FEAR."
Finally, we found that the similarity attribute of Rekognition is pretty strong, since we saw minimal influences of wearing glasses and/or masks on similarity among faces of the same person.
In general, we can see the trend that certain features of Rekognition has been affected by the person in the photo wearing glasses and/ or masks, while some features were not very much affected.