
# Appendix: IFC-to-XKT Conversion Pipelines

---
There are several pipelines through which we can import an IFC file into a xeokit Viewer.

## WebIFCLoaderPlugin

This pipeline simply uses a [WebIFCLoaderPlugin]() to load an ````.ifc```` file directly into a xeokit Viewer. This is
suitable for loading small ````.ifc```` files.

## Community Pipeline #1

* Suitable for converting medium-to-large ````.ifc```` files to ````.xkt````
* Uses all open source tools
* Creates intermediate ````.glb```` and ````.json```` metadata files
* After using this pipeline, we can then view the ````.xkt````  or ````.glb```` in a
  xeokit [Viewer](https://xeokit.github.io/xeokit-sdk/docs/class/src/viewer/Viewer.js~Viewer.html), using an
  [XKTLoaderPlugin](https://xeokit.github.io/xeokit-sdk/docs/class/src/plugins/XKTLoaderPlugin/XKTLoaderPlugin.js~XKTLoaderPlugin.html)
  or
  a [GLTFLoaderPlugin](https://xeokit.github.io/xeokit-sdk/docs/class/src/plugins/GLTFLoaderPlugin/GLTFLoaderPlugin.js~GLTFLoaderPlugin.html)
  , respectively

#### Tools used:

* [IfcConvert](http://ifcopenshell.org/ifcconvert) (MIT, from [IfcOpenShell](http://ifcopenshell.org/))
* [xeokit-metadata](https://github.com/bimspot/xeokit-metadata) (MIT, from [BIMSpot](https://bimspot.io))
* [convert2xkt](https://github.com/xeokit/xeokit-convert) (AGPL3, from [xeolabs](https://xeolabs.com))

#### More info:

* Tutorial: [Converting IFC Models to XKT using Open Source Tools - A Simpler Pipeline](https://www.notion.so/xeokit/Converting-IFC-Models-to-XKT-using-Open-Source-Tools-A-Simpler-Pipeline-02d45ba457eb4f808f63bcacb71a4fb3)

![](assets/oss_xkt_conversion_v2.png)

## Community Pipeline #2

* Suitable for converting small ````.ifc```` files to ````.xkt````.
* Uses a single open source tool to directly convert each ````.ifc```` file to ````.xkt````, without creating
  intermediate files.
* After using this pipeline, we can then view the ````.xkt````  in a
  xeokit [Viewer](https://xeokit.github.io/xeokit-sdk/docs/class/src/viewer/Viewer.js~Viewer.html), using an
  [XKTLoaderPlugin](https://xeokit.github.io/xeokit-sdk/docs/class/src/plugins/XKTLoaderPlugin/XKTLoaderPlugin.js~XKTLoaderPlugin.html)

#### Tools used:

* [convert2xkt](https://github.com/xeokit/xeokit-convert) (AGPL3, from [xeolabs](https://xeolabs.com))

#### More info:

* Tutorial: [Converting Models to XKT with convert2xkt](https://www.notion.so/xeokit/Converting-Models-to-XKT-with-convert2xkt-fa567843313f4db8a7d6535e76da9380)

![](assets/oss_xkt_conversion.png)

## Enterprise Pipeline #1

* Best-performing pipeline, suitable for converting large ````.ifc```` files to ````.xkt````
* Uses a combination of proprietary and open source tools
* Creates intermediate ````.glb```` and ````.json```` metadata files
* After using this pipeline, we can then view the ````.xkt````  or ````.glb```` in a
  xeokit [Viewer](https://xeokit.github.io/xeokit-sdk/docs/class/src/viewer/Viewer.js~Viewer.html), using an
  [XKTLoaderPlugin](https://xeokit.github.io/xeokit-sdk/docs/class/src/plugins/XKTLoaderPlugin/XKTLoaderPlugin.js~XKTLoaderPlugin.html)
  or
  a [GLTFLoaderPlugin](https://xeokit.github.io/xeokit-sdk/docs/class/src/plugins/GLTFLoaderPlugin/GLTFLoaderPlugin.js~GLTFLoaderPlugin.html)
  , respectively

#### Tools used:

* [ifc2gltf](https://creoox.com/en/contact/) (Closed source, from [Creoox AG](https://creoox.com/en/contact/))
* [convert2xkt](https://github.com/xeokit/xeokit-convert) (AGPL3, from [xeolabs](https://xeolabs.com))

#### More info:

* Tutorial: [Converting IFC to XKT using ifc2gltf](https://www.notion.so/xeokit/Converting-IFC-to-XKT-using-ifc2gltf-a2e0005d00dc4f22b648f1237bc3245d)

  ![](assets/creoox_oss_xkt_conversion.png)