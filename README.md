# astro-equipment-db

An open and collaborative data base of astronomical equipments

## Concepts

The data base is composed 4 top-level directories, each containing a set of json files:

 * Equipment/: description of an astronomical equipment such as a telescope, a mount or binoculars. Each Equipment has an EquipmentType (e.g. telescope, mount, binoculars etc..), is made by an EquipmentManufacturer (meade, celestron, etc..), and can be connected to other Equipment using EquipmentConnector.
 * EquipmentType/: for each type, define a set of properties. E.g. for an optical tube, the diameter and focal length are properties which must be defined.
 * EquipmentConnector/: connectors describe the link between different Equipments, e.g. an optical tube is often connected to a mount using a dovetail bar/clamp, an eyepiece is usually connected to an optical tube using a 1.25" Eyepiece Male connector. 
 * EquipmentManufacturer/: information about a manufacturer

All json files contain a list of items which form together a large flat list of items.


An observing setup is described by a collection of Equipments connected together with EquipmentConnectors.
