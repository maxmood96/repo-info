## `ros:melodic-ros-core-stretch`

```console
$ docker pull ros@sha256:f6719a6e2ddb2cf7b91baaa0bff4e66ee4da11a513a0fe2671c8c061318b7cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-stretch` - linux; amd64

```console
$ docker pull ros@sha256:f26f15cee68bd179c2347e21abfef9827ae3d9b0a12fff8a596adbd048452155
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.5 MB (391477395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e62867ad6d3bef5f3ac014722e59df050a9fe63fdf986fe668bc9b131492bab`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 18:17:30 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 18:17:35 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 26 Feb 2020 18:17:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 26 Feb 2020 18:18:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 18:18:26 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 18:18:26 GMT
ENV LC_ALL=C.UTF-8
# Wed, 26 Feb 2020 18:18:26 GMT
ENV ROS_DISTRO=melodic
# Wed, 26 Feb 2020 18:18:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 26 Feb 2020 18:20:45 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 18:20:47 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 26 Feb 2020 18:20:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 26 Feb 2020 18:20:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7851b385b3454126f02da75d871c31cab343adb6252f96c606208321ebe5f424`  
		Last Modified: Wed, 26 Feb 2020 18:26:49 GMT  
		Size: 10.5 MB (10476682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0f3c809d5bd964fa9c99f4d533d31508fe61ced1652651935ec77d4fa693fe`  
		Last Modified: Wed, 26 Feb 2020 18:26:46 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d860519553be9002ec6cc168b986adc95e13723c9d114964b18cbea0e19c90`  
		Last Modified: Wed, 26 Feb 2020 18:26:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf16b9d760787b93bb8c3f0c7872b401fb00d96f3fd2a870a6f83e531d20d85e`  
		Last Modified: Wed, 26 Feb 2020 18:27:07 GMT  
		Size: 64.8 MB (64770161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9baabdeab314d3737e662c388e0b2b03c57de9e21f1e9e6aad43c4f78764c81`  
		Last Modified: Wed, 26 Feb 2020 18:26:45 GMT  
		Size: 426.8 KB (426764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b928396e18c50dff7d8bbe31d6340783a3d4472fa5f16f33a49fab28739f228`  
		Last Modified: Wed, 26 Feb 2020 18:27:50 GMT  
		Size: 270.4 MB (270426039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647876d988155403f463b985cdcbf476c331e01ce9b2bfd71b391abd87b27540`  
		Last Modified: Wed, 26 Feb 2020 18:26:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ebc508de00e07a81fec2a8879ca2586e6f349084f26214bd5650a13c105cc6ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.9 MB (345869566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04169349285fa621134bc32957e6407afdf324cd590f41c89eb6e46003729d11`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 08:50:19 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 08:50:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Mar 2020 08:50:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Mar 2020 08:51:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 08:51:56 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 08:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Mar 2020 08:52:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Mar 2020 08:52:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Mar 2020 08:55:22 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 08:55:32 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Mar 2020 08:55:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Mar 2020 08:55:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ffb04892983b197ec2012ff1e5f489d298a3d1e097fd400e600d9f5ba5b696`  
		Last Modified: Tue, 31 Mar 2020 09:05:05 GMT  
		Size: 9.8 MB (9774723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6b8b721a085eab12f64779dec536ba34ac8f16dd1717c52ef7b9c274c7dcec`  
		Last Modified: Tue, 31 Mar 2020 09:05:02 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a13c4ba112de5fca316200409698b68af67bb359c22880fedb9f0c978529dae`  
		Last Modified: Tue, 31 Mar 2020 09:05:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550ce74e2e465788ad2b3705897a2121bdf9917d0c435e7fdda3fbf0ff46e225`  
		Last Modified: Tue, 31 Mar 2020 09:05:18 GMT  
		Size: 62.1 MB (62092992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1d9278a758d83e399e2983b086d9bb98a57834e9baab02613f2bf95d5eca06`  
		Last Modified: Tue, 31 Mar 2020 09:05:01 GMT  
		Size: 440.0 KB (439964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c288a14eff30367048e215968facd583b69208c88f246db36f95de84f9f95f2`  
		Last Modified: Tue, 31 Mar 2020 09:06:04 GMT  
		Size: 230.4 MB (230401952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869ba1a44b39237de723e6eda8cbc9d92fa5702dd1accdffa458c18710105b60`  
		Last Modified: Tue, 31 Mar 2020 09:05:00 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
