# ![LOGO](logo.png) Car Configurator **flow**ground Connector

## Description

A generated **flow**ground connector for the Car Configurator API (version 1.0).

Generated from: https://api.apis.guru/v2/specs/mercedes-benz.com/configurator/1.0/swagger.json<br/>
Generated at: 2019-05-07T17:42:58+03:00

## API Description

The Car Configurator API offers access to the Mercedes-Benz car configuration functions. It provides required reference data such as the masterdata of all Mercedes-Benz vehicles as well as functions to retrieve initial and changed configurations. In addition to that is is possible to save a newly created configuration so that it can be easily restored or shared with others.

## Authorization

This API does not require authorization.

## Actions

### Get all available markets.

> Get all available `Markets`. Optional query params **language** or **country** may be used to filter the result.

*Tags:* `References`

#### Input Parameters
* `language` - _optional_ - This is a ISO language string e.g. 'de' and is spoken in Austria 'AT', Germany 'DE' and Swiss 'CH'.
* `country` - _optional_ - This is a ISO country string e.g. Germany 'DE' or Swiss 'CH'.
* `fieldsFilter` - _optional_ - Specifies which fields should be included in the result. If this filter is not used, per default all fields are returned.

### x_swagger_router_controller_markets

### Get the market with the given marketId.

> Gets the `Market` for the given **marketId**. There are no query parameters to filter the result.

*Tags:* `References`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `fieldsFilter` - _optional_ - Specifies which fields should be included in the result. If this filter is not used, per default all fields are returned.

### x_swagger_router_controller_markets__marketId_

### Get all available bodies for the given marketId.

> Get all available `VehicleBodies` for the given **marketId**. Optional query params **classId** **bodyId** or **productGroups** may be used to filter the result and must conform to the pattern [0-9A-Z_-]+.

*Tags:* `References`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `classId` - _optional_ - This is a class id e.g. '176' for 'A-Class' in Germany.
* `bodyId` - _optional_ - This is a body id e.g. '1' for 'Limousine' in Germany.
* `productGroups` - _optional_ - Specifies to which product groups the vehicles belong which should be returned. The product groups are separated from each other by a comma and are case sensitive. Allowed values are:
  * PKW
  * VAN
  * SMART
* `fieldsFilter` - _optional_ - Specifies which fields should be included in the result. If this filter is not used, per default all fields are returned.

### x_swagger_router_controller_markets__marketId__bodies

### Get the body for the given marketId and bodyId.

> Get the `VehicleBody` for the given **marketId** and **bodyId**.

*Tags:* `References`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `bodyId` - _required_ - This is a body id e.g. '1' for 'Limousine' in Germany.
* `fieldsFilter` - _optional_ - Specifies which fields should be included in the result. If this filter is not used, per default all fields are returned.

### x_swagger_router_controller_markets__marketId__bodies__bodyId_

### Get all available classes for the given marketId.

> Get all available `VehicleClasses` objects for the given **marketId**. Optional query params **classId**, **bodyId** or **productGroups** may be used to filter the result and must conform to the pattern [0-9A-Z_-]+.

*Tags:* `References`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `classId` - _optional_ - This is a class id e.g. '176' for 'A-Class' in Germany.
* `bodyId` - _optional_ - This is a body id e.g. '1' for 'Limousine' in Germany.
* `productGroups` - _optional_ - Specifies to which product groups the vehicles belong which should be returned. The product groups are separated from each other by a comma and are case sensitive. Allowed values are:
  * PKW
  * VAN
  * SMART
* `fieldsFilter` - _optional_ - Specifies which fields should be included in the result. If this filter is not used, per default all fields are returned.

### x_swagger_router_controller_markets__marketId__classes

### Get the class for the given marketId and classId.

> Get the `VehicleClass` for the given **marketId** and **classId**.

*Tags:* `References`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `classId` - _required_ - This is a class id e.g. '176' for 'A-Klasse' in Germany.
* `fieldsFilter` - _optional_ - Specifies which fields should be included in the result. If this filter is not used, per default all fields are returned.

### x_swagger_router_controller_markets__marketId__classes__classId_

### Get all available models for the given marketId.

> Get the available `VehicleModels` for the given **marketId**. Optional query params **classId**, **bodyId**, **baumuster4prefix**, **baumuster**, **nationalSalesType** or **productGroups** maybe used to filter the result. The baumuster4prefix must conform to the pattern [0-9]{4}.

