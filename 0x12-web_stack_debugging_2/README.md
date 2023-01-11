Web stack debugging #2

This was the third in a series of web stack debugging projects. In these projects, I was given broken/bugged webstacks in isolated containers, and tasked with fixing the web stack to a working state. For each task, I wrote a script automating the commands necessary to fix the web stack.
Tasks page_with_curl

    0. Run software as another user
        0-iamsomeonelese: Bash script that runs the command whoami under the user passed as argument.
        Usage: ./0-iamsomeonelese <user>

    1. Run Nginx as Nginx
        1-run_nginx_as_nginx: Bash script that fixes a web server to run Nginx listening on port 8080 as the nginx user.

    2. 7 lines or less
        100-fix_in_7_lines_or_less: Bash script that fixes a web server to run Nginx listening on port 8080 as the nginx user.
        7 lines long.

