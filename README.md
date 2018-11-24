# ansible-digicert-plugin
Ansible plugin that order and fetch Digicert Certificate

# How does it work ?
This plugin uses the Digicert v2 Api to communicate with the certificate service. The service works this way :
- Whenever you want a signed certificate you make a certificate request
- The certificate request must be accepted or refused by an administrator
- When accepted it triggers an order

The plugin will check for accepted orders based matching the common name, alternative dns names and Certicate Signing Request. It will pick the most recent order, and if not found, will check for a pending certificate request.

# What is supported with the plugin

Digicert API has many options and a small set is covered by this plugin. 
