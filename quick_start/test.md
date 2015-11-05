<!--
The MIT License (MIT)

Copyright (c) 2014, 2015 IBM Corporation
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
-->

# Test Your Map


## Prepare private map list file

This is a sample list file for your private map. The file is in **JSON** format.
Please save this file as "**PrivateMapList.json**" in NavCog app.
You can add another map as an object of **maps** list.

You need to set the name of your map file to the same with the **name** property. (ie. "**Sample Map.json**")

```
{
  "title": "NavCog Private Map Data List",
  "maps": [
    {
      "name": "Sample Map"
    }
  ]
}
```

## Copy your map data to your device
1. connect iPhone to your Mac (USB)
2. open iTunes and select your device listed in iTunes
3. select apps view

    ![Apps menu image](./images/apps_menu.png)
4. Find "NavCog" app in the Apps list of File Shareing section
5. 	Click "Add..." button to add your map files
6. Select the list file and map file

    If there is a file with same name already, then you first need to delete the file (select files and type **delete** key)


## Test the map with NavCog app
Here is a list of checkpoint for testing your map.

|Test item|Check points|
|---|---|
|Localization accuracy (average error) is about less than 7 feet|[Sampling Data](beacon.md#fingerprinting) [Edge Coordination](map.md#add_edge)|
|Navigation command is announced as you expected|[Accessibility Info.](map.md#add_acc_info) [Edge Orientation](map.md#add_edge)|
|App can track location in transition (if you have transition)|[Manage Transition](appendix.md#transition)|


## Distribute your map
If you want to distribute your map for everyone, please contact [NavCog support](mailto:navcog.calab@gmail.com) and ask to add your map in the public map list.
