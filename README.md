# LandBroker MLS Feeds API Documentation

## Overview

This API allows you to retrieve properties based on specified query parameters. The feed returns all current and past properties that are active, under contract, sold, expired, and withdrawn.

## Base URL

```
https://feeds.app.landbrokermls.com
```

## Authentication

Ensure that you include the necessary authentication headers in your requests.

- **x-data-api-key**: Your API Key

#### Example Header

```bash
-H "x-data-api-key: your_api_key"
```

## Endpoints

### Get CamoAG Properties

#### Request

- **Method**: GET
- **Endpoint**: `/pt/camo-ag`
- **Query Parameters**:

  - `page` (optional): page number
  - `last_modified` (optional): Last modified date for filtering (Format: yyyy-mm-dd).

#### Example Request

```bash
curl -X GET "https://feeds.app.landbrokermls.com/pt/camo-ag?page=1&last_modified=2022-01-11" -H "x-data-api-key: your_api_key"
```

#### Responses

- **200 OK**: Successfully retrieved properties.
  - Example Response Body:

    ```json
    {
      "total": 1,
      "current_page": 1,
      "properties": [
        {
          "acreagesize": "5.58",
          "address1": "CR 150 ",
          "agent": {
              "agent-email": "info@trinityranchland.com",
              "agent-id": 82012,
              "agent-name": "Karen Lenz",
              "agent-phone": "(254) 725-4181"
          },
          "arialmapimage": "https://property-photos-eastwood.s3.us-east-2.amazonaws.com/propdocs/1070945_c1d1b3ec-601a-487b-9550-4c391c27218b.pdf",
          "bathrooms": "0",
          "brokerage": {
              "brokerage-name":"Trinity Ranch Land",
              "brokerage-email":"info@trinityranchland.com",
              "brokerage-id":"82012",
              "brokerage-phone":"(254) 725-4181",
              "brokerage-website":"www.trinityranchland.com",
              "brokerage-address": {}
          },
          "city": "Abilene",
          "country": "United States",
          "county": "Shackelford",
          "description": "These prime home tracts are conveniently located approx. 5 miles from Chick-Fil-A, Tractor Supply, Starbucks, Lowe's, Wal-Mart, Hooters, and more! All the convenience of the country with the unprecedented plethora of amenities just moments away. These tracts have Hamby water available, as well as electricity. A survey has already been completed. Owner financing is available with the seller's approval and $8,500 down. The property is restricted but mobile homes and manufactured homes are allowed. (See restrictions) Call today for your showing!!\n\n**Buyer's representative to verify all utilities and school districts.\n\n**Trinity Ranch Land, LLC gladly participates with other brokers. Buyer's agent must accompany buyer at first showing to receive full buyer's agent commission.\n\nAt Trinity Ranch Land, LLC we strive to bring you accurate, informative and relevant information in a readable and understandable manner. We do not assume liability for typographical errors, misprints or misinformation that may have been given us, nor do we guarantee its reliability. All property is subject to change, withdrawal or prior sale. We will assist all buyers in verifying the above information to the best of our ability.**",
          "features": [
          "Electricity",
          "Hwy-County Rd Frontage"
          ],
          "images": [
              {
              "url": "https://property-photos-eastwood.s3.us-east-2.amazonaws.com/propImages/1070945_39d95a9f-eca7-47de-bf09-22ac0fe18986.JPG"
              },
              {
              "url": "https://property-photos-eastwood.s3.us-east-2.amazonaws.com/propImages/1070945_686bc1f9-4829-484b-8a09-b81c4f1583e1.JPG"
              },
              {
              "url": "https://property-photos-eastwood.s3.us-east-2.amazonaws.com/propImages/1070945_724a8d3e-79b8-4ff6-93e3-cb54b2900c63.JPG"
              },
              {
              "url": "https://property-photos-eastwood.s3.us-east-2.amazonaws.com/propImages/1070945_83cb76a8-e517-4b59-9f94-76dff7804a47.JPG"
              },
              {
              "url": "https://property-photos-eastwood.s3.us-east-2.amazonaws.com/propImages/1070945_b6624e4f-5aa0-4639-9618-5ecdb0ca2110.JPG"
              },
              {
              "url": "https://property-photos-eastwood.s3.us-east-2.amazonaws.com/propImages/1070945_4cc38da6-8e25-41d2-9482-e35de67c2f25.JPG"
              },
              {
              "url": "https://property-photos-eastwood.s3.us-east-2.amazonaws.com/propImages/1070945_c2aeb2bd-e6e6-441a-9e3f-bc82a9f8634b.JPG"
              },
              {
              "url": "https://property-photos-eastwood.s3.us-east-2.amazonaws.com/propImages/1070945_ad07e7c1-5194-4974-a6c4-132db2796519.JPG"
              },
              {
              "url": "https://property-photos-eastwood.s3.us-east-2.amazonaws.com/propImages/1070945_379212a1-7048-4f72-b9a3-50f44b5a0ef1.JPG"
              },
              {
              "url": "https://property-photos-eastwood.s3.us-east-2.amazonaws.com/propImages/1070945_44e02812-0651-40e1-bd3c-e0c4901d30ed.JPG"
              },
              {
              "url": "https://property-photos-eastwood.s3.us-east-2.amazonaws.com/propImages/1070945_0fe7cb2c-1d36-4056-b433-a38aa6507833.JPG"
              }
          ],
          "last_modified": "2024-01-16",
          "latitude": "32.5185",
          "ldxid": 82012,
          "listdate": "2022-12-06",
          "locationmapimage": "https://property-photos-eastwood.s3.us-east-2.amazonaws.com/propdocs/1070945_29fd9734-037a-4501-8e8e-12af6ffd307c.pdf",
          "longitude": "-99.6119",
          "price": 78000,
          "propdocs": [
              {
              "url": "https://property-photos-eastwood.s3.us-east-2.amazonaws.com/propdocs/1070945_91eaa2f1-7b89-47ee-8549-232a90ac941c.pdf"
              },
              {
              "url": "https://property-photos-eastwood.s3.us-east-2.amazonaws.com/propdocs/1070945_b11df204-cc5f-4cd7-a34e-573d99a76855.pdf"
              }
          ],
          "propid": 1070945,
          "schooldistrict": "Clyde Cons I.S.D.",
          "sqftsize": "0",
          "state": "Texas",
          "status": "Under Contract",
          "terrain": "Flat",
          "terrastridemapurl": "https://mapright.com/ranching/maps/1b0172ad5ade7c24f1022a5016cf5a45/share",
          "title": "Under Contract!! 5.58 Ac CR 150, Abilene (Tract 1)",
          "tractmapimage": "https://property-photos-eastwood.s3.us-east-2.amazonaws.com/propdocs/1070945_efc636e7-33de-4068-b799-9c350a0ec048.pdf",
          "types": [
              "Acreage"
          ],
          "zip": "79601",
          "zoning": "No Zoning"
      }
     ]
    }
    ```

