# kokrooPAD
macOS userspace driver for creating virtual DS4/Xbox 360 controllers.

Etymology:

I wanted to give it a better name like MUDpad, ViGEmac, etc. but I ended up naming it kokrooPAD to avoid any trademark issues like the one faced by ViGEmBus. If anyone can suggest a better trademark-free name, I am all ears.

Goals:

The primary motivation for creating this library/software is to allow Parsec developers to incorporate this to enable the emulation of gamepad controllers on macOS hosts.
Feel free to incorporate this into other projects, free or commercial.

ToDo List:

1. Sign the driver with a development certificate for testing locally without entitlements from Apple.
2. Develop an interface to create, destroy, and list a controller.
3. Create an interface to send input states to them.
4. Provide the ability to have multiple controllers simultaneously.

Done:
1. Created a virtual DS4 Controller which is visible to Chrome, PCSX2, Crossover.

Research Notes:
1. VirtualHere is able to successfully create a virtual DS4 controller over the network on macOS and relays the inputs correctly. However, it's sometimes a bit laggy and out of order, probably due to inefficiencies in the networking code/protocol. This proved to me that virtual controllers can be created and controlled on macOS.
2. Karabiner for macOS uses the same mechanisms to create virtual keyboards and mice.
