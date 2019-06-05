![SocialWall Pro](https://www.socialwallpro.com/files/design/socialwallpro_logo_800px.png)

# SocialWall Pro - Get and Create Content API Documentation

## Endpoints
[Get Content API](#get-content-api)
- [GET api/event/{wallId}/messages/{number}](#get-apieventwallidmessagesnumber)
- [GET api/event/{wallId}/messages/last/{messageId}/{number}](#get-apieventwallidmessageslastmessageidnumber)

[Create Content API](#create-content-api)
- [POST api/event/inject](#post-apieventinject)
- [POST api/event/inject/{wallId}](#post-apieventinjectwallid)


## Get Content API

### API Access and usage

Get Content API must be enabled on your account to be used. Contact our team using the [contact form](https://www.socialwallpro.com/contact) or our chat system on our [website](https://www.socialwallpro.com). Get Content API is part of our Premium offer.

Note that only *accepted* messages will be returned. If the Manual Moderation is enabled, first accept messages before calling the API to get messages back.

Caller has to check if the messages returned have already been received.

### GET api/event/{wallId}/messages/{number}

Return the last `number` *accepted* messages for the wall number `wallId`

#### Example
`https://tool.socialwallpro.com/api/event/9074/messages/10`

Will return the last 10 *accepted* messages.

#### Parameters

`wallId` : id of the Wall from which you want to obtain the accepted messages. You can find that `wallId` in the URL of your Wall while in the Tool.

![wallId](https://www.socialwallpro.com/files/Image/20190605-wallid.png?uniqID=54548)

`number` : number of *accepted* messages you want to obtain. Note that you'll get always the last ones. If you want to paginate, use the [paginated version](#get-apieventidmessageslastmessageidnumber) of this API.

### GET api/event/{wallId}/messages/last/{messageId}/{number}

Return the last `number` *accepted* messages for the wall number `id` started the message `messageId`

#### Example
`https://tool.socialwallpro.com/api/event/9074/messages/last/907222538828369920/10`

Will return the last 10 *accepted* messages following the message with id 907222538828369920.

#### Parameters
`wallId` : id of the Wall from which you want to obtain the accepted messages. You can find that wallId in the URL of your Wall while in the Tool.

`messageId` : id of the message from which you will get the following

`number` : number of *accepted* messages you want to obtain.

### Result
Set of messages in JSON format

#### Example
```
{
  "result": true,
  "messages": [
    {
      "tweetId": null,
      "mediaJsons": [
        {
          "mediaType": 2,
          "relativeMediaURL": "//pic.tezaki.com/atotwp/55895/1544094750745-670881861.jpg",
          "originalURL": "https://scontent-frx5-1.cdninstagram.com/vp/8197cc36589c6a6cf41950ea62ed532b/5C9FEF50/t51.2885-15/e35/46730663_2575454119162030_8215657494427739618_n.jpg",
          "localURL": "55895/1544094750745-670881861.jpg"
        }
      ],
      "sent": true,
      "moderationLevel": 0,
      "avatarMediaJson": {
        "mediaType": 0,
        "relativeMediaURL": "https://scontent-frx5-1.cdninstagram.com/vp/d0e6fc07595d03a8672fe2ce63942c6b/5C97C1A9/t51.2885-19/s150x150/46271169_753176581683811_6773271547298709504_n.jpg",
        "originalURL": "https://scontent-frx5-1.cdninstagram.com/vp/d0e6fc07595d03a8672fe2ce63942c6b/5C97C1A9/t51.2885-19/s150x150/46271169_753176581683811_6773271547298709504_n.jpg",
        "localURL": null,
        "twitterUserId": 0,
        "twitterUserScreenName": "adababyyyyy",
        "twitterUserName": "Ada Baby"
      },
      "highlightType": null,
      "validated": true,
      "mediaTreated": true,
      "avatarMediaTreated": true,
      "creationDate": 1544049595000,
      "text": "In love ☀☀",
      "grabOrigin": "Instagram",
      "vote": false,
      "retweetCount": null,
      "lang": null,
      "tagJsons": null,
      "stringMessageId": "1927950199376995079",
      "bannedTopRetweet": false,
      "inReplyStringMessageId": null,
      "stringTweetId": "1927950199376995079",
      "tags": {
        "instagram": "Instagram",
        "accepted": "Accepted"
      },
      "type": "instagram",
      "sentAt": 1544097830836,
      "customHighlight": null,
      "socket": null,
      "search": false,
      "moderated": true,
      "moderatedAt": 1544097842633
    },
    {
      "tweetId": null,
      "mediaJsons": [
        {
          "mediaType": 2,
          "relativeMediaURL": "//pic.tezaki.com/atotwp/55895/1544093340530-341508167.jpg",
          "originalURL": "https://scontent-prg1-1.cdninstagram.com/vp/bd5208c959853a379fe0860c87a26ba5/5CA52421/t51.2885-15/e35/46399770_376376476257419_4716033363303365782_n.jpg?_nc_ht=scontent-prg1-1.cdninstagram.com",
          "localURL": "55895/1544093340530-341508167.jpg"
        }
      ],
      "sent": true,
      "moderationLevel": 0,
      "avatarMediaJson": {
        "mediaType": 0,
        "relativeMediaURL": "https://scontent-prg1-1.cdninstagram.com/vp/8a4a692a77ac3d44ed68c85336613da7/5C8ECBC1/t51.2885-19/s150x150/38812824_1726960147433498_4819909498976075776_n.jpg",
        "originalURL": "https://scontent-prg1-1.cdninstagram.com/vp/8a4a692a77ac3d44ed68c85336613da7/5C8ECBC1/t51.2885-19/s150x150/38812824_1726960147433498_4819909498976075776_n.jpg",
        "localURL": null,
        "twitterUserId": 0,
        "twitterUserScreenName": "__alo",
        "twitterUserName": "🌺Aloha"
      },
      "highlightType": null,
      "validated": true,
      "mediaTreated": true,
      "avatarMediaTreated": true,
      "creationDate": 1544036288000,
      "text": "Riflessi. 🌬  #nord#scandinavia#sweden#stockholm #mornings",
      "grabOrigin": "Instagram",
      "vote": false,
      "retweetCount": null,
      "lang": null,
      "tagJsons": null,
      "stringMessageId": "1927838572843158768",
      "bannedTopRetweet": false,
      "inReplyStringMessageId": null,
      "stringTweetId": "1927838572843158768",
      "tags": {
        "instagram": "Instagram",
        "accepted": "Accepted"
      },
      "type": "instagram",
      "sentAt": 1544097830836,
      "customHighlight": null,
      "socket": null,
      "search": false,
      "moderated": true,
      "moderatedAt": 1544097835803
    },...
```

## Create Content API

### API access and usage

Create Content API needs an *API key* to be used. Contact our team using the [contact form](https://www.socialwallpro.com/contact) or our chat system on our [website](https://www.socialwallpro.com) to get it. Create Content API is part of our Premium offer.

*API key* put it in the `header request` under the `x-api-key` key or as an URL argument using `api_key` key.

Arguments must be passed in JSON format. The following table shows what fields are mandatory/optional and the format to be used.

All injected Web Messages are available under the Manual Moderation panel (if enabled) or under the Message Review panel.


### POST api/event/inject

Inject the Web Message in all your Walls not yet stopped (so in preparation or activated or running)

#### Example

`POST https://tool.socialwallpro.com/api/event/inject/123`

```
{
    "text": "Hello World",
    "avatarName": "socialwallpro",
    "realName": "SocialWall Pro",
    "mediaUrl": "https://pbs.twimg.com/media/DzTH_6kXgAEswfw.png:large"
}
```

![Injected Message](https://www.socialwallpro.com/files/Image/20190605-api-injection.png)

#### Parameters

`avatarName` (string - mandatory) : unique identifier of the user

`realName` (string - optional - default: "Web Message") : display name

`text` (string) : message itself

`mediaURL` (URL - optional) : URL of an hosted media

### POST api/event/inject/{wallId}

Inject the Web Message in the Wall corresponding the `wallId` if the Wall is not stopped (so in preparation or activated or running).

#### Example

`POST https://tool.socialwallpro.com/api/event/inject/123`

```
{
    "text": "Hello World",
    "avatarName": "socialwallpro",
    "realName": "SocialWall Pro",
    "mediaUrl": "https://pbs.twimg.com/media/DzTH_6kXgAEswfw.png:large"
}
```


#### Parameters

`wallId` : id of the Wall in which you want to inject the message. You can find that `wallId` in the URL of your Wall while in the Tool.

![wallId](https://www.socialwallpro.com/files/Image/20190605-wallid.png?uniqID=54548)



`avatarName` (string - mandatory) : unique identifier of the user

`realName` (string - optional - default: "Web Message") : display name

`text` (string) : message itself

`mediaURL` (URL - optional) : URL of an hosted media

## Result

### Success
```
{
    "error": false,
    "injected": [
        912
    ]
}
```

If no `wallId` is specified during the request, injected array will list all the Walls ids where the Web Message has been injected into.
If a `wallId` is specified during the request, injected array will contain only that specific id.

### Error messages

Mandatory field missing
```
{
   "error": true,
   "message" : "Mandatory field missing"
}
```

Media URL is not a valid URL
```
{
    "error": true,
    "message": "The media URL provided isn't a valid URL"
}
```

JSon not valid
```
{
   "error": true,
   "message": "Request malformed"
}
```

API key is invalid
```
{
    "error": true,
    "message": "API Key is incorrect"
}
```

API key is not provided
```
{
    "error": true,
    "message": "API Key is missing (from header or query string)"
}
```

If you user doesn’t own that Wall with that `wallId`
```
{
    "error": true,
    "message": "You can't use that event"
}
```

If Wall with `wallId` does not exist in the system
```
{
    "error": true,
    "message": "Event not found"
}
```

If Wall with `wallId` is already stopped
```
{
    "error": true,
    "message": "You can't use that event (event is stopped)"
}
```
