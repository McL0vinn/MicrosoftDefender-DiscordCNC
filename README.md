# MicrosoftDefender_DiscordCNC

Below is a Threat-Hunting KQL query I wrote which identifies machines that utilize powershell, cmd or wmic to connect to any URL that includes “cdn.discordapp.com”  ,where the action was initiated by a script execution ( .vbs , .bat etc)
The inspiration for that query was a Phishing Incident i responded to last month, where the User downloaded a .vbs script from a phishing email and Upon execution the User's machine was instructed to download via powershell a .txt file from a “cdndiscordapp.com” URL  which included powershell commands and then save it as .ps1 locally.

The intention of this activity was to evade detection since Discord is a legit application thats being used for teams collaboration (more than ever right now during the COVID-19 pandemic) as well as downloading a .ps1 script straight away would have triggered a bunch of alerts compared to downloading a .txt

You can run the below query in Microsoft Defender for Endpoint, Microsoft Security Center or Azure Sentinel
