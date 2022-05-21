# Halo_ServiceDesk Module
Powershell wrapper for HaloPSA REST API

This was my first attempt at a HaloPSA REST wrapper for use in automation. I've moved on to a more advanced version internally so I'm making my (working) v1 code available for anyone who might need some basic functionality.

Cmdlets:

Connect-HaloPSA - Connects to HaloPSA and gets a bearer token.

Example: Connect-HaloPSA -ClientID "<your client ID>" -ClientSecret "<your client secret>"

Get-Token - Gets a bearer token via REST API .
Example: Get-Token -ClientID 'value1' -ClientSecret 'value2'
