+++
template = "en_index.html"
title = "Questions"

[extra]
lang = "en"
+++

# Frequently Asked Questions and Answers

## How do mechanical engineering projects get implemented?

If there is no CAD plan available, the first step is analysis and providing a
offer.

* Send photos. Preferably 2-3 images that show the product from all angles – the
  more data provided, the more accurate the offer
* Dimensions in mm, or use a measuring tape or ruler in the photos
* Optionally: product weight in grams, color and material type (e.g. ABS, PLA,
  PP, etc.)
* Offer provided by me

If you accept the offer, then:

* sample product shipment (can be slightly damaged, locally broken, the
  important thing is that the geometry can be extracted). It can also be a
  mirror image if that's all that's available
* 3D scanning, or in simpler cases manual measurement
* 3D CAD data is created from the product, programming will be based on this
* programming using a slicing software
* 3D printing
* if necessary, post-processing for FDM – filament-based 3D printing (removing
  supports, sanding, hole calibration…)
* for SLA (liquid resin printing) (removing supports, sanding, hole calibration,
  isopropyl alcohol washing, drying, UV treatment…)

## If CAD plan is available

* Send CAD data. Preferably step, iges or high-quality STL file as email
  attachment or large file transfer
* Optionally: color and material type (e.g. ABS, PLA, PP, etc.)
* Offer provided by me
* If you accept the offer, then:
* Programming will be based on the received CAD data. CAD data modifications
  will be made in consultation with you – if necessary, otherwise the original
  model will be 3D printed
* Programming using slicing software
* 3D printing
* If necessary, post-processing for FDM – filament-based 3D printing (removing
  supports, sanding, hole calibration…)
* For SLA (liquid resin printing) (removing supports, sanding, hole calibration,
  isopropyl alcohol washing, drying, UV treatment…)

## I've seen in videos that 3D printing is a fast technology, practically finished in minutes or 1-2 hours.

In the vast majority of cases, this is not true. There are short printing times
and with technology development, manufacturing times have decreased to 1/5-1/10
of what they were 5 years ago. Fundamentally, compared to pressure casting in
forming tools, this is a fairly time-consuming manufacturing technology.
High-speed recordings, so-called timelapse videos, show the product being built
up in an accelerated manner, making the work process visually impressive.

## Can only decorative items be made with 3D printing, not functional (load-bearing) parts?

Of course not. In casting, material particles are connected to each other
through cohesive bonding, which indeed enables greater load capacity. However,
in 3D printing, adhesive bonding forms along the layers. Nevertheless, load
capacity can be increased to the level of cast parts through geometry
optimization and appropriate material selection (see printer-friendly product
design).

## If a product is 3D printed solid – with 100% infill – do we achieve maximum strength?

No, that's not the case, because strength is achieved primarily by increasing
the number of walls. For example, 4-5 walls instead of 2 already provides
significant strength improvement. Secondly, infill provides rigidity – 70%
infill delivers almost the same physical characteristics as 100%, and in this
case the material savings is not negligible.

## If I have a sample product, I just need to have it 3D scanned, and then 3D printing starts "automatically"!

Unfortunately, that's not the case, or only in very rare cases and mainly for
decorative items. In any case, a CAD model must be built or the scanned STL file
must be corrected.

## Does software automatically "create" a CAD model from a scanned file, making reverse engineering automatic?

This is only rarely a viable approach. The scan must be hole-free and have proper geometry – for example, it may work with fish lure figures or other bodies bounded by freeform surfaces. This is called auto meshing, but even then, directed mesh auto generation is preferable, which is already a "semi-automatic" method. Therefore, in most cases it is necessary to build a CAD model from the scanned mesh.

## Why is reverse engineering relatively expensive?

Because relatively few people perform this work process and it requires
significant expertise and – as the name suggests – reverse CAD engineering
thinking. Additionally, the designer must assess which parts are worn and need
to be modeled correctly on the CAD model.

## Does a 3D scanner create 3D CAD data?

No, the result is a point cloud in space, which the software "triangulates",
resulting in stereolithography data – data represented by triangles (STL file).

## Does a 3D scanner use a laser to create STL data?

No, the laser is used for measurement – to determine the spatial position of points. The surface is scanned using optical equipment.

## Why is the 3D scanned surface sprayed with white powder or paint?

This is also called anti-reflective spray, used to prevent light reflection from shiny surfaces – the "glare" effect. Similar to conventional photography.

## Does poor quality, coarse mesh STL file not cause problems because the printer "corrects" it anyway?

Unfortunately, that's not the case. Geometry distortion caused by coarse meshing – for example, polygonal circular cross-sections – "appears" in the print, which is why a high-quality mesh file is important.
