# Install

`npm install`

---

# Things to add

- Create a `.env` file in config folder and add the following as `key = value`
  - PORT = 2121 (can be any port example: 3000)
  - DB_STRING = `your database URI`
  - CLOUD_NAME = `your cloudinary cloud name`
  - CLOUD_API_KEY = `your cloudinary api key`
  - CLOUD_API_SECRET = `your cloudinary api secret`
  - MS_COMPUTER_VISION_SUBSCRIPTION_KEY = `MS Azure computer vision sub key`
  - MS_COMPUTER_VISION_ENDPOINT = `MS Azure computer vision sub key`

---

# Why does this exist?
This is a project meant to demonstrate the use of Microsoft Azure's cognitive services API. There are a number of interesting APIs available that offer trained machine learning models for consumer use; this particular app uses the "computer vision" services to analyze uploaded images.

## How It's Made:

**Tech used:** HTML, CSS, JavaScript, Express, Node, Tailwind, EJS, Cloudinary, Microsoft Azure Cognitive Services API

This is a simple app. The user uploads an image to Cloudinary. Cloudinary returns both the image itself to the user (via EJS) and a URL (to the backend). The URL is fed to the Azure Cognitive Services API, which allows the API to analyze the contents of the image.

## Lessons Learned:


 
## Optimizations:

The app itself is simple and doesn't necessarily have any elements to be optimized. I think the concept can be optimized based on specific use cases: ex: I work for a sneaker company that allows users to upload images for reivews. This technology can be used to identify if the user is uploading images that contain sneakers.

It should also be noted that the machine learning models are not perfect and have room to improve. For example, if I upload an image of a water bottle, the first result is usually quite generic (ex: "beverage") - not incorrect, but not really what I'm looking for. There are ways to address this via the code (usually the second result is more accurate (ex: "bottled water")), but this should also improve moving forward as the models are further trained.
