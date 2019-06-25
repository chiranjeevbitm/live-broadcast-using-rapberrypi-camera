
	        Broadcasting the live stream using the camera module and raspberry pi 
			
				* * *
	   
DESCRIPTION
	Used camera module and the "Motion" software
	About Motion
		Motion which is an open source software with a number of configuration options which can be changed according to our needs. Here configurations are to be made so that it allows you to create a remote webcam for your Raspberry Pi so that you can view it from any computer on the local network.



Prerequisites & Equipment:

	A Raspberry Pi 3.

	A camera module.

	An SD Card flashed with the Raspbian OS

	Access to the Raspberry either via a keyboard and a monitor or remotely.


COMPILATION

	Update the Raspberry pi

		sudo apt-get update


	Installing the Motion

		sudo apt-get install motion

						(it will ask you (Y/n)  type y then installation will start)


	Configure the software
		First thing we have to edit is the motion.conf file. Type the below command

				sudo nano /etc/motion/motion.conf
					(just modify --  DAEMON = OFF (change to ON))

		Next we need to enable the Daemon (service):

				sudo nano /etc/default/motion
				(start_motion_daemon = no (change to yes))

	 Start the webcam server

	 				sudo service motion start
	 		OR
	 				
	 		for this just type the <ip-address of rasp>:8080   in the web browser to access the stream

	 		in some case port no is  8081

	 If you want to stop the service, then use the command:

					sudo service motion stop

	To restart the service, then use the command:

					sudo service motion restart



