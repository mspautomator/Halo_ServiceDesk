# Halo_ServiceDesk Module
Powershell wrapper for HaloPSA REST API

This was my first attempt at a HaloPSA REST wrapper for use in automation. I've moved on to a more advanced version internally so I'm making my (working) v1 code available for anyone who might need some basic functionality.

Cmdlets:

Connect-HaloPSA - Connects to HaloPSA and gets a bearer token.

  Example: Connect-HaloPSA -ClientID "<your client ID>" -ClientSecret "<your client secret>"

Get-Token - Gets a bearer token via REST API .
  
  Example: Get-Token -ClientID 'value1' -ClientSecret 'value2'
  
Check-Token - Checks for a valid bearer token
  
Read-Token - Reads token from cache
  
Write-Log - Logging function
  
Get-Ticket - Gets a ticket
  
  Example: Get-Ticket -TicketID 123456
  
Get-TicketStatus - Gets the current status of a ticket
 
  Example: Get-TicketStatus -TicketID 123456
  
Create-Ticket - Creates a new Ticket. This function has parameters available for most HaloPSA fields.
  
  Example: Create-Ticket -Summary $summary -Details $details
  
Update-Ticket - Updates a ticket. This function has parameters available for most HaloPSA fields.
  
  Example: Update-Ticket -TicketID $TicketID -status_id 31 -Team "Team Name"
  
Create-HaloPrivateNote - Creates a private note on a ticket. Useful for automation logging back to a ticket.
  
  Example: Create-HaloPrivateNote -TicketID $TicketID -Note $Note
