
## API Reference
Base Url - /api/v3/app/

### Create a new nudge ~

```http
  POST /nudges/
```

The body should contain these palyloads. ( The Data Model for Nudge )
| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `event` | `ObjectID` | The ID of the Event goes here. |
| `title` | `string` | The Title of the nudge |
| `img` | `string` | The Image of the nudge ( base64 ) |
| `time` | `timestamp` | The date and time goes here |
| `description` | `string` | The Description of the nudge |
| `icon` | `string` | The Icon of the nudge (base 64) |
| `oneline` | `string` | One line for displaying when minimized |


### Get all nudges ~

```http
  GET /nudges/
```

This request returns list of all the nudges.
We can filter according to our needs by adding queries.

```http
  GET /nudges?type=upcoming&limit=20&page=1
```

```http
  GET /nudges?type=past&limit=20&page=1
```
Or we can get a specific nudge by giving its ID in the query Parameter
```http
  GET /nudges?id=nudge_id
```

### Update a nudge ~

```http
  PUT /nudges/:id
```

This request will update the nudge according to the ID given.
The body can have the following payload.
| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `event` | `ObjectID` | The ID of the Event goes here. |
| `title` | `string` | The Title of the nudge |
| `img` | `string` | The Image of the nudge ( base64 ) |
| `time` | `timestamp` | The date and time goes here |
| `description` | `string` | The Description of the nudge |
| `icon` | `string` | The Icon of the nudge (base 64) |
| `oneline` | `string` | One line for displaying when minimized |

### Delete a nudge ~

```http
  DEL /nudges/:id
```
This request will delete the nudge according to the ID given.
