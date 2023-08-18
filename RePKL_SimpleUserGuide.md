RePKL Simple User Guide

RePKL is designed to separate a multi-CPL (or “merged”) IMP into single-CPL IMPs. In short it is an “unmerge tool.”

Basic Commands

|--help|Displays the help message |
|--action <action>|Indicates whether assets will be copied or moved to the new Mapped File Set.<br><copy, move, dryrun, skip, symlink>|
|--ov <path to OV CPL xml>|Path to an OV CPL from which IMP will unmerge. If --ov command is omitted the target CPL will be created as a new OV.|
|--delivery <path to the delivery>|<p>Path to an Mapped File Set where the assets of the target CPL are found. If omitted, the target and OV CPLs are assumed to be at the root of a mapped file set.|

Basic syntax

Create an unmerged supplemental:

--action <action> --ov <path to OV CPL xml> <path to supplemental CPL xml> <destination of unmerged supplemental>

Create an unmerged OV:

--action <action> <path to OV xml> <destination of unmerged OV IMP>

***Example***

An IMP is delivered with both an English OV and German Supplemental in a single IMP. The user wants to copy the Supplemental into its own folder.

--action copy --ov A:\Media\Title\_IMP\_Delivery\CPL\_Title\_ENG\_IMF\_OV.xml A:\Media\Title\_IMP\_Delivery\CPL\_Title\_DEU\_IMF\_Supp.xml A:\Media\Unmerged\_DEU\_IMP\_Supp

***Example #2***

The user wants to copy the English OV into its own folder.

--action copy A:\Media\Title\_IMP\_Delivery\CPL\_Title\_ENG\_IMF\_OV.xml A:\Media\Unmerged\_ENG\_IMP\_OV

***Example #3***

The user wants to create a supplemental symlinked to the source assets.

--action symlink --ov A:\Media\Title\_IMP\_Delivery\CPL\_Title\_ENG\_IMF\_OV.xml A:\Media\Title\_IMP\_Delivery\CPL\_Title\_DEU\_IMF\_Supp.xml A:\Media\Symlinked\_DEU\_IMP\_Supp

***Example #4***

The user wants to test unmerging a supplemental IMP.

--action dryrun --ov /mnt/Drive/Title\_IMP\_Delivery/CPL\_Title\_ENG\_IMF\_OV.xml /mnt/Drive/Title\_IMP\_Delivery/CPL\_Title\_DEU\_IMF\_Supp.xml /mnt/Drive/Unmerged\_DEU\_IMP\_Supp






