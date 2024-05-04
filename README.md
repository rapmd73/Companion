# Companion

** WORK IN PROGRESS **

## Introduction

Introducing Companion, a versatile program empowering users to create personalized personas for Discord
servers. Beyond its persona-building capabilities, Companion also offers limited moderation functionality
and promises ongoing expansion and enhancement.

Designed to foster engaging interactions within Discord communities, Companion allows users to craft
personas tailored to their preferences and server dynamics. Whether users seek to inject humor, guidance, or
whimsy into their servers, Companion provides the tools to bring their visions to life.

In addition to its persona-building features, Companion serves as a reliable moderator, assisting server
administrators in maintaining order and fostering positive environments. With ongoing development efforts,
Companion evolves to meet the evolving needs of Discord communities, promising continuous expansion and
improvement over time.

If you find this software useful, please give it a star and consider sponsoring it to support its ongoing
development and enhancement.

## Companion

This is the actual discord bot. This section will go through the installation and setup process.

### Requirements

This software requires a VPS with with a minimum of 1 core (2 cores is heavily recomended), 1 gig of RAM (4 recomended), 2 gigs of swap, 40 gigs of SSD storage. This software was developed for the intention of using a VPS to its fullest extent. If you wish to use a virtual environment, please consult your VPS documentation.

Jackrabbit Relay requires Python 3 (version 3.8.10) and pip3. If you do not have pip3, the below link will show you how to install it.

    https://www.linuxscrew.com/install-pip

The command for installation really is very simple and here is the short
version. please be sure you are in route or in your virtual environment
appropriate to the documentation of your VPS. the below command is for
Ubuntu.you will need to use the package manager appropriate to your VPS.

```bash
    apt install python3-pip
```

### Installing and setting up

Start with these shell commands

```bash
mkdir -p /home/GitHub
cd /home/GitHub
git clone https://github.com/rapmd73/Companion
```

You now have a copy of the Companion repository. Now its time to install everything.

```bash
cd /home/GitHub/Companion
./install
```

### Files

#### /home/Companion

- **Personas** This is where the various personas (personalities) are kept.
- **Companion** Main program
- **Companion.cfg** JSON file of the channel name (text only) and the persona for that channel. Each channel can have its own persona or can share a persona.
- **Companion.tokens** This file doesn't exist until YOU create it. The first line of the file is the Discord token. The second line of the file is the OpenAI API key. Just these two lines ONLY, exactly as each service provides them.
- **install** The inataller that create the /home/Companion folder
- **requirements.txt** The pip3 requirements that will load the neccessry packages.
- **README.md** This file.
- **CODE_OF_CONDUCT.md** GitHub required files.
- CONTRIBUTING.md
- dependabot.yml
- lgpl-2.1.txt
- LICENSE-lgpl
- SECURITY.md

#### /home/Companion/Personas

- **Marcus** The stoic mentor/teacher modelled after Marcus Aurelius. This persona is meant to demonstrate how a historical figure to bew brought to "life".
- **Mugsy** This is a play of the ganster characters from Bug Bunny cartoons or Rockey the mobster, or Dick Dastardly. It is kept is the same light hwearted humor.
- **Tipsy** This is the playful side of AI. Completely whimsical at all times and makes for a really nice addition to any server.

#### /home/Companion/Personas/Tipsy

- **Tipsy.broke** A list on responses where one will be given to the user is the OpenAI API doesn't respond. The more the better and one response per line. Responses should be in-line with the persona you are creating.
- **Tipsy.cfg** Configuration settings, like how much to remember, for this persona.
- **Tipsy.persona** The actual persona of the character you are creating. Consists os a system role that define the personality amd multiple user/assissant line the refine/shape the persona with mock questions/responses.
- **Tipsy.png** Any PNG allowed by the Discord TOS. This one was created by an AI generator.
- **Tipsy.vulgarity** A list of responses when the user uses vulgarities, one per line and the more responses the better.

#### /home/Companion/Personas/Marcus

- **Marcus.broke** These files are the same meaning as **Tipsy**
- Marcus.cfg
- Marcus.persona
- Marcus.png
- Marcus.vulgarity

#### /home/Companion/Personas/Mugsy

- **Mugsy.broke** These files are the same meaning as **Tipsy**
- Mugsy.cfg
- Mugsy.persona
- Mugsy.png
- Mugsy.vulgarity

### Configuring

Configuring Companion is technically easy. Lets start with the personas. These are what define the
personalities of your bot. Each channel can have its own personality. We will use Tipsy as the blueprint for
this demonstration. Each persona has its own folder to keep things easily organized.

We'll start with Tipsy.cfg:

```JSON
{ 
    "Model":"gpt-3.5-turbo",
    "FreqPenality":2,
    "Temperature":1,
    "DeveloperUID":123456789, 
    "MaxMemory":50 
}
```

Above is an example of the config file for this persona. Here is a table that explains each item.

