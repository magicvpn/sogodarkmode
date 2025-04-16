# sogodarkmode

Not perfect, but it works :) (as long as you don't use the calendar that much, the menu to add items to it has a broken dark mode)

Put the css override in: /opt/mailcow-dockerized/data/conf/sogo/dark-theme.css

Add "- ./data/conf/sogo/dark-theme.css:/usr/lib/GNUstep/SOGo/WebServerResources/css/theme-default.css:z" under "sogo-mailcow:" in "/opt/mailcow-dockerized/docker-compose.yml"

After that run: cd /opt/mailcow-dockerized/ && docker compose up -d
Your SOGo should have dark mode now.

Made by lots of different AI's and a lot of time spent testing this out.
