Updated Luci frontend for AdGuardHome

original project from rufengsuixing/luci-app-adguardhome 

Project Aims :

Complex openwrt AdGuardHome luci

 - can manage browser port
 - compress core with upx
 - redirect dns
   - as the upstream of dnsmasq
   - redirect port 53 to AdGuardHome（ipv6 need to install ipv6 nat redirect or  if client use ipv6 redirect is invalid）
   - replace dnsmasq with port 53 (need to set AGH,dnsip=0.0.0.0,the port of dnsmasq and AGH will be exchange)
 - change bin path
 - change config path
 - change work dir(support tmp,auto redownload after reboot)
 - change runtime log path
 - modify browser login passord
 - Positive/reverse order see/del/backup runtime log which update every 3 second
 - modify config manually(support yaml editor)
 - use template to fast config(when no config file)
 - Keep bin file and config when system upgrade (database and querylog can be choose) 
 - when boot wait for network access （3min timeout）
 - backup workdir when shutdown
