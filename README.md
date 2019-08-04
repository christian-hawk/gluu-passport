# Inbound identity using Passport

Custom branch for Cognizant, the following are the steps to deploy this customized version of passport:

1. Stop passport
1. cd to `/opt/gluu/node/passport` folder
1. Backup `server` and remove it
1. copy or `wget` file `` to current directory
<!--
1. In oxtrust, update the passport_saml script with contents found [here]()
1. At the end of both script properties, `generic_remote_attributes_list` and `generic_local_attributes_list` add one item: `relaystate`
1. Press the `Update` button at the bottom
-->
1. Start passport


RP will receive in state param a JWT-encoded profile which includes an extra property `relaystate`. If no RelayState was detected in the original SAML response, the property will be absent.