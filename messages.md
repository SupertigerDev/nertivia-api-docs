# Messagse
### Context
[Get Messages](#get-messages)

## Get Messages
**Description**: This request allows you to get the last 50 messages in the channel.

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
