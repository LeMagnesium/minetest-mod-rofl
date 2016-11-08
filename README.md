ROFL mod for Minetest
=====================

An area saver/applier. But a tad weird.

# Configuration

 - `rofl.conf.Tick` : The tick interval between each processing
 - `rofl.conf.Rpertick` : Maximum of reading operations per tick
 - `rofl.conf.Wpertick` : Same as above but writing
 - `rofl.conf.Apertick` : Same as above but for application on the map
 - `rofl.conf.Lpertick` : Same as above but for loading in the application buffer

# Commands

 - roflCapture name pos1 pos2 :
   - name is the name of the area save
   - pos1 is a (x,y,z) tuple
   - pos2 is also a pos tuple
   - This command captures the nodes in the parallelepiped delimited by pos1 and po2 and saves it in the file 'name' in the rofl folder inside your world's folder

 - roflPaste name pos :
   - name is the name of the area to load
   - pos is optional, if not provided, then the mod tries to find your position. If it cannot, then it lets you know and dies lamely
   - This command applies the nodes saved into the file called name at the given position if provided, or your position if available

 - roflFlush buff :
   - buff is a character, either A or W
   - This flushes either the Application or Writing buffer (both outputs) from all pending operations

 - roflReset name :
   - name is a buffer file's name
   - This initializes/resets the data in the buffer 'name'
