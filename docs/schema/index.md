# Neptune EEW Schema

**Data Models for Neptune EEW**

_version: 1.5.0_

## EEWDevice

An Early Earthquake Warning Device

- `areaServed`: The geographic area where a service or offered item is provided
  - Attribute type: **Property**. [Text](https://schema.org/Text)
  - Optional
- `category`: Sensor: A device that detects and responds to events or changes in the physical environment such as light, motion, or temperature changes. https://w3id.org/saref#Sensor.
  - Attribute type: **Property**. [Text](https://schema.org/Text)
  - Optional
- `configuration`: Device's technical configuration. This attribute is intended to be a array properties and their values which capture parameters which have to do with the configuration of a device (timeouts, reporting periods, etc.) and which are not currently covered by the standard attributes defined by this model.
  - Attribute type: **Property**. [StructuredValue](https://schema.org/StructuredValue)
  - Optional
- `dateCreated`: Entity creation timestamp. This will usually be allocated by the storage platform.
  - Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
  - Optional
- `dateFirstUsed`: A timestamp which denotes when the device was first used.
  - Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
  - Optional
- `dateInstalled`: A timestamp which denotes when the device was installed (if it requires installation).
  - Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
  - Optional
- `dateLastCalibration`: A timestamp which denotes when the last calibration of the device happened.
  - Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
  - Optional
- `dateLastValueReported`: A timestamp which denotes the last time when the device successfully reported data to the cloud.
  - Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
  - Optional
- `dateManufactured`: A timestamp which denotes when the device was manufactured.
  - Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
  - Optional
- `dateModified`: Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.
  - Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
  - Optional
- `dateObserved`: Date of the observed entity defined by the user.
  - Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
  - Optional
- `depth`: Location of this device represented by a depth from a starting point. All units are accepted in [CEFACT](https://www.unece.org/cefact.html) code
  - Attribute type: **Property**. [depth](https://schema.org/depth)
  - Optional
- `description`: A description of this item
  - Attribute type: **Property**.
  - Optional
- `deviceState`: State of this device from an operational point of view. Its value can be vendor dependent.
  - Attribute type: **Property**. [Text](https://schema.org/Text)
  - Optional
- `elevation`: Elevation (in meters) at the spot the device is installed.
  - Attribute type: **Property**. [elevation](https://schema.org/elevation)
  - Optional
- `firmwareVersion`: The firmware version of this device.
  - Attribute type: **Property**. [Text](https://schema.org/Text)
  - Optional
- `hardwareVersion`: The hardware version of this device.
  - Attribute type: **Property**. [Text](https://schema.org/Text)
  - Optional
- `id`: Unique identifier of the entity
  - Attribute type: **Property**.
  - Required
- `location`: Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon
  - Attribute type: **Geoproperty**.
  - Optional
- `macAddress`: The MAC address of the device.
  - Attribute type: **Property**. [Text](https://schema.org/Text)
  - Optional
- `mcc`: This property identifies the Mobile Country Code
  - Attribute type: **Property**. [Text](https://schema.org/Text)
  - Optional
- `mnc`: This property identifies the Mobile Network Code (MNC) of the network the device is attached to. The MNC is used in combination with a Mobile Country Code (MCC) (also known as a 'MCC / MNC tuple') to uniquely identify a mobile phone operator/carrier using the GSM, CDMA, iDEN, TETRA and 3G / 4G public land mobile networks and some satellite mobile networks.
  - Attribute type: **Property**. [Text](https://schema.org/Text)
  - Optional
- `name`: The name of this item.
  - Attribute type: **Property**. [Text](https://schema.org/Text)
  - Optional
- `osVersion`: The version of the host operating system device.
  - Attribute type: **Property**. [Text](https://schema.org/Text)
  - Optional
- `owner`: A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)
  - Attribute type: **Property**.
  - Optional
- `rssi`: Received signal strength indicator for a wireless enabled device. It must be expressed in dBm or mW, use unitcode to set it out.
  - Attribute type: **Property**. [Number](https://schema.org/Number)
  - Optional
- `seeAlso`: list of uri pointing to additional resources about the item
  - Attribute type: **Property**.
  - Optional
- `serialNumber`: The serial number assigned by the manufacturer.
  - Attribute type: **Property**. [serialNumber](https://schema.org/serialNumber)
  - Optional
- `softwareVersion`: The software version of this device.
  - Attribute type: **Property**. [Text](https://schema.org/Text)
  - Optional
- `source`: A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object.
  - Attribute type: **Property**. [URL](https://schema.org/URL)
  - Optional
- `supportedProtocol`: Supported protocol(s) or networks
  - Attribute type: **Property**. [3g, bluetooth, bluetooth LE, cat-m, coap, ec-gsm-iot, gprs, http, lwm2m, lora, lte-m, mqtt, nb-iot, onem2m, sigfox, ul20, websocket](3g, bluetooth, bluetooth LE, cat-m, coap, ec-gsm-iot, gprs, http, lwm2m, lora, lte-m, mqtt, nb-iot, onem2m, sigfox, ul20, websocket)
  - Optional
- `type`: NGSI Entity type. It has to be Device. One of : `Device`.
  - Attribute type: **Property**.
  - Required

## Event

- `id`: Unique identifier of the entity
  - Attribute type: **Property**.
  - Required
- `type`: NGSI Entity type. It has to be Event. One of : `Event`.
  - Attribute type: **Property**.
  - Required
- `publicId`:
  - Attribute type: **Property**. [URL](https://schema.org/URL)
  - Optional
- `eventType`: . One of : `not existing`, `not reported`, `earthquake`.
  - Attribute type: **EnumProperty**. [Text](https://schema.org/Text)
  - Optional

## Origin

- `id`: Unique identifier of the entity
  - Attribute type: **Property**.
  - Required
- `type`: NGSI Entity type. It has to be Origin. One of : `Origin`.
  - Attribute type: **Property**.
  - Required
- `publicId`:
  - Attribute type: **Property**. [URL](https://schema.org/URL)
  - Optional
- `time`:
  - Attribute type: **Property**.
  - Optional
- `location`:
  - Attribute type: **GeoProperty**. [Point](https://purl.org/geojson/vocab#Point)
  - Optional
  - Normative References: http://geojson.org/geojson-spec.html#geometry-objects
- `latitude`:
  - Attribute type: **Property**.
  - Optional
- `longitude`:
  - Attribute type: **Property**.
  - Optional
- `depth`:
  - Attribute type: **Property**.
  - Optional
- `associatedEvent`:
  - Attribute type: **Relationship**. [URL](https://schema.org/URL)
  - Optional

## Magnitude

- `id`: Unique identifier of the entity
  - Attribute type: **Property**.
  - Required
- `type`: NGSI Entity type. It has to be Magnitude. One of : `Magnitude`.
  - Attribute type: **Property**.
  - Required
- `publicId`:
  - Attribute type: **Property**. [URL](https://schema.org/URL)
  - Optional
- `mag`:
  - Attribute type: **Property**.
  - Optional
- `associatedEvent`:
  - Attribute type: **Relationship**. [URL](https://schema.org/URL)
  - Optional

## Pick

- `id`: Unique identifier of the entity
  - Attribute type: **Property**.
  - Required
- `type`: NGSI Entity type. It has to be Pick. One of : `Pick`.
  - Attribute type: **Property**.
  - Required
- `publicId`:
  - Attribute type: **Property**. [URL](https://schema.org/URL)
  - Optional
- `time`:
  - Attribute type: **Property**.
  - Optional
- `waveformId`:
  - Attribute type: **Property**.
  - Optional
- `associatedEvent`:
  - Attribute type: **Relationship**. [URL](https://schema.org/URL)
  - Optional
