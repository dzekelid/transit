{
  "info": {
    "name": "Youtube Add Live Broadcasts Transition",
    "_postman_id": "b8656037-3c0b-4d22-a330-f984e8c733ec",
    "description": "Changes the status of a YouTube live broadcast and initiates any processes associated with the new status. For example, when you transition a broadcast's status to testing, YouTube starts to transmit video to that broadcast's monitor stream. Before calling this method, you should confirm that the value of the status.streamStatus property for the stream bound to your broadcast is active.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "livebroadcasts",
      "item": [
        {
          "id": "db44125b-bc8e-4fe8-904d-f28b2394257d",
          "name": "postLivebroadcastsTransition",
          "request": {
            "url": "http://www.googleapis.com/youtube/v1/liveBroadcasts/transition?broadcastStatus=%7B%7D&id=%7B%7D&onBehalfOfContentOwner=%7B%7D&onBehalfOfContentOwnerChannel=%7B%7D&part=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Changes the status of a YouTube live broadcast and initiates any processes associated with the new status"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e0d0fc7f-baed-41cd-88f2-48ff04f25a6f"
            }
          ]
        }
      ]
    }
  ]
}