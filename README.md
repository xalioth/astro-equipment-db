# astro-equipment-db

An open and collaborative data base of astronomical equipments

## Concepts

The data base is a simple file tree containings json files. Each file describes an item, and must be named after the item id. Item can be of the following types (and must be located is the directory corresponding to there type):

 * Equipment: description of an equipment such as a telescope, a mount or binoculars. Each Equipment has an EquipmentType (e.g. telescope, mount, binoculars etc..), is made by an EquipmentManufacturer (meade, celestron, etc..), and can be connected to other Equipment using EquipmentConnector.
 * EquipmentType: for each type, define a set of properties. E.g. for an optical tube, the diameter and focal length are properties which must be defined.
 * EquipmentConnector: connectors describe the link between different Equipments, e.g. an optical tube is often connected to a mount using a dovetail bar/clamp, an eyepiece is usually connected to an optical tube using a 1.25" Eyepiece Male connector. 
 * EquipmentManufacturer: information about a manufacturer

An observing setup is described by a collection of Equipments connected together with EquipmentConnectors.
