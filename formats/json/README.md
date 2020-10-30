# HME-1 JSON Format (Under Construction)

The most detailed format of HME-1. Contains **all metadata** unlike other formats. 
Use this format if you are not training a pre-trained network. 

Metadata format: 

```
{
    item_id: 0,                                   // int
    local_name: "",                               // string
    annotations_darknet: [id1, id2, id3, etc.]    // [int list] references ids of annotations, stored elsewhere.
}

```