*Tags:* `References`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `classId` - _optional_ - This is a class id e.g. '176' for 'A-Class' in Germany.
* `bodyId` - _optional_ - This is a body id e.g. '1' for 'Limousine' in Germany.
* `baumuster4prefix` - _optional_ - The first four digits of a baumuster are called baumuster4prefix e.g. '1760' for 'Berline' in France.
* `baumuster` - _optional_ - This is a baumuster e.g. '176042' for 'A 180 Limousine' in Germany.
* `nationalSalesType` - _optional_ - This is the national sales type (NST) of a distinct baumuster. There is no predefined pattern for the NST, each market defines its NST. e.g. 'E07' in France, 0001 in Germany and ZA1 in South Africa Using the NST markets can define market specific conditions. e.g. different initial configuration, etc.
* `productGroups` - _optional_ - Specifies to which product groups the vehicles belong which should be returned. The product groups are separated from each other by a comma and are case sensitive. Allowed values are:
  * PKW
  * VAN
  * SMART
* `fieldsFilter` - _optional_ - Specifies which fields should be included in the result. If this filter is not used, per default all fields are returned.

### x_swagger_router_controller_markets__marketId__models

### Get the model for the given marketId and modelId.

> Get the `VehicleModel` object for the given **marketId** and **modelId**.

*Tags:* `References`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `modelId` - _required_ - Minimal string that identifies a model e.g. '176042_002'. If no nationalSalesType is available, the modelId only consists of the baumuster e.g. '176042'.
* `fieldsFilter` - _optional_ - Specifies which fields should be included in the result. If this filter is not used, per default all fields are returned.

### x_swagger_router_controller_markets__marketId__models__modelId_

### Get the initial configuration for the given marketId and modelId.

> Get the initial `VehicleConfiguration` for the given **marketId** and **modelId**.

*Tags:* `Configurations`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `modelId` - _required_ - Minimal string that identifies a model e.g. '176042_002'. If no nationalSalesType is available, the modelId only consists of the baumuster e.g. '176042'.
* `fieldsFilter` - _optional_ - Specifies which fields should be included in the result. If this filter is not used, per default all fields are returned.

### x_swagger_router_controller_markets__marketId__models__modelId__configurations_initial

### Get the configuration for the given marketId, modelId and configurationId.

> Get the `VehicleConfiguration` for the given **marketId**, **modelId** and **configurationId**.

*Tags:* `Configurations`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `modelId` - _required_ - Minimal string that identifies a model e.g. '176042_002'. If no nationalSalesType is available, the modelId only consists of the baumuster e.g. '176042'.
* `configurationId` - _required_ - Minimal string that identifies a configuration e.g. 'E-D15-D18-D41-D46-D49-D52-D53-D54-D59-D60-D71-F32-F36-F88-F98-G03-G05-G36-G56-I61-J53-J67-L08-M23-M70-N18-N62-N92-O76-Q29-Q56-Q79-Q92-S01-S05-S08-S63-S92-T05-T07-T62-T84-T88_I-953_L-696_P-001_S-152-160-161-171-258-290-292-294-351-360-411-440-442-470-472-475-485-520-533-538-560-570-573-580-584-58U-591-620-70B-808-888-893-B03-B16-K11-L18-R43-U60'. A codeType is only once within the configurationId e.g 'S-152-160-161' stands for the components with the componentId 'S-152', 'S-160' and 'S-161'. A new codeType is divided from the codes with a underscore e.g 'S-152-160-161_I-953_L-696'.
* `fieldsFilter` - _optional_ - Specifies which fields should be included in the result. If this filter is not used, per default all fields are returned.

### x_swagger_router_controller_markets__marketId__models__modelId__configurations__configurationId_

### Get the alternatives for the given marketId, modelId, configurationId and componentList.

> Get the `VehicleAlternatives` for the given **marketId**, **modelId** and **configurationId** and the given **componentList** of changes.

