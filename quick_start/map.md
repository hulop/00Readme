<!--

What you have to do is to edit routes information on [online mapeditor](https://navcog.mybluemix.net/map) and to distribute BLE beacons aroud your routes for localization.


Here is an example of map in CMU campus.

![Example of map](images/cmu_map.png)

## <a name="add_area"></a>Add Area
1. Select `Map` Tab.
2. Add **Layer**

  Layer is a concept of same level of ground to show same level height floor plan images. Sometimes a certain floor of a building is connected to different floor of another building because of ground level difference and so on. You need to add at least one layer to the map by clicking `Add Layer` button with filling z-index of the layer. Usually you can specify the floor number to the z-index value. (2nd floor = 2)
3. Add **Region** to the **Layer**

4. Adjust the **Region** size, rotate, and location

  You can adjust the position, size, and rotation of the floor.

* **Type**
|--------|------------|
| `Door`, `Stair`, `Elevator` | Set if the node is in front of these features in your environment. This will be used for transition (see [Appendix](appendix.md#transition).) |
|`Destination`|NavCog app shows a list of Destination node. |
    This will use for destination list and navigation.

    Automatically assigned






    This information will be announced when user is reached to the node through Edge #


    The app will read when the user approaching to the node.

    Select a destination node on the selected layer. You can specify transition for each destination layer. (See [Appendix](appendix.md#transition)
* <a name="acc_info4"></a>**Enable transit to Node # with Info**
    App read this information when the system tries to navigate the user to this transition
2. `Click` on another node.

   Edge represents a connection between two nodes and has a fingerprinting data for better localization.
    Automatically assigned



    * **North** : 0 degree
    * **East** : 90 degree (-270 degree)
    * **South** : 180 degree (-180 degree)
    * **West** : 270 degree (-90 degree)

    You don’t need to measure accurate orientation of the edge because the system use just difference between two edge’s orientations when it navigate the user from edge to edge. In this case several degree of error is not so critical for the navigation.



    [See Appendix](Appedix.md#knnDist)


You can add accessibility information for specific timing in navigation state.

### Navigation states and accessibility information




Item|Timing
---|---
[**Info needed when coming from this Edge #**](#acc_info1)|`Go and Next - Arrival`
[**Destination Information when coming from this Edge**](#acc_info2)|`Destination - Arrival`
[**Tricky node info from this Edge**](#acc_info3)|`Tricky information`
[**Enable transit to Node # with Info**](#acc_info4)|`Transit - Activate`
[**Info needed when coming from node #**](#acc_info5)|`Go and Next - Activate`

1. Select `Beacon` tab
2. Choose `Layer`
2. `Click` on the map where you want to add a beacon with pressing `a key`

### Beacon Information
 |description
---|---
UUID|UUID string of the beacon like "f4376677-0906-41a4-b3ab-949bd675e58c"
Major ID|Major ID of the beacon
Minor ID|Minor ID of the beacon
Product ID|You can use as a note
Beacon ID|Automatically assigned


* select **File** tab
* click **Save to Download** button to download the map file (.json file)