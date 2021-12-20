# API HTTP

## ADMIN

### NFT cards

#### Hero

- **GET** `/nft/hero/get`

  - Return hero inforamtion.
    - path params:
    - query params:
      - `id` integer, required: id of hero
  - Response sample: (application/json)
    ```json
    {
      "id": 1,
      "name": "Morgul",
      "rarirty": "Epic"
    }
    ```
  - Responses:
    - `200`: success
    - `400`: incorrect `id`
    - `404`: problems

- **GET** `/nft/hero/get`

  - Return hero inforamtion.

    - path params:
    - query params:
    - `id` integer, required: id of hero

  - Response sample: (application/json)
    ```json
    {
      "id": 1,
      "name": "Morgul",
      "rarirty": "Epic"
    }
    ```
  - Responses:
    - `200`: success
    - `400`: incorrect `id`
    - `404`: problems

- **GET** `/nft/hero/getall`

  - Return all hero inforamtion from `offset` to `offset + limit`.

    - path params:
    - query params:
      - `limit` integer, optional (by default `-1`, return all): max lengths of returned list
      - `offset` integer, optional (by default `0`): offset from zero

  - Response sample: (application/json)
    ```json
    [
      {
        "id": 1,
        "name": "Morgul",
        "rarirty": "Epic"
      },
      {
        "id": 3,
        "name": "Trom",
        "rarirty": "Legendary"
      }
    ]
    ```
  - Responses:
    - `200`: success
    - `400`: incorrect `limit` or `offset`
    - `404`: problems

- **POST** `/nft/hero/create`

  - Create hero with provided data
    - path params:
    - query params:
    - body: (application/json)
      ```json
      {
        "name": "Winchester",
        "rarity": "Rare"
      }
      ```
  - Response sample: (application/json)
    ```json
    {
      "id": 2,
      "name": "Winchester",
      "rarity": "Rare"
    }
    ```
  - Responses:
    - `200`: success
    - `400`: bad fields
    - `404`: problems

- **DELETE** `/nft/hero/remove`
  - Remove hero with id `id`
    - path params:
  - query params:
    - `id` integer, required: id of hero
  - Response sample: (application/json)
    ```json
    {
      "id": 1,
      "name": "Morgul",
      "rarirty": "Epic"
    }
    ```
  - Responses:
    - `200`: success
    - `400`: incorrect `id`
    - `404`: problems

#### Item

- **GET** `/nft/item/get`

  - Return item inforamtion.

    - path params:
    - query params:
      - `id` integer, required: id of item

  - Response sample: (application/json)
    ```json
    {
      "id": 1,
      "name": "Telescope",
      "max_level": 3
    }
    ```
  - Responses:
    - `200`: success
    - `400`: incorrect `id`
    - `404`: problems

- **GET** `/nft/item/getall`

  - Return all items inforamtion from `offset` to `offset + limit`.

    - path params:
    - query params:
      - `limit` integer, optional (by default `-1`, return all): max lengths of returned list
      - `offset` integer, optional (by default `0`): offset from zero

  - Response sample: (application/json)

    ```json
    [
      {
        "id": 1,
        "name": "Telescope",
        "max_level": 3
      },
      {
        "id": 3,
        "name": "Revolver",
        "max_level": 5
      }
    ]
    ```

  - Responses:
    - `200`: success
    - `400`: incorrect `limit` or `offset`
    - `404`: problems

- **POST** `/nft/item/create`

  - Create item with provided data.

    - path params:
    - query params:
    - body: (application/json)

    ```json
    {
      "name": "Gun",
      "max_level": 4
    }
    ```

  - Response sample: (application/json)
    ```json
    {
      "id": 2,
      "name": "Gun",
      "max_level": 4
    }
    ```
  - Responses:
    - `200`: success
    - `400`: bad fields
    - `404`: problems

- **DELETE** `/nft/item/remove`

  - Remove item with id `id`
    - path params:
    - query params:
      - `id` integer, required: id of item
  - Response sample: (application/json)

    ```json
    {
      "id": 2,
      "name": "Gun",
      "max_level": 4
    }
    ```

  - Responses:
    - `200`: success
    - `400`: incorrect `id`
    - `404`: problems

#### Spaceship