*Tags:* `Configurations`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `modelId` - _required_ - Minimal string that identifies a model e.g. '176042_002'. If no nationalSalesType is available, the modelId only consists of the baumuster e.g. '176042'.
* `configurationId` - _required_ - Minimal string that identifies a configuration e.g. 'E-D15-D18-D41-D46-D49-D52-D53-D54-D59-D60-D71-F32-F36-F88-F98-G03-G05-G36-G56-I61-J53-J67-L08-M23-M70-N18-N62-N92-O76-Q29-Q56-Q79-Q92-S01-S05-S08-S63-S92-T05-T07-T62-T84-T88_I-953_L-696_P-001_S-152-160-161-171-258-290-292-294-351-360-411-440-442-470-472-475-485-520-533-538-560-570-573-580-584-58U-591-620-70B-808-888-893-B03-B16-K11-L18-R43-U60'. A codeType is only once within the configurationId e.g 'S-152-160-161' stands for the components with the componentId 'S-152', 'S-160' and 'S-161'. A new codeType is divided from the codes with a underscore e.g 'S-152-160-161_I-953_L-696'.
* `componentList` - _required_ - A string representing the changes, in other words a list of components that will be added and removed. The following syntax is used for the components to be added and the components to be removed. The added components e.g. '+I-950_L-890' and the removed components e.g. '-I-953_L-696' and the delimiter between the added and removed components is ','. In one components string '+I-950_L-890,-I-953_L-696'.
* `fieldsFilter` - _optional_ - Specifies which fields should be included in the result. If this filter is not used, per default all fields are returned.

### x_swagger_router_controller_markets__marketId__models__modelId__configurations__configurationId__alternatives__componentList_

### Returns URLs pointing to images in JPG format in the highest available resolution (depending on the component) of the vehicle's:<br/>
>   * engine (1024x576 px),<br/>
>   * rim (710x710 px),<br/>
>   * trim (800x600 px),<br/>
>   * paints (800x600 px),<br/>
>   * upholstery (800x600 px) and<br/>
>   * equipments (740x416 px).

*Tags:* `Images`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `modelId` - _required_ - Minimal string that identifies a model e.g. '176042_002'. If no nationalSalesType is available, the modelId only consists of the baumuster e.g. '176042'.
* `configurationId` - _required_ - Minimal string that identifies a configuration e.g. 'E-D15-D18-D41-D46-D49-D52-D53-D54-D59-D60-D71-F32-F36-F88-F98-G03-G05-G36-G56-I61-J53-J67-L08-M23-M70-N18-N62-N92-O76-Q29-Q56-Q79-Q92-S01-S05-S08-S63-S92-T05-T07-T62-T84-T88_I-953_L-696_P-001_S-152-160-161-171-258-290-292-294-351-360-411-440-442-470-472-475-485-520-533-538-560-570-573-580-584-58U-591-620-70B-808-888-893-B03-B16-K11-L18-R43-U60'. A codeType is only once within the configurationId e.g 'S-152-160-161' stands for the components with the componentId 'S-152', 'S-160' and 'S-161'. A new codeType is divided from the codes with a underscore e.g 'S-152-160-161_I-953_L-696'.

### x_swagger_router_controller_markets__marketId__models__modelId__configurations__configurationId__images_components

### Returns a URL pointing to an image of the vehicles engine.  These images are available in the resolution 1024x576 px.

*Tags:* `Images`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `modelId` - _required_ - Minimal string that identifies a model e.g. '176042_002'. If no nationalSalesType is available, the modelId only consists of the baumuster e.g. '176042'.
* `configurationId` - _required_ - Minimal string that identifies a configuration e.g. 'E-D15-D18-D41-D46-D49-D52-D53-D54-D59-D60-D71-F32-F36-F88-F98-G03-G05-G36-G56-I61-J53-J67-L08-M23-M70-N18-N62-N92-O76-Q29-Q56-Q79-Q92-S01-S05-S08-S63-S92-T05-T07-T62-T84-T88_I-953_L-696_P-001_S-152-160-161-171-258-290-292-294-351-360-411-440-442-470-472-475-485-520-533-538-560-570-573-580-584-58U-591-620-70B-808-888-893-B03-B16-K11-L18-R43-U60'. A codeType is only once within the configurationId e.g 'S-152-160-161' stands for the components with the componentId 'S-152', 'S-160' and 'S-161'. A new codeType is divided from the codes with a underscore e.g 'S-152-160-161_I-953_L-696'.

### x_swagger_router_controller_markets__marketId__models__modelId__configurations__configurationId__images_components_engine

### Returns URLs pointing to images of this vehicle's equipments. The images are available in the highest possible resolution (usually 740x416 px).

