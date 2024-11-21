# Zensocial

Post to Farcaster and X from Telegram with less distraction

## Features

- Cross-post text content to X and Farcaster simultaneously
- Support for images (automatically uploaded to Imgur for Farcaster)
- URL embedding in Farcaster posts
- Line break preservation
- Independent posting (continues if one platform fails)
- Rate limit handling with exponential backoff

## Setup

1. Clone the repository:
```bash
git clone https://github.com/wbnns/aetherbeam.git
cd aetherbeam
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
- "Posted to Farcaster, X" - Successfully posted to both platforms
- "Posted to Farcaster, X failed" - Posted to Farcaster only
- "Posted to X, Farcaster failed" - Posted to X only
- "Failed posting to Farcaster and X" - Both platforms failed

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
