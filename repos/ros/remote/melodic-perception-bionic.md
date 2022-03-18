## `ros:melodic-perception-bionic`

```console
$ docker pull ros@sha256:22701f5b68be30dfd9a46a88095e8c40a61069854ab929da1eac5395287586ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception-bionic` - linux; amd64

```console
$ docker pull ros@sha256:e4706211e9fb242a325422ca078700b9b4acd3c9fcba786379e524df63fdbe77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.7 MB (742726447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f653c3f29d5782e426aba9f3174eca54428737a5c0da8219d001ed64b6dd707`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:30:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:41:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 22:44:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:44:41 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:44:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:44:41 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:45:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:45:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:53:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb61ec94593913764bceda6f5225dfb36c85ab821bba51cfc351aee5c0d15bf9`  
		Last Modified: Thu, 03 Mar 2022 21:53:03 GMT  
		Size: 838.9 KB (838912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842eb625b70f7cd66ae8b93c358fac16bc433d0810c8ad1b72e31f0fb51166d7`  
		Last Modified: Thu, 03 Mar 2022 23:19:58 GMT  
		Size: 4.9 MB (4872136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52318dcbcc7ab7aed846173e137fac8dcca9fd5a9e31f387253baac28a116b29`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7493a4839f98183bd1f660117bc0db64ff324c2821edf758cbac92100fb196`  
		Last Modified: Thu, 03 Mar 2022 23:19:56 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d7cd6f01398c2360ed50375d1d7dd55bcfa633c0d22f561ac31fff3a382158`  
		Last Modified: Thu, 03 Mar 2022 23:20:41 GMT  
		Size: 259.5 MB (259471543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1c8834da4a4cd3b6cd4a81f3da74c08dd5eff8e5057788bac9d716d9c5b70`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d60b18cea4bea769d9f920f3dec216d47f7abc629c2e3247d1c8bcb9664fc`  
		Last Modified: Thu, 03 Mar 2022 23:21:02 GMT  
		Size: 70.2 MB (70235171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb4815cafc69491f37c4c880c78fa1db27e0958876cf27ecf99773e197520f3`  
		Last Modified: Thu, 03 Mar 2022 23:20:51 GMT  
		Size: 277.4 KB (277396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6520e34a3cdb3a45de4b4329914faade54515b3c32762ef0cd1139b67ebd19d5`  
		Last Modified: Thu, 03 Mar 2022 23:21:07 GMT  
		Size: 75.0 MB (74994244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ca478d4105a8544fb086f107bc416fb0bfb1e1cc29001d54364b46a16bc30f`  
		Last Modified: Thu, 03 Mar 2022 23:22:25 GMT  
		Size: 305.3 MB (305326304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:0b619d91f10af18861121af80082d33d2455d2b06201a5dc5045d23a0abb5ce2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.9 MB (645940163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07eead6460f5298b4eb7da1c492fda741ab2b5ba2a684ed2cd7ca7d8ffbaf23`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 21:21:10 GMT
ADD file:c60e89df1905b44d4771a78ca9fa8113b55681f00e5bb55e798028b77ce6c120 in / 
# Thu, 03 Mar 2022 21:21:11 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 04:01:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 04:01:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 04:01:50 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 04 Mar 2022 04:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 04 Mar 2022 04:02:07 GMT
ENV LANG=C.UTF-8
# Fri, 04 Mar 2022 04:02:07 GMT
ENV LC_ALL=C.UTF-8
# Fri, 04 Mar 2022 04:02:08 GMT
ENV ROS_DISTRO=melodic
# Fri, 04 Mar 2022 04:05:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 04:05:23 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 04 Mar 2022 04:05:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 04 Mar 2022 04:05:24 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 04:06:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 04:06:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 04 Mar 2022 04:07:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 04:11:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f04b2e36c59d7fb6bb1129d2ffaff71df9aa51f235875df61b423ebbdfcc1ae3`  
		Last Modified: Thu, 03 Mar 2022 21:24:40 GMT  
		Size: 22.3 MB (22308282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f380d69841025e6b63e2dfc0e56d213259f355d6de16eadef37b5fdf89a94bc`  
		Last Modified: Fri, 04 Mar 2022 04:24:44 GMT  
		Size: 840.0 KB (840032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c451fb3d45a2005005eb76d822d0d911049f61e3e2766b8adb8037a33ff01c`  
		Last Modified: Fri, 04 Mar 2022 04:24:43 GMT  
		Size: 4.1 MB (4086038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb788eb112007cab18af1df4dff153476a67d6db031ba82c4fe4c4cf22a36806`  
		Last Modified: Fri, 04 Mar 2022 04:24:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b555a52539c176b32f1ba8e4d84b3ee4af604117fe9e82353fd5ee6ff165bd27`  
		Last Modified: Fri, 04 Mar 2022 04:24:41 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e603a55f4738ebbe181eac105a1524b72ca02900ec83c27a393000ea15daebc`  
		Last Modified: Fri, 04 Mar 2022 04:27:16 GMT  
		Size: 238.9 MB (238941322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a938efde971f033f21d599b2c079f40fdafceeea24a4e352916fdd28eac4a79d`  
		Last Modified: Fri, 04 Mar 2022 04:24:41 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9052660c8da0f2d1b6ba3eb1009500a24908a0a4abe701875edf3f464678ed49`  
		Last Modified: Fri, 04 Mar 2022 04:27:59 GMT  
		Size: 54.7 MB (54704995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dd558dd49dc1a13f86bd8636fc88cb462bdfa2dbfa8d11f05f33c844e132c8`  
		Last Modified: Fri, 04 Mar 2022 04:27:29 GMT  
		Size: 277.4 KB (277393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a563438123d69eb5dce390a433289616176f63814bdb23e8a7ebe6e9cda87ad`  
		Last Modified: Fri, 04 Mar 2022 04:28:13 GMT  
		Size: 64.7 MB (64746047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83271773f74565e028d98570e65a45299b4e3fd626619a0089f5baae8e1dcb00`  
		Last Modified: Fri, 04 Mar 2022 04:31:34 GMT  
		Size: 260.0 MB (260033645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:edacfc7a87b90c24654282216023c773c523f48e64c97d5b852eec4ce7855ff5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702932603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b814ca31a82a239dbb0e7c34ae11450922fdc45b7933fb7ca9fb9b369aaeb28`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 00:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 00:44:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 00:44:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 18 Mar 2022 00:44:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Mar 2022 00:44:50 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 00:44:51 GMT
ENV LC_ALL=C.UTF-8
# Fri, 18 Mar 2022 00:44:52 GMT
ENV ROS_DISTRO=melodic
# Fri, 18 Mar 2022 00:46:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 00:46:18 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 18 Mar 2022 00:46:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Mar 2022 00:46:21 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 00:46:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 00:46:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 18 Mar 2022 00:47:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 00:49:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3ab66e8231603adb03d0ab793fb0e59972981a99ffc720e57c383f793946d1`  
		Last Modified: Fri, 18 Mar 2022 01:19:05 GMT  
		Size: 839.7 KB (839706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c205e19bfaf7b34cc3a9b24062d2decf853a9385f3fef4d92087fb5f722c192f`  
		Last Modified: Fri, 18 Mar 2022 01:19:03 GMT  
		Size: 4.3 MB (4264013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ecfed1d8156c3c766d1cf52767451b94c4bddebf47c6077a252748e8a8efe14`  
		Last Modified: Fri, 18 Mar 2022 01:19:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944bedb1f36c611f0fb39e835b936986f1dff2992e5b1af78dd788f93c8935ec`  
		Last Modified: Fri, 18 Mar 2022 01:19:03 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01676100b2c71e8cba083dac9fa5b52bcc5bb6ce3e9f6aa8e7df42107bee34ab`  
		Last Modified: Fri, 18 Mar 2022 01:19:38 GMT  
		Size: 252.4 MB (252367186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fbf59c647844e4d4b6adb832d7aa654d99f008356bfa2e20f9326b02133b43`  
		Last Modified: Fri, 18 Mar 2022 01:19:03 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e032b61c129c218c14d1f7db94a569b57660cf8588cc7f05f693eda8c43209`  
		Last Modified: Fri, 18 Mar 2022 01:19:59 GMT  
		Size: 63.1 MB (63067569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab07924ab6769ed024d06805340c41da0fa74e475f78c54e27d5d9e9e0c7fa2`  
		Last Modified: Fri, 18 Mar 2022 01:19:50 GMT  
		Size: 277.6 KB (277589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6507226de0a55e0899df013993c3ba1708f3ba1f41e91ad8b92287104a4aad`  
		Last Modified: Fri, 18 Mar 2022 01:20:01 GMT  
		Size: 67.0 MB (67001735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0825d2c20990804559f3d682273fea296981f238be61747781d6dfa41d0f41f`  
		Last Modified: Fri, 18 Mar 2022 01:21:16 GMT  
		Size: 291.4 MB (291383332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