*Tags:* `Images`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `modelId` - _required_ - Minimal string that identifies a model e.g. '176042_002'. If no nationalSalesType is available, the modelId only consists of the baumuster e.g. '176042'.
* `configurationId` - _required_ - Minimal string that identifies a configuration e.g. 'E-D15-D18-D41-D46-D49-D52-D53-D54-D59-D60-D71-F32-F36-F88-F98-G03-G05-G36-G56-I61-J53-J67-L08-M23-M70-N18-N62-N92-O76-Q29-Q56-Q79-Q92-S01-S05-S08-S63-S92-T05-T07-T62-T84-T88_I-953_L-696_P-001_S-152-160-161-171-258-290-292-294-351-360-411-440-442-470-472-475-485-520-533-538-560-570-573-580-584-58U-591-620-70B-808-888-893-B03-B16-K11-L18-R43-U60'. A codeType is only once within the configurationId e.g 'S-152-160-161' stands for the components with the componentId 'S-152', 'S-160' and 'S-161'. A new codeType is divided from the codes with a underscore e.g 'S-152-160-161_I-953_L-696'.

### x_swagger_router_controller_markets__marketId__models__modelId__configurations__configurationId__images_components_equipments

### Returns URLs pointing to images of this vehicle's equipments. The images are available in the highest possible resolution (usually 740x416 px).

*Tags:* `Images`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `modelId` - _required_ - Minimal string that identifies a model e.g. '176042_002'. If no nationalSalesType is available, the modelId only consists of the baumuster e.g. '176042'.
* `configurationId` - _required_ - Minimal string that identifies a configuration e.g. 'E-D15-D18-D41-D46-D49-D52-D53-D54-D59-D60-D71-F32-F36-F88-F98-G03-G05-G36-G56-I61-J53-J67-L08-M23-M70-N18-N62-N92-O76-Q29-Q56-Q79-Q92-S01-S05-S08-S63-S92-T05-T07-T62-T84-T88_I-953_L-696_P-001_S-152-160-161-171-258-290-292-294-351-360-411-440-442-470-472-475-485-520-533-538-560-570-573-580-584-58U-591-620-70B-808-888-893-B03-B16-K11-L18-R43-U60'. A codeType is only once within the configurationId e.g 'S-152-160-161' stands for the components with the componentId 'S-152', 'S-160' and 'S-161'. A new codeType is divided from the codes with a underscore e.g 'S-152-160-161_I-953_L-696'.
* `componentCode` - _required_ - The value of the requested component group, e.g. '245'.

### x_swagger_router_controller_markets__marketId__models__modelId__configurations__configurationId__images_components_equipments__componentCode_

### Returns URLs pointing to images of this vehicles paint.  These images are available in resolution 800x600 px.  Note there might be two paints (e.g. Smart, 'paint' for body panel and 'paint2' for the tridion cell)

*Tags:* `Images`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `modelId` - _required_ - Minimal string that identifies a model e.g. '176042_002'. If no nationalSalesType is available, the modelId only consists of the baumuster e.g. '176042'.
* `configurationId` - _required_ - Minimal string that identifies a configuration e.g. 'E-D15-D18-D41-D46-D49-D52-D53-D54-D59-D60-D71-F32-F36-F88-F98-G03-G05-G36-G56-I61-J53-J67-L08-M23-M70-N18-N62-N92-O76-Q29-Q56-Q79-Q92-S01-S05-S08-S63-S92-T05-T07-T62-T84-T88_I-953_L-696_P-001_S-152-160-161-171-258-290-292-294-351-360-411-440-442-470-472-475-485-520-533-538-560-570-573-580-584-58U-591-620-70B-808-888-893-B03-B16-K11-L18-R43-U60'. A codeType is only once within the configurationId e.g 'S-152-160-161' stands for the components with the componentId 'S-152', 'S-160' and 'S-161'. A new codeType is divided from the codes with a underscore e.g 'S-152-160-161_I-953_L-696'.

### x_swagger_router_controller_markets__marketId__models__modelId__configurations__configurationId__images_components_paint

### Returns a URL pointing to an image of the vehicles rim.  These images are available in the resolution 710x710 px.

