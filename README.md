# ufw-monitor-script-for-i3blocks
i3blocks blocklet script to monitor and change ufw status

  * Enable and disable "Uncomplicated Firewall" ufw on single click.
  * Display current status (active/inactive). 
  * Right click launches gufw for profile switching.

##Requirements
  * Allow user to execute ufw without password - Add <code>bsmith ALL = NOPASSWD: /usr/bin/ufw</code> to <code>/etc/sudoers</code> (''sudo visudo'')
  * gksudo and gufw (Or add gufw to suderos and skip gksudo) - Right click on blocklet launches gufw to switch profiles/adjust ufw.

##Blocklet code
<pre><code>[firewall]
command=~/bin/ufw_status.sh
label=FW:
align=right
color=#80ff00
interval=5
</code></pre>
  
###Note: 
Would like to find a way to list gufw profile name when ufw is active and to switch between gufw profiles with the middle button - Doesn't seem possible.
