# Useful commands using `screen` application in Unix/Ubuntu systems

**Using `screen` to keep process running on the AWS EC2 without hangup**

I recently started to run python scripts on my AWS EC2 instances to gather tweet streams about new games. The always-on nature of a low-power instance (t2.micro) with relatively small SSD volume (20G) can keep my twitter streaming listener running for days (check out the codes I used for tweet streaming [here](https://github.com/ElvinOuyang/social-media-mining)). However, when I was using the EC2 instances with SSH connections, I found out that the instance will shut down the process I initiated through SSH soon after I disconnect. I then did some research online and figured out that you can keep your ssh session running without being disrupted by a "hangup" by putting your sessions in "screens" with `screen`.

`$screen -ls`

`$screen -r screen-id`
`$screen -r screen-title`

`$screen -S screen-title`

CTRL-A C: create new screen
CTRL-A N: next screen
CTRL-A P: previous screen
CTRL-A D: detach current screen session
