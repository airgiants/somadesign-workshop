# somadesign-workshop

The nodes connect to a provided wifi accesspoint with a mqtt server runnin in a container within it. 

they connect to mqtt.airgiants.co.uk:44920 which also listens to the standard mwtt port mqtt.airgiants.co.uk:1883.
This is unauthenticated.


Each node publishes and subscribes a topic of the folling form:

airgiants/$(InstallationName)/debug/out/$(CreatureName)/$(nodenumber)/knobs/setDrive
Publishing a message with an a float integer -1.0...1.0 drives the chamber open and closed. 

For the hexagorgon the string is rougly this:

airgiants/hexagorgon/debug/out/hexagorgon/$(NodeName)/knobs/setDrive, with nodename n1-n6.

Please see attached untested python. 
Thios should work with python 3

pip3 install paho-mqtt




