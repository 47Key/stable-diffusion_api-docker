# Docker Container for a Flask App that Communicates with the Stability AI Image Generation API (DreamStudio)

* This app will generate an image based upon the prompt you provide it, and return a JSON object with a base64 encoded image, meant to be queried as an API
* The prompt is accessed by the following url query
    * /prompt/?prompt=YOUR_PROMPT_HERE
    * you will have to URI encode the prompt from your front-end
* In theory the returned Image can be used in a html image tag, like this: <img src=`data:image/png;base64, ${json.image}` />

* Please report any issues you have, and submit a pull request if you have a better way.

## To Get Started

* Build the docker image
    * move to the root folder and run "docker build -t my-stable-diffusion_app:latest ."
* Run the docker image
    * run the command "docker run -d -p 5000:5000 my-stable-diffusion_app:latest"
* Test the container locally before deployment, navigate to "localhost:5000" after running it to make sure everything works, and follow the prompt command above
* You will need somewhere to deploy the docker container, AWS Lightsail is a beginner friendly option for this
