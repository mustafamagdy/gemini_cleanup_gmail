# Gmail Inbox Categorizer

## Description
This project is an automated Gmail inbox organizer that uses the Gmail API and Google's Gemini AI to categorize emails and move them into appropriate labels. It helps users maintain a cleaner inbox by automatically sorting incoming emails into predefined categories.

## Features
- Authenticates with Gmail using OAuth 2.0
- Fetches emails from the user's inbox
- Uses Gemini AI to categorize emails based on content
- Creates labels in Gmail for each category
- Moves emails to appropriate labels
- Handles API rate limiting with exponential backoff
- Processes emails in batches to optimize API usage

## Prerequisites
- Python 3.10+
- A Google Cloud Platform account with Gmail API enabled
- Gemini API access

## Installation
1. Clone the repository:
git clone https://github.com/mustafamagdy/gemini_cleanup_gmail.git
cd gmail-inbox-categorizer
Copy
3. Install required packages:
pip install google-auth-oauthlib google-auth-httplib2 google-api-python-client google.generativeai
Copy
4. Set up your Google Cloud Project and enable the Gmail API:
- Go to the [Google Cloud Console](https://console.cloud.google.com/)
- Create a new project or select an existing one
- Enable the Gmail API for your project
- Create OAuth 2.0 credentials (download as `client_secret.json`)

4. Get your Gemini API key from the [Google AI Studio](https://makersuite.google.com/app/apikey)

## Configuration
1. Place your `client_secret.json` file in the project directory.
2. Create a file named `api_key.txt` in the project directory and paste your Gemini API key into it.

## Usage
Run the script:
python gmail_categorizer.py
Copy
On first run, you'll be prompted to authorize the application. Follow the URL provided and enter the authorization code.

## Customization
You can modify the email categories in the `categorize_email_with_gemini` function to suit your needs.

## Limitations
- The script is subject to Gmail API usage quotas and limits.
- Processing a large number of emails may take considerable time due to API rate limits and AI processing time.

## Contributing
Contributions, issues, and feature requests are welcome. Feel free to check [issues page](https://github.com/yourusername/gmail-inbox-categorizer/issues) if you want to contribute.

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Disclaimer
This project is not affiliated with or endorsed by Google. Use at your own risk. Always be cautious when granting applications access to your Gmail account.
