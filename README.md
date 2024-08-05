# project-resources

Here you'll find a variety of resources you'll need to successfully complete your project.

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