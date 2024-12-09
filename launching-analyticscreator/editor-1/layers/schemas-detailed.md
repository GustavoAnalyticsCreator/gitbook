# Schemas detailed

Layer is the logical part of the data warehouse. There are 5 types of layer you can define:&#x20;

• Source layer. Abbreviation – SRC. This layer isn’t the part of the data warehouse. It is the logical data layer containing external data sources which data will be used in the data warehouse. You cannot create tables or transformations on this layer.&#x20;

• Staging layer. Abbreviation – IMP. Usually the data from source layer will be imported into the tables belong to this layer. Typically, the data in the import layer will be overwritten which every data import.&#x20;

• Persisted staging layer. Abbreviation – STG. Usually the data from import layer will be historicized and stored in the staging layer. Staging layer is the primary data layer of the data warehouse.&#x20;

• Transformation layer. Abbreviation – TRN. Transformation layer is the optional help layer. Usually you make here some additional transformations of the data stored in the staging layer.&#x20;

• Data warehouse layer. Abbreviation – DWH. On this layer you transform data into the facts and dimensions.&#x20;

• Data mart layer. Abbreviation – DM. This is the interface layer of your data warehouse. The logical structure of the data on this layer is usually a star containing fact and dimensions. Layers on the layer diagram are present in the following order: SRC – IMP – STG – TRN – DWH - DM There is the typical DWH layer diagram:

Layers on the layer diagram are present in the following order: SRC – IMP – STG – TRN – DWH - DM There is the typical DWH layer diagram:

{% embed url="https://www.canva.com/design/DAGY03aazHw/sA6ZbaTvhw6IJXE9-E9fWg/view?utm_campaign=designshare&utm_content=DAGY03aazHw&utm_medium=link&utm_source=editor" %}
Layers
{% endembed %}

Layers editing

{% embed url="https://www.canva.com/design/DAGY06EZevM/yO4lwQ0Zb2v1yU2Ue0okYw/view?utm_campaign=designshare&utm_content=DAGY06EZevM&utm_medium=link&utm_source=editor" %}
Layers editing
{% endembed %}

