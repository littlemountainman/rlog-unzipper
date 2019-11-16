Rlog reader for openpilot rlog files
====================================

This reader is built to extract information from the rlog files from openpilot.

## Install:
<pre>
sudo ./cereal/install_capnp.sh
python rlogreader.py <path-to-rlog-file-from-your-drive>
</pre>

## Possible parameters to look for in the file
In the code there already is the necessary code to extract all teh steering angles from one drive.

<pre>
carControl = (
    enabled = true,
    gasDEPRECATED = 0,
    brakeDEPRECATED = 0,
    steeringTorqueDEPRECATED = 0,
    cruiseControl = (cancel = true, override = true, speedOverride = 0, accelOverride = 1),
    hudControl = (
      speedVisible = true,
      setSpeed = 28.888889,
      lanesVisible = true,
      leadVisible = true,
      visualAlert = none,
      audibleAlert = none,
      rightLaneVisible = true,
      leftLaneVisible = true,
      rightLaneDepart = false,
      leftLaneDepart = false ),
    actuators = (
      gas = 0.092801958,
      brake = -0,
      steer = -0.081682287,
      steerAngle = -0.74651462 ),
    active = false )
</pre>

To see more... just do 
<pre>
for l in logs:
	print(l)
</pre>
