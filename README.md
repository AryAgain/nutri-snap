# Nutrition Analysis App

## Overview and Goals

The project introduces a unique and user-friendly React application aimed at upgrading how individuals manage their diet and nutrition. This application simplifies the process of identifying and understanding the nutritional value of food items. Users can take a picture of their meal, and the app identifies the food. Upon identification, CaloSnap provides detailed nutritional information displayed in an easy-to-understand graphical format.

![diet history](https://github.com/AryAgain/ImageEncoderSimulator/assets/5464475/6b7e9b17-3c92-45a3-bfd3-b9c60e0f5d3a)

Furthermore, this application isn't just about identifying food and its nutrients; it's also a tool for tracking dietary habits over time. This feature is particularly beneficial for those who are mindful of their eating patterns and wish to maintain a healthy lifestyle. The objective of CaloSnap is to support users in their journey toward better health and wellness, emphasizing the importance of informed food choices.

The project's motto, "Snap, Track, Thrive," captures its essence. It's more than just an app; it's a health companion that fits right into the user's pocket, making health management accessible, engaging, and straightforward. CaloSnap is not just a tool, but a health ally, epitomized by its catchy and meaningful motto: "Your health, one photo at a time."

## Architecture Diagram

![Architecture Diagram](https://github.com/AryAgain/ImageEncoderSimulator/assets/5464475/b18c37c0-d9bd-4a9b-a5e4-279bb00e981a)

## Detailed Description of AWS Technologies Used

- **Amplify**: This service lets us add user sign-up, sign-in, and access control to our web or mobile applications. This is used to deploy the frontend in our project.
- **Amazon Cognito**: This is used to store user profiles and handle user authentication.
- **Amazon S3**: This is an object storage service used to store food images for machine learning model training.
- **Amazon Rekognition**: This service makes it easy to add image and video analysis to applications. This is used to identify uploaded food items.
- **AWS API Gateway**: A fully managed service for creating, publishing, maintaining, monitoring, and securing REST, HTTP APIs. This is used to provide a communication layer between the frontend and backend.
- **AWS Lambda**: A serverless, event-driven compute service used to implement the serverless backend logic.
- **Amazon DynamoDB**: A fully managed, serverless, key-value NoSQL database used to store historical and nutritional data.
- **Cloudwatch**: A performance monitoring tool for AWS services, used to view logs and debugging.
- **Terraform**: An infrastructure as code tool to automatically spin up and manage infrastructure for our application.

## Breakdown of AWS Costs estimation

| Upfront Cost | Monthly Cost | Total 12 Months Cost |
|--------------|--------------|----------------------|
| $180.00      | $5820        | $70,023.60           |


### Lessons Learned

1. If had more time, would like to incorporate features such as the identification of multiple food items in a single image, personalized dietary and workout recommendations, or further enhancing the user interface to provide more value to the user.
2. Would also try to work with Terraform from the beginning to avoid complications when writing it later.
3. Designing the app architecture as microservices, to deploy as containers, would have made the app design more resilient and scalable.
4. A big lesson we learned is that scalable machine learning in the cloud is difficult and costly.

### Why is the Cloud Better for this Project?

- For a B2C project with significant scaling potential, the cloud allows our application to scale seamlessly.
- Using Lambdas allows us to pay only for use instead of having a server constantly running, making the deployment cost-effective.
- AWS Rekognition made it very easy to integrate machine learning into our project.
- Using managed services decreased the overall development time and effort.
- Using serverless services made the deployment cost less and future-proof for rapid scalability.
- More focus can be done on development rather than managing servers due to cloud services.
- Data corresponding to users and their activities will be stored securely in the cloud.

### Challenges with AWS Technologies

- Initially, training a model locally and uploading it to an S3 bucket to access via Lambda was not feasible as loading the model into Lambda took more than 10 minutes.
- The Custom Labels Rekognition model is difficult to share with other AWS users and requires a complex "Copy" command.
- Terraform support with AWS Amplify and Cognito is very new, so documentation and online resources are limited.


![Analysis chart](https://github.com/AryAgain/ImageEncoderSimulator/assets/5464475/15b2db7b-6680-48ac-b224-597c012bf945)

### Future Enhancements

In future, several features would be prioritized for development:
- Expansion of the food database to recognize more than 30 food items.
- Enhancing the app for full mobile device compatibility.
- Incorporating personalized dietary and workout recommendations based on user data.
- Enabling the identification of multiple food items in a single image.
- Sending notifications to users through AWS SNS based on their history, recommending workouts or dietary changes.

These enhancements would improve the user experience and increase the app's effectiveness in assisting users with their dietary management.
