# HME-1 JSON Format (Under Construction)

The most detailed format of HME-1. Contains **all metadata**, unlike other formats. 

----
# When to use the HME-1 JSON format

- To train a custom network.
- To wrangle data into different categories. (i.e. you want to train seperate Darknet models for handwritten and non-handwritten data)

Metadata format, per image: 

```
let image = {
    item_id: 0,                                   // int
    local_name: "",                               // string
    annotations_darknet: [id1, id2, id3, etc.],   // [int list] references ids of annotations.
    source: 0                                     // string, reference id of a source
}
```

Metadata format, per annotation:

```
let annotation = {
    annotation_id: 0,                           // int
    handwritten: false,                         // bool
}
```

Metadata format, per source:

```
let source = {
    source_id: 0,                                       // int
    source: "source name",                              // string
	source_type: "book",                                // string
	authors: ["author1", "author2", "etc."],            // [string list] list of author names
	links: ["link1", "link2", "etc."],                  // [string list] list of links to the source
    copyright: true                                     // bool
}
```
