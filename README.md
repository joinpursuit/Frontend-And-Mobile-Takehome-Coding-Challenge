[![Pursuit Logo](https://avatars1.githubusercontent.com/u/5825944?s=200&v=4)](https://pursuit.org)

# Frontend-And-Mobile-Takehome-Coding-Challenge

Coding challenge where you build a Raffle App client that interact with a RESTful API using React (Web) or Using Swift (Mobile)

## Prerequisites

### Web

- A [Codesandbox](https://codesandbox.io/) account
- Knowledge or JavaScript and React

### Mobile

- Xcode installed
- Knowledge of Swift

## Getting Started

### Web

1. In Codesandbox create a blank React App.
   - If you don't know how to create a React App in Codesandbox, read [this tutorial](https://react.school/hello-react)

### Mobile

1. Create a new Swift Xcode Project for your app.

### All

- Complete your client application according to the Technical requirements below.

## Technical Requirements

Create a client for a Raffle application. Users are able to:

- Create raffles
- List all raffles
- Add participants users to raffles
- Draw a winner from a raffle, etc.

**Notes**:

- You may use any 3rd-party libraries or packages for functionality or styling.
  - **Web** We recommend you use something like Bootstrap or Material UI or others to style you app.
  - **Mobile** You must write your networking layer natively, do not use Alamofire or equivalents for Network Requests.

### API

Use the details and endpoints of the API below to accomplish the Raffle App functionality. This API accepts and returns JSON payloads.

**Root Endpoint**: `https://raffle-fs-app.herokuapp.com`

| Method | Endpoint                        | Description                                                | Example JSON Body Payload                                                                              |
| ------ | ------------------------------- | ---------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| `GET`  | `/api/raffles`                  | List all raffles                                           | n/a                                                                                                    |
| `POST` | `/api/raffles`                  | Create a raffle                                            | `{ "name": "My first Raffle", "secret_token": "s3CrE7" }`                                              |
| `GET`  | `/api/raffles/:id`              | Retrieve a raffle by id                                    | n/a                                                                                                    |
| `GET`  | `/api/raffles/:id/participants` | Retrieve all participants of a raffle                      | n/a                                                                                                    |
| `POST` | `/api/raffles/:id/participants` | Sign up a participants for a raffle                        | `{ "firstname": "Jane", "lastname": "Doe", "email": "jdoe@email.com", "phone": "+1 (917) 555-1234", }` |
| `PUT`  | `/api/raffles/:id/winner`       | Pick a winner from the participants at random for a raffle | `{ "secret_token": "s3CrE7" }`                                                                         |

#### Notes

- A `secret_token` must be provided when creating a raffle. This token can be any random string and will be used when picking a winner for the raffle. Only if the creation token matches the one in the PUT request to pick a winner the raffle will be performed and a winner will be awarded.
- When adding a participant to a raffle all fields are required but `phone`

### Wireframes

Your application doesn't have to look exactly as the wireframes below, however it should have all the main components, accomplish all the functionality and be visually pleasing.

- Web Wireframes can be found [here](./Web-Raffle-App-Wireframes.pdf)
- Mobile Wireframes can be found [here](./Mobile-Raffle-App-Wireframes.pdf)

### App Pages/Views

Your Raffle App should have the following pages or views (mobile) (and be displayed at their respective browser url [Web only]).

#### Home `/`

Display a form to add a new raffle with name and token fields and a submit button. Show a success message upon successful raffle creation and an error message otherwise.

Should also display a list of all raffles and when you click in one of the raffles of the list it should take the user to that raffle's page/view.

#### Single Raffle `/raffles/:id`

Displays a nav bar or navigation menu that would take the user to **All Raffles**, **Participants** and **Pick Winner** pages/views.

Below the navbar display a form to add a new participant to the Raffle. The form must include First Name, Last Name, Email and Phone inputs. The phone input should be optional and all others required. Include two buttons one to submit and another to reset the form.

#### Raffle Participants `/raffles/:id/participants`

Display the total number of participants and a list of all users and their information.

#### Pick Winner `/raffles/:id/winner`

Displays a form where a user (the raffle admin) can input their secret token and pick a winner at random for the raffle. If a winner has already been picked this page/view should display a card with the user information and a celebratory image and never show the form again.

## Submission Guidelines

- We think this challenge would take ~7 hours to complete, so allocate your time appropriately.
- You must submit your solution no later than **Monday, May 31st at 11:59pm.**
- Submit the link to your app code using the [submission form](https://docs.google.com/forms/d/e/1FAIpQLSeY0nBqtXTV06b2CmAreHLJzVHlG0cQHUx9g1RKPYer0hNVVQ/viewform?usp=sf_link)
  - **Web** Link to your React App code in codesandbox
  - **Mobile** Link to your App's GitHub repo
- For any questions reach out to @Alejo in the [Pursuit Core Workspace](https://pursuit-core.slack.com/)

## Resources

- [React App in Codesandbox tutorial](https://react.school/hello-react)