*Tags:* `Images`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `modelId` - _required_ - Minimal string that identifies a model e.g. '176042_002'. If no nationalSalesType is available, the modelId only consists of the baumuster e.g. '176042'.
* `configurationId` - _required_ - Minimal string that identifies a configuration e.g. 'E-D15-D18-D41-D46-D49-D52-D53-D54-D59-D60-D71-F32-F36-F88-F98-G03-G05-G36-G56-I61-J53-J67-L08-M23-M70-N18-N62-N92-O76-Q29-Q56-Q79-Q92-S01-S05-S08-S63-S92-T05-T07-T62-T84-T88_I-953_L-696_P-001_S-152-160-161-171-258-290-292-294-351-360-411-440-442-470-472-475-485-520-533-538-560-570-573-580-584-58U-591-620-70B-808-888-893-B03-B16-K11-L18-R43-U60'. A codeType is only once within the configurationId e.g 'S-152-160-161' stands for the components with the componentId 'S-152', 'S-160' and 'S-161'. A new codeType is divided from the codes with a underscore e.g 'S-152-160-161_I-953_L-696'.

### x_swagger_router_controller_markets__marketId__models__modelId__configurations__configurationId__images_components_rim

### Returns a URL pointing to an image of this vehicles trim.  These images are available in resolution 800x600 px.

*Tags:* `Images`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `modelId` - _required_ - Minimal string that identifies a model e.g. '176042_002'. If no nationalSalesType is available, the modelId only consists of the baumuster e.g. '176042'.
* `configurationId` - _required_ - Minimal string that identifies a configuration e.g. 'E-D15-D18-D41-D46-D49-D52-D53-D54-D59-D60-D71-F32-F36-F88-F98-G03-G05-G36-G56-I61-J53-J67-L08-M23-M70-N18-N62-N92-O76-Q29-Q56-Q79-Q92-S01-S05-S08-S63-S92-T05-T07-T62-T84-T88_I-953_L-696_P-001_S-152-160-161-171-258-290-292-294-351-360-411-440-442-470-472-475-485-520-533-538-560-570-573-580-584-58U-591-620-70B-808-888-893-B03-B16-K11-L18-R43-U60'. A codeType is only once within the configurationId e.g 'S-152-160-161' stands for the components with the componentId 'S-152', 'S-160' and 'S-161'. A new codeType is divided from the codes with a underscore e.g 'S-152-160-161_I-953_L-696'.

### x_swagger_router_controller_markets__marketId__models__modelId__configurations__configurationId__images_components_trim

### Returns URLs pointing to images of the vehicle's upholsteries. Tge images are available in the highest possible resolution (usually 800x600 px).

*Tags:* `Images`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `modelId` - _required_ - Minimal string that identifies a model e.g. '176042_002'. If no nationalSalesType is available, the modelId only consists of the baumuster e.g. '176042'.
* `configurationId` - _required_ - Minimal string that identifies a configuration e.g. 'E-D15-D18-D41-D46-D49-D52-D53-D54-D59-D60-D71-F32-F36-F88-F98-G03-G05-G36-G56-I61-J53-J67-L08-M23-M70-N18-N62-N92-O76-Q29-Q56-Q79-Q92-S01-S05-S08-S63-S92-T05-T07-T62-T84-T88_I-953_L-696_P-001_S-152-160-161-171-258-290-292-294-351-360-411-440-442-470-472-475-485-520-533-538-560-570-573-580-584-58U-591-620-70B-808-888-893-B03-B16-K11-L18-R43-U60'. A codeType is only once within the configurationId e.g 'S-152-160-161' stands for the components with the componentId 'S-152', 'S-160' and 'S-161'. A new codeType is divided from the codes with a underscore e.g 'S-152-160-161_I-953_L-696'.

### x_swagger_router_controller_markets__marketId__models__modelId__configurations__configurationId__images_components_upholstery

### Returns URLs pointing to PNG images of a vehicle with a white background.