- **GET** `/nft/spaceship/get`

  - Return spaceship inforamtion.

    - path params:
    - query params:
      - `id` integer, required: id of spaceship

  - Response sample: (application/json)

    ```json
    {
      "id": 1,
      "name": "Starracer",
      "max_slots": 33
    }
    ```

  - Responses:
    - `200`: success
    - `400`: incorrect `id`
    - `404`: problems

- **GET** `/nft/spaceship/getall`

  - Return all spaceships inforamtion from `offset` to `offset + limit`.

    - path params:
    - query params:
      - `limit` integer, optional (by default `-1`, return all): max lengths of returned list
      - `offset` integer, optional (by default `0`): offset from zero

  - Response sample: (application/json)

    ```json
    [
      {
        "id": 1,
        "name": "Starracer",
        "max_slots": 33
      },
      {
        "id": 3,
        "name": "SpaceX",
        "max_slots": 49
      }
    ]
    ```

  - Responses:
    - `200`: success
    - `400`: incorrect `limit` or `offset`
    - `404`: problems

- **POST** `/nft/spaceship/create`

  - Create spaceship with provided data

    - path params:
    - query params:
    - body: (application/json)
      ```json
      {
        "name": "Craftship",
        "max_slots": 45
      }
      ```

  - Response sample: (application/json)

    ```json
    {
      "id": 2,
      "name": "Craftship",
      "max_slots": 45
    }
    ```

  - Responses:
    - `200`: success
    - `400`: bad fields
    - `404`: problems

- **DELETE** `/nft/spaceship/remove`

  - Remove spaceship with id `id`
    - path params:
  - query params:
    - `id` integer, required: id of spaceship
  - body:
  - Response sample: (application/json)
    ```json
    {
      "id": 2,
      "name": "Craftship",
      "max_slots": 45
    }
    ```
  - Responses:
    - `200`: success
    - `400`: incorrect `id`
    - `404`: problems

### Player

#### Inventory

- **GET** `/player/inventory/{type}`

  - Return list of object with `type`
    - path params:
      - `type` string, required (`hero` | `item` | `spaceship`): type of object
  - query params:
    - `address` string, required: address of player in blockchain
    - `compact` integer, optional (by default = 0): return _IDs_ of object if `compact` = 1, and _FULL_ if `compact` = 0
      - `limit` integer, optional (by default `-1`, return all): max lengths of returned list
      - `offset` integer, optional (by default `0`): offset from zero
  - Response sample: (application/json)

    ```json
    [
      {
        "id": 1,
        "name": "Starracer",
        "slots": 30
      },
      {
        "id": 1,
        "name": "Starracer",
        "slots": 21
      },
      {
        "id": 2,
        "name": "Craftship",
        "slots": 20
      },
      {
        "id": 3,
        "name": "SpaceX",
        "slots": 15
      }
    ]
    ```

    ```json
    [
      {
        "id": 1,
        "name": "Telescope",
        "level": 1
      },
      {
        "id": 3,
        "name": "Revolver",
        "level": 2
      }
    ]
    ```

  - Responses:
    - `200`: success
    - `400`: incorrect query pramas
    - `404`: problems

#### Craft

- **POST** `/player/craft/{type}`

  - Consumes from player two objects and give him third one
    - path param:
      - `type` string, required (`spacehip`): type of object
    - query params:
      - `address` string, required: address of player in blockchain
    - body: (application/json) 
    
      ```json
      [
        {
          "id": 2,
          "name": "Craftship",
          "max_slots": 45
        },
        {
          "id": 3,
          "name": "SpaceX",
          "max_slots": 10 
        },
        {
          "id": 2,
          "name": "Craftship",
          "max_slots": 50 
        }
      ]
      ```
  - Response sample: (application/json)

    ```json
    {
      "id": 2,
      "name": "Craftship",
      "max_slots": 50 
    }
    ```

  - Responses:
    - `200`: success
    - `400`: incorrect pramas
    - `404`: problems   

#### Reward

- **POST** `/player/reward`

  - Consumes from player two objects and give him third one
    - path param:
    - query params:
      - `address` string, required: address of player in blockchain
    - body: (application/json) 
    
      ```json
      {
        "reward": "1000000000000000000" // amount of tokens in uint
      }
      ```
  - Response sample: (application/json)

  - Responses:
    - `200`: success
    - `400`: incorrect pramas
    - `404`: problems  

## USER 

### PLAYER

#### Market

#### Buy Card Packs

#### Open Card
