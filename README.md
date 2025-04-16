# sogodarkmode

Not perfect, but it works :)
Put the css override in: /opt/mailcow-dockerized/data/conf/sogo/dark-theme.css
Add "- ./data/conf/sogo/dark-theme.css:/usr/lib/GNUstep/SOGo/WebServerResources/css/theme-default.css:z" under "sogo-mailcow:" in "/opt/mailcow-dockerized/docker-compose.yml"
After that run: cd /opt/mailcow-dockerized/ && docker compose up -d
Your SOGo should have dark mode now.
