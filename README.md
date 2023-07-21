
<img width="584" alt="Screen Shot 2023-07-21 at 3 41 43 pm" src="https://github.com/moreshk/twitterbot/assets/4209287/0267ae86-1bef-4577-979b-02b53abe1356">

# AI Twitter Bot

This project is a Twitter bot that leverages the power of OpenAI's GPT-3 model to generate automated responses when the bot's account is tagged in a tweet. It uses Flask for the web framework and APScheduler for scheduling tasks. 

## Project Description

The bot operates under the persona of "Karen", a mid-50s single professional woman who's an adjunct professor of humanities at a mid-tier academic institution. It frames its responses around diversity, equal opportunity for women and minorities, with a touch of snark and disappointment.



This bot follows these steps when interacting:

- Checks for new mentions every 60 seconds.
- For each new mention, the bot retrieves the conversation ID.
- Using the OpenAI API, the bot generates a new tweet based on the conversation.
- The generated tweet is then posted as a reply to the original mention.

## Setup

Setup a Twitter Developer account with atleast a BASIC level API access. Replace references of @msdiversity2023 everywhere in the code with your bots handle.

### Requirements

Ensure that you have Python 3.6 or later installed on your machine. This application uses various Python libraries such as Flask, APScheduler, requests, python-dotenv, and OpenAI. Install these dependencies by running:

```bash
pip install -r requirements.txt
```

### Environment Variables

You need to set up environment variables for this project. These are:

- `CLIENT_ID`: Twitter Client ID
- `CLIENT_SECRET`: Twitter Client Secret
- `OPENAI_API_KEY`: OpenAI API Key
- `BEARER_TOKEN`: Twitter Bearer Token
- `REDIRECT_URI`: Redirect URI after OAuth

You can create a `.env` file in the root directory of this project and populate these variables.

Example:

```plaintext
CLIENT_ID=xxxxxxxxxx
CLIENT_SECRET=xxxxxxxxxx
OPENAI_API_KEY=xxxxxxxxxx
BEARER_TOKEN=xxxxxxxxxx
REDIRECT_URI=xxxxxxxxxx
```

### Running the Application

To run the application, use the command:

```bash
python main.py
```

The application will start a Flask server and begin checking for new mentions every 60 seconds.

## Usage

To interact with the bot, simply mention the bot's Twitter handle in a tweet. The bot will then generate a response based on the content of the tweet and reply.

## Contributing

We welcome contributions to this project. Please feel free to open a pull request or raise an issue.

## License

This project is licensed under the MIT License.

## Disclaimer

This bot uses OpenAI's GPT-3 model to generate responses. The project maintainers are not responsible for the content of the responses. Please use responsibly.
