![StoryEchoes Logo](/assets/logo.png)

# StoryEchoes - Echo your imagination, one story at a time.

## Description

Create personalized storybooks effortlessly! Combine images, voice-to-text recordings, and narration to craft engaging books. Kids can read, listen to narrations, or revisit their favorites using bookmarks. Edit and enhance your creations anytime!
This project provides backend to the below project.</br>
https://github.com/priya337/StoryEchoes


## How to setup the project

- Git clone the below project</br>
https://github.com/priya337/StoryEchoes

- run "npm i" to install the packages

- run "npm run dev"

## How to run the project

- This backend is deployed on Vercel with below domain.</br>
_(https://github.com/nehais/StoryEchoes-backend)_

- The frontend using this project is deployed on Netlify.</br>
_(https://storyechoes.netlify.app/)_

# APIs
The mock API is powered by json-server and uses the db.json file to simulate a backend. Below are the API details:

1. Get All Stories<br/>
**Endpoint**: {DOMAIN}/stories<br/>
**Method**: GET<br/>
**Response JSON**:<br/>
[
  {
    "id": "1",
    "title": "Nibbles and the Perfect Hat",
    "imageforstorytile": "./src/assets/Story1images/imageforstorytile.jpg",
    "description": "Follow Nibbles the garden gnome as he embarks on an adventure to find the perfect hat fit."
  },
  ...
]

2. Get Single Story<br/>
**Endpoint**: {DOMAIN}/stories/:id<br/>
**Method**: GET<br/>
**Response JSON**:<br/>
{
  "id": "1",
  "title": "Nibbles and the Perfect Hat",
  "front_cover": "/path_to_image/front_cover.jpg",
  "back_cover": "/path_to_image/back_cover.jpg",
  "content": [
    {
      "page": 1,
      "text": "Nibbles the garden gnome loved his hat...",
      "image": "/path_to_image/Story1images/page1.jpg"
    },
    ...
  ]
}

3. Add a New Story. Here the id for the new books is assigned by the json server. <br/>
**Endpoint**: {DOMAIN}/stories<br/>
**Method**: POST<br/>
**Request JSON**:<br/>
{
  "id": "3",
  "title": "A New Adventure",
  "description": "An amazing new story for young readers.",
  "front_cover": "/path_to_image/front_cover.jpg",
  "back_cover": "/path_to_image/back_cover.jpg",
  "content": [
    {
      "page": 1,
      "text": "This is the first page of the new adventure.",
      "image": "/path_to_image/page1.jpg"
    },
    {
      "page": 2,
      "text": "This is the second page of the new adventure.",
      "image": "/path_to_image/page2.jpg"
    }
  ]
}<br/>
**Response JSON**:<br/>
{
  "id": "3",
  "title": "A New Adventure",
  "description": "An amazing new story for young readers.",
  "front_cover": "/path_to_image/front_cover.jpg",
  "back_cover": "/path_to_image/back_cover.jpg",
  "content": [
    {
      "page": 1,
      "text": "This is the first page of the new adventure.",
      "image": "/path_to_image/page1.jpg"
    },
    {
      "page": 2,
      "text": "This is the second page of the new adventure.",
      "image": "/path_to_image/page2.jpg"
    }
  ]
}

4. Get All Users<br/>
**Endpoint**: {DOMAIN}/users<br/>
**Method**: GET<br/>
**Response JSON**:<br/>
[
  {
    "id": 1,
    "user": "polly",
    "bookIds": [
        "fd2a",
        "d807",
        "fd2e",
        "fd2b"
      ]
  },
  ...
]

# Please Note : 

As this is a Mock backend ensure port 9001 is free while starting the db json:

json-server --watch db.json --port 9001 


# API Integration: 

Fetches and manages story data dynamically for a mock backend.
