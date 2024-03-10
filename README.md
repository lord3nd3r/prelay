This Python script is an IRC bot that relays text between channels on multiple networks. It supports SSL and SASL/nickserv options and allows admins to add and delete channels, as well as manage user authentication.

Requirements

    Python 3.6 or higher
    Python libraries:
        irc or irc3 (for SASL/nickserv support)
        ssl (for SSL connections)


Installation

    Clone or download the repository:

bash

git clone https://github.com/lord3nd3r/prelay.git

    Install the required Python libraries:

bash

pip install -r requirements.txt

    Create a .env file in the project directory with the following variables:
        NETWORKS: A list of networks in JSON format (e.g., '[{"name": "Network1", "channels": ["#channel1", "#channel2"]}]')
        ADMINS: A list of admins in JSON format (e.g., '[{"username": "admin1", "password": "admin1password"}, {"username": "admin2", "password": "admin2password"}]')


Usage

    Run the script:

bash

python main.py

    The bot will connect to the specified networks and join the specified channels.
    To add a new channel, send a private message to the bot with the command !add_channel <channel_name>.
    To delete a channel, send a private message to the bot with the command !delete_channel <channel_name>.
