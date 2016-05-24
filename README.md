# Dockerize a RobotFramework

Main focus of this project is to get Robot Framework http://robotframework.org/ source code https://github.com/robotframework to be dockerized.<br>
Target is get official Robot Framework image to docker hub https://hub.docker.com/explore/ . Contributing of this project should follow guidlines that are defined in here https://github.com/docker-library/official-images

# Benefits of Robot Framework container 
* Easy installation just <b>docker run -P -d robot_framework</b>
* Container include: a) IDE and execution tools b) Libraryes => No any more version conflicts between development/testing pipeline
* Easy to scale multible instances by using docker micro servers => Papot library https://github.com/mkorpela/pabot change sequentally test cases execution to parallel execution that brings many huge benefits to picture (e.g. poor man performance testing and speed up of testing pipelines)

# Container deloploy time usage:
Define user to SSH connection: <b>-e SSHUSER=< username ></b>
<br><b><i>Basic auth:</b></i> Define user password to SSHUSER: <b>-e SSHUSERPW=< password ></b>
<br><b><i>OR Key based auth:</b></i> Define user public key to SSHUSER: <b>-e SSHUSERKEY="ssh-rsa < public key >"</b>

# Add more libraryes to container:
* Base your docker file to robot framework container <i>FROM robotframework</i>
* Add required libraryes to your docker file by using any method what you want (e.g. pip, easyinstall, apt-get, etc.)
* Define your docker file entrypoint as <i>ENTRYPOINT ["/rfw_df_entrypoint.sh"]</i>

# INFO:
* Daylight of idea released in http://www.cs.tut.fi/tapahtumat/testaus16/