- **400 Bad Request**: Invalid request parameters.
  - Example Response Body:

    ```json
    {
      "error": "Expected valid date format yyyy-mm-dd"
    }
    ```

- **500 Internal Server Error**: Server encountered an error.

## Response Fields

1. **total**: Total number of properties in the response. In this case, there is 1 property.

2. **current_page**: Current page number in the pagination. Here, it's page 1.

3. **properties**: An array containing property details. Each element in the array represents a property.

   - **acreagesize**: Size of the acreage (e.g., "5.58").
   - **address1**: Street address (e.g., "CR 150").
   - **agent**: Details about the agent associated with the property.

     - **agent-email**: Email of the agent.
     - **agent-id**: ID of the agent.
     - **agent-name**: Name of the agent.
     - **agent-phone**: Phone number of the agent.

   - **arialmapimage**: URL to an aerial map image related to the property.

   - **bathrooms**: Number of bathrooms in the property (e.g., "0").

   - **brokerage**: Details about the brokerage associated with the property.
     - **brokerage-name**: Name of the brokerage.
     - **brokerage-email**: Email of the brokerage.
     - **brokerage-id**: ID of the brokerage.
     - **brokerage-address**: Brokerage Address Details
       - **brokerage-street-address**: Brokerage street address.
       - **brokerage-city-name**: Brokerage city name.
       - **brokerage-zipcode**: Brokerage zipcode.
       - **brokerage-state-code**: Brokerage State

   - **city**: City where the property is located (e.g., "Abilene").

   - **country**: Country where the property is located (e.g., "United States").

   - **county**: County where the property is located (e.g., "Shackelford").

   - **description**: Detailed description of the property, including information about amenities, utilities, financing options, restrictions, and more.

   - **features**: An array of features associated with the property from the below list:
      - Lake Frontage
      - Creek
      - Irrigated
      - Spring
      - Hunting
      - Equine Facilities
      - Orchard
      - Vineyard
      - Pivot Irrigation
      - Home
      - Grain Storage
      - Overhead Feed Bins
      - Corrals
      - Livestock Scales
      - Arena
      - Barn
      - Work Shop
      - Wildlife Feeders
      - Landing Strip
      - Water Well
      - Game-Proof Fence
      - Electricity
      - Rural Water
      - Hwy-County Rd Frontage
      - Lake
      - Lodge
      - Development Potential
      - Feedlot
      - River
      - River Frontage
      - Minerals
      - Timber
      - National Forest Access
      - Borders National Forest
      - Borders State/BLM Land
      - Guest Ranch
      - Water Rights
      - Cabins
      - Borders Corp of Engineer Land
      - Pond
      - Fishing
      - Coastline
      - Ocean Frontage
      - Beach
      - Hunt Club Shares
      - Owner Financing

   - **images**: An array containing URLs to property images.

   - **last_modified**: Last modified date of the property.

   - **latitude**: Latitude coordinate of the property (e.g., "32.5185").

   - **listdate**: Listing date of the property (e.g., "2022-12-06").

   - **locationmapimage**: URL to an image related to the property's location.

   - **longitude**: Longitude coordinate of the property (e.g., "-99.6119").

   - **price**: Price of the property (e.g., 78000).

   - **propdocs**: An array containing URLs to property documents.

   - **propid**: Property ID (e.g., 1070945).

   - **schooldistrict**: School district associated with the property (e.g., "Clyde Cons I.S.D.").

   - **sqftsize**: Size of the property in square feet (e.g., "0").

   - **state**: State where the property is located (e.g., "Texas").

   - **status**: Status of the property ("Active", "Under Contract", "Sold", "Withdrawn", "Expired").

   - **terrain**: Terrain information for the property (e.g., "Flat").

   - **terrastridemapurl**: URL to a terrain map related to the property.

   - **title**: Title or name of the property (e.g., "Under Contract!! 5.58 Ac CR 150, Abilene (Tract 1)").

   - **tractmapimage**: URL to an image related to the property's tract map.

   - **types**: An array of property types from the below list:
      - Farm
      - Ranch
      - Acreage
      - Recreational Land
      - Farm Auction
      - Ranch Auction
      - Land Auction
      - Commercial Acreage
      - Hunting Land
      - Fishing Land
      - Equestrian Property
      - Mountain Land
      - Coastal Property
      - River Frontage
      - Timberland
      - Rural Business
      - Agriculture Business
      - Home with Acreage
      - Cattle Ranch
      - Vineyard
      - Home
      - Resort
      - Condo/Townhome
      - Lake Frontage

   - **zip**: ZIP code of the property (e.g., "79601").

   - **zoning**: Zoning information for the property (e.g., "No Zoning").


## Notes

- Pagination is applied with a default page size of 100 items.
- When using the `last_modified` parameter, the properties are sorted in ascending order based on the last modified date.

