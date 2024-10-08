# project-resources

Here you'll find a variety of resources you'll need to successfully complete your project.

## troubleshooting

- If both ports (80 and 3306) aren't showing, open up a terminal and run these two commands in this order:
    1. **docker compose down**
    2. **docker compose up -d**

- If things are acting wonky, push all work that you don't want to lose, then try the following things - in order from least drastic to most drastic - stopping when things aren't wonky anymore:
    1. `Ctrl+Shift+P` > Reload Window
    2. `Ctrl+Shift+P` > Rebuild Container > Rebuild button (**Not the `Full Rebuild`!**)
    4. Delete the Codespace, then create a new one. (**Don't forget to push beforehand!**)

## travel photos

The `3512-2024-04-project-photos.zip` file ([downloadable here on Google Drive](https://drive.google.com/file/d/1ds9Jsq8c0wMemvKC35Cwe3G0Rpr2pn42/view?usp=drive_link) - it's too big for GitHub!) contains 152 travel photos to be used in the Project. You will need to unzip the photo files and upload them to your Cloudinary media library, preferably into a well-named folder.

## travel db

The `travel-db-dump-2024-fall.sql` script can be used to create the travel db on your Codespace and GCP site and populate that db with the necessary tables and records.

There are a number of ways to accomplish this, but here are two suggestions. The first is my recommendation, because it's faster and every opportunity you have to use a command line is a good opportunity.

### use a mysql command from your Codespace's terminal

1. Copy the sql script into your Codespace.
2. Open up a terminal in your Codespace.
3. Run the following command `mysql -h 127.0.0.1 -P 3306 -u root -p'root' < travel-db-dump-2024-fall.sql`.

### use DBeaver

If you've installed DBeaver **and** are using a locally installed VS Code instance, you can run the script inside of DBeaver.

1. Connect to your Codespace inside of you're locally-installed VS Code instance.
2. Connect to your Codespace via DBeaver.
3. Right-click on your connection in the DBeaver window > SQL Editor > New SQL script.
    1. This will open up a new tab in DBeaver.
4. Paste the contents of the script into the tab.
5. Click the Execute SQL Script icon (orange scroll one).
    1. A dialog will pop up, warning you about large script execution. Just click the **Yes** button.
