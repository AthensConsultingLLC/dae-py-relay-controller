Denkovi Relay Board Controller v1.3
===================================

Copyright (c) Peter Bingham  (petersbingham@hotmail.co.uk)  

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:  
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.  
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Known Limitations and Assumptions
_________________________________
1. Written and Tested in Python 2.7 only. (Look at the Python3 branch for experiemental Python 3 support).
2. 4 and 8 relay boards do not handle connection to multiple devices. Connects to first found Denkovi.
3. Not thread safe. 
4. Possible race conditions with device plugging.
5. Uses a VCP delay of 50ms. Documentation specifies 5ms but was still seeing corruption at 20ms. Could be improved for the gets by doing an initial sync and then keeping track of the states in the class.


Help
____
 * Install using "python setup.py install" in this directory at thecommand line.
 * Both installions require serial module. The Linux version requires pylibftdi. For Windows FTD2XX.dll will need to be in your path.
 * Usage is pretty simple. Have a look at the examples and test code in the "Example & Test" folder. Look at the dae_RelayBoard file to see the interface functions.
 * To run "Example & Test\example16.py", for example, set the com port in the file and then open a cmd and cd into "Example & Test" folder and type "python example16.py".


Change Log
__________
1.3 - setup.py package installer added.  
1.2 - Linux support added.  
1.1 - Fixed serial not being flagged as close on disconnect and failure to ensure disconnection on a reconnect.  
