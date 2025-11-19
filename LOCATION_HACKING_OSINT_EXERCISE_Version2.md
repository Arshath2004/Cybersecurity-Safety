# LOCATION HACKING & OSINT EXERCISE

## AIM
To perform Open-Source Intelligence (OSINT) on a public or mock social profile to identify location leaks (e.g., geotags, check-ins, location metadata).

### Deliverables
- Examples of publicly visible location data
- Recommendation for improving privacy

## COMMANDS

```bash
git clone https://github.com/thewhiteh4t/seeker.git
cd seeker
python seeker.py
```

During usage, user selects options for templates such as:
- [0] NearYou
- [1] Google Drive
- [2] WhatsApp
- [3] WhatsApp Redirect
- [4] Telegram
- [5] Zoom
- [6] Google ReCaptcha
- [7] Custom Link Preview

After starting the PHP server, to generate a public URL:
```bash
ssh -R 80:localhost:8080 serveo.net
Forwarding HTTP traffic from https://66314604e9d8d9316214cea842463ee5.Serveo.net
```

## Example Output

- Waiting for client, with HTTP forwarding URL created.

## RESULT

- **Disable Geotagging:** Turn off location services for social media and camera apps to prevent photos from storing location data.
- **Review Third-Party App Permissions:** Regularly audit and revoke access for apps that unnecessarily request location data in the background.
- **Avoid Real-Time Sharing:** Wait a few hours (or days) to post location-specific content (check-ins, event photos) to obscure your immediate physical location.