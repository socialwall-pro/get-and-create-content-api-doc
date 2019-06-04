# SocialWall Pro - Get and Create Content API Documentation

## Get Content API

### API Access and usage

Get Content API must be enabled on your account to be used. Contact our team using the [contact form](https://www.socialwallpro.com/contact) or our chat system on our [website](https://www.socialwallpro.com).

Note that only *accepted* messages will be returned. If the Manual Moderation is enabled, first accept messages before calling the API to get messages back.

Caller has to check if the messages returned have already been received.

### Endpoint
- [GET api/event/{id}/messages/{number}](#get-apieventidmessagesnumber)
- [GET api/event/{id}/messages/last/{messageId}/{number}](#get-apieventidmessageslastmessageidnumber)


#### GET api/event/{wallId}/messages/{number}

Return the last `number` *accepted* messages for the wall number `wallId`

##### Example
`https://tool.socialwallpro.com/api/event/9074/messages/10`

Will return the last 10 *accepted* messages.

##### Parameters

`wallId` : id of the Wall from which you want to obtain the accepted messages. You can find that wallId in the URL of your Wall while in the Tool.
`number` : number of *accepted* messages you want to obtain. Note that you'll get always the last ones. If you want to paginate, use the [paginated version](#get-apieventidmessageslastmessageidnumber) of this API.

#### GET api/event/{id}/messages/last/{messageId}/{number}

Return the last `number` *accepted* messages for the wall number `id` started the message `messageId`

##### Example
`https://tool.socialwallpro.com/api/event/9074/messages/last/907222538828369920/10`

Will return the last 10 *accepted* messages following the message with id 907222538828369920.

##### Parameters
`wallId` : id of the Wall from which you want to obtain the accepted messages. You can find that wallId in the URL of your Wall while in the Tool.
`messageId` : id of the message from which you will get the following
`number` : number of *accepted* messages you want to obtain.

