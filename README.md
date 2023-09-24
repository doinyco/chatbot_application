# Chatbot Application

Welcome to the Chatbot application! This application provides a simple web-based chat interface that interacts with the OpenAI GPT-3.5 model to generate responses to user messages.

## Table of Contents

- [Introduction](#introduction)
- [Getting Started](#getting-started)
- [Application Structure](#application-structure)
- [Usage](#usage)
- [Configuration](#configuration)
- [DEMO](https://www.youtube.com/watch?v=GIxmI2cO_YU)

## Introduction

The Chatbot application is designed to facilitate conversations between users and an AI-powered chatbot. This chatbot leverages the capabilities of the OpenAI GPT-3.5 model to generate responses based on user input.

## Getting Started

To get started with the Chatbot application, follow these steps:

1. **Clone the Repository:** Clone this repository to your local machine using the following command:
   ```shell```
     git clone <repository-url>


2. **Open the Project:** Open the project in your preferred development environment.

3. **Configure the API Key:** Replace `"API-KEY"` in the `SendMessage` method with your OpenAI API key. Obtain an API key by signing up on the [OpenAI website](https://beta.openai.com/signup/).

4. **Build and Run:** Build and run the application.

## Application Structure

The Chatbot application is built using Blazor and consists of the following main components:

- `Index.razor`: The main page displaying the chat interface.
- `SendMessage`: Method for sending user messages to the OpenAI GPT-3.5 model.
- `OnInitializedAsync`: Overridden method for initialization tasks.
- `message`: Represents the user's input message.
- `messages`: A list for storing chat messages.
- `HttpClient Http`: Used for making API requests to OpenAI.
- API Call to OpenAI: Sends a POST request to `https://api.openai.com/v1/completions` to interact with the GPT-3.5 model and retrieve responses.

## Usage

To use the Chatbot application:

1. Open the application in a web browser.

2. Type a message in the input field and click the "Send" button.

3. The application sends your message to the OpenAI GPT-3.5 model, and the generated response appears in the chat interface.

4. Continue the conversation by typing more messages and clicking "Send."

## Configuration

### API Key Configuration

To configure your OpenAI API key:

1. Replace `"API-KEY"` in the `SendMessage` method with your actual OpenAI API key:

```csharp
var apiKey = "YOUR-API-KEY";
Http.DefaultRequestHeaders.Add("Authorization", $"Bearer {apiKey}");
