# CVAT-Home-Depot
To semantically segment objects shown in the so called “buyers guide” videos for Home Depot. You are to segment the objects that their customers can purchase in their stores.

## UBUNTU
When Ubuntu is to used by the system, it will ask for the password and will then let me into ubuntu. After this authentication process, we open the ubuntu terminal to proceed with the installation of Docker and CVAT.  

![Image 1](https://user-images.githubusercontent.com/115740214/198404898-a9650de3-d894-406c-b474-1768e4c93656.png)

![Image 2](https://user-images.githubusercontent.com/115740214/198405282-9402a1cb-fee1-4ab2-aa09-eae20cad5884.png)

## LIST OF THE INSTRUCTIONS REQUIRED FOR THE INSTALLATION OF DOCKER AND CVAT

## •	To run the commands mentioned below so as to complete the installation of Docker and CVAT.

## Step 1: sudo apt-get update

## Step 2: sudo apt-get install -y \
##         apt-transport-https \
##         ca-certificates \
##         curl \
##         gnupg-agent \
##         software-properties-common

![Image 3](https://user-images.githubusercontent.com/115740214/198405310-8b64891f-2365-4b16-b00b-05086a481150.png)

![Image 4](https://user-images.githubusercontent.com/115740214/198405327-268c491a-8efb-4e66-8c67-3a91af731ab0.png)


## Step 3: curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo    apt-key add –

## Step 4: sudo add-apt-repository \
##         "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
##         $(lsb_release -cs) \
##         stable"


![Image 5](https://user-images.githubusercontent.com/115740214/198405337-360884f6-8a66-4878-8de4-38a3a34bd6a6.png)

## Step 5: sudo apt-get update

## Step 6: sudo apt-get install -y docker-ce docker-ce-cli containerd.io


![Image 6](https://user-images.githubusercontent.com/115740214/198405353-f1d38ddd-76b1-47e3-a35b-145bf84d5d37.png)

![Image 7](https://user-images.githubusercontent.com/115740214/198405360-a41c0d2f-ab5a-4038-89a0-cc992e5679d6.png)

![Image 8](https://user-images.githubusercontent.com/115740214/198405372-13e1be41-5b2b-48cd-9961-54755f9ddaad.png)


## Step 7: sudo groupadd docker

## Step 8: sudo usermod -aG docker $USER

## Step 9: sudo apt-get install -y python3-pip


![Image 9](https://user-images.githubusercontent.com/115740214/198405389-0741ac6c-1eb9-41dd-96cd-7b9e027d3989.png)

![Image 10](https://user-images.githubusercontent.com/115740214/198405409-4e5b905e-0ef8-4388-a1c1-6c0abd712300.png)

![Image 11](https://user-images.githubusercontent.com/115740214/198405425-68ae7111-59aa-43e1-a5d9-8508aa9c1a0e.png)

![Image 12](https://user-images.githubusercontent.com/115740214/198405437-db45776a-c8c8-4f67-90d9-b260def8e800.png)

![Image 13](https://user-images.githubusercontent.com/115740214/198405461-c7befd14-4f3e-473b-8c38-c444f2bb20fb.png)

![Image 14](https://user-images.githubusercontent.com/115740214/198405475-994ba631-e034-4e65-8a0d-7f13040c41d9.png)

![Image 15](https://user-images.githubusercontent.com/115740214/198405496-fcf2e285-cf11-4d3a-a78c-3f8323368d3d.png)

![Image 16](https://user-images.githubusercontent.com/115740214/198405513-1e23fe0c-85d2-4e07-abd9-1dd3504316e9.png)

![Image 17](https://user-images.githubusercontent.com/115740214/198405526-1bf19b90-d723-4a58-83d5-2c917f79592c.png)

![Image 18](https://user-images.githubusercontent.com/115740214/198405541-c898662c-d5d2-4401-b9dd-9fb2ec028fc1.png)

![Image 19](https://user-images.githubusercontent.com/115740214/198405566-3e62b60c-8a64-4966-9314-e5b3ace3a2a0.png)

![Image 20](https://user-images.githubusercontent.com/115740214/198405587-715196a6-8908-4fae-a1e4-65a9607fe0e7.png)

![Image 21](https://user-images.githubusercontent.com/115740214/198405604-6104ec50-6407-4662-9231-def5a7a02886.png)


## Step 10: sudo pip3 install docker-compose


![Image 22](https://user-images.githubusercontent.com/115740214/198405617-7faeefee-7a81-48f6-a937-ebae4341f57f.png)

![Image 23](https://user-images.githubusercontent.com/115740214/198405633-96e485af-34a1-4edb-a80b-6a2f3985ae32.png)

![Image 24](https://user-images.githubusercontent.com/115740214/198405655-dbc755c8-6ce2-42c0-92dd-5df63c0cb083.png)


## Step 11: sudo apt-get install -y git

## Step 12: git clone https://github.com/opencv/cvat


![Image 25](https://user-images.githubusercontent.com/115740214/198405663-8d57bb56-e503-48c0-8bea-85730f8f6f82.png)

## Step 13: cd cvat

![Image 26](https://user-images.githubusercontent.com/115740214/198405681-e95b2782-d668-4182-b41e-5cbd0c2783a4.png)


## Step 14: docker-compose build

## Step 15: docker-compose up -d


![Image 27](https://user-images.githubusercontent.com/115740214/198405704-c6a87d9b-4cd7-48ed-a52b-5cb166224779.png)

![Image 28](https://user-images.githubusercontent.com/115740214/198405721-c18188be-0dd5-4c9b-a521-f33c986c95d4.png)

![Image 29](https://user-images.githubusercontent.com/115740214/198405746-2b7a7f7e-ebbe-4305-be76-fc605dc4ac61.png)

![Image 30](https://user-images.githubusercontent.com/115740214/198405761-918e1cb9-8896-4c87-b9f9-47bb5748b90b.png)


## Step 16: sudo docker exec -it cvat_server bash -ic 'python3 ~/manage.py createsuperuser'

![Image 31](https://user-images.githubusercontent.com/115740214/198405781-6a31836e-692f-4982-864e-555411dbd265.png)


## Step 17: wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add –

## Step 18: sudo sh -c 'echo "deb [arch=amd64]    http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'

## Step 19: sudo apt-get update

## Step 20: sudo apt-get install -y google-chrome-stable


![Image 32](https://user-images.githubusercontent.com/115740214/198405800-4316c83b-24d1-4915-8f9a-fbba31bccc15.png)

![Image 33](https://user-images.githubusercontent.com/115740214/198405820-3e4f682e-cc18-4aae-a8c8-f49cfe0a404c.png)


## •	Google Chrome is successfully installed. Once google chrome is installed in ubuntu, go to localhost:8080.
## •	A login window pops up where in we have to mention our username/email address and our password which have entered in Step 16. In step 16, we create a user while entering our username, email id and password. Once the correct credentials are entered, press the Sign in button. This leads to the Computer Vision Annotation Tool (CVAT) tab. 
## •	CVAT is a free, open source, web-based image and video annotation tool which is used for labeling data for computer vision algorithms. CVAT is designed for use by a professional data annotation team, with a user interface optimized for computer vision annotation tasks. 


![Image 34](https://user-images.githubusercontent.com/115740214/198405842-8aff08b3-1010-4aed-b7d3-0c78c8242348.png)

![Image 35](https://user-images.githubusercontent.com/115740214/198405856-819fa0ae-15ee-4e14-9fd0-6654a418a809.png)


## CONCLUSION:
Docker and CVAT have been successfully installed on the Ubuntu 18.04 terminal