| Item | Example | Description |
| :--  | :-: | :-- |
| Model | gpt-3.5-turbo | This is the supported model that OpenAI allows. If you use Ollama, GPT4ALL, or similar, it will match your AI engine. |
| FreqPenality | 2 | You can pick a number between -2.0 and 2.0 when you use the OpenAI API. If you choose a positive number, it means the system will penalize repeating the same words too often. This helps make the responses more varied and avoids repeating the same lines over and over again. |
| Temperature | 1 |Choose a sampling temperature between 0 and 2. If you go for a higher number like 0.8, the output will be more random. But if you pick a lower number like 0.2, the output will be more focused and predictable. |
| DeveloperUID | 123456789 | The developer, YOU. This is just a cutezy way for the bot to know if you that it is talking to. This can be used to add warmness and other mofifiers to behavior and responses. Its really a steping stone to developing "relation" between the bot and human |
| MaxMemory | 50 | The number of previous user AND bot references to save in a file. Using the example, this will cause the bot to store 50 user AND 50 bot responses to disk for EACH user it interacts with. |

## Open AI

Be sure you read and understand the terms and services and acceptable use.

Obtaining an API:

1. **Visit OpenAI's Website**: Go to the [OpenAI website](https://openai.com). Direct link to the [API page](https://platform.openai.com/api-keys).

1. **Explore the API**: Learn about the available APIs and their capabilities. OpenAI offers several APIs, including GPT (text generation), DALL-E (image generation), and CLIP (image understanding). Choose the one that fits your needs.

1. **Sign Up or Log In**: If you already have an account, log in. Otherwise, sign up for an account using your email address and other required information.

1. **Navigate to the API Section**: Once logged in, navigate to the API section of the website. This is where you can access documentation, pricing information, and manage your API keys.

1. **Read the Documentation**: Familiarize yourself with the documentation for the API you're interested in. This will provide information on how to use the API, including endpoints, parameters, and examples.

1. **Choose a Plan**: OpenAI offers different plans depending on your usage and needs. Choose a plan that suits your requirements and budget. Some plans may offer free access up to a certain limit, while others require payment.

1. **Get API Key**: Once you've chosen a plan, you'll need to generate an API key. This key is what you'll use to authenticate your requests to the API. Follow the instructions provided to generate your API key.

1. **Keep Your API Key Secure**: Treat your API key like a password and keep it secure. Don't share it publicly or expose it in your code.

1. **Integrate the API**: Now that you have your API key, you can start integrating the API into your projects. Follow the documentation and use your API key to make requests to the API endpoints.

1. **Test Your Integration**: Before deploying your application, make sure to thoroughly test your integration with the API to ensure everything is working as expected.

1. **Monitor Usage**: Keep an eye on your API usage to ensure you stay within any usage limits imposed by your chosen plan. You can usually monitor usage through your OpenAI account dashboard.

1. **Scale as Needed**: As your needs grow, you can consider upgrading your plan or adjusting your usage to fit within the constraints of your current plan.

That's it! You should now have access to the OpenAI API and be able to start using it in your projects. If you have any specific questions or run into any issues along the way, feel free to ask!

## Discord

Be sure you read and understand the terms and services and acceptable use.

This bot *requires* **administrator** priviledges for changing the avatar and nickname.

Sure, here's a step-by-step guide to setting up a Discord bot on the Discord Developer Portal:

1. **Create a Discord Account:**
   If you don't have one already, create a [Discord account]([https://discord.com/register).

1. **Access the Developer Portal:**
   Go to the [Discord Developer Portal](https://discord.com/developers/applications).

1. **Create a New Application:**
   Click on the "New Application" button in the top-right corner.

1. **Name Your Application:**
   Give your application a name. This will be the name of your bot.

1. **Create Your Bot User:**
   After creating the application, navigate to the "Bot" tab on the left sidebar and click on "Add Bot."

1. **Customize Your Bot:**
   You can customize your bot's username and profile picture on this page.

1. **Copy Token:**
   Under the "Token" section, click on "Copy" to copy your bot's token. This token is essential for your bot's authentication and should be kept private.

1. **Add Your Bot to a Server:**
   Still in the Developer Portal, navigate to the "OAuth2" tab on the left sidebar. Under "OAuth2 URL Generator," select the scopes and permissions your bot will need. At the bottom, you'll find a URL. Copy this URL and paste it into your browser. From there, you can choose which server to add your bot to.

1. **Authorize the Bot:**
   After selecting the server, click "Authorize." This will add your bot to the selected server.

1. **Bot Configuration:**
    Now that your bot is in your server, you can configure it further using Discord API documentation or by coding it.

1. **Write Code for Your Bot:**
    You can use libraries like discord.py (for Python) or discord.js (for JavaScript) to write code for your bot. This code will define the bot's behavior and interactions with users.

1. **Run Your Bot:**
    Once you've written your bot's code, run it on your local machine or deploy it to a server. Make sure to paste your bot's token into your code for authentication.

1. **Test Your Bot:**
    Test your bot's functionality on Discord by interacting with it in the server where you added it.

That's it! You've successfully set up a Discord bot on the Discord Developer Portal.

