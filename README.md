# okta-sprayer
python3 script that reads usernames from an input file and a password from the command line and then attemps that password for each user against the specified domain's okta page.

First: pip3 install requests

Use: python3 okta-sprayer.py -f [input_file] -d [domain.com] -w [wait_time_in_seconds]....then enter the password to use for the spray next

For ease of use, put the input file in the same directory as the script and ensure each username is on its own line.

The script will then perform a single check for each user in the input file with the specified password from the command line and will respond with either unsuccessful or successful. The script will wait between attempts based on the number of seconds specified by the -w argument.

If performing this test for a large number of users, you may want to consider breaking the user list into smaller groups and running each group from a different source host.

Note: if the script is having trouble parsing the password, surround it in single quotes (').

