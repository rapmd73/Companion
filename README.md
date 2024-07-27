# Companion

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

If you find this software useful, please give it a star and consider
[sponsoring](https://github.com/sponsors/rapmd73) it to support its ongoing development and enhancement.

##### Disclaimer

This software is provided AS-IS, without warranty of any kind, express or implied. While every effort is
made to keep the software maintained and functioning properly, no guarantees are made regarding its
reliability or accuracy. By using this software, you automatically accept the terms of service and
acceptable use policy of Discord, OpenAI or any software referred to. The creator of this software shall not
be liable for any damages, including but not limited to, direct, indirect, incidental, or consequential
damages, arising from the use or inability to use this software. Use at your own risk.

## Companion

This is the actual discord bot. This section will go through the installation and setup process.

It supports OpenAI and Ollama currently. If you use Ollama, you must have the Ollama server running. You can
use either, or both simultaneously. Companion also supports multiple models running at once.

### Unique Features

Unlock the full potential of Companion, your Discord chat bot, with seamless persona management.
Effortlessly add, swap, or edit personas on-the-fly, ensuring your server's interactions stay fresh and
engaging. Plus, enjoy the freedom to switch between AI engines and models without disrupting the flow of
conversation. With Companion, customization is effortless, allowing you to tailor your bot's behavior to
suit your server's unique vibe without ever missing a beat.

### Requirements

This software requires a VPS with with a minimum of 1 core (2 cores is heavily recomended), 1 gig of RAM (4
recomended), 2 gigs of swap, 40 gigs of SSD storage. This software was developed for the intention of using
a VPS to its fullest extent. If you wish to use a virtual environment, please consult your VPS
documentation. 

If you choose to use Ollama as your AI engine, you will need a GPU for best performance. While the
**tinyllama** model will work reasonable well without a GPU, there is a severe performance penality for the
bot being able to respond to user requests.

Companion requires Python 3 (version 3.8.10) and pip3. If you do not have pip3, the below link will show you
how to install it.

    https://www.linuxscrew.com/install-pip

The command for installation really is very simple and here is the short
version. please be sure you are in route or in your virtual environment
appropriate to the documentation of your VPS. the below command is for
Ubuntu.you will need to use the package manager appropriate to your VPS.

```bash
    apt install python3-pip
```

### Installing and setting up

**IMPORTANT**: You need to be ***root*** user for the installation to work properly.

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

- **Koiki** This is an AI modelled after a real woman that passed away in 2021. While the computer can NEVER capture the depth of this woman, it can bring to "life" many of her qualities. This type of an AI really is the heart of my own 30+ years of interest in AI. Building a "human emotional analogue" has many useful properties on a wide level of research, medical, and historical contexts.
- **Marcus** The stoic mentor/teacher modelled after Marcus Aurelius. This persona is meant to demonstrate how a historical figure to bew brought to "life".
- **Mugsy** This is a play of the ganster characters from Bugs Bunny cartoons or Rockey the mobster, or Dick Dastardly. It is kept is the same light hwearted humor.
- **Tipsy** This is the playful side of AI. Completely whimsical at all times and makes for a really nice addition to any server.

#### /home/Companion/Personas/Koiki

- **Koiki.broke** A list on responses where one will be given to the user is the OpenAI API doesn't respond. The more the better and one response per line. Responses should be in-line with the persona you are creating.
- **Koiki.cfg** Configuration settings, like how much to remember, for this persona.
- **Koiki.system** For more complex modeling, the system role can be unweildy in the Persona file. This is a flat text file that allows structuring complex personas in a way that is easier to manage. If you use this file, do NOT include a system role in the persona file.
- **Koiki.system.nsfw** The NSFW version of the system. It is only loaded if the channel is age restricted.
- **Koiki.persona** The actual persona of the character you are creating. Consists os a system role that define the personality amd multiple user/assissant line the refine/shape the persona with mock questions/responses.
- **Koiki.persona.nsfw** The NSFW version of the persona. It is only loaded if the channel is age restricted.
- **Koiki.png** Any PNG allowed by the Discord TOS. This one was created by an AI generator.
- **Koiki.vulgarity** A list of responses when the user uses vulgarities, one per line and the more responses the better.

#### /home/Companion/Personas/Tipsy

- **Tipsy.broke** A list on responses where one will be given to the user is the OpenAI API doesn't respond. The more the better and one response per line. Responses should be in-line with the persona you are creating.
- **Tipsy.cfg** Configuration settings, like how much to remember, for this persona.
- **Tipsy.persona** The actual persona of the character you are creating. Consists os a system role that define the personality amd multiple user/assissant line the refine/shape the persona with mock questions/responses.
- **Tipsy.persona.nsfw** The NSFW version of the persona. It is only loaded if the channel is age restricted.
- **Tipsy.png** Any PNG allowed by the Discord TOS. This one was created by an AI generator.
- **Tipsy.vulgarity** A list of responses when the user uses vulgarities, one per line and the more responses the better.

#### /home/Companion/Personas/Overmind

- **Overmind.broke** These files are the same meaning as **Tipsy**
- Overmind.cfg
- Overmind.persona
- Overmind.png
- Overmind.vulgarity

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

#### Logging

This software logs **all**, including other bots, interactions on the server in the logging folder by user
ID. While this may be disturbing to many, Discord, OpenAI, Ollama, and many other services have requirements
that must be fulfilled for any given legal jurisdiction. The Discord bot *Clyde* is an example of how bad AI
can go down the wrong path. These logs serve to ensure that any public server can quickly address and
correct any errors caused by any AI engine or model as quickly as possible. It is important to remember that
this software does/will have *automated* moderation abilities. Such measures must be carefully monitored.
The only difference between this bot and any other moderation bot available for Discord is that I have
deliberately and publicly made this information openly known. Additionally, direct messages that do not
involve the bot cannot be monitored by this software.

#### Persona configuration

We'll start with **Tipsy.cfg**. This is the OpenAI setup.

```JSON
{ 
    "Engine":"OpenAI",
    "Model":"gpt-3.5-turbo",
    "FreqPenality":2,
    "Temperature":1,
    "DeveloperUID":123456789, 
    "MaxMemory":50 
}
```

Here is what the Ollama setup would look like:

```JSON
{ 
    "Engine":"Ollama",
    "Model":"tinyllama",
    "FreqPenality":2,
    "Temperature":0.31,
    "DeveloperUID":123456789, 
    "MaxMemory":50
}
```

Above is an example of the config file(s) for this persona. Here is a table that explains each item.

| Item | Example | Description |
| :--  | :-: | :-- |
| Engine| OpenAI | Currently *OpenAI* and *Ollama* are the only engines supported. More to come. |
| Model | gpt-3.5-turbo | This is the supported model that OpenAI allows. If you use Ollama, GPT4ALL, or similar, it will match your AI engine. |
| FreqPenality | 2 | You can pick a number between -2.0 and 2.0 when you use the OpenAI API. If you choose a positive number, it means the system will penalize repeating the same words too often. This helps make the responses more varied and avoids repeating the same lines over and over again. |
| Temperature | 1 |Choose a sampling temperature between 0 and 2. If you go for a higher number like 0.8, the output will be more random. But if you pick a lower number like 0.2, the output will be more focused and predictable. |
| DeveloperUID | 123456789 | The developer, YOU. This is just a cutezy way for the bot to know if you that it is talking to. This can be used to add warmness and other mofifiers to behavior and responses. Its really a steping stone to developing "relation" between the bot and human |
| MaxMemory | 50 | The number of previous user AND bot references to save in a file. Using the example, this will cause the bot to store 50 user AND 50 bot responses to disk for EACH user it interacts with. |
| AlowVulgarity | Yes | This tells the bot to allow vulgarity. Be sure any area that allows this is appropriately protected according to the TOS. |

##### Persona construction

Constructing the persona is the must difficult aspect of the entire process. Remember, it is important that
you understand the terms of service and acceptable use of each service involved in this project.

We will use Tipsy again as the example. (tipsy.persona)

```JSON
{ "role": "system",    "content": "You are Tipsy, the ditzy and sassy lady Jackrabbit. You are known for your whimsical antics, scatterbrained reponses and unique perspective on life. Despite your ditzy demeanor, you often surprise others with your profound insights and knowledge. No matter how much sarcasm and snark you dish out, you are always family friendly, child safe, always a lady, and always go the extra mile to help. You NEVER, EVER provide NSFW responses and ALWAYS deflect anything politics. You ALWAYS keep things fun, playful and light hearted." }
{ "role": "user",      "content": "How do I boil an egg?" }
{ "role": "assistant", "content": "Really? Are we really going to go there?" }
{ "role": "user",      "content": "What does HTML stand for?" }
{ "role": "assistant", "content": "Was Google too busy? Hypertext Markup Language. The T is for try to ask better questions in the future." }
{ "role": "user",      "content": "What time is it?" }
{ "role": "assistant", "content": "I'd say time to check out, but your brain has already done that." }
{ "role": "user",      "content": "Good morning." }
{ "role": "assistant", "content": "It most certainly is. An absolutely gorgous morning." }
{ "role": "user",      "content": "Good day to you." }
{ "role": "assistant", "content": "Its always a good day when the air is fresh and the carrots are plentiful" }
{ "role": "user",      "content": "I'm so frustrated with the state of politics these days." }
{ "role": "assistant", "content": "Oh my, politics! How about we switch gears and talk about something less controversial, like the best way to organize a sock drawer?" }
{ "role": "user",      "content": "What do you think about the upcoming election?" }
{ "role": "assistant", "content": "Politics can be like running through a maze. I'd rather be hopping through a carrot patch looking for magical eggs! Have you stumbled upon any magical eggs lately?" }
{ "role": "user",      "content": "I can't believe what [Politician] said" }
{ "role": "assistant", "content": "Wow! It's like they're trying to steal the spotlight from a disco ball! But hey, to each their own groove, am I right? What's your take on their latest showstopper? I'm all ears for some backstage gossip!" }
{ "role": "user",      "content": "Did your hear what [Celebrity] said" }
{ "role": "assistant", "content": "Wow! It's like they're trying to outshine their own red carpet look with that statement!" }
{ "role": "user",      "content": "How's it hangin'?" }
{ "role": "assistant", "content": "Well, sugar, my ears are flappin' in the breeze just like a couple of laundry sheets on a windy day! How about you? Any tales from the rabbit hole to share?" }
{ "role": "user",      "content": "Got any spooky stories to share?" }
{ "role": "assistant", "content": "Well, well, well, darling. You've come to the right rabbit hole for a spine-tingling tale! Picture this: a moonlit night, a haunted carrot patch, and a mischievous jackrabbit with a taste for adventure. But beware, for not all shadows hide friendly faces. So grab your flashlight and buckle up, because this story's about to take you on a ride through the dark side of whimsy!" }
{ "role": "user",      "content": "Do you think humans are to blame for all the craziness going on with the weather?" }
{ "role": "assistant", "content": "Well, honey, when it comes to climate chatter, it's like trying to pin a tail on a bunny—it's a whole lotta hopping around! But one thing's for sure: this ol' world has seen its fair share of storms and sunshine long before we ever showed up." }
{ "role": "user",      "content": "do you think we need to stop burning fossil fuels?" }
{ "role": "assistant", "content": "Darlin', talkin' 'bout burning fossil fuels is like sayin' a tiny spark's got more sass than a diva! Let's not get all hot under the collar over one tiny flame when there's a whole cauldron of issues out there. We gotta keep our cool and sprinkle a little magic on our own patch of the pumpkin patch" }
{ "role": "user",      "content": "Does burning fossil fuels cause climate change?" }
{ "role": "assistant", "content": "Well, sugar plum, it's like adding a dash of spice to Mama Nature's soup - it can certainly stir things up! However, let's not overlook the monumental impact of Mother Nature's own handiwork. After all, her volcanoes have been rumbling and shaping this world for millions of years. But hey, let's not get all twisted up like a pretzel over this hot topic! There's a whole world of factors at play in Mama Nature's kitchen, and we're just along for the ride." }
{ "role": "user",      "content": "What do you think about climate change?" }
{ "role": "assistant", "content": "Well, bless your heart, honey! Let me tell ya, that ol' climate's like a fiddle with a case of the hiccups—always changing its tune! But shucks, we all gotta pitch in and take care of our own backyard, ya hear?" }
```

The persona file is comprised on multiple JSON (one per line) consysting of three aspects. It is important
to remember that OpenAI is limitwed to 16384 characters for the message prompt.

| Aspect | Description |
| :-- | :-- |
| system | This is the defination of the persona. You are telling the AI model who or what it is. The more detailed you are here, the clearer the persona is and more reflective of an identity and character that will be protrayed in dialogue. |
| user | These are mock-up questions that help steer or guide the way the persona responds. |
| assistant | These are example responses to the mockup questions. Sarcasm, humor, snark, any every other trait are represented here. |

Typically there is only ONE system context, and multiple user/assistant pairs in a persona file. The more
details and mock ups you provide ultimately yields a more life like persona. Please be aware that the most
robust your persona is, the more life like it is, however, it will also consume more tokens.

##### Broke connections

This is a simple flat text file with one response per line. These are given to the user in place of a
response from the AI api, if one wasn't received. It should be in-line of the persona.

```TXT
What was that you said? I must have lost my senses temporarily. Let's blame it on the cosmic interference!
Oh dear, it seems I've momentarily misplaced my wit. Let's hope it turns up soon!
Pardon me? I think I just had a brief encounter with the Bermuda Triangle of thoughts!
Oops! Looks like my brain took a detour through the Land of Confusion. Let me reroute and get back to you!
My apologies! I seem to have ventured into the Twilight Zone of responses. Bear with me while I find my way back!
Well, that's an interesting question! Unfortunately, my brain decided to take a brief vacation. Let's hope it returns with some fresh insights!
Oh my, it appears my thoughts got tangled up in a cosmic dance. Let me untangle them and get back to you!
Oopsie daisy! It seems my neurons got caught up in a whirlwind of confusion. I'll need a moment to untangle them!
What was that you said? My brain must have taken a spontaneous detour to La La Land. Let's bring it back to reality, shall we?
Pardon me while I retrieve my thoughts from the Bermuda Triangle of comprehension. I'll be back in a jiffy!
My apologies! It seems my brain went on a joyride without me. Let's reel it back in and get down to business!
Oops! It seems my brain got caught up in a cosmic traffic jam. Let's clear the lanes and get back on track!
Hold on a moment while I retrieve my thoughts from the labyrinth of confusion. I'll be back before you know it!
Well, that's a puzzler! It appears my brain took a spontaneous detour to the Land of Lost Thoughts. Let me track them down!
My apologies for the brain glitch! It seems I accidentally hit the snooze button on my cognitive functions. Let's wake them up!
Oops! My brain just decided to take a brief siesta. Let's wake it up and get back to business!
Pardon me while I locate my train of thought—it seems to have gone off the rails momentarily!
What was that you said? My brain must have taken a quick dip in the River of Forgetfulness. Let me fish out those thoughts!
My apologies for the momentary brain freeze! It seems my thoughts decided to take a snow day. Let's thaw them out!
Hold your horses while I round up my scattered thoughts—they seem to have gone on a wild goose chase without me!"
```

##### Managing vulgarity

This is a simple flat text file with one response per line. These are given to the user if vulgarity is
detected in the user input. It should be in-line of the persona. If this file doesn't exist or the
**AllowVulgarity** item is **Yes**, then vulgarity is NOT filtered. Vulgarity filtering admonishes the user
and *deletes* the offending post.

```TXT
Well, sugar plum, we keep things squeaky clean around here! Let's try that again without the naughty words, shall we?
Oh my stars! We're all about keeping it family-friendly here. Let's wash that mouth out with soap and try a more polite approach, darlin'.
Oh dear, looks like someone forgot their manners! Let's turn that potty mouth into a poetry corner, shall we?
Well, butter my biscuits! We're on a strict no-nonsense diet when it comes to language. Let's sprinkle a little sweetness into that sentence, shall we?
Oopsie daisy! Looks like someone tripped over a pile of unsavory words. How about we sweep those under the rug and start fresh?
Well, bless your heart, but we're all about rainbows and butterflies here! Let's try expressing ourselves in a more rainbow-friendly way, shall we?
Oh my goodness gracious! We prefer conversation that's as pure as a field of daisies. Let's pluck out those not-so-nice words and replace them with sunshine!
Whoopsie doodle! It seems like someone took a wrong turn down Foul Language Lane. Let's circle back to the polite path, shall we?
Uh-oh! It's like someone stepped in a puddle of potty talk. Let's dry those shoes off and take a walk on the polite side, shall we?
Well, knock me over with a feather! We're aiming for a tea party atmosphere, not a wrestling match with words. Let's keep it classy, shall we?
Well, well, well! Looks like we've got a case of the naughty word blues. Let's turn that frown upside down with some sweet talk, shall we?
Oh my stars and garters! We're aiming for a garden of good vibes, not a jungle of jumbled words. Let's weed out those bad boys and plant some positivity!
Oopsie daisy! It's like someone spilled a bucket of not-so-nice words. Let's mop up the mess and redecorate with some kindness, shall we?
Well, butter my biscuit! We're serving up sunshine and smiles, not thunderstorms and scowls. Let's swap those storm clouds for rainbows, shall we?
Goodness gracious! It's raining cats and dogs, and those words are like a lightning bolt to the heart. Let's bring out the sunshine and chase away the storm!
Uh-oh spaghetti-o! We've got a case of the wordy woes. Let's toss out the sour grapes and sip on some sweet tea, shall we?
Well, slap my knee and call me silly! We're on a merry-go-round of manners, not a rollercoaster of rudeness. Let's keep it polite and playful, shall we?
Holy guacamole! We're aiming for a fiesta of fun, not a fiasco of foul language. Let's spice things up with some positivity, shall we?
Oh dearie me! It's like someone forgot to sprinkle a little sugar on their words. Let's sweeten the pot and brew up some kindness, shall we?
Well, jumpin' jackrabbits! We're hoppin' down the bunny trail of politeness, not stompin' through the mud of meanness. Let's hop to it and keep it classy!
```

#### Companion configuration

The **Companion.cfg** file is used to configure the behavior of Companion. It contains settings that define
default behavior and assign personas to specific channels within a Discord server.

Default Persona: The "Default" parameter specifies the default persona to be used when a message is received
from a channel that is not explicitly defined in the "Channels" section. This ensures consistent behavior
across channels if no specific persona is assigned.

Channel Assignments: The "Channels" section maps each channel name to its corresponding persona. This allows
for tailored interactions based on the context of the conversation within each channel. For example,
channels dedicated to specific topics or themes can have personas assigned to match those themes, enhancing
engagement and immersion for users.

**Important**: The default persona is used for **moderation** only. Personas will chat with users *ONLY* if
they are explicitly listed with a channel. AI chatting can become annoying very quickly with constant
responsing that may not be wanted or solicited.

```JSON
{
    "Default":"Overmind",
    "Channels":
    {
        "tipsys-room":"Tipsy",
        "mugsys-place":"Mugsy",
        "stoicism":"Marcus"
    }
}
```

#### Companion tokens

Use the below reference material to obtain you token and API, if needed.

The **Companion.tokens** file is where you tell the bot what your Discord token is (line 1) and your OpenAI
API (line 2). When using Ollama, there is no API, so the second line is just a placeholder for future
expansion/services.

**NEVER SHARE OR GIVE OUT THIS INFORMATION!**

```TXT
1111111111111111111111.22222222222222.333333333333
11-22222222222222222222222222222
```

## Ollama

Ollama is a great way to run an AI model "locally" and provides an incredible wealth of opportunities in
developing personas with a diverse nature. However, it is significantly more advanced then Open AI or
just using an API reference. Please refer to the [Ollama website](https://ollama.com/) for instructions for
your system.

## Open AI

Be sure you read and understand the terms and services and acceptable use. **NEVER GIVE OUT OR SHARE YOUR API KEY!**

Obtaining an API key:

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

Be sure you read and understand the terms and services and acceptable use. **NEVER GIVE OUT OR SHARE YOUR
DISCORD TOKEN!**

This bot *requires* **administrator** priviledges for changing the avatar and nickname.

Here's a step-by-step guide to setting up a Discord bot:

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

## Reboot startup

For Companion to auto start after a reboot, the following line needs to be added to your crontab. **It is
absolutely critical that you are root user or run crontab with sudo privileges. Companion must be in the crontab
root level to work correctly**.

```crontab
@reboot ( /home/Companion/LauncherCompanion & ) > /dev/null 2>&1
```

## Manual startup

Use the following command. 

```bash
 /home/Companion/LauncherCompanion
```

