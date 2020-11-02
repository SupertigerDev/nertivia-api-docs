# Messagse
• [Get Messages](#get-messages)  
• [Send Message](#send-message)

## Get Messages
**Description**: This request allows you to get the last 50 messages in a channel.

**URL**: `https://supertiger.tk/api/messages/channels/{channel_id}` 

**Request Type**: `GET`  

**Required Header**: `{authorization: "your token"}`

 **Response**:
 ```
 channelID: string
  messages: [
    {
      channelID: string,
      created: number
      creator: {username: string, uniqueID: string, tag: string}
      files: []
      mentions: []
      message: string
      messageID: string
      type: number
    }
  ]
  status: bool
 ```
 ## Send Message
**Description**: This request allows you to send a message to a channel.

**URL**: `https://supertiger.tk/api/messages/channels/{channel_id}` 

**Request Type**: `POST`  

**Required Header**: `{authorization: "your token"}`

**Body**: 
```
{
   message: string
   socketID?: string
   tempID?: string
}
```

**Response**:
 ```
{
   {
     "channelID": string,
     "message": message,
     "creator": {
        "uniqueID": string,
        "username": string,
        "tag": string,
        "avatar": string,
        "admin": number
     },
     "created": number,
     "mentions": [],
     "quotes": [],
     "messageID": string,
   },
   status: bool
   tempID: string
}
 ```
 
 
