# release - Eng-rc342
## fix bugs:
1.Now supports WEB UI based seemless firmware upgrade</br>
2.Support WEB UI pair Wi-Fi network and network mode switch</br>
3.Fix for SSIDbug  where it was not supporting special character</br>
4.Fix Alexa SDK DSN bug where now we dont need to set it after every update</br>
5.Fix media format bug. Previous versions could not support some format of iHeartRadio station</br>
6.Perform the response of ASR event</br>

# NOTE:
 Before you start upgrading, please confirm that if your board version is the previous version of RC-342, you must use the TFTP tool to upgrade firmware, otherwise you will be able to use webui cheerfully!</br>

Suppose you are lower than rc-342 version of the user, you must know the following steps:</br>
 However, since this is Beta sample, We have changed the format of the DSN, so once you complete the firmware upgrade, you have to Set the DSN manually, please refer to the procedure below (after performing the upgrade) to understand how to write the DSN to protected area in the Nor-flash:</br>

1: You need switch to Serial Console after complete the firmware upgrade, the method to entry, pls click the link:https://github.com/RAKWireless/wiscore/wiki/Access-serial-console </br>
2: When you success to entry the Console, pls press"enter", then insert the DSN command as:</br>
<<$</br>
<<$set -dsn Wiscore.Alexa.000000    //You can randomly generate 6 characters instead of `000000`</br>
<<$ok</br>
<<$q</br>

Don't worry, the future release(higher version) will not need you to re write the DSN again and upgrades will be seemless and will get you up and running in no time. </br>