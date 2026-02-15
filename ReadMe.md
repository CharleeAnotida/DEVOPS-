Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

Install the latest PowerShell for new features and improvements! https://aka.ms/PSWindows

PS C:\Users\charl> docker pull alpine
Using default tag: latest
latest: Pulling from library/alpine
Digest: sha256:25109184c71bdad752c8312a8623239686a9a2071e8825f20acb8f2198c3f659
Status: Image is up to date for alpine:latest
docker.io/library/alpine:latest
PS C:\Users\charl> docker tag alpine charlenn/ap1:v1.1
PS C:\Users\charl> docker login
Authenticating with existing credentials... [Username: charlenn]

i Info → To login with a different account, run 'docker logout' followed by 'docker login'


Login Succeeded
PS C:\Users\charl> docker run -it --name a1 charlenn/ap1:v1.1
/ # apt update
/bin/sh: apt: not found
/ # apt add php
/bin/sh: apt: not found
/ # apk update
v3.23.3-94-g22e1801794f [https://dl-cdn.alpinelinux.org/alpine/v3.23/main]
v3.23.3-125-g705b1aac651 [https://dl-cdn.alpinelinux.org/alpine/v3.23/community]
OK: 27572 distinct packages available
/ # apk add php
(1/9) Installing php84-common (8.4.17-r0)
(2/9) Installing argon2-libs (20190702-r5)
(3/9) Installing ncurses-terminfo-base (6.5_p20251123-r0)
(4/9) Installing libncursesw (6.5_p20251123-r0)
(5/9) Installing libedit (20251016.3.1-r0)
(6/9) Installing pcre2 (10.47-r0)
(7/9) Installing xz-libs (5.8.2-r0)
(8/9) Installing libxml2 (2.13.9-r0)
(9/9) Installing php84 (8.4.17-r0)
Executing busybox-1.37.0-r30.trigger
OK: 18.7 MiB in 25 packages
/ # php -v
PHP 8.4.17 (cli) (built: Jan 20 2026 19:04:32) (NTS)
Copyright (c) The PHP Group
Built by Alpine Linux aports
Zend Engine v4.4.17, Copyright (c) Zend Technologies
/ # exit
PS C:\Users\charl>        
