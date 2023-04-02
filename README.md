# Mterial-Coding-for-Inventory

Material-Coding-for-Inventory is a material/item coding system specially made for **HKD Outdoor Innovations Ltd.**

## Task

The task was to design a material coding system based on the material name, color, and size.

The proposed system offers a nine-digit coding system.
## Issues
1. There was no database for existing or usable material and so on.
2. BOMs (Bill of Materials) are the primary source of data and respective departments used to maintain data based on the BOM. The main problem was that the BOMs are not standard in format. As the BOMs were solely human-made; data were corrupted and scattered. Sometimes data of a designated field were put on a different field. Sometimes data were missing. Misspelling is a regular scene in the BOMS.

## The proposed system offers a nine-digit coding system.
1. The first three digits are alpha-alpha-numeric. It denotes the name of the material.
2. The second three digits are alpha-alpha-numeric. It denotes the color of the material.
3. The last three digits are also alpha-alpha-numeric. This part denotes the size of the material.

## How it works
1. The system first concatenates all columns of the BOM.
2. Then the system matches the name, color, and size for each tuple on the input.
3. For any match; the system writes the respective three-digit codes for each tuple. The system looks for a match in name, color, and size. So it puts a total of nine-digit code for each tuple.
4. If the system does not find a match for a name; it writes *none1*. If it can not find a match for color; it writes *none2*. It writes *none3* for a not found in size. For example, if the system can not find a match for name, color, and size- the code will be none1none2none3. 



## Usage
### To make the item, color, and size database-
1. List all items, colors, and sizes in three different text files (.txt). See the codes to fix/adjust the file names and header names.
2. Use **1_remove_duplicates.ipynb** to remove all duplicate entries in the database files.
3. Then use **2_sort.ipynb** to sort all entries in descending order of tuple length.
4. Then use **3_assigncode.ipynb** to assign a three-digit code for all entries.
5. Repeat processes 2, 3, and 4 for all three tex files (name, color, size).
5. Finally, use **4_material_Coding.ipynb** to assign nine-digit codes on any BOM.


## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
