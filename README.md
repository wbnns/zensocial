# Zensocial

![Alt](https://repobeats.axiom.co/api/embed/ad68b3ae22cfd10a0d261f83bbe72dcadb0770d1.svg "Zensocial")

## About

Post to Bluesky, Farcaster and X from Telegram with less distraction

## Features

- Cross-post text content to Bluesky, X and Farcaster simultaneously
- Support for images (automatically uploaded to Imgur for Farcaster)
- URL embedding
- Line break preservation
- Independent posting (continues if one platform fails)
- Rate limit handling with exponential backoff

## Setup

1. Clone the repository:
```bash
git clone https://github.com/wbnns/zensocial.git
cd zensocial
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Create a `.env` file from the example:
```bash
cp .env.example .env
```

4. Configure your environment variables in `.env`:
- Get a Telegram Bot Token from [@BotFather](https://t.me/botfather)
- Create a Twitter Developer account and get API keys
- Get your Farcaster authorization header
- Create an Imgur application and get client ID
- Generate an app password for your Bluesky account

## Usage

1. Start the bot:
```bash
python src/app.py
```

2. In Telegram:
- Send text to cross-post
- Optionally send an image within 36 seconds
- The bot will post to both platforms and report the status

## Status Messages

The bot provides clear status messages:
- "Posted: Bluesky, Farcaster, X" - Successfully posted to all platforms
- "Posted: Bluesky, Farcaster | Failed: X " - Posted to Bluesky and Farcaster only

## Development

The code is organized into two main parts:
1. Platform-independent utilities and configurations
2. Platform-specific posting logic with independent error handling

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built with python-telegram-bot
- Uses Tweepy for X integration
- Uses Imgur for image hosting

## Support

For support, please create an issue in the GitHub repository.
