# Hacker Scripts

## Usage

You need these environment variables:

```sh
# used in `smack-my-bitch-up` and `hangover` scripts
TWILIO_ACCOUNT_SID=ACxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
TWILIO_AUTH_TOKEN=yyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy

# used in `kumar_asshole` script
GMAIL_USERNAME=admin@example.org
GMAIL_PASSWORD=password
```

For Ruby scripts you need to install gems:
`gem install dotenv twilio-ruby gmail`

## Cron jobs

```sh
# Runs `smack-my-bitch-up.sh` monday to friday at 9:20 pm.
20 21 * * 1-5 /path/to/scripts/smack-my-bitch-up.sh >> /path/to/smack-my-bitch-up.log 2>&1

# Runs `hangover.sh` monday to friday at 8:45 am.
45 8 * * 1-5 /path/to/scripts/hangover.sh >> /path/to/hangover.log 2>&1

# Runs `kumar-asshole.sh` every 10 minutes.
*/10 * * * * /path/to/scripts/kumar-asshole.sh

# Runs `fucking-coffee.sh` hourly from 9am to 6pm on weekdays.
0 9-18 * * 1-5 /path/to/scripts/fucking-coffee.sh
```

---
Code is released under WTFPL.
