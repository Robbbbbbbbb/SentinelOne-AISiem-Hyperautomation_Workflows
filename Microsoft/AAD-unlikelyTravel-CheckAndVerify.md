# AAD-unlikelyTravel-CheckAndVerify

This Hyperautomation workflow will monitor Microsoft Entra logs for Unlikely Travel events. When one is flagged, it will compare the event against the SentinelOne workstation that the affected user last logged into. If the external NAT of the workstation does not match the IP of the logon event, it will ping the user over Microsoft Teams with an Adaptive Card. The user can then respond and either confirm the logon or pass a webhook to another workflow to begin revoking sessions and a credential reset.
