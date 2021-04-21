# Autopsy-Plaso
NP CSF DF Module Assignment

Digital Forensics Assignment using the GUI based Autopsy 4 and Plaso software kit on SANS SIFT Workstation.

Used to simulate how these two Digital Forensic tools can aid evidence extraction for solving digital crimes

**Case Scenario: Autopsy Training Renzik Dognapping Case** (available for download through [Autopsy 8 hour training](https://dfir-training.basistech.com/courses/autopsy-basics-8-hours))


![eposter](https://github.com/RyanNgCT/Autopsy-Plaso/blob/main/DF-EPoster.jpg)

### Requirements
- SANS SIFT Workstation
- Windows VM with [Timeline Explorer](https://ericzimmerman.github.io/#!index.md) and [Autopsy 4.x+](https://www.autopsy.com/download/) installed

### Plaso Commands
1. Log2Timeline.py

*Purpose: create a dump file based on the acquired image. May need to select partition to be processed.*
```
$ log2timeline.py [-f <filter_filename>] <output_filename> <input_filename>
```

2. pinfo.py and `file` command

*Purpose: gather information of the type of dump file and properties (registry, file, warnings etc.).*
```
$ file <output_filename>
$ pinfo.py <output_filename>
```

3. psort.py

*Purpose: create the timeline of events for analysis in Timeline Explorer.*
```
$ psort.py [-z <zone_identifier>] -o <output_type> -w <output_timeline> <input_dump_filename> [--slice <timeslice>] [timefilter]
```
* `-z`: e.g. UTC, GMT+8 etc.
* `<output_type>`: xlsx (smaller timelines) or tcsv (can be processed with Timeline Explorer in Windows)
* `-w`: file to write to (a.k.a. output timeline file)


## Contributors
- [@EzraHoJC](https://github.com/ezrahojc)
- [@RyanNgCT](https://github.com/ryanngct)
