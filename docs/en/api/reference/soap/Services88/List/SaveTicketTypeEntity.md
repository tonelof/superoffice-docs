---
title: Services88.ListAgent.SaveTicketTypeEntity SOAP
generated: true
uid: Services88-List-SaveTicketTypeEntity
---

# Services88 List SaveTicketTypeEntity

SOAP request and response examples **Remote/Services88/List.svc**
Implemented by the <see cref="M:SuperOffice.Services88.IListAgent.SaveTicketTypeEntity">SuperOffice.Services88.IListAgent.SaveTicketTypeEntity</see> method.

## SaveTicketTypeEntity





[WSDL file for Services88/List](../Services88-List.md)

Obtain a ticket from the [Services88/SoPrincipal.svc](../SoPrincipal/index.md)

Application tokens must be specified if calling an Online installation. ApplicationTokens are not checked for on-site installations.

## SaveTicketTypeEntity Request

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices882="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices881="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:List="http://www.superoffice.net/ws/crm/NetServer/Services88">
  <List:ApplicationToken>1234567-1234-9876</List:ApplicationToken>
  <List:Credentials>
    <List:Ticket>7T:1234abcxyzExample==</List:Ticket>
  </List:Credentials>
 <SOAP-ENV:Body>
   <List:SaveTicketTypeEntity>
    <List:TicketTypeEntity xsi:type="List:TicketTypeEntity">
     <List:TicketTypeId xsi:type="xsd:int">0</List:TicketTypeId>
     <List:Name xsi:type="xsd:string"></List:Name>
     <List:Rank xsi:type="xsd:short">0</List:Rank>
     <List:Tooltip xsi:type="xsd:string"></List:Tooltip>
     <List:Icon xsi:type="xsd:string"></List:Icon>
     <List:DefaultTicketStatus xsi:type="xsd:int">0</List:DefaultTicketStatus>
     <List:TicketStatuses xsi:type="NetServerServices882:ArrayOfint">
      <NetServerServices882:int xsi:type="xsd:int">0</NetServerServices882:int>
     </List:TicketStatuses>
     <List:DefaultTicketPriority xsi:type="xsd:int">0</List:DefaultTicketPriority>
     <List:TicketPriorities xsi:type="NetServerServices882:ArrayOfint">
      <NetServerServices882:int xsi:type="xsd:int">0</NetServerServices882:int>
     </List:TicketPriorities>
     <List:ReplyTemplate xsi:type="xsd:int">0</List:ReplyTemplate>
     <List:IsExternalVisible xsi:type="xsd:boolean">false</List:IsExternalVisible>
     <List:IsDefault xsi:type="xsd:boolean">false</List:IsDefault>
    </List:TicketTypeEntity>
   </List:SaveTicketTypeEntity>

 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


## SaveTicketTypeEntity Response

```xml
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
 xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"
 xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:NetServerServices882="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
 xmlns:NetServerServices881="http://schemas.microsoft.com/2003/10/Serialization/"
 xmlns:List="http://www.superoffice.net/ws/crm/NetServer/Services88">
 <SOAP-ENV:Body>
  <List:SaveTicketTypeEntityResponse>
   <List:Response xsi:type="List:TicketTypeEntity">
    <List:TicketTypeId xsi:type="xsd:int">0</List:TicketTypeId>
    <List:Name xsi:type="xsd:string"></List:Name>
    <List:Rank xsi:type="xsd:short">0</List:Rank>
    <List:Tooltip xsi:type="xsd:string"></List:Tooltip>
    <List:Icon xsi:type="xsd:string"></List:Icon>
    <List:DefaultTicketStatus xsi:type="xsd:int">0</List:DefaultTicketStatus>
    <List:TicketStatuses xsi:type="NetServerServices882:ArrayOfint">
     <NetServerServices882:int xsi:type="xsd:int">0</NetServerServices882:int>
    </List:TicketStatuses>
    <List:DefaultTicketPriority xsi:type="xsd:int">0</List:DefaultTicketPriority>
    <List:TicketPriorities xsi:type="NetServerServices882:ArrayOfint">
     <NetServerServices882:int xsi:type="xsd:int">0</NetServerServices882:int>
    </List:TicketPriorities>
    <List:ReplyTemplate xsi:type="xsd:int">0</List:ReplyTemplate>
    <List:IsExternalVisible xsi:type="xsd:boolean">false</List:IsExternalVisible>
    <List:IsDefault xsi:type="xsd:boolean">false</List:IsDefault>
   </List:Response>
  </List:SaveTicketTypeEntityResponse>
 </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