*Tags:* `Images`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `modelId` - _required_ - Minimal string that identifies a model e.g. '176042_002'. If no nationalSalesType is available, the modelId only consists of the baumuster e.g. '176042'.
* `configurationId` - _required_ - Minimal string that identifies a configuration e.g. 'E-D15-D18-D41-D46-D49-D52-D53-D54-D59-D60-D71-F32-F36-F88-F98-G03-G05-G36-G56-I61-J53-J67-L08-M23-M70-N18-N62-N92-O76-Q29-Q56-Q79-Q92-S01-S05-S08-S63-S92-T05-T07-T62-T84-T88_I-953_L-696_P-001_S-152-160-161-171-258-290-292-294-351-360-411-440-442-470-472-475-485-520-533-538-560-570-573-580-584-58U-591-620-70B-808-888-893-B03-B16-K11-L18-R43-U60'. A codeType is only once within the configurationId e.g 'S-152-160-161' stands for the components with the componentId 'S-152', 'S-160' and 'S-161'. A new codeType is divided from the codes with a underscore e.g 'S-152-160-161_I-953_L-696'.
* `perspectives` - _optional_ - One or more perspectives as a comma separated String list e.g. 'EXT000,EXT010,INT1'.  The following perspectives are available:
  * EXT000-EXT350: EXT000 defines the front view, EXT010 defines a rotation of 10 degress and so forth.
  * INT1-INT4: These are the 4 available interior perspectives.

The default value is EXT020,INT1 if no value is provided.
* `roofOpen` - _optional_ - Set 'true', if you are looking for images with the roof open. This option is only valid for cabrios. Default is 'false'.
* `night` - _optional_ - Set 'true', if you are looking for images with a darker background and the vehicle's headlights turned on. Default is 'false'.

### x_swagger_router_controller_markets__marketId__models__modelId__configurations__configurationId__images_vehicle

### Get the selectable components for the given marketId, modelId and configurationId.

> Get the selectable `VehicleComponents` and the `ComponentCategories` of the `VehicleConfiguration` for the given **marketId**, **modelId** and **configurationId**. Optional query param **componentType** may be used to filter the result.

*Tags:* `Configurations`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `modelId` - _required_ - Minimal string that identifies a model e.g. '176042_002'. If no nationalSalesType is available, the modelId only consists of the baumuster e.g. '176042'.
* `configurationId` - _required_ - Minimal string that identifies a configuration e.g. 'E-D15-D18-D41-D46-D49-D52-D53-D54-D59-D60-D71-F32-F36-F88-F98-G03-G05-G36-G56-I61-J53-J67-L08-M23-M70-N18-N62-N92-O76-Q29-Q56-Q79-Q92-S01-S05-S08-S63-S92-T05-T07-T62-T84-T88_I-953_L-696_P-001_S-152-160-161-171-258-290-292-294-351-360-411-440-442-470-472-475-485-520-533-538-560-570-573-580-584-58U-591-620-70B-808-888-893-B03-B16-K11-L18-R43-U60'. A codeType is only once within the configurationId e.g 'S-152-160-161' stands for the components with the componentId 'S-152', 'S-160' and 'S-161'. A new codeType is divided from the codes with a underscore e.g 'S-152-160-161_I-953_L-696'.
* `componentTypes` - _optional_ - A list of component types separated by a comma case insensitive. If nothing is defined all component types are returned. Allowed values are:
  - WHEELS
  - PAINTS
  - UPHOLSTERIES
  - TRIMS
  - PACKAGES
  - LINES
  - SPECIAL_EDITION
  - SPECIAL_EQUIPMENT
* `fieldsFilter` - _optional_ - Specifies which fields should be included in the result. If this filter is not used, per default all fields are returned.

### x_swagger_router_controller_markets__marketId__models__modelId__configurations__configurationId__selectables

### Stores the configuration of the given configurationId and modelId

> Stores the configuration of the given **configurationId** and **modelId**

*Tags:* `Saved configurations`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.

### x_swagger_router_controller_markets__marketId__onlinecode

### Get the configuration of the given onlineCode and marketId.

> Gets the configuration for the given marketId and onlineCode.

*Tags:* `Saved configurations`

#### Input Parameters
* `onlineCode` - _required_ - OnlineCode string that identifies a vehicle configuration e.g. 'M6882554'.
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `fieldsFilter` - _optional_ - Specifies which fields should be included in the result. If this filter is not used, per default all fields are returned.

### x_swagger_router_controller_markets__marketId__onlinecode__onlineCode_

### Get all configured active product groups for the given marketId.

> Get all configured active product groups for the given **marketId**.

*Tags:* `References`

#### Input Parameters
* `marketId` - _required_ - This is a ISO 3166 language country string e.g. 'de_DE' or 'en_GB'.
* `fieldsFilter` - _optional_ - Specifies which fields should be included in the result. If this filter is not used, per default all fields are returned.

### x_swagger_router_controller_markets__marketId__productgroups

## License

**flow**ground :- Telekom iPaaS / mercedes-benz-com-configurator-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
