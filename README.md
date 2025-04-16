# SOGo Dark Mode for Mailcow Dockerized

This guide explains how to change to dark mode for your SOGo webmail interface within a Mailcow Dockerized setup.

**Important Note:** This dark mode implementation is not perfect. Specifically, the menu for adding items to the calendar currently has a broken dark theme. Please be aware of this limitation if you heavily rely on the calendar.

## Installation Instructions

Follow these steps to apply the dark mode:

1.  **Create the CSS Override File:**
    Create a new file named `dark-theme.css` and place your custom CSS code inside it. Save this file in the following directory on your Mailcow server:
    ```
    /opt/mailcow-dockerized/data/conf/sogo/
    ```

2.  **Modify `docker-compose.yml`:**
    Edit the `/opt/mailcow-dockerized/docker-compose.yml` file. Locate the `sogo-mailcow:` service definition. Under this section (specifically within the `volumes:` section), add the following line:
    ```yaml
    volumes:
      # ... other volumes ...
      - ./data/conf/sogo/dark-theme.css:/usr/lib/GNUstep/SOGo/WebServerResources/css/theme-default.css:z
    ```
    **Note:** Ensure you are adding this line under the `volumes:` key, and maintain the correct indentation. If the `volumes:` section doesn't exist under `sogo-mailcow:`, you will need to add it.

3.  **Apply the Changes:**
    Navigate to the Mailcow directory in your terminal:
    ```bash
    cd /opt/mailcow-dockerized/
    ```
    Then, apply the changes and restart the SOGo container by running the following command:
    ```bash
    docker compose up -d
    ```

4.  **Verification:**
    Once the containers are back up, open your SOGo webmail interface in your browser. You should now see the dark mode applied.

## Disclaimer

Please note that this is provided as a "use at your own risk" solution. I'm not responsible for any issues, data loss, or unexpected behavior that may arise from following these instructions. No support will be provided for this modification.

## Credits

This dark mode implementation was made possible through the contributions of various AI models and significant time spent testing and refining the solution.
