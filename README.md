[![Pursuit Logo](https://avatars1.githubusercontent.com/u/5825944?s=200&v=4)](https://pursuit.org)

# Web-Frontend-Takehome-Coding-Challenge

Front-End coding challenge where you build a Raffle App with React and interact with a RESTful API.

## Prerequisites

- A [Codesandbox](https://codesandbox.io/) account
- Knowledge or JavaScript and React

## Getting Started

1. In Codesandbox create a blank React App.
   - If you don't know how to create a React App in Codesandbox, read [this tutorial](https://react.school/hello-react)
2. Complete your application server according to the Technical requirements below.
3. You may use any 3rd-party libraries for functionality or styling.

## Technical Requirements

Create a Front-end application for a Raffle application. Users are able to:

- Create raffles
- List all raffles
- Add participants users to raffles
- Draw a winner from a raffle, etc.

### API

Use the details and endpoints of the API below to accomplish the Raffle App functionality

**Root Endpoint**: `https://raffle-fs-app.herokuapp.com`

| Method | Endpoint                        | Description                                                |
| ------ | ------------------------------- | ---------------------------------------------------------- |
| `GET`  | `/api/raffles`                  | List all raffles                                           |
| `GET`  | `/api/raffles/:id`              | Retrieve a raffle by id                                    |
| `GET`  | `/api/raffles/:id/participants` | Retrieve all participants of a raffle                      |
| `POST` | `/api/raffles/:id/participants` | Sign up a participants for a raffle                        |
| `PUT`  | `/api/raffles/:id/winner`       | Pick a winner from the participants at random for a raffle |


### Wireframes

Wireframes can be found [here](./Raffle-App-Wireframes.pdf)

### App Pages

Your Raffle App should have the following pages and be displayed at their respective browser url.


#### Home Page `/`

Display a form to add a new raffle with name and token fields and submit button. Show a success messages upon successful raffle creation and an error message otherwise.

Should also display a list of all raffles and when you click in one of the raffles of the list it should take the user to that raffle's page.

#### Single Raffle Page `/raffles/:id`

Displays a nav bar with links to **All Raffles**, **Participants** and **Pick Winner**

Below the navbar display a form to add a new participant to the Raffle. The form must include First Name, Last Name, Email and Phone inputs. The phone input should be optional and all others required. Include two buttons one to submit and another to reset the form.

#### Raffle Participants Page `/raffles/:id/participants`

Displays a list of all users and their information.

#### Pick Winner Page `/raffles/:id/winner`

Displays a form where a user (the raffle admin) can input their secret token and pick a winner at random for the raffle. If a winner has already been picked this page should display a card with the user information and a celebratory image and never show the form again.

## Submission Guidelines

- You should take no more than 5 hours on this challenge.
- Submit the link to your React App code in codesandbox using the [submission form](https://docs.google.com/forms/d/e/1FAIpQLSeY0nBqtXTV06b2CmAreHLJzVHlG0cQHUx9g1RKPYer0hNVVQ/viewform?usp=sf_link)
- For any questions reach out to @Alejo in the [Pursuit Core Workspace](https://pursuit-core.slack.com/)

## Resources

- [React App in Codesandbox tutorial](https://react.school/hello-react)
